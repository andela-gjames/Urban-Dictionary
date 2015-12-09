#Checkpoint One [![StyleCI](https://styleci.io/repos/47337499/shield)](https://styleci.io/repos/47337499)
<p>
    
    In this task, an application that serves as a dictionary for urban words and slangs is created.
    A class was created that contains a static associative array to hold urban words 
    `UrbanWord`. 
    <br/>
    Also, a dictionary class is created that can add, retrieve, update and delete meanings of urban words from 
    `UrbanWord` thrown in as arguments to the class functions. 
    <br/>
    PHPUnit was also used to effectively test classes and functions to ensure they do are effective.
</p>

<h2>Features</h2>

<ul>
  <li><b>Urban Word:</b> A simple app to store new urban words `UrbanWord.php`</li>
  <li><b>UrbanDictionary:</b> A app for manipulating UrbanWord class, to perform basic CRUD operations `UrbanDictionary.php`</li>
  <li><b>Group:</b> A app for manipulating UrbanWord class, to perform basic CRUD operations `Group.php`</li>
  <li><b>Test:</b> Contains test files for the apps in `./src` using PHPUnit Framework</li>
</ul>

<h2>Usage</h2>
To use any of the apps follow the steps below:

<h3>UrbanDictionary</h3>

<h5>Create new Word</h5>
```php
    $urban = new UrbanDictionary();

    //To create new urban word, pass  
    //slang, description and sentence-example respectively
    //to create function the function

    $urban->create
    (
      "Kpom-Kpi",
      "Means to chill, cool-down, mellow",
      "Bros, please can you Kpom-Kpi right there"
    );

```

<h5>Get/Retrieve a word</h5>
```php
    //Get a slang
    $urban->get("Kpom-Kpi"); //Returns an array of the word, description and sentence-example
```

<h5>Update a word</h5>
```php
    //Update Slang
    //Updates the slang/word of Kpom-Kpi to Chillax
    $urban->update("Kpom-Kpi", array("slang"=>"Chillax"))

    //or
    //Updates the slang and description
    $urban->update("Kpom-Kpi", array("slang"=>"Chillax", description=>"To become peaceful"))

    //or
    $urban->update
    (
      "Kpom-Kpi",
       array
       (
         "slang"=>"Chillax",
         "description"=>"To become peaceful",
         "example-sentence"=>"Please Chillax"
         )
    )
  ?>

```
<h5>Delete a word</h5>
```php
  $urban->delete('Chillax');
```
<h3>Group (Require src/Group.php)</h3>
```php
  <?php
    //Returns an array of words in string in descending order
    //of Highest occurence
    $group = Group::build("Let us go boom boom clark");
```


<h2>Testing</h2>
<p>
  The test require PHPunit to run
  To test the files, navigate to the `/tests` directory and run
</p>
```console
  phpunit GroupTest.php
  phpunit UrbanDictionaryTest.php
  phpunit UrbanWordTest.php
```
