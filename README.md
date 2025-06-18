
# Splic Docs: Splitting Huge Transcript Documents into Individual Transcripts

QDR often receives transcripts consisting of multiple compiled interviews or stories, which sometimes need to be manually split into individual scripts. While Microsoft Word offers features to do this manually, the process is time-consuming and repetitive. This code aims to automate the splitting process efficiently.

## Why Use This?

Manual splitting requires:
- Opening each new document
- Copy-pasting content
- Renaming and saving files individually

This code automates all of that by:
- Identifying specific heading patterns
- Automatically splitting the transcript into multiple documents
- Saving each section as a new document

## Requirements Before Running the Code

1. **Formatting Consistency**:
   - Ensure the document has consistent formatting in terms of font, size, and color.
   - This can be addressed during the de-identification process.

2. **Consistent Headings**:
   - Most transcripts begin with a consistent pattern like `## Respondent 1: XYZ` or `## Respondent ABC`.
   - The script uses this heading (`## Respondent`) to detect where each new transcript begins.

3. **Custom Headings**:
   - If your document uses different headings like `Interview 1`, simply search (`Ctrl + F`) for `## Respondent` in the code and replace it with your desired pattern (`Interview`).
   - This will ensure the split occurs based on your custom headings.

## For Inconsistent or Manual Headers

- If headings are inconsistent or absent, add `## Respondent` at each point where a new transcript begins.
- After the documents are split, you can delete these manually inserted headings from the resulting documents.
- Alternatively, coordinate with the data depositor to use a unique marker like `START`, `**`, or something meaningful at the top of each transcript. This can be used as a reliable anchor for splitting.

## Summary

This tool saves time, reduces manual effort, and improves the accuracy and consistency of transcript management. With minimal formatting effort, you can make transcript processing much quicker and more automated.
