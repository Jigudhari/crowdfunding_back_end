1.Create User
    curl --request POST \
    --url https://jignasa-crowdfunding-back-end.fly.dev/users/ \
    --header 'Content-Type: application/json' \
    --data '{
        "username": "<insert_unique_username>",
        "email": "<insert_unique_email>",
        "password":"<insert_password>",
    }"

2.Sign in user
    curl --request POST \
    --url https://jignasa-crowdfunding-back-end.fly.dev/api-token-auth/ \
    --header 'Content-Type: application/json' \
    --data '{
        "username": "<insert_unique_username>",
        "password": "<insert_password>"
    }'

3.Create project
    curl --request POST \
    --url https://jignasa-crowdfunding-back-end.fly.dev/projects/ \
    --header 'Content-Type: application/json' \
    --data '{
        "title": "<unique_title>",
        "description": "<project_description>",
        "goal": <integer>,
        "image": "<image_url>",
        "is_open": <boolean>,
        "date_created": "<auto_filled as today>"
    }'