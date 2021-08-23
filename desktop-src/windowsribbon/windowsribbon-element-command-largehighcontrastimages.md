---
title: Command. LargeHighContrastImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les grandes images à utiliser avec les paramètres système à contraste élevé.
ms.assetid: e25f207f-ac3f-4a5f-8104-c928b38a52a8
keywords:
- propriété Command. LargeHighContrastImages Windows ruban
topic_type:
- apiref
api_name:
- Command.LargeHighContrastImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d59c1e760565443c286969cc92b3b0c4a6b83a2513587f424ebcda366b1b8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710509"
---
# <a name="commandlargehighcontrastimages-property"></a>Command. LargeHighContrastImages, propriété

Représente un conteneur d’images ; dans ce cas, les grandes images à utiliser avec les paramètres système à contraste élevé.

## <a name="usage"></a>Usage

``` syntax
<Command.LargeHighContrastImages>
  child elements
</Command.LargeHighContrastImages>
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

Cette section de code montre les déclarations de commande [**SplitButton**](windowsribbon-element-splitbutton.md) et [**MenuGroup**](windowsribbon-element-menugroup.md) avec des ressources d’image à contraste élevé et de petite taille. Un [**groupe**](windowsribbon-element-group.md) associé qui agit en tant que conteneur parent de l’élément **SplitButton** est également déclaré.


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

[IU \_ \_ LargeHighContrastImage](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md)
</dt> </dl>

 

 





