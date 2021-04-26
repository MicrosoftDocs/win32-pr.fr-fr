---
description: Indicateurs de capacité du pilote D3DDEVCAPS2.
ms.assetid: 3f3b9f86-dee3-4506-bd2e-1dcc8ba617ed
title: D3DDEVCAPS2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ef30540f19add130aaca6eb48655a5ac47b2b4
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999466"
---
# <a name="d3ddevcaps2"></a>D3DDEVCAPS2

Indicateurs de capacité du pilote D3DDEVCAPS2.



| \#définition                                        | Description                                                                                                                                                                                                               |
|-------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DDEVCAPS2 \_ ADAPTIVETESSRTPATCH                | L’appareil prend en charge le pavage adaptatif des correctifs RT                                                                                                                                                                       |
| D3DDEVCAPS2 \_ ADAPTIVETESSNPATCH                 | L’appareil prend en charge le pavage adaptatif des N-patchs.                                                                                                                                                                       |
| D3DDEVCAPS2 \_ peut \_ STRETCHRECT \_ des \_ textures   | L’appareil prend en charge [**StretchRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-stretchrect) à l’aide d’une texture comme source.                                                                                                                       |
| D3DDEVCAPS2 \_ DMAPNPATCH                         | L’appareil prend en charge les mappages de déplacement pour N-patchs.                                                                                                                                                                          |
| D3DDEVCAPS2 \_ PRESAMPLEDDMAPNPATCH               | L’appareil prend en charge les mappages de remplacement prééchantillonnés pour les N-patchs. Pour plus d’informations sur le mappage de déplacement, consultez [mappage de déplacement (Direct3D 9)](displacement-mapping.md).                                           |
| D3DDEVCAPS2 \_ STREAMOFFSET                       | L’appareil prend en charge les décalages de flux.                                                                                                                                                                                           |
| D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET | Plusieurs éléments vertex peuvent partager le même offset dans un flux si D3DDEVCAPS2 \_ VERTEXELEMENTSCANSHARESTREAMOFFSET est défini par l’appareil et que la déclaration de vertex n’a pas d’élément avec D3DDECLUSAGE \_ POSITIONT0. |



 

## <a name="constant-information"></a>Informations constantes



|                          |            |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
