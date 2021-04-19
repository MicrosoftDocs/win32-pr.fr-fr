---
title: PLAYLIST. colonnes
description: L’attribut Columns définit les colonnes qui apparaissent dans l’élément PLAYLIST.
ms.assetid: a805ee06-cf73-4eab-bcda-c374e55cd11a
keywords:
- SÉLECTION. colonnes lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.columns
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc5f8ef5dc76428ca892d079b60692e6949a5ca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530441"
---
# <a name="playlistcolumns"></a>PLAYLIST. colonnes

L’attribut **Columns** définit les colonnes qui apparaissent dans l’élément **playlist** .

``` syntax
        elementID.columns
```

## <a name="possible-values"></a>Valeurs possibles

Cet attribut est une **chaîne** en lecture/écriture au format suivant :

nom de la base de noms \_ = nom convivial ; nom de la base de noms \_ \_ = \_ nom convivial ;

\_Nom convivial est la valeur indiquée dans l’en-tête de colonne de l’élément playlist et le nom de la base de \_ code est une valeur du tableau suivant. Notez qu’un élément de sélection peut être un élément multimédia de la bibliothèque ou d’un CD, ou qu’il peut s’agir d’une autre **sélection** créée par l’utilisateur ou effectuée à partir d’un CD. Certaines colonnes sont valides uniquement avec certains éléments de playlist comme indiqué dans la colonne Description.



| Valeur             | Description                                                                                                             |
|-------------------|-------------------------------------------------------------------------------------------------------------------------|
| Album             | Nom de l’album. Utilisé avec les éléments multimédias uniquement.                                                                      |
| Peinture            | Nom de l’artiste. Non utilisé avec les sélections créées par l’utilisateur.                                                           |
| Auteur            | Nom de l’artiste.                                                                                                 |
| Bitrate           | Vitesse de transmission du contenu. Utilisé uniquement avec les éléments multimédias de la bibliothèque.                                               |
| CDTrackEnabled    | Indique si la piste CD est activée. Utilisé uniquement avec les éléments de support CD.                                               |
| Activée           | Réservé pour un usage futur.                                                                                                |
| copyright         | Copyright de la sélection. Non utilisé avec les sélections de CD ou les éléments multimédias.                                               |
| CreationDate      | Date et heure de création de l’entrée dans la bibliothèque. Utilisé uniquement avec les éléments de la bibliothèque.                     |
| DigitallySecure   | Indique si l’élément est protégé par le gestionnaire de droits Windows Media. Utilisé uniquement avec les éléments multimédias de la bibliothèque. |
| Duration          | Durée de l’élément multimédia.                                                                                         |
| FileType          | Réservé pour un usage futur.                                                                                                |
| Genre             | Genre de la sélection. Non utilisé avec les playlists des CDs.                                                            |
| MediaAttribute    | Réservé pour un usage futur.                                                                                                |
| MediaType         | Type de l’élément multimédia (audio ou vidéo).                                                                            |
| Sous-dataSource    | Source des métadonnées de cette piste de CD (AMG, WindowsMedia.com, etc.). Utilisé uniquement avec les éléments de support CD.         |
| ModifiedBy        | Réservé pour un usage futur.                                                                                                |
| Nom              | Nom de la sélection.                                                                                               |
| OriginalIndex     | Le cas échéant, l’identificateur de piste CD correspondant. Utilisé uniquement avec les éléments de support CD.                                    |
| PlayCount         | Nombre de fois où le contenu a été lu jusqu’à la fin. Utilisé uniquement avec les éléments multimédias de la bibliothèque.        |
| PlaylistAttribute | Réservé pour un usage futur.                                                                                                |
| Rating            | Réservé pour un usage futur.                                                                                                |
| SourceURL         | Chemin d’accès ou URL du contenu. Utilisé uniquement avec les éléments multimédias de la bibliothèque.                                            |
| Statut            | État de copie d’une piste de CD en cours de copie. Utilisé uniquement avec les éléments de support CD.                                           |
| Style             | Réservé pour un usage futur.                                                                                                |
| Table des matières               | Le cas échéant, l’identificateur de la table des matières du CD correspondant. Non utilisé avec les sélections créées par l’utilisateur.                 |



 

## <a name="remarks"></a>Notes

Si l’une des colonnes n’existe pas dans la bibliothèque, elle est laissée vide.

Vous pouvez spécifier au maximum 31 colonnes.

Si vous spécifiez une colonne dupliquée, les données de la première colonne sont alignées à gauche, mais toutes les autres colonnes dupliquées sont alignées à droite. Par exemple, si vous avez deux colonnes de durée, les données sont alignées à gauche dans le premier et aligné à droite dans la seconde.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. columnsVisible**](playlist-columnsvisible.md)
</dt> </dl>

 

 





