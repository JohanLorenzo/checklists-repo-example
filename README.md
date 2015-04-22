# Functional

## Launch suite

### fxos.func.sanity.launch-contacts
`Bug 2 `
`Story 1`
`Draft`

Launch contacts! this is an updated version

### fxos.func.sanity.launch-music
`Bug 3 `
`Story 3`
`Disabled`

Launch music


### fxos.func.sanity.launch-sms-repeated
`Bug 3 `
`Story 3`
`Xfail`

Launch SMS and measure elapsed time
Do it again.
And again.


### fxos.func.parameterized.test
Launch the dialog, insert :val1, :val2, :val3 and hit enter.

ID  | val1 | val2 | val3 |
--- | ---- | ---- | -----
id1 | a    | 1    | one one
id2 | b    | 2    | two two


### fxos.func.sanity.launch-rocketbar
`Bug 4`
`Story 3`
`Draft`

Launch rocketbar

### fxos.func.state-diagram
digraph G {
  node [label="" shape=diamond]; choice1;  choice2;  choice3;  choice4;  choice5;
  node [shape=box];
  start [shape=doublecircle];
  end [shape=doublecircle];
  start -> homescreen;
  homescreen -> choice1;
  choice1 -> longPress [label="tap on search bar"];
  longPress -> choice2;
  choice2 -> editMode [label="long tap on collection"];
  editMode -> choice3;
  choice3 -> homescreen;
  choice3 -> collectionRemoved [label="tap x on collection icon"];
  collectionRemoved -> choice3;
  collectionRemoved -> end;
  choice3 -> addToCollection [label="drag app to collection"];
  addToCollection -> choice3;
  choice3 -> tapNameOfCollection;
  tapNameOfCollection -> choice4;
  choice4 -> choice3;
  choice4 -> editNameOfCollection;
  editNameOfCollection -> choice5;
  choice5 -> choice3  [label="cancel or home button"];
  choice5 -> nameCommits;
  nameCommits -> choice3
  homescreen[label="Homescreen"];
  longPress[label="Long press an icon"];
  editMode[label="Homescreen edit mode"];
  collectionRemoved[label="Collection remove"];
  addToCollection[label="Add to collection"];
  tapNameOfCollection[label="Tap name of collection"];
  editNameOfCollection[label="Edit name of collection"];
  nameCommits[label="Name commits"];
}
