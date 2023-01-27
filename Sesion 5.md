{
 "cells": [
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "# Session 04\n",
    "\n",
    "## Python Programming\n",
    "\n",
    "![Course Hero](images/hero.png)\n",
    "\n",
    "As we saw earlier, Python has several variable types:\n",
    "\n",
    "- Strings: `\"David\"`\n",
    "- Numbers: `10` or `3.14.15`\n",
    "- Booleans: `True` and `False`\n",
    "\n",
    "And even some more specific ones:"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "from datetime import datetime\n",
    "\n",
    "right_now = datetime.now()\n",
    "print(right_now)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "But we also have **Data Structures**. These are way to store related data.\n",
    "\n",
    "## Lists\n",
    "\n",
    "It lets us store several pieces of information in a single variable, it is ordered, mutable (we can change the elements) and allows duplicates."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_list = [3, 6, 9, 2, 3]\n",
    "print(my_list)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Experiment with some list methods:\n",
    "\n",
    "- Indexing and Splitting: `list[start:end:step]`\n",
    "- Length: `len(list)`\n",
    "- Inserting and appending: `list.insert(index, element)` and `list.append(element)`\n",
    "- Removing: `list.remove(element)` and `list.pop(index)`\n",
    "- Sorting: `list.sort()`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "print(my_list[0:2])"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Tuples\n",
    "\n",
    "Similar to lists, but are immutable (we can't change the elements)."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_tuple = (\"we\", \"cannot\", \"add\", \"or\", \"delete\", \"elements\", \"after\", \"creation\")\n",
    "my_tuple2 = \"the\", \"parenthesis\", \"are\", \"optional\"\n",
    "\n",
    "print(my_tuple, my_tuple2)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Experiment with some tuple methods:\n",
    "\n",
    "- Indexing and Splitting: `tuple[start:end:step]`\n",
    "- Length: `len(tuple)`\n",
    "- Unpacking: `var1, var2 = tuple`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "first, second, third, fourth = my_tuple2\n",
    "print(first, second, third, fourth, sep=\"||\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Sets\n",
    "\n",
    "Similar to lists, but the elements cannot be duplicated."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_set = {\"apple\", \"banana\", \"cherry\", \"banana\"}\n",
    "print(my_set)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Experiment with some set methods:\n",
    "\n",
    "- Length: `len(set)`\n",
    "- Inserting and appending: `set.add(element)`\n",
    "- Removing: `set.remove(element)`"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_set.add(\"date\")\n",
    "print(my_set)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## Dictionary\n",
    "\n",
    "This is a collection of key:value values. It is ordered, changeable and the keys cannot be duplicated."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_dictionary = {\n",
    "    \"Name\": \"David\",\n",
    "    \"Age\": 49,\n",
    "    \"Married\": True,\n",
    "    \"Hobbies\": [\n",
    "        \"Movies\",\n",
    "        \"Books\",\n",
    "        \"Comics\",\n",
    "    ],\n",
    "}\n",
    "\n",
    "print(my_dictionary)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "We can improve the visibility using the pprint (Pretty-print) function."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "from pprint import pprint\n",
    "\n",
    "pprint(\n",
    "    my_dictionary,\n",
    "    indent=2,\n",
    "    width=10,\n",
    ")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "As you can see, we can have nested data structures."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "nested_dictionary = {\n",
    "    \"nested_set\": {\"red\", \"green\", \"blue\"},\n",
    "    \"nested_list\": [\"this\", \"one\", \"allows\", \"duplicates\", \"duplicates\"],\n",
    "    \"nested_tuple\": (\"one\", \"two\", \"three\"),\n",
    "    \"nested_dict\": my_dictionary\n",
    "}\n",
    "\n",
    "pprint(nested_dictionary)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## If command"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "if 6 in my_list:\n",
    "    print(\"Yes, 6 is in the list\")\n",
    "elif 9 in my_list:\n",
    "    print(\"No, but 9 is\")\n",
    "else:\n",
    "    print(\"No, no 6 in my_list\")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "## For command"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "The Range function is a `generator`, the data doesn't \"exist\" (consume space in the memory) until it is requested. We have generators in many Python modules."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "range(1,10)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "We can use it in a for loop.\n",
    "\n",
    "Remember, in Python the last value is exclusive, it is not included in the result."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for counter in range(1,10):\n",
    "    print(counter)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "In Python we can use lists in the for loops directly."
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "print(len(my_list))"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "This is the non-Pythonic way of iterating over a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for counter in range(0,len(my_list)):\n",
    "    print(counter, my_list[counter])"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "This is the Pythonic way of iterating over a list"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for element in my_list:\n",
    "    print(element)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "What about if we want the element number?"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for index, element in enumerate(my_list):\n",
    "    print(index, element)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "We can get the keys for a dictionary"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for key in my_dictionary.keys():\n",
    "    print(key, my_dictionary[key], sep=\": \")"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Or the values"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for value in my_dictionary.values():\n",
    "    print(value)"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": [
    "Or both things at the same time"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "for key, value in my_dictionary.items():\n",
    "    if key == \"Name\":\n",
    "        print(\"The recorded Name is \" + value)\n",
    "    if isinstance(value, list):\n",
    "        print(\"The most important \" + key + \" are:\")\n",
    "        for element in value:\n",
    "            print(\"- \", element)"
   ]
  },
  {
   "cell_type": "code",
   "execution_count": null,
   "metadata": {},
   "outputs": [],
   "source": [
    "my_dictionary[\"Books\"] = [\n",
    "    \"The Hitchhikers' Guide to the Galaxy\",\n",
    "    \"The Seder Masochism\",\n",
    "    \"The Phoenix Project\",\n",
    "    \"2034\",\n",
    "]\n"
   ]
  },
  {
   "cell_type": "markdown",
   "metadata": {},
   "source": []
  }
 ],
 "metadata": {
  "kernelspec": {
   "display_name": "Python 3.9.13 ('venv': venv)",
   "language": "python",
   "name": "python3"
  },
  "language_info": {
   "codemirror_mode": {
    "name": "ipython",
    "version": 3
   },
   "file_extension": ".py",
   "mimetype": "text/x-python",
   "name": "python",
   "nbconvert_exporter": "python",
   "pygments_lexer": "ipython3",
   "version": "3.9.13"
  },
  "orig_nbformat": 4,
  "vscode": {
   "interpreter": {
    "hash": "455b77b79d849357f9b743ccea562fca837859d4f59bf8c2736ba0c9f0692a9e"
   }
  }
 },
 "nbformat": 4,
 "nbformat_minor": 2
}
