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
ms.openlocfilehash: b6aeaea0e51960f8f4bf768b855ac31236b2bb330cfda3390fd9e61dab4ec1f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854579"
---
# <a name="fog-register"></a>Registre de brouillard

Ce registre de sortie du nuanceur de sommets contient une couleur de brouillard par vertex.

Un registre se compose de propriétés qui déterminent le comportement de chaque registre.



| Propriété        | Description                                                                                     |
|-----------------|-------------------------------------------------------------------------------------------------|
| Name            | oFog                                                                                            |
| Count           | Un vecteur, dont un seul composant peut être utilisé et doit être spécifié par le masque de composant |
| Autorisations d’e/s | En écriture seule.                                                                                     |



 

La valeur de brouillard de sortie est inscrite. La valeur est le facteur de brouillard à interpoler, puis est routé vers la table de brouillard. Seul le composant x scalaire du brouillard est utilisé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Registres de nuanceur vertex](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




