# 2023-05-14
1、抓包版本更新配合抓包工具获取相应参数可获取相应的链接以及文章标题
2、暂未解决的问题暂时无法获取相应的文章阅读量等关键信息
3、其他大佬所说的获取文章数量限制问题暂时还未发现
4、部分文章的标题链接正表达式有点小问题，暂时未发现何种原因


# 2022-12-02
项目准备换种思路重新获取文章信息

**设想功能**

任意公众号可获取信息，无需登录

获取标题、链接、浏览数、点赞数等

支持下载文章、封面图片等

将文章保存为word


**更新进度**

使用 Fiddler 抓包成功获取文章链接

了解了链接中参数意义

        # 微信公众唯一ID
        biz = 'MzI0MTA3NDU4OQ'
        # 个人微信id
        uin = 'MjU4MjYwMDIxNA%3D%3D'
        # 定时获取验证的key
        key = 'a5caf4e3c7ba63cbe6c4fbb37d4d7577c07d617c1cf1e1a7f4129caa82848ea81191282b75ca5c8fc51f8983154937450fe4ea59321c' \
            '1f871acbca4de8c24d21878e66d69763a29352ee8a7c329ebc0decb43e65c9f8fcaaf301bf0bac283614bef3626139bcd0d' \
            '81052f3cc6594b893d92fdd5a834e9820bc601f458ac0c5a3'
        offset = '0'  # 页数，0开始，每10增长
        count = '30'  # 每页限时的数量，有限制最多数
        rul = f"https://mp.weixin.qq.com/mp/profile_ext?action=getmsg&__biz={biz}==&" \
            f"f=json&offset={offset}&count={count}&is_ok=1&scene=&uin={uin}&" \
            f"key={key}"


**下一步计划**

在 key 值的有效时间内获取完所有的网页返回文本

利用正表达式获取标题，文章链接，图片链接等有效信息


# 2022-11-27
1、目前存在问题，需要获取完成所有的文章后才会写入excl
2、需要登录管理员后台



