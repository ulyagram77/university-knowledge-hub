<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Markdown Tabs Example</title>
    <style>
        .tab {
            display: none;
        }
        .tab-buttons {
            margin-bottom: 10px;
        }
        .tab-buttons button {
            padding: 10px;
            cursor: pointer;
            background-color: #f1f1f1;
            border: none;
            outline: none;
        }
        .tab-buttons button.active {
            background-color: #ccc;
        }
        .tab-content {
            padding: 10px;
            border: 1px solid #ccc;
        }
    </style>
</head>
<body>

<div class="tab-buttons">
    <button class="tab-link" onclick="openTab(event, 'tab1')">Tab 1</button>
    <button class="tab-link" onclick="openTab(event, 'tab2')">Tab 2</button>
    <button class="tab-link" onclick="openTab(event, 'tab3')">Tab 3</button>
</div>

<div id="tab1" class="tab tab-content">
    <p>Content for Tab 1 goes here.</p>
</div>

<div id="tab2" class="tab tab-content">
    <p>Content for Tab 2 goes here.</p>
</div>

<div id="tab3" class="tab tab-content">
    <p>Content for Tab 3 goes here.</p>
</div>

<script>
    function openTab(evt, tabId) {
        var i, tabContent, tabLinks;
        tabContent = document.getElementsByClassName("tab");
        for (i = 0; i < tabContent.length; i++) {
            tabContent[i].style.display = "none";
        }
        tabLinks = document.getElementsByClassName("tab-link");
        for (i = 0; i < tabLinks.length; i++) {
            tabLinks[i].className = tabLinks[i].className.replace(" active", "");
        }
        document.getElementById(tabId).style.display = "block";
        evt.currentTarget.className += " active";
    }

    // Set default open tab
    document.getElementsByClassName("tab-link")[0].click();
</script>

</body>
</html>
