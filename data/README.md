# Freelance Data Management

This directory contains the data files for the interactive freelance dashboard.

## How to Update Your Dashboard Data

The dashboard displays data from `freelance-data.json`. To update the information shown on your dashboard:

1. Open [`freelance-data.json`](freelance-data.json) in any text editor
2. Modify the values according to the structure below
3. Save the file
4. Refresh the freelance data page to see your changes

## Data Structure

### Overview Section
```json
"overview": {
  "totalProjects": 24,      // Total number of completed projects
  "totalClients": 18,       // Total number of clients
  "yearsActive": 3,         // Years in business
  "successRate": 100        // Success rate percentage (0-100)
}
```

### Industries Section
Add or modify industries you've worked in:
```json
"industries": [
  {
    "name": "SaaS & Technology",  // Industry name
    "projects": 12,               // Number of projects
    "percentage": 50              // Percentage of total projects
  }
]
```

### Company Sizes Section
Update the distribution of company sizes:
```json
"companySizes": [
  {
    "size": "1-10 employees",  // Company size range
    "count": 8                 // Number of clients in this range
  }
]
```

### Top Reviews Section
Add your best client testimonials:
```json
"topReviews": [
  {
    "rating": 5.0,                           // Rating (1.0-5.0)
    "review": "Client testimonial text...",  // The review text
    "client": "CEO, SaaS Startup",           // Client role and company
    "project": "Process Documentation"       // Project type
  }
]
```

### Project Types Section
Track different types of projects you've completed:
```json
"projectTypes": [
  {
    "type": "Process Mapping",  // Project type name
    "count": 15,                // Number of projects
    "avgDuration": "4 weeks"    // Average project duration
  }
]
```

## Tips

- Make sure the percentages in the "industries" section add up to 100
- Keep the JSON format valid (proper commas, brackets, and quotes)
- Use a JSON validator if you're unsure about syntax: https://jsonlint.com/
- Backup the file before making significant changes

## Example: Adding a New Industry

```json
{
  "name": "Manufacturing",
  "projects": 3,
  "percentage": 10
}
```

Don't forget to adjust other industry percentages so the total remains 100%!
