# テーブル設計

  ## usersテーブル

| Column             | Type   | Options     |
| ------------------ | ------ | ----------- |
| email              | string | null: false |
| password           | string | null: false |
| name               | string | null: false |
| profile            | text   | null: false |
| occupation         | text   | null: false |
| position           | text   | null: false |

  ### Association

- has_many :comments
- has_many :prototypes

  ## commentsテーブル

| Column             | Type       | Options     |
| ------------------ | ------     | ----------- |
| text               | text       | null: faise |
| user               | references |             |
| prototype          | references |             |

  ### Association

- belongs_to user
- belongs_to prototype

  ## prototypesテーブル

| Column             | Type       | Options     |
| ------------------ | ------     | ----------- |
| title              | string     | null: faise |
| catch_copy         | text       | null: faise |
| concept            | text       | null: faise |
| user               | references |             |