# README

# アプリ名
search_app

# URL
Herokuによるデプロイ
https://search-app-20201229.herokuapp.com/

# 説明

[ransack](https://github.com/activerecord-hackery/ransack)というgemを導入し、複数条件にあった検索や「〜以下」の検索条件で商品を選択のうえ結果を表示することができます。


# テーブル設計

## categories テーブル

| Column   | Type    | Options     |
| :------- | :-----  | :---------- |
| name     | string  | null: false |

### Association

- has_many :products

<br>

## products テーブル

| Column   | Type       | Options           |
| :------- | :--------- | :---------------- |
| name     | string     | null: false       |
| size     | string     | null: false       |
| status   | string     | null: false       |
| price    | integer    | null: false       |
| category | references | foreign_key: true |


### Association

- belongs_to :category

# clone
```
% git clone https://github.com/erika618/search_app.git
% cd search_app
% bundle install
% yarn install
% rails db:create
% rails db:migrate
% rails db:seed
```
