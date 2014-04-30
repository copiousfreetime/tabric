# What is your project, Explain what you propose to build as a result of this grant

I propose to create Tabric, a human-readable, table-oriented file format
specification that includes provisions for data integrity and quality. I will
create full implementations of specification in a variety of programming
languages (initially Ruby and Python) for reading and writing the format, and
conversion utilties between it and other popular file formats. Namely CSV (Comma
Separated Values) and Avro.

# Who is the audience/user of this project? How will they be impacted? What challenge/need are you addressing? Why do you believe this approach will work?

Tabric is a tool for anyone involved in open data, data journalism, data
analysis, data quality, or similar spaces. This new file format and the tools
surrounding it will reduce the effort it takes in having to do data conversion,
analysis, and quality assurance with their data.

Currently, when doing any sort of data analysis or investigation, using one or
more 3rd party data sets, the data must first be converted to a common, easily
usable format. Many times this is CSV. CSV is a good enough general format for
some purposes, but does not support other aspects of data quality and data
integrity checking that are useful for long term usage or more rigorous
analysis.

In particular, the ability to record the data types and formats of the
individual columns of the data, noting the valid constraints (for instance
bounds checking) to be placed on the values, annotate the data set as a whole
with additional meta data, and have all of this additional meta data be built
into the file format and usable by the tools that manipulate the data.

The challenge being addressed is the need for a standard and specification for a
"better CSV". I want to take the best aspects of CSV, specifically the human
readability and the record oriented format, combine that with data type
checking, the anti data-corruption aspects, and the Hadoop friendliness of the
Avro Container Format, all the while keeping the meta data overhead of the file
to a minimum (i.e. the repetition of XML tags and JSON field names).

I think this combines the best aspects of all the commonly used data file
formats together, and removes the portions that are detrimental into a nice,
easily usable and understandable file that is usable by both technologists and
intuitive to non-technologists alike.

# Who is on your team -- describe your team members background and experience

Jeremy Hinegardner - A programmer and data wrangler with 10+ years of experience
dealing with data quality, movement and storage.

# What assumptions will you test -- How will you know if the project worked or not.

The major assumption being tested is, is there a widespread need for a tool like
this? 

I will consider the project successful if people start using the libraries and
tools developed, and other people also implement the specificiation in their
programming languages of choice.

# What have you made so far.

So far, there has been initial discussion of the goals of the file format, a
considerable amount of research into seeing if there are existing formats that
meet the goals, and some initial rough drafts of the specification.
