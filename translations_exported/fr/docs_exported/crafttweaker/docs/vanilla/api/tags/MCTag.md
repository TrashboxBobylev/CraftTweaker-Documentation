# MCTag

This class was added by a mod with mod-id `crafttweaker`. So you need to have this mod installed if you want to use this feature.

## Importing the class
It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import.
```zenscript
crafttweaker.api.tag.MCTag
```

## Implemented Interfaces
MCTag implements the following interfaces. That means any method available to them can also be used on this class.
- [crafttweaker.api.brackets.CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)
- [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient)

## Methods
### addBlocks

```zenscript
myMCTag.addBlocks(blocks as crafttweaker.api.block.MCBlock[]);
```

| Parameter | Type                                                            | Description             |
| --------- | --------------------------------------------------------------- | ----------------------- |
| blocks    | [crafttweaker.api.block.MCBlock](/vanilla/api/blocks/MCBlock)[] | No description provided |


### addEntityTypes

```zenscript
myMCTag.addEntityTypes(entities as crafttweaker.api.entity.MCEntityType[]);
```

| Parameter | Type                                                                         | Description             |
| --------- | ---------------------------------------------------------------------------- | ----------------------- |
| entities  | [crafttweaker.api.entity.MCEntityType](/vanilla/api/entities/MCEntityType)[] | No description provided |


### addFluids

```zenscript
myMCTag.addFluids(fluides comme crafttweaker.api.fluid.MCFluid[]);
```

| Parameter | Type                                                           | Description             |
| --------- | -------------------------------------------------------------- | ----------------------- |
| fluids    | [crafttweaker.api.fluid.MCFluid](/vanilla/api/fluid/MCFluid)[] | No description provided |


### addItems

Ajoute des éléments à ce tag, échouera si ce n'est pas un tag qui peut contenir des éléments

```zenscript
myMCTag.addItems(objets comme crafttweaker.api.item.IItemStack[]);
myMCTag.addItems(<item:minecraft:dirt>);
```

| Parameter | Type                                                                | Description               |
| --------- | ------------------------------------------------------------------- | ------------------------- |
| items     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)[] | Éléments à ajouter au tag |


### anyDamage

Type de retour : [crafttweaker.api.item.MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
null.anyDomage();
```

### createBlockTag

Type de retour : [crafttweaker.api.tag.MCTag](/vanilla/api/tags/MCTag)

```zenscript
myMCTag.createBlockTag();
```

### createEntityTypeTag

Type de retour : [crafttweaker.api.tag.MCTag](/vanilla/api/tags/MCTag)

```zenscript
myMCTag.createEntityTypeTag();
```

### createFluidTag

Type de retour : [crafttweaker.api.tag.MCTag](/vanilla/api/tags/MCTag)

```zenscript
myMCTag.createFluidTag();
```

### createItemTag

Type de retour : [crafttweaker.api.tag.MCTag](/vanilla/api/tags/MCTag)

```zenscript
myMCTag.createItemTag();
```

### getRemainingItem

When this ingredient stack is crafted, what will remain in the grid? Does not check if the stack matches though! Used e.g. in CrT's net.minecraft.item.crafting.ICraftingRecipe

Return type: [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)

```zenscript
null.getRemainingItem(stack as crafttweaker.api.item.IItemStack);
null.getRemainingItem(<item:minecraft:iron_ingot>);
```

| Parameter | Type                                                              | Description                               |
| --------- | ----------------------------------------------------------------- | ----------------------------------------- |
| stack     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | The stack to provide for this ingredient. |


### matches

Does the given stack match the ingredient?

Return type: boolean

```zenscript
null.matches(stack as crafttweaker.api.item.IItemStack);
null.matches(<item:minecraft:iron_ingot>);
```

| Parameter | Type                                                              | Description        |
| --------- | ----------------------------------------------------------------- | ------------------ |
| stack     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | The stack to check |



Does the given stack match the ingredient?

Return type: boolean

```zenscript
null.matches(stack as crafttweaker.api.item.IItemStack, ignoreDamage as boolean);
```

| Parameter          | Type                                                              | Description                               |
| ------------------ | ----------------------------------------------------------------- | ----------------------------------------- |
| stack              | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | The stack to check                        |
| Ignorer les dégâts | boolean                                                           | Les dommages devraient-ils être vérifiés? |


### onlyDamaged

Type de retour : [crafttweaker.api.item.MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
null.onlyDamaged();
```

### onlyIf

Type de retour : [crafttweaker.api.item.MCIngredientConditioned](/vanilla/api/items/MCIngredientConditioned)&lt;[crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient)&gt;

```zenscript
null.onlyIf(uid en tant que chaîne, fonction en tant que function.Predicate<crafttweaker.api.item.IItemStack>);
```

| Parameter | Type                                                                                                    | Description             | IsOptional | Default Value |
| --------- | ------------------------------------------------------------------------------------------------------- | ----------------------- | ---------- | ------------- |
| uid       | String                                                                                                  | No description provided | false      | `null`        |
| function  | function.Predicate&lt;[crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)&gt; | No description provided | true       | `null`        |


### removeBlocks

```zenscript
myMCTag.removeBlocks(blocks as crafttweaker.api.block.MCBlock[]);
```

| Parameter | Type                                                            | Description             |
| --------- | --------------------------------------------------------------- | ----------------------- |
| blocks    | [crafttweaker.api.block.MCBlock](/vanilla/api/blocks/MCBlock)[] | No description provided |


### removeEntityTypes

```zenscript
myMCTag.removeEntityTypes(entities as crafttweaker.api.entity.MCEntityType[]);
```

| Parameter | Type                                                                         | Description             |
| --------- | ---------------------------------------------------------------------------- | ----------------------- |
| entities  | [crafttweaker.api.entity.MCEntityType](/vanilla/api/entities/MCEntityType)[] | No description provided |


### enlever les fluides

```zenscript
myMCTag.removeFluids(fluides comme crafttweaker.api.fluid.MCFluid[]);
```

| Parameter | Type                                                           | Description             |
| --------- | -------------------------------------------------------------- | ----------------------- |
| fluids    | [crafttweaker.api.fluid.MCFluid](/vanilla/api/fluid/MCFluid)[] | No description provided |


### removeItems

supprime des éléments de ce tag, échouera si ce n'est pas un tag qui peut contenir des éléments

```zenscript
myMCTag.removeItems(items as crafttweaker.api.item.IItemStack[]);
myMCTag.removeItems(<item:minecraft:dirt>);
```

| Parameter | Type                                                                | Description                 |
| --------- | ------------------------------------------------------------------- | --------------------------- |
| items     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)[] | Éléments à supprimer du tag |



## Properties

| Name            | Type                                                                             | Has Getter | Has Setter |
| --------------- | -------------------------------------------------------------------------------- | ---------- | ---------- |
| blocks          | [crafttweaker.api.block.MCBlock](/vanilla/api/blocks/MCBlock)[]                  | true       | false      |
| commandString   | String                                                                           | true       | false      |
| entityTypes     | [crafttweaker.api.entity.MCEntityType](/vanilla/api/entities/MCEntityType)[]     | true       | false      |
| premierBloc     | [crafttweaker.api.block.MCBlock](/vanilla/api/blocks/MCBlock)                    | true       | false      |
| Première entité | [crafttweaker.api.entity.MCEntityType](/vanilla/api/entities/MCEntityType)       | true       | false      |
| firstFluid      | [crafttweaker.api.fluid.MCFluid](/vanilla/api/fluid/MCFluid)                     | true       | false      |
| firstItem       | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)                | true       | false      |
| fluids          | [crafttweaker.api.fluid.MCFluid](/vanilla/api/fluid/MCFluid)[]                   | true       | false      |
| id              | [crafttweaker.api.util.MCResourceLocation](/vanilla/api/util/MCResourceLocation) | true       | false      |
| isBlockTag      | boolean                                                                          | true       | false      |
| isEntityTypeTag | boolean                                                                          | true       | false      |
| isFluidTag      | boolean                                                                          | true       | false      |
| isItemTag       | boolean                                                                          | true       | false      |
| items           | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)[]              | true       | false      |

## Operators
### OR

```zenscript
<tag:ingotIron> | autres que crafttweaker.api.item.IIngredient
```

| Parameter | Type                                                                | Description             |
| --------- | ------------------------------------------------------------------- | ----------------------- |
| other     | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | No description provided |

## Casters

| Result type                                                | Is Implicit |
| ---------------------------------------------------------- | ----------- |
| [crafttweaker.api.data.IData](/vanilla/api/data/IData)     | true        |
| [crafttweaker.api.data.MapData](/vanilla/api/data/MapData) | true        |

