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
