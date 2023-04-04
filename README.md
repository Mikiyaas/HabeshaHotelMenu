# Hotel Menu

# **Habesha Hotel Menu**

## **Introduction**

This is the menu for Habesha Hotel's restaurant. We offer a variety of Ethiopian dishes, prepared with the finest ingredients and spices. From traditional stews and curries to vegetarian and vegan options, we have something to satisfy every palate.

## **Menu**

Here are some of the dishes we offer:

### **Appetizers**

- Sambusa (spicy beef or lentil turnovers)
- Shiro (chickpea or lentil dip)
- Injera (Ethiopian sourdough flatbread)

### **Entrees**

- Doro Wat (spicy chicken stew)
- Tibs (sauteed beef or lamb with vegetables)
- Yebeg Alicha (mild lamb stew)
- Misir Wat (spicy red lentil stew)
- Atakilt Wat (cabbage, carrot, and potato stew)

### **Vegetarian and Vegan Options**

- Shiro (chickpea or lentil dip)
- Misir Wat (spicy red lentil stew)
- Atakilt Wat (cabbage, carrot, and potato stew)
- Gomen (collard greens)

## ****Code for Adding Menu Items****

```jsx
<script>
    $("#menu-form").submit(function(event) {
       event.preventDefault(); 
       
       var id = Math.floor(Math.random() * 1000000); // Generate a random ID for the item
       
       var name = $("#name").val();
       var recipie = $("#recipie").val();
       var price = $("#price").val();
       
       // Create a remove button for the item
       var removeBtn = $('<button/>')
          .addClass('btn btn-danger btn-sm remove-button')
          .text('Remove');
          
       // Create a new row for the item
       var newRow = $('<tr/>')
          .append($('<td/>').text(id))
          .append($('<td/>').text(name))
          .append($('<td/>').text(recipie))
          .append($('<td/>').text('ETB ' + price))
          .append($('<td/>').append(removeBtn));
       
       // Add the new row to the table
       $("#menu-items").append(newRow);
       
       // Clear the form inputs
       $("#name").val("");
       $("#recipie").val("");
       $("#price").val("");
    });
    
    $(document).on("click", ".remove-button", function() {
       $(this).closest("tr").remove();
    });
 </script>
```

This code allows users to add and remove items from a table that represents the menu for Habesha Hotel.

### **How to Add an Item**

To add an item, users can follow these steps:

1. Fill out the "name" field with the name of the item.
2. Fill out the "recipe" field with the recipe for the item.
3. Fill out the "price" field with the price of the item.
4. Click the "Add" button.

The item will be added to the table, along with a remove button in case the user wants to remove it later.

### **How to Remove an Item**

To remove an item, users can follow these steps:

1. Click the "Remove" button next to the item they want to remove.
2. The item will be removed from the table.

Note: The ID for each item is generated automatically and cannot be changed by the user.

### **Link to Live Demo**

The live demo for this code Habesha Hotel Menu can be accessed at [Click here](https://mikiyaas.github.io/HabeshaHotelMenu/).
