# StoneCutterManager



Этот класс был добавлен модом с mod-id `crafttweaker`. Так что если вы хотите использовать эту функцию, вам нужно установить этот мод.

## Импорт класса
Вам может потребоваться импортировать пакет, если вы столкнетесь с какими-либо проблемами (например, с заливкой массива), так что лучше быть в безопасности, чем извиняться и добавлять импорт.
```zenscript
crafttweaker.api.StoneCutterManager
```

## Implemented Interfaces
StoneCutterManager implements the following interfaces. That means any method available to them can also be used on this class.
- [crafttweaker.api.brackets.CommandStringDisplayable](/vanilla/api/brackets/CommandStringDisplayable)
- [crafttweaker.api.registries.IRecipeManager](/vanilla/api/managers/IRecipeManager)

## Methods
### addJSONRecipe

Adds a recipe based on a provided IData. The provided IData should represent a DataPack JSON, this effectively allows you to register recipes for any DataPack supporting IRecipeType systems.

```zenscript
stoneCutter.addJSONRecipe(name as String, data as crafttweaker.api.data.IData);
stoneCutter.addJSONRecipe("recipe_name", {ingredient:{item:<item:minecraft:gold_ore>.registryName},result:<item:minecraft:cooked_porkchop>.registryName,experience:0.35 as float, cookingtime:100});
```

| Параметр | Тип                                                    | Description                     |
| -------- | ------------------------------------------------------ | ------------------------------- |
| name     | String                                                 | name of the recipe              |
| data     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data representing the json file |


### addRecipe

Adds a recipe to the stone cutter

```zenscript
stoneCutter.addRecipe(recipeName as String, output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient);
stoneCutter.addRecipe("recipe_name", <item:minecraft:grass>, <tag:minecraft:wool>);
```

| Параметр   | Тип                                                                 | Description                                                                 |
| ---------- | ------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| recipeName | String                                                              | name of the recipe                                                          |
| output     | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | output [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)    |
| input      | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | вводите [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) |


### getAllRecipes

Return type: List&lt;[crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)&gt;

```zenscript
stoneCutter.getAllRecipes();
```

### getRecipeByName

Return type: [crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)

```zenscript
stoneCutter.getRecipeByName(name as String);
```

| Параметр | Тип    | Description          |
| -------- | ------ | -------------------- |
| name     | String | Описание отсутствует |


### getRecipesByFrom

Return type: List&lt;[crafttweaker.api.recipes.WrapperRecipe](/vanilla/api/recipe/WrapperRecipe)&gt;

```zenscript
stoneCutter.getRecipesByOutput(output as crafttweaker.api.item.IIngredient);
```

| Параметр | Тип                                                                 | Description          |
| -------- | ------------------------------------------------------------------- | -------------------- |
| output   | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | Описание отсутствует |


### removeAll

Remove all recipes in this registry

```zenscript
stoneCutter.removeAll();
```

### removeByModid

Remove recipe based on Registry name modid

```zenscript
stoneCutter.removeByModid(modid as String);
stoneCutter.removeByModid("minecraft");
```

| Параметр | Тип    | Description                    |
| -------- | ------ | ------------------------------ |
| modid    | String | modid of the recipes to remove |



Удалите рецепт на основе мода названия реестра с добавленной проверкой исключения, так что вы можете удалить весь мод кроме нескольких указанных модификаций.

```zenscript
stoneCutter.removeByModid(modid as String, exclude as crafttweaker.api.recipe.RecipeFilter);
stoneCutter.removeByModid("minecraft", (name as string) => {return name == "orange_wool";});
```

| Параметр  | Тип                                                                      | Description                         |
| --------- | ------------------------------------------------------------------------ | ----------------------------------- |
| modid     | String                                                                   | modid of the recipes to remove      |
| исключить | [crafttweaker.api.recipe.RecipeFilter](/vanilla/api/recipe/RecipeFilter) | рецепты для exlude от быть удалены. |


### removeByName

Remove recipe based on Registry name

```zenscript
stoneCutter.removeByName(name as String);
stoneCutter.removeByName("minecraft:furnace");
```

| Параметр | Тип    | Description                       |
| -------- | ------ | --------------------------------- |
| name     | String | registry name of recipe to remove |


### removeByRegex

Remove recipe based on regex

```zenscript
stoneCutter.removeByRegex(regex as String);
stoneCutter.removeByRegex("\\d_\\d");
```

| Параметр | Тип    | Description            |
| -------- | ------ | ---------------------- |
| regex    | String | regex to match against |


### removeRecipe

Remove a recipe based on it's output.

```zenscript
stoneCutter.removeRecipe(output as crafttweaker.api.item.IItemStack);
stoneCutter.removeRecipe(<item:minecraft:glass>);
```

| Параметр | Тип                                                               | Description          |
| -------- | ----------------------------------------------------------------- | -------------------- |
| output   | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | output of the recipe |



## Свойства

| Название      | Тип    | Имеет Getter | Имеет Setter |
| ------------- | ------ | ------------ | ------------ |
| commandString | String | true         | false        |

