# How to add new questions.
Each question and answer is stored in a separate file inside the "_posts" directory. Traditionally files in this directory adhere to the default Jekyll format of having the timestamp and then the name as it would appear in the URL.

However for the FAQ, since there is no need for a date, nor a URL (since they are all on the same page), it has been repurposed.  The year part of the timestamp is now used to determine the FAQ order.  The higher the value, the closer to the top it will be.  The rest is just a label for the file name, it is **not** used at all in rendering the items

Inside the file there are some YAML parameter that need to be set, following by any markdown for the FAQ answer.
```
    ---
    title:  "This is the title of the FAQ"
    anchor: this-is-a-faq-id
    ---
```

There is an optional related question list.  This allows an anchor linking of FAQs to one another.  These are one directional, so if you intend to two questions link to each other, this markup needs to be in both questions YAML.
```
    ---
    title:  "This is the title of the FAQ"
    anchor: this-is-a-faq-id                 
    related:
      - id: this-is-the-faq-id-of-the-related-item
        label: "this is any label you want for the FAQ"
    ---
```
