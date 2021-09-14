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
ms.openlocfilehash: 36dbc6dc20d61baf4e0820dd0b6e10d3e6e918ae
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922436"
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

 

 




