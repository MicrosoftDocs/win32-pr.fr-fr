---
title: Section bitmaps
description: Section bitmaps
ms.assetid: db2801e5-c55a-4681-9fe9-6027f28653e0
keywords:
- Lecteur Windows Media Skins mobiles, bitmaps
- habillages, images bitmap
- création d’habillages, section bitmaps
- écriture de code pour les habillages, section bitmaps
- bitmaps dans une apparence, section bitmaps
- fichiers de définition d’apparence, section bitmaps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3062a8679e916fc8eaa733ab82c3df51845969873fcf83534be5f9ec6e4c6f14
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573459"
---
# <a name="bitmaps-section"></a>Section bitmaps

Ensuite, vous devez disposer d’une section qui définit chacun de vos fichiers bitmap. Un fichier doit être assigné à chaque type de bitmap que vous allez utiliser, même si vous pouvez avoir plusieurs types utilisant la même bitmap.


```C++
[ Bitmaps ]

//  <Name>      <File name>     <X,Y>
//  ------      -----------     -----
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



La section bitmaps doit commencer par le mot bitmaps entre crochets, puis une ligne pour chaque type de bitmap que vous souhaitez définir. Dans cet exemple, cinq types de bitmaps ont été définis. Pour plus d’informations sur la section bitmaps, consultez [bitmaps](bitmaps.md) dans la référence d’apparence.

> [!Note]  
> la région et les Super bitmaps sont dépréciées dans Lecteur Windows Media 10 apparences Mobile ou ultérieures.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Écriture du code**](writing-the-code.md)
</dt> </dl>

 

 




