---
title: Command. SmallImages, propriété
description: Représente un conteneur d’images ; dans ce cas, les petites images.
ms.assetid: 15c00e61-543a-4cc8-b329-516985d02359
keywords:
- Ruban Windows de la propriété Command. SmallImages
topic_type:
- apiref
api_name:
- Command.SmallImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b18556cf519c21b01c3e80b63cbfc9cdf9d7d153
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466579"
---
# <a name="commandsmallimages-property"></a>Command. SmallImages, propriété

Représente un conteneur d’images ; dans ce cas, les petites images.

## <a name="usage"></a>Utilisation

``` syntax
<Command.SmallImages>
  child elements
</Command.SmallImages>
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



## <a name="remarks"></a>Notes

Optionnel.

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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Spécification des ressources d’image du ruban](windowsribbon-imageformats.md)
</dt> <dt>

[IU \_ \_ SmallImage](windowsribbon-reference-properties-uipkey-smallimage.md)
</dt> </dl>

 

 





