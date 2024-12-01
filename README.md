# Hi there 👋

<!--
**alejandromumo/alejandromumo** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

🔭 I’m currently working on [Zenodo](https://zenodo.org/), an open-access digital repository for research data, built to ensure everyone can join Open Science.

👯 Part of the [InvenioRDM](https://inveniosoftware.org/products/rdm/) community and core developer of the [InvenioRDM framework](https://inveniordm.docs.cern.ch/).

# 😎 Things I built so far

At Zenodo, I worked on multiple features such as:

## European Open Repository Collections

Collections organize the contents of a Zenodo community in logical sets of records. For the European Open Repository, these can be a set of records that share the same funding or are from the same discipline (e.g. `Natural Sciences`).

Have a look at the screenshots:

<img width="1080" alt="browse page of a community with collections" src="https://github.com/user-attachments/assets/58bc8207-b636-468f-8d03-c447117a5f3e">

Each collection can then be accessed to inspect its contents:

<img width="1080" alt="collection of natural science records" src="https://github.com/user-attachments/assets/31d91c98-fb51-4623-841a-f9c63169ef65">

These records can be further filtered by using the left-hand facets, providing multiple layers of organization and discoverability of the community contents.

### 🤓 How it works

The underlying concept of collections is that they are tree-like structures that store an OpenSearch query (to fetch the records). Therefore, we store each collection in the DB as a tree-like structure using the materialized path pattern. Here is a nice guide from the MongoDB folks: 

- [Model Tree Structures with Materialized Paths](https://www.mongodb.com/docs/manual/tutorial/model-tree-structures-with-materialized-paths/)

If you are curious (and courageous), you can read the [Request for Comments](https://github.com/inveniosoftware/rfcs/blob/master/rfcs/rdm-0079-collections.md) document where all the technical nuts and bolts are discussed.

📺 See this feature live at Zenodo 📺

- https://zenodo.org/communities/eu/browse

## Zenodo and Software Heritage integration

Zenodo archives openly disseminated software source code in Software Heritage, in a combined effort to "create an interconnected and interoperable academic ecosystem, (...) contributing to the global software commons" ([blog post](https://blog.zenodo.org/2024/10/21/2024-10-21-swh/))

This means that Zenodo needed to:
- Support software field in its metadata schema
- Integrate with Software Heritage
- Support metadata formats that are suited for the serialization of software-type records

Have a look at some screenshots of this feature:

<img width="903" alt="zenodo upload form with software fields" src="https://github.com/user-attachments/assets/421bd531-2209-4152-8a56-bff804b82dee">

Zenodo's deposit form supports software-specific fields, including a controlled vocabulary of programming languages. 

<img width="390" alt="zenodo record archived in software heritage" src="https://github.com/user-attachments/assets/bfd56e8c-57ea-4758-aeb7-c94d28fbb4c6">

After a record is archived in Software Heritage, the user can navigate to the archive's landing page.

<img width="350" alt="image" src="https://github.com/user-attachments/assets/a82421a3-a049-4968-ae42-f86096e2b3bf">

New export formats were added to support the serialization of software records to common software formats (e.g. `CITATION.cff` and `CodeMeta`)

At the time of this writing, more than 5000 software records have been archived using this integration!



