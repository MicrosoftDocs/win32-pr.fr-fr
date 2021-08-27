---
description: Une carte de relief est un objet IDirect3DTexture9 qui utilise un format de pixel spécialisé.
ms.assetid: 7f405cb9-9512-44da-8a85-4b7d22017284
title: Formats de pixel de la carte de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f627ce95151207c25e2365d2e467fb94b93cfb5c1bf54ce0c3df401891fcafc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118805724"
---
# <a name="bump-map-pixel-formats-direct3d-9"></a>Formats de pixel de la carte de relief (Direct3D 9)

Une carte de relief est un objet [**IDirect3DTexture9**](/windows/desktop/api) qui utilise un format de pixel spécialisé. Au lieu de stocker les composants de couleur rouge, vert et bleu, chaque pixel d’une carte de relief stocke les valeurs Delta pour vous et v (D<sub>U</sub> et d<sub>v</sub>) et parfois un composant de luminance, L. Ces valeurs sont appliquées par le système, comme décrit dans la rubrique [formules de mappage de relief (Direct3D 9)](bump-mapping-formulas.md) .

Vous pouvez spécifier un format de pixel de la carte de relief en définissant le format sur l’un des éléments suivants : D3DFMT \_ CxV8U8, D3DFMT \_ V8U8, D3DFMT \_ L6V5U5, D3DFMT \_ X8L8V8U8, D3DFMT \_ Q8W8V8U8 ou D3DFMT V16U16 \_ . Pour obtenir des descriptions, consultez [D3DFORMAT](d3dformat.md).

Les composants D<sub>U</sub> et d<sub>V</sub> d’un pixel sont des valeurs signées comprises entre-1,0 et + 1,0. Le composant luminance, lorsqu’il est utilisé, est une valeur entière non signée comprise entre 0 et 255.

> [!Note]  
> Avant de choisir un format de pixel de placage de relief, vérifiez si le format particulier est pris en charge. Pour plus d’informations, consultez [utilisation du mappage de relief (Direct3D 9)](using-bump-mapping.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Placage de relief](bump-mapping.md)
</dt> </dl>

 

 



