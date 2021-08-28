---
title: bitmaps (kit de développement logiciel (SDK) Lecteur Windows Media)
description: Images bitmap
ms.assetid: cd10bc7d-1167-485e-8acf-13c021bc608b
keywords:
- Lecteur Windows Media Skins mobiles, bitmaps
- habillages, images bitmap
- informations de référence sur les apparences, les bitmaps
- bitmaps dans les apparences, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33ff4689c052162d8addfb9a66aeb6b227916f0e22e21de3e3572ea265380664
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123859"
---
# <a name="bitmaps-windows-media-player-sdk"></a>bitmaps (kit de développement logiciel (SDK) Lecteur Windows Media)

Vous devez utiliser une ou plusieurs images dans votre apparence, et chaque image doit être définie dans le fichier de définition d’apparence. Si vous ne définissez pas d’image dans cette section, votre apparence ne sera pas en mesure de l’utiliser.

Le terme « bitmap » est utilisé tout au long de la référence, et fait référence aux images bitmap avec une extension de .bmp, aux images GIF avec une extension de .gif, aux images JPEG avec une extension de .jpg et aux images PNG avec une extension de .png.

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

 

 




