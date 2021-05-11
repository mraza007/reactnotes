# List and Keys.

1. When mapping over data and returning components,you get a warning about keys for list items.
2. **key** is a special string attr include when creating list of elements.
3. Keys helped react identify which items have changed or added.
4. make sure you are using the unique keys.


#### Picking a Key.

- Best way: use a string that uniquely identifies item among siblings.
- Most often you would use IDs from your data as keys:
- If you don't have the stable ids for rendered items you may use the iteration index as a key as a last resort.
