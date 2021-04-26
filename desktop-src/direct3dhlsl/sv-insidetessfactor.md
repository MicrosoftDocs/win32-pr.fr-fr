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
ms.openlocfilehash: 4d047f7961868de020ac50ffce22b6ce02d078a5
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996916"
---
# <a name="sv_insidetessfactor"></a>SV \_ InsideTessFactor

Définit la quantité de pavage dans une surface corrective.

## <a name="type"></a>Type



|            |                |
|------------|----------------|
| Type       | Topologie d’entrée |
| float \[ 2\] | correctif Quad     |
| float      | correctif triple      |
| unused     | isoligne        |



 

Les facteurs de pavage doivent être déclarés en tant que tableau ; ils ne peuvent pas être empaquetés dans un seul vecteur.

## <a name="remarks"></a>Remarques

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

 

 




