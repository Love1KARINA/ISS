运行在8081端口
接口名process_image
参数以json格式，如：

````
{
    "image_path": "006.jpg"
}
````

返回值以json格式，如下：

````
{
    "res": [
        [
            -1.0,
            "null"
        ],
        [
            0.40028388238325097,
            "./segment/res/result2.jpg"
        ],
        [
            -1.0,
            "null"
        ],
        [
            -1.0,
            "null"
        ]
    ]
}
````

部署可以考虑将yolo识别结果不保存，污渍识别结果保存在./segment/res/下，mask_image.jpg为总览结果，result*.jpg为单块污渍识别结果，warped_image*.jpg为分割结果（*代表序号）
