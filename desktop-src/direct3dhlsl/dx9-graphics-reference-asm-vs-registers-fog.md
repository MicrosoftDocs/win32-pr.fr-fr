---
title: Registre de brouillard
description: Ce registre de sortie du nuanceur de sommets contient une couleur de brouillard par vertex.
ms.assetid: b2b06aa9-ad75-48df-857d-fd8719176713
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c3f0e39c0670176b6233f61f0ba50596c92ca4d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104971423"
---
# <a name="fog-register"></a>Registre de brouillard

Ce registre de sortie du nuanceur de sommets contient une couleur de brouillard par vertex.

Un registre se compose de propriétés qui déterminent le comportement de chaque registre.



| Propriété        | Description                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Nom            | oFog                                                                                            |
| Count           | Un vecteur, dont un seul composant peut être utilisé et doit être spécifié par le masque de composant |
| Autorisations d’e/s | En écriture seule.                                                                                     |



 

La valeur de brouillard de sortie est inscrite. La valeur est le facteur de brouillard à interpoler, puis est routé vers la table de brouillard. Seul le composant x scalaire du brouillard est utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




