---
title: "Suggestion"
---

![screenshot](/screenshots/compo-suggestion.png "screenshot")

## Typescript
Using type Suggestion from [LineWarning](/types/line-warning)
```typescript
interface Suggestion {
    warningCodeStr: string;
    fileName: string;
    line: number;
    description: string;
    codeSuggestions: string[];
}
```

## Example

See [type LineWarning](/types/line-warning)
