---
description: Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré D3DTEXTUREADDRESS, fait en sorte que Direct3D répète la texture sur chaque jonction d’entier.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Mode d’adressage de texture de retour à la ligne (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200676"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a>Mode d’adressage de texture de retour à la ligne (Direct3D 9)

Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fait en sorte que Direct3D répète la texture sur chaque jonction d’entier. Supposons, par exemple, que votre application crée une primitive carrée et spécifie des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0). La définition du mode d’adressage de la texture sur D3DTADDRESS \_ encapsule les résultats dans la texture appliquée trois fois dans les directions u et v, comme indiqué dans l’illustration suivante.

![illustration d’une texture faciale encapsulée dans la direction u et l’axe v](images/wrap.png)

Les effets de ce mode d’adresse de texture sont similaires à ceux du mode miroir, mais diffèrent de ceux-ci. Pour plus d’informations, consultez [mode d’adresse de texture miroir (Direct3D 9)](mirror-texture-address-mode.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes d’adressage de la texture](texture-addressing-modes.md)
</dt> </dl>

 

 
