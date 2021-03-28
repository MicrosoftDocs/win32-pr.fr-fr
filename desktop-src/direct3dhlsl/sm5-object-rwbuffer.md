---
title: RWBuffer
description: Mémoire tampon de lecture/écriture.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- HLSL RWBuffer
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312559"
---
# <a name="rwbuffer"></a>RWBuffer

Mémoire tampon de lecture/écriture.



| Méthode                                                     | Description                            |
|------------------------------------------------------------|----------------------------------------|
| [**GetDimensions**](sm5-object-rwbuffer-getdimensions.md) | Obtient les dimensions de ressource.          |
| [**Load**](rwbuffer-load.md)                              | Obtient une valeur dans un tampon en lecture-écriture. |
| [**Opérateur\[\]**](sm5-object-rwbuffer-operatorindex.md)  | Retourne une variable de ressource.           |



 

Une variable de ressource peut également être passée dans une opération non ordonnée ou verrouillée.

Les objets **RWBuffer** peuvent être précédés de la classe de stockage **globallycoherent**. Cette classe de stockage entraîne des barrières et des synchronisations de la mémoire pour vider les données sur l’ensemble du GPU, de telle sorte que les autres groupes puissent voir les écritures. Sans ce spécificateur, une barrière de mémoire ou une synchronisation vide un UAV uniquement dans le groupe actuel.

## <a name="minimum-shader-model"></a>Modèle de nuanceur minimal

Cet objet est pris en charge dans les modèles de nuanceur suivants.



| Modèle de nuanceur                                                                | Prise en charge |
|-----------------------------------------------------------------------------|-----------|
| [Nuancier modèle 5](d3d11-graphics-reference-sm5.md) et modèles de nuanceur supérieurs | Oui       |



 

Cet objet est pris en charge pour les types de nuanceurs suivants :



| Sommet | Forme | Domain | Géométrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     | x       |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Shader Model 5](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




