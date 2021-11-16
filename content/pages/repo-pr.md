---
title: "Repository - PR"
date: 2021-11-14T00:54:05+07:00
---

[js file example](/example/page-pr-file.ts "example file")

![page screenshot](/screenshots/page-repository-pr.png "screenshot")

## typescript
```typescript
type RepoPRPage{
    topSection: TopSection;
    rawGitDiffOutput: string;    
    summary: FileSummary;
    fileWarnings: FileWarning[];
}

type TopSection {
    title: string;
    priority: "high" | "medium" | "low";
    totalFileChange: number;
    totalWarning: number;
    totalLineChange: number;
}

type FileSummary{
    stepMetric: StepMetric[];
}

```

> NOTE THAT any multiline string must be inside ` `` ` like example below
```typescript
const sourceCode = `
    const renderFile = ({oldRevision, newRevision, type, hunks}) => (
    <Diff key={oldRevision + '-' + newRevision} viewType="split" diffType={type} hunks={hunks}>
        {hunks => hunks.map(hunk => <Hunk key={hunk.content} hunk={hunk} />)}
    </Diff>
);`
```


## Ref types
- [File/Line Warning](/types/line-warning)
    - for type `FileWarning`
- [StepMetric](/types/components/step-metric/)
