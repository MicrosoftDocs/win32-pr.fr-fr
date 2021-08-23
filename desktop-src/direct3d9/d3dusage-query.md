---
description: Ces options identifient les types de ressources de requête.
ms.assetid: d2030002-bd44-443f-8235-978919ebbda6
title: D3DUSAGE_QUERY
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d681b093b8dacbd78e42ff2d8fa700954b3efb02b571d0b33097d29152e1d82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988859"
---
# <a name="d3dusage_query"></a>\_Requête D3DUSAGE

Ces options identifient les types de ressources de requête.



| \#définition                                   | Description                                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_Filtre de requête D3DUSAGE \_                    | Interrogez le format de ressource pour voir s’il prend en charge les types de filtre de texture autres que le point de D3DTEXF \_ (qui est toujours pris en charge).                                                                                                                                                                                                                         |
| D3DUSAGE \_ requête \_ LEGACYBUMPMAP             | Interrogez la ressource sur une carte d’un relief hérité.                                                                                                                                                                                                                                                                                                         |
| \_ \_ Fusion POSTPIXELSHADER de requête D3DUSAGE \_ | Interrogez la ressource pour vérifier la prise en charge de la prise en charge de la fusion de nuanceur de pixels. Si [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) échoue avec la \_ fusion de POSTPIXELSHADER de requêtes D3DUSAGE \_ \_ , les opérations de fusion de pixels ne sont pas prises en charge. Il s’agit notamment du test alpha, du brouillard de pixel, de la fusion de cibles de rendu, de l’activation de l’écriture des couleurs et du tramage. |
| D3DUSAGE \_ requête \_ SRGBREAD                  | Interrogez la ressource pour vérifier si une texture prend en charge la correction gamma au cours d’une opération de lecture.                                                                                                                                                                                                                                                        |
| D3DUSAGE \_ requête \_ SRGBWRITE                 | Interrogez la ressource pour vérifier si une texture prend en charge la correction gamma au cours d’une opération d’écriture.                                                                                                                                                                                                                                                       |
| D3DUSAGE \_ requête \_ VERTEXTEXTURE             | Interrogez la ressource pour vérifier la prise en charge de l’échantillonnage de texture vertex shader.                                                                                                                                                                                                                                                                            |
| D3DUSAGE \_ requête \_ WRAPANDMIP                | Interrogez la ressource pour vérifier la prise en charge de l’encapsulation de texture et du mappage MIP.                                                                                                                                                                                                                                                                          |



 

Utilisez [**CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) pour interroger la prise en charge matérielle de ces utilisations et d’autres utilisations listées dans [D3DUSAGE](d3dusage.md).

## <a name="constant-information"></a>Informations constantes



| Condition requise                         | Valeur            |
|--------------------------|-------------|
| En-tête                   | d3d9types. h |
| Système d’exploitation minimal | Windows 98  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
