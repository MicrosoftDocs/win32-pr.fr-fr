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
ms.openlocfilehash: 90d31aa6a11ce8e2bdd75ff1171705cc9b3de437
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826613"
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

## <a name="remarks"></a>Remarques

Cette valeur doit être définie au cours de la fonction de constante de patch du nuanceur de coque.

Valeur de sortie requise pour le nuanceur de coque si vous utilisez des correctifs quad ou tri. Cette valeur est une entrée requise pour le nuanceur de domaine afin que le matériel corresponde aux signatures via le du paveur.

Cette fonction est prise en charge dans les types de nuanceurs suivants :



| Sommet | Forme | Domaine | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    | x      |          |       |         |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sémantique](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




