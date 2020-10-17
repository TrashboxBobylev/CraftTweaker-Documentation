# IBlock

Un objeto IBlock consiste en un [IBlockDefinition](/Vanilla/Blocks/IBlockDefinition/), un metadata y un TileData.  
Se refiere a un bloque en el juego.

## Importing the package

Podría ser necesario que importes el paquete si encuentras algún problema (como lanzar un [array](/AdvancedFunctions/Arrays_and_Loops/)), más vale estar seguro que lo siento y añadir la importación.  
`importar crafttweaker.block.IBlock;`

## Llamando a un objeto de IBlock

Hay varias maneras en las que devuelve un objeto de IBlock:

* Lanzar un [ItemStack](/Vanilla/Items/IItemStack/) como IBlock (usando la palabra clave `AS` , o el método `asBlock()`)
* Usando el getBlock(x,y,z) en un [IWorld](/Vanilla/World/IWorld/).
* Usando getBlock() en ContentTweaker [ICTBlockState](/Mods/ContentTweaker/Vanilla/Types/Block/ICTBlockState/)

Advertencia: ¡Sólo usar el segundo método es posible que `data` ZenGetter devuelva un ID no null!

## Zengetters

| Getter     | What does it do                   | Return Type                                               |
| ---------- | --------------------------------- | --------------------------------------------------------- |
| definition | Devuelve la definición del Bloque | [Definición de IBlock](/Vanilla/Blocks/IBlockDefinition/) |
| meta       | Devuelve los metadatos del Bloque | int                                                       |
| datos      | Devuelve el tileData del Bloque   | [IData](/Vanilla/Data/IData/)                             |
| fluid      | Devuelve el fluido del Bloque     | [ILiquidDefinition](/Vanilla/Liquids/ILiquidDefinition/)  |

# Patrón de IBlock

Los IBlocks extienden [Objetos IBlockPattern](/Vanilla/Blocks/IBlockPattern/). Esto significa que todas las funciones que están disponibles para los objetos IBlockPattern también pueden utilizarse para objetos de IBlock:

* Usa los bloques `` de ZenGetter
* OR'ing
* Coincidiendo con la palabra clave `en`
* Utilice el `displayName` ZenGetter