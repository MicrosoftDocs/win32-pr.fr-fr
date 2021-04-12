---
title: Bitmaps (kit de développement logiciel Windows Media Player)
description: Images bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Apparences mobiles du lecteur Windows Media, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ad690b691c22154bad4db0981e2b5ab760400b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104464006"
---
# <a name="bitmaps-windows-media-player-sdk"></a>Bitmaps (kit de développement logiciel Windows Media Player)

Vous devez utiliser une ou plusieurs images dans votre apparence, et chaque image doit être définie dans le fichier de définition d’apparence. Si vous ne définissez pas d’image dans cette section, votre apparence ne sera pas en mesure de l’utiliser.

Le terme « bitmap » est utilisé tout au long de la référence, et fait référence aux images bitmap avec une extension. bmp, aux images GIF avec une extension. gif, aux images JPEG avec une extension. jpg et aux images PNG avec une extension. png.

La section bitmaps du fichier de définition d’apparence commence par cette ligne :


```C++
[ Bitmaps ]

```



Vous devez ensuite ajouter une ou plusieurs lignes qui contiennent des informations sur chacune des images de votre apparence.

Une ligne classique peut être :


```C++
    Background  Background.bmp  0,0

```



Vous pouvez utiliser le modèle suivant pour la section bitmaps de votre fichier de définition d’apparence :


```C++
//  <Type>      <Filename>      <X,Y>
//  ------      -----------     -----

```



Vous devez utiliser l’ordre suivant pour les informations de bitmap pour chaque ligne dans la section bitmap. Chaque partie de la ligne est requise.

1.  [Type de bitmap](bitmap-type.md)
2.  [Nom de fichier](file-name.md)
3.  [Coordinates](coordinates.md)

Pour obtenir un exemple de code bitmap, consultez la [section exemple de bitmap](sample-bitmap-section.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




