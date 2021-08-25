---
description: Le mode d’adresse de texture clamp, identifié par le \_ membre D3DTADDRESS clamp du type énuméré D3DTEXTUREADDRESS, amène Direct3D à fixer vos coordonnées de texture à la \[ plage 0,0 1,0 \] .
ms.assetid: 8efed38d-4c9f-4a8d-9d1b-af1c8df9292a
title: Mode d’adresse de texture clamp (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0602b66c28dfbd48cc7ac3504ff643cd0ffe31769ee8edbeede5b4b870914289
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751353"
---
# <a name="clamp-texture-address-mode-direct3d-9"></a>Mode d’adresse de texture clamp (Direct3D 9)

Le mode d’adresse de texture clamp, identifié par le \_ membre D3DTADDRESS clamp du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , amène Direct3D à fixer vos coordonnées de texture à \[ la plage 0,0 1,0 \] . Autrement dit, il applique la texture une seule fois, puis frotte la couleur des pixels du bord. Supposons, par exemple, que votre application crée une primitive carrée et assigne des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0) aux sommets de la primitive. Si vous définissez le mode d’adressage de la texture sur D3DTADDRESS \_ clamp, la texture est appliquée une seule fois. Les couleurs de pixel en haut des colonnes et la fin des lignes sont étendues respectivement en haut et à droite de la primitive.

L’illustration suivante montre une texture débloquée.

![illustration d’une texture et d’une texture débloquée](images/clamp.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes d’adressage de la texture](texture-addressing-modes.md)
</dt> </dl>

 

 
