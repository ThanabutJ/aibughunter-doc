---
title: "Repository - File page"
date: 2021-11-14T00:54:05+07:00
draft: true
---

[json file example](/json/file-detail.json "example file")

![page screenshot](/screenshots/page-repository-file.png "screenshot")


## typescript
```typescript
type RepoFilePage{
    fileName: string;
    grade: string;
    sourceCode: string;
    lineWaring: LineWaring[];
    Summary: FileSummary;
}

type FileSummary{
    stepMetric: StepMetric[];
}
```

types
- [LineWarning](/types/line-warning)
- [StepMetric](/types/components/step-metric/)
