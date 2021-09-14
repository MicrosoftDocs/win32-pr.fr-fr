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
ms.openlocfilehash: 00b05183be7ba56ed5b00a6bfd26ee6162e008cd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010877"
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

 

 




