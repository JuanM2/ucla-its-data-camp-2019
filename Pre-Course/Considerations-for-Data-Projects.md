# Considerations for Data Projects
Take a look at the [Cookiecutter Data Science Page](https://drivendata.github.io/cookiecutter-data-science/) for some general guidelines for data science projects. 
### Use Notebooks to Tell the Data Story
For this course we will be working with Notebooks. A Notebook is a small web-based application that combines code, text, and visualizations into one logical place. This makes it easy to communicate the work of your project to others. The most widely used type of notebook is the Jupyter Notebook, developed by [Project Jupyter](https://jupyter.org/), and included within our Anaconda installation. The project's namesake refers to the multitude of supported languages ("Ju"=Julia, "Py"=Python, "R"=R) supported, though it is primarily used for Python projects.
### Keep Your Projects Organized

Staying organzied will make it easy for someone else (or you at a later date!) to quickly navigate the project and make changes when needed. As with code Style Guides, there is no one way to organize your project, and you should pay attention to the particulars of your project to help you make decisions. A project might have the following directory structure:

```
prj/                  <- Project name  
├── src/              <- Any code for this project that is not contained within the notebook  
├── data/  
│   ├── raw/          <- Raw data, exactly as you received it  
│   └── processed/    <- Data that has been processed as part of the project  
├── doc/              <- Additional documentation (output PDFs, etc) 
├── fig/              <- Figures / images generated from notebook
├── output/           <- Any other output (model, etc)
└── prj.ipynb         <- Jupyter Notebook(s)
```
### Make your Projects Reproducible
You should aim for your data projects to be reproducible. With minimal effort, someone should be able to download your project and run your notebook to obtain the same results. One way to put this into practice is to make sure that you keep your data immutable - that it is never written over. Instead, maintain versions of the data, such as "raw" and "processed".
### Write Readable Code
Notebooks go a long way to help make your work understandable by others. However, in addition to providing appropriate narrative, structure, and visualization for your project, it is also good practice to be comfortable with writing clean code and commenting where necessary. This makes it easy for those who want to re-use or modify your code to understand what is happening.

##### Style Guides Provide Guidance
Most programming languages have at least one gtyle guide to help you format your code in a way that will be easily read and understood by others. The most popular style guide for Python is [PEP-8 -- Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/). Take some time to read through this document to get a sense of what you _should_ do, what you _shouldn't_ do, and what you _may_ do. Even more important than following a particular style guide is to keep your code syntax _consistent_ throughout the project. There are multiple ways to write readable code, but changing your syntax midway through a project will make it difficult to follow.

##### Add Comments where Necessary 
In addition to following conventional code guidelines, it also helps others if you place terse & descriptive comments throughout your code, which you can do by placing a `#` at the beginning of your code line. For Example:

```python
# This is a comment. Extend it by adding another "#" at the beginning of each line.
# The next 2 lines have code that will be interpreted by Python.
def hi():
    print('Hello World') # You can also comment inline, like this.
```