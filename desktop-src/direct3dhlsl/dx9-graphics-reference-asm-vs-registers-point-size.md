---
title: Registre de la taille du point
description: Ce registre de sortie du nuanceur de vertex contient des données de taille de point par vertex.
ms.assetid: 1aa6cd7d-9d29-4e7e-8448-8b9a6b251a02
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6de5c2fba55ce9cdfcee535ec001a89cbebcdddc5e3685224f9eb0c560870534
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119663"
---
# <a name="point-size-register"></a>Registre de la taille du point

Ce registre de sortie du nuanceur de vertex contient des données de taille de point par vertex.



| Versions de nuanceur vertex | 1\_1 | 2 \_ 0 | 2 \_ logiciels | 2 \_ x | 3 \_ 0 | 3 \_ logiciels |
|------------------------|------|------|-------|------|------|-------|
| Registre de la taille du point    | x    | x    | x     | x    | x    | x     |



 

Un registre se compose de propriétés qui déterminent le comportement de chaque registre.



| Propriété        | Description                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nom            | Décide                                                                                            |
| Count           | 1 vecteur, dont 1 seul composant peut être utilisé et doit être spécifié par le masque de composant. |
| Autorisations d’e/s | En écriture seule.                                                                                     |



 

Seul le composant x scalaire de la taille en points est utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




