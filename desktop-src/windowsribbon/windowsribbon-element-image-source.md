---
title: Image. source, propriété
description: Représente le chemin d’accès au répertoire d’une image.
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- Image. source, ruban Windows
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740997"
---
# <a name="imagesource-property"></a>Image. source, propriété

Représente le chemin d’accès au répertoire d’une image.

## <a name="usage"></a>Utilisation

``` syntax
<Image.Source/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                                                 |
|---------------------------------------------------------|
| [**Image**](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a>Notes

Optionnel.

Peut se produire au plus une fois pour chaque [**image**](windowsribbon-element-image.md).

Cet élément contient une valeur de type *XS : anyURI* ou toute séquence de caractères qui représente un Uniform Resource Identifier (Uri). La valeur URI est un chemin d’accès de répertoire absolu ou relatif (au fichier de balisage du ruban) d’une ressource image de type bitmap (BMP).

## <a name="examples"></a>Exemples

L’exemple de code suivant montre le balisage requis pour déclarer, via un ensemble d’éléments [**image**](windowsribbon-element-image.md) , une collection de ressources d’image conçues pour prendre en charge quatre paramètres de résolution d’écran spécifiques. La propriété **image. source** est utilisée pour spécifier le chemin d’accès à la ressource d’image.


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



 

 





