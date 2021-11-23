---
title: "Repository - PR Page"
date: 2021-11-14T00:54:05+07:00
---


![page screenshot](/screenshots/page-repository-pr.png "screenshot")

## JSON Object Types
[RepoPRPage js file example](/example/page-pr-file.ts "example file")

**filewarnings**

[FileWarning js file example](/example/page-pr-file-warning.ts "example file") and [FileWarning json file example](/example/page-pr-file-warning.ts "example file")

```typescript
// Main object for the page
type RepoPRPage{
    pageSummary: PageSummary;
    rawGitDiffOutput: string;    
    metricSummary: MetricSummary;
    fileWarnings: FileWarning[];
}
```

### Subtypes
```typescript
type PageSummary {
    title: string;
    priority: "high" | "medium" | "low";
    totalFileChange: number;
    totalWarning: number;
    totalLineChange: number;
}

type MetricSummary{
    stepMetric: StepMetric[];
}
```
### Link to Other type 
- [File/Line Warning](/types/line-warning)
    - for type `FileWarning`
- [StepMetric](/types/components/step-metric/)

## NOTE
> any multiline string must be inside ` `` ` like example below
```typescript
const sourceCode = `
    const renderFile = ({oldRevision, newRevision, type, hunks}) => (
    <Diff key={oldRevision + '-' + newRevision} viewType="split" diffType={type} hunks={hunks}>
        {hunks => hunks.map(hunk => <Hunk key={hunk.content} hunk={hunk} />)}
    </Diff>
);`
```


