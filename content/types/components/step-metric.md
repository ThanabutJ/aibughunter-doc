---
title: "Step Metric"
---

![screenshot](/screenshots/compo-step-metric.png "screenshot")

## typescript

```typescript
export type StepMetric = {
  title: string;
  score: number;
  maxScore: number;
  recommendedScore: number;
  icon: IconGuildLine;
  showRecommendTag: boolean;
  type: "hsb" | "lsb";
  unit?: string;
};

type IconGuildLine = "shield" | "document" | "compass";
```

## JSON

Key | type | default | Description
--- | --- | --- | ---
title | string | | 
score | number | | 
maxScore | number | | 
recommendedScore | number | |
showRecomBadge | boolean | false | 
type | "hsb" \| "lsb" | "hsb" | either "hsb" higher is better or "lsb" lower is better
unit | string | | (optional) 
icon | string(icon) | |

#### icon
(string) "shield" | "document" | "compass"

## Example
example in javascript array

```javascript
[
    {
        title: "Write shoter file",
        icon: "shield",
        showRecommendTag: true,
        score: 1,
        recommendedScore: 2,
        maxScore: 10,
        type: "lsb",
        unit: "MB",
    },
    {
        title: "Reduce complexity",
        icon: "document",
        showRecommendTag: true,
        score: 6,
        recommendedScore: 4,
        maxScore: 10,
        type: "lsb",
    },
    {
        title: "Increase Reviewer",
        icon: "compass",
        showRecommendTag: false,
        score: 9,
        recommendedScore: 4,
        maxScore: 12,
        type: "hsb",
    },
]
```
