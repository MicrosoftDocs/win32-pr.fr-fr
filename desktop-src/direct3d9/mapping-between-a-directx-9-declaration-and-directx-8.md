---
title: Mappage entre les déclarations D3D9 et D3D8
description: Ce tableau mappe les membres d’une déclaration D3DVERTEXELEMENT9 à une déclaration Direct3D 8.
ms.assetid: da02b2cd-5221-4d37-97d5-840df91e39a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5c52bd804907f201916386ef5fa5776a32a046b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745549"
---
# <a name="map-between-d3d9-and-d3d8-declarations"></a>Mappage entre les déclarations D3D9 et D3D8

Ce tableau mappe les membres d’une déclaration [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) à une déclaration Direct3D 8.



| Utilisation de Direct3D 9           | Index d’utilisation Direct3D 9 | Direct3D 8            |
|----------------------------|------------------------|-----------------------|
| \_Position D3DDECLUSAGE     | 0                      | \_Position D3DVSDE     |
| \_Position D3DDECLUSAGE     | 1                      | D3DVSDE \_ POSITION2    |
| D3DDECLUSAGE \_ normal       | 0                      | D3DVSDE \_ normal       |
| D3DDECLUSAGE \_ normal       | 1                      | D3DVSDE \_ NORMAL2      |
| D3DDECLUSAGE \_ BLENDWEIGHT  | 0                      | D3DVSDE \_ BLENDWEIGHT  |
| D3DDECLUSAGE \_ BLENDINDICES | 0                      | D3DVSDE \_ BLENDINDICES |
| D3DDECLUSAGE \_ psize        | 0                      | D3DVSDE \_ psize        |
| \_Couleur D3DDECLUSAGE        | 0                      | \_Diffusion D3DVSDE      |
| \_Couleur D3DDECLUSAGE        | 1                      | D3DVSDE \_ spéculaire     |
| D3DDECLUSAGE \_ texcoord     | n                      | D3DVSDE \_ TEXCOORDn    |



 

Quand une déclaration est utilisée avec le traitement du vertex matériel sur un pilote Direct3D 7, le runtime Direct3D le convertit en une Commission des prix à la une, avec les règles suivantes :

-   Seul Stream 0 doit être utilisé (évident à partir de l’extrémité MaxStreams).
-   L’ordre des éléments de vertex doit être le même que l’ordre des bits de la Commission.
-   Les écarts dans les coordonnées de texture ne sont pas autorisés.
-   Tout élément vertex non décrit la table ne peut pas être convertie en une Commission valide pour tous les pilotes antérieurs à DirectX 8 et, par conséquent, ne peut pas être utilisée sur ces pilotes.
-   Seul D3DDECLTYPE \_ FLOAT2 est autorisé pour les éléments de vertex avec D3DDECLUSAGE \_ texcoord si l’appareil n’a pas défini l’une des deux \_ majuscules D3DPTEXTURECAPS Projected ou D3DPTEXTURECAPS carte cubique \_ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclaration de vertex](vertex-declaration.md)
</dt> </dl>

 

 



