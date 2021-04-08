---
title: Exemple de section bitmap
description: Exemple de section bitmap
ms.assetid: 51b84b34-3cbb-4863-b7dc-e33e80d6ba23
keywords:
- Apparences mobiles du lecteur Windows Media, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans une apparence, section bitmaps
- fichiers de définition d’apparence, section bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840453"
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
> La région et les super bitmaps sont dépréciées dans les habillages pour Windows Media Player 10 mobile ou version ultérieure.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Images bitmap**](bitmaps.md)
</dt> </dl>

 

 




