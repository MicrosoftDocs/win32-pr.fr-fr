---
title: Registre d’entrée
description: Registre d’entrée
ms.assetid: 7cd8e555-4e69-4905-a541-62e09b41a602
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b6682d8987f2df3ba3fb06427d41b722abb5eb003a4226a155c104cc3239d0f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982759"
---
# <a name="input-register"></a>Registre d’entrée

Registre d’entrée du nuanceur de sommets.

Les données de chaque vertex (à l’aide d’un ou plusieurs flux de vertex d’entrée) sont chargées dans les registres d’entrée de vertex avant l’exécution du nuanceur de sommets. Les registres d’entrée sont constitués de vecteurs à virgule flottante 16 4 composant, désignés comme v0 par v15. Ces registres sont en lecture seule. Un registre d’entrée est lié aux données de vertex par le biais d’une déclaration de vertex.

Les propriétés de Registre suivantes contrôlent le comportement de chaque registre :



| Propriété        | Description                                                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|
| Nom            | v \[ n \] -n est un numéro de Registre facultatif. 0 est la valeur par défaut utilisée, si elle est omise.     |
| Count           | Un maximum de 16 registres, V0-v15.                                                          |
| Autorisations d’e/s | Lecture seule. Ce registre ne peut pas être écrit par l’API ou dans le nuanceur.                   |
| Ports de lecture      | 1. il s’agit du nombre de fois qu’un registre peut être lu dans une instruction unique. Voir ci-dessous. |



 

Toute instruction unique ne peut accéder qu’à un seul registre d’entrée de vertex. Toutefois, chaque source de l’instruction peut Swizzle et inverser ce vecteur au fur et à mesure de sa lecture.

## <a name="example"></a>Exemple

Voici un exemple d’utilisation d’une déclaration de vertex pour lier des données de position de vertex 2D pour inscrire v0.

La déclaration de vertex appartient à l’application :


```
D3DVERTEXELEMENT9 decl[] =
{
    { 0, 0, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
      D3DDECL_END()
};
```



Voici la déclaration du nuanceur de sommets correspondant :


```
dcl_position v0
```





| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de position      | x    | x    | x     | x    | x    | x     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




