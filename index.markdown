---
layout: home
---

<!-- Search Container -->
<div id="search-container">
  <input type="search" name="search" id="search-input" placeholder=" What are you looking for?">
  <ul id="results-container"></ul>
</div>

<!-- Inline CSS -->
<style>
/* Container styling */
#search-container {
  max-width: 500px;
  margin: 40px auto;
  position: relative;
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}

/* Search input */
#search-input {
  width: 100%;
  padding: 12px 20px;
  border: 2px solid #ddd;
  border-radius: 30px;
  font-size: 16px;
  transition: all 0.3s ease;
  box-shadow: 0 2px 5px rgba(0,0,0,0.1);
}

#search-input:focus {
  outline: none;
  border-color: #6c63ff;
  box-shadow: 0 4px 10px rgba(108, 99, 255, 0.2);
}

/* Results container */
#results-container {
  list-style: none;
  padding: 0;
  margin-top: 10px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0,0,0,0.1);
  max-height: 300px;
  overflow-y: auto;
}

/* Individual result items */
#results-container li {
  background: #fff;
  padding: 10px 20px;
  border-bottom: 1px solid #eee;
  transition: background 0.2s ease;
}

#results-container li:last-child {
  border-bottom: none;
}

#results-container li a {
  text-decoration: none;
  color: #333;
  display: block;
}

/* Hover effect */
#results-container li:hover {
  background: #f0f0ff;
}

/* Scrollbar styling for results */
#results-container::-webkit-scrollbar {
  width: 6px;
}

#results-container::-webkit-scrollbar-track {
  background: #f1f1f1;
  border-radius: 10px;
}

#results-container::-webkit-scrollbar-thumb {
  background: #c1c1ff;
  border-radius: 10px;
}

/* Responsive adjustments */
@media (max-width: 600px) {
  #search-container {
    max-width: 90%;
  }

  #search-input {
    font-size: 14px;
    padding: 10px 15px;
  }

  #results-container li {
    padding: 8px 15px;
  }
}
</style>


<!-- Script pointing to search-script.js -->
<script src="search-script.js" type="text/javascript"></script>

<!-- Simple-Jekyll-Search config -->
<script>
  SimpleJekyllSearch({
    searchInput: document.getElementById('search-input'),
    resultsContainer: document.getElementById('results-container'),
    json: 'search.json',
    noResultsText: '<p>No results found!</p>',
    searchResultTemplate: '<li><a href="{url}">{title}</a></li>'
  });
</script>

