---
description: Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré D3DTEXTUREADDRESS, fait en sorte que Direct3D répète la texture sur chaque jonction d’entier.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Mode d’adressage de texture de retour à la ligne (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 820273a68754c11f17f4f2762c7e824562b8e52bfc0b2b097c21e82789ce4168
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627822"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Mode d’adressage de texture de retour à la ligne (Direct3D 9)

Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fait en sorte que Direct3D répète la texture sur chaque jonction d’entier. Supposons, par exemple, que votre application crée une primitive carrée et spécifie des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0). La définition du mode d’adressage de la texture sur D3DTADDRESS \_ encapsule les résultats dans la texture appliquée trois fois dans les directions u et v, comme indiqué dans l’illustration suivante.

![illustration d’une texture faciale encapsulée dans la direction u et l’axe v](images/wrap.png)

Les effets de ce mode d’adresse de texture sont similaires à ceux du mode miroir, mais diffèrent de ceux-ci. Pour plus d’informations, consultez [mode d’adresse de texture miroir (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes d’adressage de la texture](texture-addressing-modes.md)
</dt> </dl>

 

 
