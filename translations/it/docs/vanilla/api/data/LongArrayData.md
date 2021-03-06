# LongArrayData



Questa classe è stata aggiunta da una mod con ID `crafttweaker`. Perciò, è necessario avere questa mod installata per poter utilizzare questa funzione.

## Importing the class
Potrebbe essere necessario importare il pacchetto, se si incontrano dei problemi (come castare un vettore), quindi meglio essere sicuri e aggiungere la direttiva di importazione.
```zenscript
crafttweaker.api.data.LongArrayData
```

## Interfacce Implementate
LongArrayData implements the following interfaces. Ciò significa che ogni metodo presente nell'interfaccia può essere usato anche per questa classe.
- [crafttweaker.api.data.ICollectionData](/vanilla/api/data/ICollectionData)

## Constructors
```zenscript
new crafttweaker.api.data.LongArrayData(internal as long[]);
```
| Parameter | Type   | Description                 |
| --------- | ------ | --------------------------- |
| internal  | long[] | Nessuna descrizione fornita |



## Methods
### add

```zenscript
[100000, 800000, 50000].add(value as crafttweaker.api.data.IData);
[100000, 800000, 50000].add("today");
```

| Parameter | Type                                                   | Description                  |
| --------- | ------------------------------------------------------ | ---------------------------- |
| value     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The value to add to the list |



```zenscript
[100000, 800000, 50000].add(index as int, value as crafttweaker.api.data.IData);
[100000, 800000, 50000].add(1, "beautiful");
```

| Parameter | Type                                                   | Description                                                          |
| --------- | ------------------------------------------------------ | -------------------------------------------------------------------- |
| index     | int                                                    | The index to add to. Subsequent items will be moved one index higher |
| value     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The value to add to the list                                         |


### asList

Gets a List<IData> representation of this IData, returns null on anything but [crafttweaker.api.data.ListData](/vanilla/api/data/ListData).

 Returns: `null if this IData is not a list.`

Returns List<[crafttweaker.api.data.IData](/vanilla/api/data/IData)>

```zenscript
[100000, 800000, 50000].asList();
```

### asMap

Gets a Map<String, IData> representation of this IData, returns null on anything but [crafttweaker.api.data.MapData](/vanilla/api/data/MapData).

 Returns: `null if this IData is not a map.`

Returns [crafttweaker.api.data.IData](/vanilla/api/data/IData)[String]

```zenscript
[100000, 800000, 50000].asMap();
```

### asString

Gets the String representation of this IData

 Returns: `String that represents this IData (value and type).`

Ritorna una stringa

```zenscript
[100000, 800000, 50000].asString();
```

### clear

Removes every element in the list

```zenscript
[100000, 800000, 50000].clear();
```

### contains

Checks if this IData contains another IData, mainly used in subclasses of [crafttweaker.api.data.ICollectionData](/vanilla/api/data/ICollectionData), is the same as an equals check on other IData types

Restituisce un booleano

```zenscript
[100000, 800000, 50000].contains(data as crafttweaker.api.data.IData);
[100000, 800000, 50000].contains("Display");
```

| Parameter | Type                                                   | Description                      |
| --------- | ------------------------------------------------------ | -------------------------------- |
| data      | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data to check if it is contained |


### copy

Makes a copy of this IData.

 IData is immutable by default, use this to create a proper copy of the object.

 Returns: `a copy of this IData.`

Returns [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[100000, 800000, 50000].copy();
```

### get

Retrieves the [crafttweaker.api.data.IData](/vanilla/api/data/IData) stored at the given index.

Returns [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[100000, 800000, 50000].get(index as int);
[100000, 800000, 50000].get(0);
```

| Parameter | Type | Description         |
| --------- | ---- | ------------------- |
| index     | int  | The index (0-based) |


### getId

Gets the ID of the internal NBT tag.

 Used to determine what NBT type is stored (in a list for example)

 Returns: `ID of the NBT tag that this data represents.`

Returns byte

```zenscript
[100000, 800000, 50000].getId();
```

### getString

Gets the String representation of the internal INBT tag

 Returns: `String that represents the internal INBT of this IData.`

Ritorna una stringa

```zenscript
[100000, 800000, 50000].getString();
```

### remove

Removes the [crafttweaker.api.data.IData](/vanilla/api/data/IData) stored at the given index.

Returns [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[100000, 800000, 50000].remove(index as int);
[100000, 800000, 50000].remove(0);
```

| Parameter | Type | Description         |
| --------- | ---- | ------------------- |
| index     | int  | The index (0-based) |


### set

Sets the item at the provided index to the given value

Returns [crafttweaker.api.data.IData](/vanilla/api/data/IData)

```zenscript
[100000, 800000, 50000].set(index as int, value as crafttweaker.api.data.IData);
[100000, 800000, 50000].set(0, "Bye");
```

| Parameter | Type                                                   | Description                |
| --------- | ------------------------------------------------------ | -------------------------- |
| index     | int                                                    | The index to set (0-based) |
| value     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | The new Value              |



## Properties

| Name | Type | Ha Getter | Ha Setter |
| ---- | ---- | --------- | --------- |
| size | int  | true      | false     |

