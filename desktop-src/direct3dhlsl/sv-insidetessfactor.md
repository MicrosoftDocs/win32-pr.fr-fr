---
title: SV_InsideTessFactor
description: Définit la quantité de pavage dans une surface corrective.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 043d1a43186623e81cb529d2906d4475291547d326bf2d75758c8ee696a812b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285505"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Définit la quantité de pavage dans une surface corrective.

## <a name="type"></a>Type



|  Type          | Topologie d’entrée               |
|------------|----------------|
| float \[ 2\] | correctif Quad     |
| float      | correctif triple      |
| unused     | isoligne        |



 

Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.

## <a name="remarks"></a>Notes

Cette valeur doit être définie au cours de la fonction de constante de patch du nuanceur de coque.

Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri. Cette valeur est une entrée requise pour le nuanceur de domaine afin que le matériel corresponde aux signatures via le du paveur.

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Calcul |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




