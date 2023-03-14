# AI Study Notes

## Summary
This is a collection of my AI notes on SoftUni's course in Artificial Intelligence. The notes are in English and Bulgarian: I found that translating a phrase helps me better grasp the material. The course had four parts: Math and Statistics, Data Science, Machine Learning, and Deep Learning.

There are undoubtedly inaccuracies, the formatting is also not always pretty. However, I created the book mainly for myself, as a way to combine all information in one document and easily access it online. Below is also a list of my projects so far.

## Update procedure
To update the book, run the following commands:
- in parent folder (of the main folder):
	- `conda activate ENVNAME`
	- `jb build 2023-ai-study-notes`
- in the main folder:
	- `cd 2023-ai-study-notes` 
	- `git add`, `commit` and `push`
	- `ghp-import -n -p -f _build/html`