# Page Map v1

## Information architecture
```text
Login / Role recognition
├── Boss
│   ├── Overview
│   ├── Store list
│   ├── Store detail
│   ├── Action card center
│   ├── Task/feedback center
│   └── Weekly review
└── Manager
    ├── Daily todo
    ├── Data entry
    ├── OCR-assisted upload
    ├── Task feedback
    └── Store summary
```

## Boss pages
### Overview
- period filter
- total store status cards
- top issues this week
- pending action cards
- store status list
- last-week review summary

### Store list
- store name
- weekly revenue
- status label
- issue summary
- pending task count

### Store detail
- store basic info
- key weekly metrics
- issue summary
- action cards
- past execution results
- manager feedback history

### Action card center
- to assign
- assigned
- completed
- pending review

### Task / feedback center
- pending feedback
- submitted feedback
- overdue feedback

### Weekly review
- what was done
- what worked
- what failed
- what to continue / adjust

## Manager pages
### Daily todo
- data to enter
- assigned tasks
- pending feedback
- alerts

### Data entry
- weekly revenue
- order count
- dine-in revenue
- delivery revenue
- purchase amount
- food cost
- labor cost
- notes

### OCR-assisted upload
Flow: take photo → OCR extract → rough category → manager confirms → save

### Task feedback
- task title
- done / not done
- feedback text
- optional image proof

### Store summary
- brief weekly store status
- pending issues
- completed tasks
