# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...


## Models
- Users
    - id: integer [unique]
    - username: string [unique, 4-20 chars, present]
    - password: string [4-20 chars, present]
    - email: string [unique, present]
    - created_at:datetime
    - updated_at:datetime
    - NOTE: has_many comments
    - NOTE: has_many posts
- Posts
    - id: integer [unique]
    - title: string [present]
    - body: text [present]
    - user_id: integer [present]
    - created_at:datetime 
    - updated_at:datetime
    - NOTE: has_many comments
- Comments
    - id: integer [unique]
    - body: text [present]
    - user_id: integer [present]
    - post_id: integer [present]
    - created_at:datetime
    - updated_at:datetime
    - belongs_to user
    - belongs_to post


