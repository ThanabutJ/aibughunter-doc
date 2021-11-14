---
title: "Repository - File page"
date: 2021-11-14T00:54:05+07:00
---

[json file example](/example/page-repo-file.js "example file")

![page screenshot](/screenshots/page-repository-file.png "screenshot")


## typescript
```typescript
type RepoFilePage{
    fileName: string;
    fileType: string;
    grade: Grade;
    sourceCode: string;
    lineWaring: LineWaring[];
    summary: FileSummary;
}

type FileSummary{
    stepMetric: StepMetric[];
}

type Grade = "A" | "B" | "C" | "D"
```

### keys 
#### fileType
list of file types available [here](https://github.com/react-syntax-highlighter/react-syntax-highlighter/blob/master/AVAILABLE_LANGUAGES_HLJS.MD)

This will be determined by file extension in the future.


types
- [LineWarning](/types/line-warning)
- [StepMetric](/types/components/step-metric/)
