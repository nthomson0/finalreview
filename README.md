# written 50%
two JSON files: soccer players, games they've played

four questions related to the json:
first 3 questions related to reading the soccer players json
4th question related to reading the games json

question 1: something like, who is the tallest soccer player? write code that grabs that player by looping and comparing height

question 4: reading both files and comparing
to get 100%: read the lists in parallel, not one at a time
probably use promises, either async await or .then

example structure:
```
const fs = require("fs/promises");

async function main() {
    // Takes an array of operations and runs them in parallel
    const [file1, file2] = await Promise.all([fs.readFile("file1.json", "utf8"), fs.readFile("file2.json", "utf8")]) 

    // Same as above but runs file1 then file2, do not do this
    // const file1 = await fs.readFile("file1.json");
    // const file2 = await fs.readFile("file2.json");
}

// then we can make helper function for the questions:
function question1(data) {
    //If given a JSON:
    const dict = JSON.parse(data); // parses the data into a regular dictionary
    dict.forEach(); // Use the data in some way

    //if given a CSV
    const csv = data.split(EOL);

}

// then run the questions
question1(file1);
question2(file1);
question3(file1);
question4(file1, file2);
```

# mc/tf 50%
some questions are EXACTLY same as midterm (the hard questions)

## format
rest of the questions coming from express.js
most of the questions are coming from week 9 pdf
watch the express workshop lectures from week 9
difference between req.query and req.params

## questions 1
2 questions related to streams, otherwise no stream stuff
do you always get faster performance if you use streams? answer is no, only with large files it makes a big difference
png js question: read documentation related to pngjs, understand what type of stream the `new PNG({ filterType: 4,})` should be transform

## questions 2
1 question related to database
what is the bridge that facilitates the communication between flask or express and SQL? database driver