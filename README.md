Daily learning

# __*Creating a Fully Managed Hadoop Ecosystem with Google Cloud Dataproc*__

The challenge is to perform data processing using the Dataproc product from GCP. This processing will count the words of a book and inform how many times each word appears in it.

---

### Challenge Steps

1. Create a bucket in Cloud Storage
1. Update the ```counter.py``` file with the name of the Bucket created in the lines that contain ```{YOUR_BUCKET}```.
1. Upload the ```counter.py``` and ```book.txt``` files to the created bucket (instructions below)
    - https://cloud.google.com/storage/docs/uploading-objects

1. Use the code in a Dataproc cluster, running a PySpark Job calling ```gs://{YOUR_BUCKET}/counter.py```
1. The Job will generate a folder in the bucket called ```result```. Inside this folder the file ```part-00000``` will contain the word list and how many times it is repeated throughout the book.

### Delivery of Result

1. Create a file called ```result.txt```. Inside this file, put the 10 words that are most used in the book, according to the Job result.
2. Insert the files ```result.txt``` and ```part-00000``` in the repository.

[LICENSE](./LICENSE)

---

### Final considerations

NOTE: If the Job shows an Interrupt WARN, just ignore it. There is a bug in Hadoop that is known. This does not impact processing.

Any suggestions, feel free to get in touch.

Nivaldo Beirão - njtsb1@gmail.com
