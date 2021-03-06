# List

A [list component](https://www.google.com/design/spec/components/lists.html) consists of a single continuous column of tessellated sub-divisions of equal width called rows that function as containers for tiles. Tiles hold content, and can vary in height within a list. 

Lists are best suited to presenting a homogeneous data type or sets of data types, such as images and text, optimized for reading comprehension with the goal of differentiating between like data types or qualities within a single data type. You can compose lists based on subcomponents.

<!-- example -->
```jsx
import { List, ListItem, ListSubHeader, ListDivider, ListCheckbox } from 'react-toolbox';

const ListTest = () => (
  <List selectable ripple>
    <ListSubHeader caption='Explore characters' />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/m.jpg'
      caption='Dr. Manhattan'
      legend="Jonathan 'Jon' Osterman"
      rightIcon='star'
    />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/o.jpg'
      caption='Ozymandias'
      legend='Adrian Veidt'
      rightIcon='star'
    />
    <ListItem
      avatar='https://dl.dropboxusercontent.com/u/2247264/assets/r.jpg'
      caption='Rorschach'
      legend='Walter Joseph Kovacs'
      rightIcon='star'
    />
    <ListSubHeader caption='Configuration' />
    <ListCheckbox checked caption='Notify new comics' legend='You will receive a notification when a new one is published' />
    <ListItem caption='Contact the publisher' leftIcon='send' />
    <ListItem caption='Remove this publication' leftIcon='delete' />
  </List>
);
```

## List

Is used as a wrapper for the list. It can hold properties that affect to the whole list and also it can get styles for the wrapper.

| Name          | Type        | Default    | Description|
|:-----|:-----|:-----|:-----|
| `className`   | `String`    |  `''`      | Sets a class to give custom styles to the list wrapper.| 
| `ripple`      | `Boolean`   | `false`    | If true, each element in the list will have a ripple effect on click | 
| `selectable`  | `Boolean`   | `false`    | If true, the elements in the list will display a hover effect and a pointer cursor. |

## List Item

Represents a list item that can have avatar, icons, title and subtitle, etc. It's important to notice that you have to set it as an inmediate child of `List` component.

| Name              | Type          | Default         | Description|
|:-----|:-----|:-----|:-----|
| `avatar`   | `String`    |        | A string URL to specify an avatar in the left side of the item.| 
| `caption`   | `String`    |       | Main text of the item. Required.| 
| `className`   | `String`    |  `''`    | Set a class to give custom styles to the list item.| 
| `disabled`   | `String`    |  `false`    | If true, the item is displayed as disabled and it's not clickable.| 
| `leftIcon`    | `String`       |    | A string key of a font icon to display an icon in the left side of the item. |
| `legend`   | `String`      |       | Secondary text to display under the caption.|
| `onClick`   | `Function`      |       | Callback the is invoked when the item is clicked if it's not disabled. |
| `rightIcon`  | `String`      |       | The same as the `leftIcon` but in this case the icon is displayed in the right side.|
| `ripple` | `Boolean`      |   `false`  | If true, the item displays a ripple effect on click. By default it's inherited from the parent element.|
| `selectable` | `Boolean`      |   `false`    | If true, the elements in the list will display a hover effect and a pointer cursor. Inherited from the parent |
| `to` | `String`      |       | In case you want to provide the item as a link, you can pass this property to specify the href. |

## List Checkbox

A special type of item that has a checkbox control on the left side. It implements similar methods to the `ListItem` component and some additional to control the checkbox.

| Name              | Type          | Default         | Description|
|:-----|:-----|:-----|:-----|
| `caption`   | `String`    |       | Main text of the item. Required.| 
| `checked`   | `Boolean`    |  `false`    | If true the checkbox appears checked by default.| 
| `disabled`   | `String`    |  `false`    | If true, the item is displayed as disabled and it's not clickable.| 
| `legend`   | `String`      |       | Secondary text to display under the caption.|
| `name`  | `String`      |       | Name for the checkbox input item.|
| `onBlur` | `Function`      |    | Callback called when the input element is blurred.|
| `onFocus` | `Function`      |    | Callback called when the input element is focused.|
| `onChange` | `Function`      |    | Callback called when the input element is changed.|

## List Subheader

Simple subcomponent used to give a title to a list area. It only have a property `caption` which is a `String` to set the text that should be displayed.

## List Divider

Simple subcomponent used to separate list sections or items. It has only one property `inset` which is a `Boolean` that indicates if the divider should be full with or should leave an space to the left side.

