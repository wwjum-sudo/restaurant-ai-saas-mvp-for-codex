# Fields v1

## Users
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| phone | string | yes | login phone |
| role | enum | yes | boss / manager |
| name | string | no | display name |
| created_at | datetime | yes | created time |

## Stores
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| owner_user_id | uuid | yes | boss user id |
| store_name | string | yes | store name |
| city | string | yes | city |
| category | string | yes | cuisine/category |
| area_size | number | no | sqm |
| staff_count | number | no | current staff count |
| has_delivery | boolean | yes | delivery enabled |
| created_at | datetime | yes | created time |

## Weekly reports
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| store_id | uuid | yes | store reference |
| report_week | string | yes | week identifier |
| revenue | number | yes | weekly revenue |
| orders_count | number | yes | weekly order count |
| dine_in_revenue | number | no | dine-in revenue |
| delivery_revenue | number | no | delivery revenue |
| food_cost | number | no | food cost |
| labor_cost | number | no | labor cost |
| rent_cost | number | no | weekly allocated rent |
| marketing_cost | number | no | promo/ad spend |
| hot_items_text | text | no | top-selling items |
| slow_items_text | text | no | slow-selling items |
| note_text | text | no | manager notes |
| created_by | uuid | yes | input user |
| created_at | datetime | yes | created time |

## OCR uploads
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| store_id | uuid | yes | store ref |
| image_url | string | yes | uploaded image |
| raw_text | text | no | OCR result |
| detected_vendor | string | no | vendor |
| detected_amount | number | no | extracted amount |
| detected_category | enum | no | rough category |
| confirmed_category | enum | no | manager-confirmed category |
| status | enum | yes | pending / confirmed |
| created_at | datetime | yes | created time |

### OCR categories v1
- vegetables
- meat
- seasoning
- office
- delivery_supplies
- other

## Issue results
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| weekly_report_id | uuid | yes | report ref |
| issue_type | enum | yes | issue type |
| severity | enum | yes | low / medium / high |
| title | string | yes | issue title |
| summary | text | yes | issue summary |
| status | enum | yes | open / closed |
| created_at | datetime | yes | created time |

## Action cards
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| issue_result_id | uuid | yes | issue ref |
| store_id | uuid | yes | store ref |
| card_title | string | yes | title |
| action_text | text | yes | recommended action |
| why_text | text | no | why this action |
| verify_text | text | no | how to validate |
| priority | number | yes | sorting priority |
| assigned_to | uuid | no | manager user id |
| due_date | date | no | target completion |
| status | enum | yes | draft / assigned / done / review |
| created_at | datetime | yes | created time |

## Action feedback
| Field | Type | Required | Notes |
|---|---|---|---|
| id | uuid | yes | primary key |
| action_card_id | uuid | yes | action card ref |
| executed | boolean | yes | whether executed |
| feedback_text | text | no | feedback |
| image_url | string | no | proof image |
| result_summary | text | no | result summary |
| created_by | uuid | yes | feedback user |
| created_at | datetime | yes | created time |
