---
title: "File/Line Warning"
date: 2021-11-14T01:22:14+07:00
---

```typescript
type FileWarning {
    fileName: string;
    fileType: string;
    fileID: number;
    lineWarings: LineWarning[];
}

interface LineWarning {
    line: number;
    suggestions: Suggestion[];
}

interface Suggestion {
    matchingStr: string;
    fileName: string;
    line: number;
    description: string;
    codeSuggestions: string[];
}
```

## Example
example in js array format

```typescript
const fileWarning: FileWarning = {
    fileName:  "metrices_test.py",
    fileType: "python",
    lineWarnings: lineWarnings, //from variable below
}

const lineWarnings: LineWarning[] = [
    {
        line: 4,
        suggestions: [
            {
                fileName: "metrices_test.py",
                line: 4,
                description: `urpis. Mauris rutrum efficitur porttitor. Cras rhoncus, justo sit amet congue viverra, sapien quam aliquam neque, erat enim eu ,
Donec vel scelerisque nulla. Nunc ante mi, pretium non ornare convallis, lobortis at nisi. Integer at facilisis dolor. Etiam iaculis urna a nibh porta elementum. Aliquam vestibulum ornare congue. Sed elementum ante ac ex aliquam, eget sodales nunc ultrices. Sed urna elit, ultrices nec gravida at, accumsan vel elit. Cras tincidunt mauris quis risus sollicitudin, sit amet ultrices lectus varius.`,
                matchingStr: "codeString",
                codeSuggestions: [
                    `const renderFile = ({oldRevision, newRevision, type, hunks}) => (
    <Diff key={oldRevision + '-' + newRevision} viewType="split" diffType={type} hunks={hunks}>
        {hunks => hunks.map(hunk => <Hunk key={hunk.content} hunk={hunk} />)}
    </Diff>
);`,
                    `const codeString = '(num) => num + 1';`,
                    `<SyntaxHighlighter language="javascript" style={docco}>
            {1}
</SyntaxHighlighter>
`,
                ],
            },
        ],
    },
    {
        line: 7,
        suggestions: [
            {
                matchingStr: "Hello",
                fileName: "metrices_test.py",
                line: 7,
                description:
                    "urpis. Mauris rutrum efficitur porttitor. Cras rhoncus, justo sit amet congue viverra, sapien quam aliquam neque, erat enim eu ",
                codeSuggestions: [
                    `<SyntaxHighlighter language="javascript" style={docco}>
    {1}
</SyntaxHighlighter>`,
                    `const codeString = '(num) => num + 1';
const codeString = '(num) => num + 1';


const codeString = '(num) => num + 1';
const codeString = '(num) => num + 1';
const codeString = '(num) => num + 1';
`,
                ],
            },
        ],
    },
    {
        line: 8,
        suggestions: [
            {
                matchingStr: "</",
                fileName: "metrices_test.py",
                line: 8,
                description: `Nullam malesuada rhoncus diam, in elementum lectus luctus sed. Aliquam ac metus velit. Nullam vel sem et odio sagittis volutpat. Suspendisse potenti. Nunc id orci mollis, sollicitudin metus vel, faucibus enim. In a libero eget nunc pellentesque volutpat sit amet sed sapien. Suspendisse in nisi turpis. Vestibulum aliquet, tortor vitae dignissim finibus, odio lorem maximus leo, nec interdum mauris dolor id nibh. Nulla iaculis odio enim, quis porta magna mollis ac.

Donec vel scelerisque nulla. Nunc ante mi, pretium non ornare convallis, lobortis at nisi. Integer at facilisis dolor. Etiam iaculis urna a nibh porta elementum. Aliquam vestibulum ornare congue. Sed elementum ante ac ex aliquam, eget sodales nunc ultrices. Sed urna elit, ultrices nec gravida at, accumsan vel elit. Cras tincidunt mauris quis risus sollicitudin, sit amet ultrices lectus varius.`,
                codeSuggestions: [
                    `<SyntaxHighlighter language="javascript" style={docco}>
    {1}
</SyntaxHighlighter>`,
                ],
            },
        ],
    },
];

```
