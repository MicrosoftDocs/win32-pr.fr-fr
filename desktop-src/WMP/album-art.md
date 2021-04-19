---
title: Pochette de l’album
description: Pochette de l’album
ms.assetid: a5996232-e1ee-41ae-a6ca-f841321644fe
keywords:
- Windows Media Player Mobile Skins, pochette d’album
- apparences, pochette d’album
- référence pour les habillages, la pochette d’album
- fichiers art pour les habillages, la pochette d’album
- pochette d’album dans des habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0974f8683da98469e75a4472d086dcb1a244c75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509993"
---
# <a name="album-art"></a>Pochette de l’album

Quand vous créez une apparence pour Windows Media Player 10 mobile ou version ultérieure, vous pouvez afficher une pochette d’album qui se réfère à l’élément multimédia en cours de lecture. Lorsque vous concevez votre apparence, vous souhaiterez réserver de l’espace dans l’image d’arrière-plan pour contenir la pochette de l’album.

La section de la pochette de l’album du fichier de définition d’apparence doit commencer par la ligne suivante :


```C++
[ Album Art ]

```



Vous devez ensuite ajouter des informations qui spécifient l’emplacement et la taille de la pochette de l’album dans votre apparence. Vous devez entrer quatre entiers positifs, séparés par des virgules qui définissent la gauche, le haut, la largeur et la hauteur de la pochette de l’album, en pixels, par rapport à l’image d’arrière-plan. L’exemple suivant montre comment spécifier des dimensions :


```C++
//  <Location>
//  ----------
   5,37,230,155

```



Si vous envisagez d’inclure une section vidéo dans votre apparence, vous pouvez utiliser la même taille et l’emplacement de votre pochette pour économiser de l’espace.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Référence d’apparence**](skin-reference.md)
</dt> </dl>

 

 




