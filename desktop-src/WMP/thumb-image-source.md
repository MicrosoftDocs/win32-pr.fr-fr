---
title: Source de l’image Thumb
description: Source de l’image Thumb
ms.assetid: dca1f54d-ee79-4fd4-9c4e-8226f65c9515
keywords:
- Windows Media Player Mobile Skins, trackbars
- habillages, trackbars
- informations de référence sur les habillages, trackbars
- trackbars dans les apparences, source d’image
- trackbars dans les habillages, source d’image Thumb
- source de l’image pour les apparences, trackbars
- Thumb, source de l’image
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac19053b58c7d12543d38c639abe5a43c01ff64
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028872"
---
# <a name="thumb-image-source"></a>Source de l’image Thumb

Vous devez définir le nom du fichier qui contient l’image Thumb. Il doit s’agir d’un nom de fichier valide avec l’extension. bmp,. gif,. jpg ou. png. Le fichier doit contenir trois images côte à côte de taille identique. Ils doivent être adjacents les uns aux autres sans espace. La position supérieure gauche de l’image de gauche doit être située dans l’angle supérieur gauche du fichier. L’image sur le côté gauche est l’image normale de l’image Thumb, tandis que l’image du milieu représente l’état de l’envoi et l’image à droite illustre l’état désactivé.


```C++
SeekThumb.bmp

```



Vous pouvez faire en sorte que certaines zones de l’image Thumb soient transparentes. Cela vous permettra de créer des images Thumb dans des formes autres que rectangulaires. Toute région de l’image Thumb que vous remplissez avec la couleur spécifiée par la valeur RVB 255, 0, 255 apparaîtra transparente dans votre apparence.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Trackbars**](trackbars.md)
</dt> </dl>

 

 




