# Users

| Column    | Type    | Options     |
| --------- | ------- | ----------- |
| nickname  | string  |  null: false        | 
| username  | string  |         null: false         |
| email           | string  | null: false, unique: true |
| encrypted_password | string  | null: false         |

### Association

- Recipes: has_many
- Likes: has_many

# Recipes

| Column       | Type    | Options     |
| ------------ | ------- | ----------- |
| title        | string  |    null: false          |
| description  | string  |    null: false          |
| user_id      | integer | foreign key |

### Association

- User: belongs_to

# Likes

| Column    | Type    | Options     |
| --------- | ------- | ----------- |
| user_id   | integer | foreign key |
| recipe_id | integer | foreign key |

### Association

- User: belongs_to
- Recipe: belongs_to
