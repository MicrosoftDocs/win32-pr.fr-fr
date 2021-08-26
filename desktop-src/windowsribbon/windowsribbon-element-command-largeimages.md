---
title: Command. LargeImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les grandes images.
ms.assetid: 9fcd3694-7847-43e2-9877-47daf47aae9a
keywords:
- propriété Command. LargeImages Windows ruban
topic_type:
- apiref
api_name:
- Command.LargeImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66214eb05910296b2c03a749d88134bef68f86badc2ffd7f7b69d0ba6adfdd5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931613"
---
# <a name="commandlargeimages-property"></a>Command. LargeImages, propriété

Représente un conteneur d’images ; dans ce cas, les grandes images.

## <a name="usage"></a>Usage

``` syntax
<Command.LargeImages>
  child elements
</Command.LargeImages>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants



| Élément                                                 | Description                                        |
|---------------------------------------------------------|----------------------------------------------------|
| [**Image**](windowsribbon-element-image.md)<br/> | Peut se produire une ou plusieurs fois<br/> <br/> |



## <a name="parent-elements"></a>Éléments parents



| Élément                                                     |
|-------------------------------------------------------------|
| [**Commande**](windowsribbon-element-command.md)<br/> |



## <a name="remarks"></a>Remarques

Facultatif.

Peut se produire au plus une fois pour chaque [**commande**](windowsribbon-element-command.md).

Les ressources d’image doivent être conformes au format graphique bitmap standard (BMP) utilisé dans Windows.

## <a name="examples"></a>Exemples

L’exemple suivant illustre le balisage de base pour le [**SplitButton**](windowsribbon-element-splitbutton.md) avec un élément [**MenuGroup**](windowsribbon-element-menugroup.md) .

Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et [**MenuGroup**](windowsribbon-element-menugroup.md) avec une grande ressource d’image. Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.


```XML
<!-- SplitButton -->
<Command Name="cmdSplitButtonGroup"
         Symbol="cmdSplitButtonGroup"
         Comment="SplitButton Group"
         LabelTitle="SplitButton"/>
<Command Name="cmdSplitButton"
         Symbol="cmdSplitButton"
         Comment="SplitButton"
         LabelTitle="SplitButton"/>
<Command Name="cmdSBButtonItem"
         Symbol="cmdSBButtonItem"
         Comment="SBButtonItem"
         LabelTitle="SB ButtonItem"/>
<Command Name="cmdSBButton1"
         Symbol="cmdSBButton1"
         Comment="SBButton1"
         LabelTitle="SB Button">
  <Command.LargeImages>
    <Image Source="res/copyL_32.bmp"/>
  </Command.LargeImages>
  <Command.SmallImages>
    <Image Source="res/copyS_16.bmp"/>
  </Command.SmallImages>
  <Command.LargeHighContrastImages>
    <Image Source="res/copyLHC_32.bmp"/>
  </Command.LargeHighContrastImages>
  <Command.SmallHighContrastImages>
    <Image Source="res/copySHC_16.bmp"/>
  </Command.SmallHighContrastImages>
</Command>
<Command Name="cmdSBMajorItems"
         Comment="Major Items Category"
         LabelTitle="Major Items"/>
<Command Name="cmdSBStandardItems"
         Comment="Standard Items Category"
         LabelTitle="Standard Items"/>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)
</dt> <dt>

[IU \_ \_ LARGEIMAGE](windowsribbon-reference-properties-uipkey-largeimage.md)
</dt> </dl>

 

 





