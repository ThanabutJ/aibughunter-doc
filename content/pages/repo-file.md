---
title: "Repository - File page"
date: 2021-11-14T00:54:05+07:00
---

[js file example](/example/page-repo-file.ts "example file")

![page screenshot](/screenshots/page-repository-file.png "screenshot")


## typescript
```typescript
type RepoFilePage{
    fileName: string;
    grade: Grade;
    sourceCode: string;
    summary: FileSummary;
    fileWarning: FileWarning;
}

type FileSummary{
    stepMetric: StepMetric[];
}

type Grade = "A" | "B" | "C" | "D"
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

### Keys 
#### fileType
list of file types available [here](https://github.com/react-syntax-highlighter/react-syntax-highlighter/blob/master/AVAILABLE_LANGUAGES_HLJS.MD)

This will be determined by file extension in the future.


## Ref types
- [File/LineWarning](/types/line-warning)
    - for type `FileWarning`
- [StepMetric](/types/components/step-metric/)
