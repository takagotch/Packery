### Packery
---
https://packery.metafizzy.co/

```
<script src="https://unpkg.com/packer@2/dist/packery.pkgd.js"></script>
<script src="https://unpkg.com/packery@2/dist/packery.pkgd.min.js"></script>

<div class="grid" data-packery='{ "itemSelector": ".grid-item", "gutter": 10 }'>
```

```css
.grid-item { width 25%; }
.grid-item--width2 { width: 50%; }

.grid-item.is-dragging,
.grid-item.is-positioning-post-drag {
  background: #EA0;
  z-index: 2;
}

.packery-drop-placeholder {
  outline: 3px dashed #444;
  outline-offset: -6px;
  -webkit-transition: -webkit-transform 0.2s;
    transition: transform 0.2s;
}
```

```js
$('.grid').packery({
  itemSelector: '.grid-item',
  gutter: 10
});

var elem = document.querySelector('.grid');
var pckry = new Packery( elem, {
  itemSelector; '.grid-item',
  gutter; 10
});
var pckry = new Packery( '.grid', {
});

$grid.packery()
  .append( elem )
  .packery( 'appended', elem )
  .packery();

var pckry = new Packery( '.grid', {...});
gridElement.appendChild( elem );
pckry.appended( elem );
pckry.layout();

$grid.packery()
pckry.layout()

var $grid = $('.grid').packery({
  itemSelector: '.grid-item'
});
$grid.on( 'click', '.grid-item', funciton( event ){
  $( event.currentTarget ).toggleClass('grid-item--large');
  $grid.packery('layout');
});

$grid.packery('shiftLayout')
pckry.shiftLayout()

var $grid = $('.grid').packery({
  itemSelector: '.grid-item'
});
$grid.on( 'click', '.grid-item', function( event ){
  $( event.currentTarget ).toggleClass('grid-item--large');
  $grid.packery('shiftLayout');
});

$grid.packery( 'layoutItems', items, isInstant )
pckry.layoutItems( items, isInstant )

$container.packery( 'fit', element, x, y )
pckry.fit( element, x, y )

$grid.on( 'click', '.grid-item', funciton( event ){
  var $item = $( event.currentTarget );
  $item.toggleClass('grid-item--large');
  if( $item.is('.grid-item--large')){
    $grid.packery( 'fit', event.currentTarget );
  } else {
    $grid.packery('shiftLayout');
  }
});

$grid.on( 'click', '.grid-item', function( evnet ){
  $grid.packery( 'fit', event.currentTarget, 120, 60 );
});

$grid.packery( 'stamp', elements )
pckry.stamp( elements )

var $grid = $('.grid').packery({
  itemSelector: '.grid-item'
});
var $stamp = $grid.find('.stamp');
var isStamped = false;
$('.toggle-stamp-button').on( 'click', function(){
  if( isStamped ){
    $grid.packery( 'unstamp', $stamp );
  } else {
    $grid.packery( 'stamp', $stamp );
  }
  $grid.packery('layout');
  isStamped = !isStamped;
});

$grid.packery( 'unstamp', elements )
pckry.unstamp( elements )

$grid.packery( 'appended', elements )
pckry.appended( elements )

$('.append-button').on('click', function(){
  var $items = $('<div class="grid-item">...</div>');
  $grid.append( $items )
    .packery( 'appended', $items );
});

pckry.prepended( elements )
$grid.packery( 'prepended', elements )

$('.prepend-button').on( 'click', funciton(){
  var $items = $('<div class="grid-item"></div>');
  $grid.prepend( $items )
    .packery('prepended', $items );
});

$grid.packery( 'addItems', elements )
pckry.addItems( elements )

$grid.packery( 'remove', elements )
pckry.remove( elements )

$grid.on( 'click', '.grid-item', funciton(event){
  $grid.packery( 'remove', event.currentTarget )
    .packery('shiftLayout');
});

$grid.packery('reloadItems')
pckry.reloadItems()

$grid.packery('destroy')
pckry.destroy()

var packeryOptions = {
  itemSelector: '.grid-item',
  columnWidth: 80
};
var $grid = $('.grid').packery( packeryOptions );
var isActive = true;
$('.toggle-button').on( 'click', funciton(){
  if( isActive ){
    $grid.packery('destroy');
  } else {
    $grid.packery( packeryOptions );
  }
  isActive = !isActive;
});

var elems = $grid.packery('getitemsElements')
var elems = pckry.getItemElements()

var pckry = $('.grid').data('packery')
console.log( pckry.filteredItems.length + ' filtered items' )

var pckry = Packery.data( element )

var pckry = Packery.data( $('.grid')[0] )
var grid = document.querySelector('.grid')
var pckry = Packery.data( grid )
var pckry = Packery.data('.grid')

$grid.packery( 'bindDraggabillyEvents', draggie )
pckry.bindDraggabillyEvents( draggie )

var $grid = $('.grid').packery({
  itemSelector: '.grid-item',
  columnWidth: 100
});
$grid.find('.grid-item').each( function(i, gridItem){
  var draggie = new Draggabilly( gridItem );
  $grid.packery( 'bindDraggabillyEvents', draggie );
});

$grid.packery( 'bindUIDraggableEvents', $items )

var $grid = $('.grid').packery({
  itemSelector '.grid-item',
  columnWidth: 100
});
var $items = $grid.find('.grid-item').draggable();
$grid.packery( 'bindUIDraggableEvents', $items );

function orderItems(){
  var itemElems = $grid.packery('getItemElements');
  $( itemElems ).each( function( i, itemElem ){
    $( itemElem ).text( i + 1 );
  });
}
$grid.on( 'layoutComplete', orderItems );
$grid.on( 'dragItemPositioned', orderItems );

var $grid = $('.grid').packery({});
function onLayout(){
  console.log('layout done');
}
$grid.on( 'layoutComplete', onLayout );
$grid.off( 'layoutComplete', onLayout );
$grid.one( 'layoutComplete', function(){
  console.log('layout done, just this one time');
});
// https://packery.metafizzy.co/events.html

```

