---
title: Exemple de section bitmap
description: Exemple de section bitmap
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Lecteur Windows Media Skins mobiles, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans une apparence, section bitmaps
- fichiers de définition d’apparence, section bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de401906896abcdda4728ff0984871ef4a399d3e223b36afd9d585eb0e4fce76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118833393"
---
# <a name="sample-bitmap-section"></a>Exemple de section bitmap

Les lignes suivantes affichent une section bitmaps standard d’un fichier de définition d’apparence :


```C++
[ Bitmaps ]

//  <Type>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0
    

```



Cela définit cinq bitmaps utilisés pour créer une image d’arrière-plan, des images pour les boutons désactivés et poussés, une image de région pour les boutons régionaux et une super image pour trackbars.

> [!Note]  
> la région et les Super bitmaps sont dépréciées dans les habillages pour Lecteur Windows Media 10 Mobile ou version ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Images bitmap**](bitmaps.md)
</dt> </dl>

 

 




