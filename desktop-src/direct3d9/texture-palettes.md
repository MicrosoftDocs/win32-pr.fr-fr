---
description: Direct3D 9 prend en charge les textures de palette via un ensemble de palettes d’entrée 256 associées à l’objet IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Palettes de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291734"
---
# <a name="texture-palettes-direct3d-9"></a>Palettes de texture (Direct3D 9)

Direct3D 9 prend en charge les textures de palette via un ensemble de palettes d’entrée 256 associées à l’objet [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) . Une palette est rendue active en appelant la méthode [**IDirect3DDevice9 :: SetCurrentTexturePalette**](/windows/desktop/api) . La palette actuelle est utilisée pour la conversion de toutes les textures de palette pour toutes les étapes de texture actives. [**IDirect3DDevice9 :: SetPaletteEntries**](/windows/desktop/api) met à jour toutes les entrées 256 de la palette. Chaque entrée est une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) au format D3DFMT \_ A8R8G8B8. Toutes les entrées ont la valeur par défaut 0xFFFFFFFF.

Les palettes [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contiennent un canal alpha. Ce canal alpha peut être utilisé lorsque l’indicateur de fonctionnalité de l' \_ appareil D3DPTEXTURECAPS ALPHAPALETTE est défini, ce qui indique que l’appareil prend en charge alpha à partir de la palette. Le canal alpha de la palette est utilisé lorsque le format de texture n’a pas de canal alpha. Si l’appareil ne prend pas en charge alpha de la palette et que le format de texture n’a pas de canal alpha, la valeur 0xFF est utilisée pour alpha.

Il y a un maximum de 65 536 (0x0000FFFF) palettes. Étant donné que les ressources mémoire associées à l’ensemble de palettes sont proportionnelles au nombre maximal de palettes référencées par une application, utilisez des numéros de palette contigus à partir de zéro.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Concepts de base de la texturation](basic-texturing-concepts.md)
</dt> </dl>

 

 
