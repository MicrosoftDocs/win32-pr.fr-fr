---
description: Direct3D utilise une forme de filtrage de texture linéaire appelée Filtrage bilinéaire.
ms.assetid: vs|directx_sdk|~\linear_texture_filtering.htm
title: Filtrage de texture linéaire (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7940bd693ec42ef4f48920a5a362fad5f5b0bf02
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521927"
---
# <a name="linear-texture-filtering-direct3d-9"></a>Filtrage de texture linéaire (Direct3D 9)

Direct3D utilise une forme de filtrage de texture linéaire appelée Filtrage bilinéaire. À l’instar [de l’échantillonnage à point le plus proche (Direct3D 9)](nearest-point-sampling.md), le filtrage de texture bilinéaire calcule d’abord une adresse Texel, qui n’est généralement pas une adresse d’entier. Le filtrage bilinéaire recherche ensuite l’Texel dont l’adresse entière est la plus proche de l’adresse calculée. En outre, le module de rendu Direct3D calcule une moyenne pondérée des texels immédiatement au-dessus, en dessous, à gauche et à droite du point d’échantillonnage le plus proche.

Sélectionnez le filtrage de texture bilinéaire en appelant la méthode [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) . Définissez la valeur du premier paramètre sur le numéro d’index entier (0-7) de la texture pour laquelle vous sélectionnez une méthode de filtrage de texture. Transmettez D3DSAMP \_ MAGFILTER, D3DSAMP \_ MINFILTER ou D3DSAMP \_ MIPFILTER pour le deuxième paramètre afin de définir le filtre d’agrandissement, de minimisation ou de mappage MIP. Transmettez D3DTEXF \_ Linear dans le troisième paramètre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage de texture](texture-filtering.md)
</dt> </dl>

 

 
