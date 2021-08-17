---
description: Le mode d’adresse de texture miroir, identifié par le \_ membre miroir D3DTADDRESS du type énuméré D3DTEXTUREADDRESS, amène Direct3D à refléter la texture à chaque limite d’entier.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Mode d’adresse de texture miroir (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10ef8731c060e95c470bbf8d34222b9ee66e7f9da2c7a6f03a09c2989986ca3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728364"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a>Mode d’adresse de texture miroir (Direct3D 9)

Le mode d’adresse de texture miroir, identifié par le \_ membre miroir D3DTADDRESS du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , amène Direct3D à refléter la texture à chaque limite d’entier. Supposons, par exemple, que votre application crée une primitive carrée et spécifie des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0). Si vous définissez le mode d’adressage de la texture sur D3DTADDRESS, \_ les résultats de la texture sont appliqués trois fois dans les directions u et v. Chaque ligne et colonne à laquelle il est appliqué est une image miroir de la ligne ou de la colonne précédente, comme indiqué dans l’illustration suivante.

![illustration d’images miroir dans une grille 3x3](images/mirror.png)

Les effets de ce mode d’adresse de texture sont similaires à ceux du mode habillage, mais diffèrent de ceux-ci. Pour plus d’informations, consultez [Wrap texture mode Address (Direct3D 9)](wrap-texture-address-mode.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes d’adressage de la texture](texture-addressing-modes.md)
</dt> </dl>

 

 
