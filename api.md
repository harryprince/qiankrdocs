FORMAT: 1A
HOST: http://121.201.7.126/

# 千刻开发者API文档

千刻为前端的JS、iOS工程师快速开发提供一份简单的API文档。

# 千刻开发者API文档  [/]


## 获取首页信息 [GET]

+ Response 200 (application/json)

        {
            "users_url": "/user"
        }

## 获取用户登录信息 [GET]

+ Response 200 (application/json)

        {
            "main_url": "/main"
        }

## 用户信息 [/user/{user_id}]

获取的用户信息如下:

+ username
+
+
+
+
+ Parameters
    + user_id: 1 (required, number) - 一个Int型的user id

### 查看用户信息详情

+ Response 200 (application/json)

        {
            "question": "Favourite programming language?",
            "published_at": "2014-11-11T08:40:51.620Z",
            "url": "/questions/1",
            "choices": [
                {
                    "choice": "Swift",
                    "url": "/questions/1/choices/1",
                    "votes": 2048
                }, {
                    "choice": "Python",
                    "url": "/questions/1/choices/2",
                    "votes": 1024
                }, {
                    "choice": "Objective-C",
                    "url": "/questions/1/choices/3",
                    "votes": 512
                }, {
                    "choice": "Ruby",
                    "url": "/questions/1/choices/4",
                    "votes": 256
                }
            ]
        }

## Choice [/questions/{question_id}/choices/{choice_id}]

+ Parameters
    + question_id: 1 (required, number) - ID of the Question in form of an integer
    + choice_id: 1 (required, number) - ID of the Choice in form of an integer

### Vote on a Choice [POST]

This action allows you to vote on a question's choice.

+ Response 201

    + Headers

            Location: /questions/1

## 专辑集合 [/album{?page}]

+ Parameters
    + page: 1 (optional, number) - The page of albums to return

### 列出所有专辑

+ Response 200 (application/json)

    + Headers

            Link: </questions?page=2>; rel="next"

    + Body

            [
                {
                    "question": "Favourite programming language?",
                    "published_at": "2014-11-11T08:40:51.620Z",
                    "url": "/questions/1",
                    "choices": [
                        {
                            "choice": "Swift",
                            "url": "/questions/1/choices/1",
                            "votes": 2048
                        }, {
                            "choice": "Python",
                            "url": "/questions/1/choices/2",
                            "votes": 1024
                        }, {
                            "choice": "Objective-C",
                            "url": "/questions/1/choices/3",
                            "votes": 512
                        }, {
                            "choice": "Ruby",
                            "url": "/questions/1/choices/4",
                            "votes": 256
                        }
                    ]
                }
            ]

### 创建新专辑 [POST]

You may create your own question using this action. It takes a JSON
object containing a question and a collection of answers in the
form of choices.

+ question (string) - The question
+ choices (array[string]) - A collection of choices.

+ Request (application/json)

        {
            "question": "Favourite programming language?",
            "choices": [
                "Swift",
                "Python",
                "Objective-C",
                "Ruby"
            ]
        }

+ Response 201 (application/json)

    + Headers

            Location: /questions/2

    + Body

            {
                "question": "Favourite programming language?",
                "published_at": "2014-11-11T08:40:51.620Z",
                "url": "/questions/2",
                "choices": [
                    {
                        "choice": "Swift",
                        "url": "/questions/2/choices/1",
                        "votes": 0
                    }, {
                        "choice": "Python",
                        "url": "/questions/2/choices/2",
                        "votes": 0
                    }, {
                        "choice": "Objective-C",
                        "url": "/questions/2/choices/3",
                        "votes": 0
                    }, {
                        "choice": "Ruby",
                        "url": "/questions/2/choices/4",
                        "votes": 0
                    }
                ]
            }
