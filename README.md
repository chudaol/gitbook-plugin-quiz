# gitbook-plugin-quiz
Allows to insert simple quizes into gitbook.

![Link](screenshot.png)

### How to use?

Add plugin to your `book.json`, then run `gitbook install`:

```
{
    plugins: ["quiz"]
}
```

It is possible to configure generic labels and text:

```
"pluginsConfig": {
    "quiz": {
        "labels": {
            "showCorrect" : "",         // default is "Show correct answers"
            "check"       : ""          // default is "Check"
        },
        "text": {
            "noChosen"    : "",         // default is "No answer is chosen"
            "rightAnswer" : "",         // default is "Right answer!"
            "wrongAnswer" : ""          // default is "Wrong answer!"
        }
    }
}
```

Add quiz markup in your gitbook:

```
<quiz name="Gitbook Quiz">
    <question multiple>
        <p>What is gitbook used for?</p>
        <answer correct>To read books</answer>
        <answer>To book hotel named git</answer>
        <answer correct>To write and publish beautiful books</answer>
        <explanation>GitBook.com lets you write, publish and manage your books online as a service.</explanation>
    </question>
    <question>
        <p>Is it quiz?</p>
        <answer correct>Yes</answer>
        <answer>No</answer>
    </question>
</quiz>
```
