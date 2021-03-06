+++
title = "Getting Around"
weight = 20
+++

After selecting a table, dynamo-browse will perform a scan and present the results in the default view mode.

{{< image src="/images/dynamo-browse/main-item-view.png" alt="Main item view" position="center" >}}

This mode consists of three panes:

- The top pane displays the result-set of the last scan or query.  The table name is at the top-left.
- The middle pane displays the attributes of the currently selected item, along with their type.
- The bottom pane displays the current query or filter, plus any messages.  Prompts for input will
  also appear at the bottom.

The result-set is sorted in ascending order based on the value and type of the partition and sort key.
Up to 1,000 rows will be displayed for the current result-set.

Since DynamoDB does not require all items to have the same attribute (unless they are pre-defined), any
attribute not set for a column is indicated with a grey tilde character `~`.

Use the following keys to change the currently selected row, which is highlighted in purple:

- <kbd>&uarr;</kbd>/<kbd>i</kbd>: Move selection up
- <kbd>&darr;</kbd>/<kbd>k</kbd>: Move selection down
- <kbd>PgUp</kbd>/<kbd>&#8679; I</kbd>: Page up
- <kbd>PgDn</kbd>/<kbd>&#8679; K</kbd>: Page down
- <kbd>Home</kbd>/<kbd>0</kbd>: First row
- <kbd>End</kbd>/<kbd>$</kbd>: Last row

The columns of the table 
consist of the top-level attributes of the result-set.  The partition key, sort key, plus any explicitly defined
attributes will always be displayed from the left margin onwards.  The other attributes are determined
from the results of the last scan or query, and may change depending on the result.

The display columns of the table can be scrolled across by using the following keys:

- <kbd>&larr;</kbd>/<kbd>j</kbd>: Scroll to the left
- <kbd>&rarr;</kbd>/<kbd>l</kbd>: Scroll to the right

The attributes of the currently selected item will appear in the middle pane.  Both the type and the value of each
attribute will be displayed.  Any nested attributes will be indented, and will below their parent item.  A value
displayed in grey does not represent the actual value of the item, but indicates some meta-information about the item,
such as the length.

## Entering Commands

Commands can be entered by pressing <kbd>:</kbd> and entering the command, with any arguments, at the prompt.