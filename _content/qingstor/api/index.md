---
---

# API 文档

- [概述](common/overview.html)
    - [总览](common/overview.html#id2)
    - [基本概念](common/overview.html#id3)
        - [Zone](common/overview.html#zone)
        - [Service](common/overview.html#service)
        - [Bucket](common/overview.html#bucket)
        - [Object](common/overview.html#object)
    - [地址构成](common/overview.html#id4)
- [公共字段](common/common_header.html)
    - [请求头字段 (Request Header)](common/common_header.html#请求头字段-request-header)
    - [响应头字段 (Response Header)](common/common_header.html#响应头字段-response-header)
- [错误信息](common/error_code.html)
    - [错误码](common/error_code.html#错误码)
    - [错误返回格式](common/error_code.html#错误返回格式)
- [签名验证](common/signature.html)
- [访问控制](../access_control.html)
    - [存储空间策略(Bucket Policy)](../access_control.html#bucket-policy)
    - [存储空间访问控制列表(Bucket ACL)](../access_control.html#bucket-acl)
    - [存储空间的跨源资源共享策略(Bucket CORS)](../access_control.html#bucket-cors)
- [数据加密](common/encryption.html)
- [自定义元数据](common/metadata.html)
- [Service API](service/index.html)
    - [GET Service](service/get.html) 列取 Bucket
- [Bucket API](bucket/index.html)
    - [GET Bucket (List Objects)](bucket/get.html) 列取对象
    - [PUT Bucket](bucket/put.html) 创建 Bucket
    - [DELETE Bucket](bucket/delete.html) 删除 Bucket
    - [Delete Multiple Objects](bucket/delete_multiple.html) 批量删除对象
    - [HEAD Bucket](bucket/head.html) 获取 Bucket 元信息
    - [GET Bucket Statistics](bucket/get_stats.html) Bucket 使用统计
    - [List Multipart Uploads](bucket/list_multipart_uploads.html) 列取分段上传
    - [Bucket ACL](bucket/acl/index.html) 用户授权
        - [PUT Bucket ACL](bucket/acl/put_acl.html)
        - [GET Bucket ACL](bucket/acl/get_acl.html)
    - [Bucket Policy](bucket/policy/index.html) 授权策略
        - [Bucket Policy Condition](bucket/policy/policy_condition.html)
        - [PUT Bucket Policy](bucket/policy/put_policy.html)
        - [GET Bucket Policy](bucket/policy/get_policy.html)
        - [DELETE Bucket Policy](bucket/policy/delete_policy.html)
    - [Bucket CORS](bucket/cors/index.html) 跨站请求设置
        - [PUT Bucket CORS](bucket/cors/put_cors.html)
        - [GET Bucket CORS](bucket/cors/get_cors.html)
        - [DELETE Bucket CORS](bucket/cors/delete_cors.html)
    - [Bucket External Mirror](bucket/external_mirror/index.html) 外部镜像
        - [PUT Bucket External Mirror](bucket/external_mirror/put_external_mirror.html)
        - [GET Bucket External Mirror](bucket/external_mirror/get_external_mirror.html)
        - [DELETE Bucket External Mirror](bucket/external_mirror/delete_external_mirror.html)
    - [Bucket Notification](bucket/notification/index.html) 事件处理
        - [PUT Bucket Notification](bucket/notification/put_notification.html)
        - [GET Bucket Notification](bucket/notification/get_notification.html)
        - [DElETE Bucket Notification](bucket/notification/delete_notification.html)
    - [Bucket Lifecycle](bucket/lifecycle/index.html) 生命周期
        - [PUT Bucket Lifecycle](bucket/lifecycle/put_lifecycle.html)
        - [GET Bucket Lifecycle](bucket/lifecycle/get_lifecycle.html)
        - [DELETE Bucket Lifecycle](bucket/lifecycle/delete_lifecycle.html)
    - [Bucket Logging](bucket/logging/index.html) 访问日志归档
        - [PUT Bucket Logging](bucket/logging/put_logging.html)
        - [GET Bucket Logging](bucket/logging/get_logging.html)
        - [DELETE Bucket Logging](bucket/logging/delete_logging.html)
    - [Bucket Replication](bucket/replication/index.html) 跨区域复制
        - [PUT Bucket Replication](bucket/replication/put_replication.html)
        - [GET Bucket Replication](bucket/replication/get_replication.html)
        - [DELETE Bucket Replication](bucket/replication/delete_replication.html)
- [Object API](object/index.html)
    - [PUT Object](object/put.html) 对象上传
    - [GET Object](object/get.html) 对象下载
    - [POST Object](object/post.html) 表单上传
    - [PUT Object - Copy](object/copy.html) 对象拷贝
    - [PUT Object - Move](object/move.html) 对象移动
    - [PUT Object - Fetch](object/fetch.html) 对象导入
    - [Append Object](object/append.html) 对象追加写
    - [DELETE Object](object/delete.html) 删除对象
    - [HEAD Object](object/head.html) 获取对象元信息
    - [OPTIONS Object](object/options.html)
    - [Multipart](object/multipart/index.html) 分段上传
        - [Initiate Multipart Upload](object/multipart/initiate_multipart_upload.html)
        - [Upload Object Part](object/multipart/upload_multipart.html)
        - [Copy Object Part](object/multipart/copy_multipart.html)
        - [List Multipart](object/multipart/list_multipart.html)
        - [Abort Multipart Upload](object/multipart/abort_multipart_upload.html)
        - [Complete Multipart Upload](object/multipart/complete_multipart_upload.html)