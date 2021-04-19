---
description: Le terme blit est raccourci pour &\# 0034 ; transfert de blocs binaires, &\# 0034 ; il s’agit du processus de transfert des blocs de données d’un emplacement à un autre dans la mémoire.
ms.assetid: 5f2aed2e-66d2-40e6-be35-92c3f92d17bd
title: Copie de surfaces (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50000e3b620c4d2fd217695551d898e5892430ba
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514542"
---
# <a name="copying-surfaces-direct3d-9"></a>Copie de surfaces (Direct3D 9)

Le terme blit est raccourci pour « transfert de blocs binaires », qui est le processus de transfert des blocs de données d’un emplacement à un autre dans la mémoire. L’interface de pilote de périphérique (DDI) blitting continue à être utilisée dans Direct3D 9 comme mécanisme principal pour déplacer de grands rectangles de pixels en fonction de la trame, le mécanisme sous-jacent de la méthode de IDirect3DDevice9 de copie [**::P**](/windows/desktop/api) renouvelée. Le transport de l’illustration dans l’opération blit est effectué par la méthode [**IDirect3DDevice9 :: UpdateTexture**](/windows/desktop/api) . L’illustration peut également être copiée dans Direct3D 9 à l’aide de la méthode [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface) , qui copie un sous-ensemble rectangulaire de pixels.

> [!Note]  
> Direct3D 9 fournit des fonctions D3DX qui vous permettent de charger des illustrations à partir de fichiers, d’appliquer une conversion des couleurs et de redimensionner des illustrations. Pour plus d’informations sur les fonctions disponibles [, consultez fonctions de texture dans D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> <dt>

[**IDirect3DDevice9::StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect)
</dt> <dt>

**IDirect3DDevice9::StretchRect**
</dt> </dl>

 

 
