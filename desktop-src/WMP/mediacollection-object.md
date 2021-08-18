---
title: Objet MediaCollection
description: L’objet MediaCollection offre un moyen d’organiser une grande collection d’éléments multimédias. Elle peut être interrogée pour générer automatiquement des sélections.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- objet MediaCollection Lecteur Windows Media
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8e529bec203b836f1f1022793a18320a7612cb242de58407ddb998c7410a47cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996249"
---
# <a name="mediacollection-object"></a>Objet MediaCollection

L’objet **MediaCollection** offre un moyen d’organiser une grande collection d’éléments multimédias. Elle peut être interrogée pour générer automatiquement des sélections.

L’objet **MediaCollection** prend en charge les méthodes suivantes.



| Méthode                                                                           | Description                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [add](mediacollection-add.md)                                                   | Ajoute un nouvel élément multimédia ou une nouvelle sélection à la bibliothèque.                                                                                                              |
| [createQuery](mediacollection-createquery.md)                                   | Crée un objet de [requête](query-object.md) .                                                                                                                |
| [getAll](mediacollection-getall.md)                                             | Récupère un objet [playlist](playlist-object.md) contenant tous les éléments multimédias de la bibliothèque.                                                                  |
| [getAttributeStringCollection](mediacollection-getattributestringcollection.md) | Récupère un objet [StringCollection](stringcollection-object.md) représentant l’ensemble de toutes les valeurs d’un attribut spécifié dans un type de média spécifié. |
| [getByAlbum](mediacollection-getbyalbum.md)                                     | Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias de l’album spécifié.                                                            |
| [getByAttribute](mediacollection-getbyattribute.md)                             | Récupère un objet de [sélection](playlist-object.md) contenant les éléments multimédias avec l’attribut spécifié ayant la valeur spécifiée.                             |
| [getByAttributeAndMediaType](mediacollection-getbyattributeandmediatype.md)     | Récupère un objet de [sélection](playlist-object.md) contenant des objets [multimédias](media-object.md) avec l’attribut et le type de média spécifiés.                 |
| [getByAuthor](mediacollection-getbyauthor.md)                                   | Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias par l’auteur spécifié.                                                             |
| [getByGenre](mediacollection-getbygenre.md)                                     | Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias avec le genre spécifié.                                                            |
| [getByName](mediacollection-getbyname.md)                                       | Récupère un objet de [sélection](playlist-object.md) contenant des éléments multimédias portant le nom spécifié.                                                             |
| [getMediaAtom](mediacollection-getmediaatom.md)                                 | Récupère l’index auquel une propriété spécifiée réside dans le jeu de propriétés disponibles.                                                              |
| [getPlaylistByQuery](mediacollection-getplaylistbyquery.md)                     | Récupère un objet de [sélection](playlist-object.md) contenant des objets [multimédias](media-object.md) qui correspondent aux conditions de requête.                               |
| [getStringCollectionByQuery](mediacollection-getstringcollectionbyquery.md)     | Récupère un objet [StringCollection](stringcollection-object.md) contenant des chaînes qui correspondent aux conditions de requête.                                         |
| [isDeleted](mediacollection-isdeleted.md)                                       | Récupère une valeur indiquant si l’élément multimédia spécifié se trouve dans le dossier éléments supprimés.                                                                  |
| [remove](mediacollection-remove.md)                                             | Supprime un élément de la collection de supports.                                                                                                                     |
| [setDeleted](mediacollection-setdeleted.md)                                     | Déplace l’élément multimédia spécifié vers le dossier éléments supprimés.                                                                                                    |



 

L’objet **MediaCollection** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                                      |
|-----------------------------|-----------------------------------------------|
| [Lecteur](player-object.md) | [mediaCollection](player-mediacollection.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




