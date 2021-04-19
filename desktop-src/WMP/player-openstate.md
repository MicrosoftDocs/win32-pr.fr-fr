---
title: Player. openState
description: La propriété openState récupère une valeur indiquant l’état de la source de contenu.
ms.assetid: d38eadad-d0f0-40a9-92c6-1c745a0d4f1b
keywords:
- Lecteur Windows Media Player. openState
topic_type:
- apiref
api_name:
- Player.openState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87ad682a0c9ea6420ec291cbe66a7f81c9062e4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532503"
---
# <a name="playeropenstate"></a>Player. openState

La propriété **openState** récupère une valeur indiquant l’état de la source de contenu.

## <a name="syntax"></a>Syntaxe

*lecteur* . **openState**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un **nombre** en lecture seule (**long**). La constante d’énumération de style C peut être dérivée en préfixant la valeur d’État avec « wmpos ». Par exemple, la constante de l’État PlaylistOpening est **wmposPlaylistOpening**.



| Valeur | State                   | Description                                                                                                                                            |
|-------|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Indéfini               | Le lecteur Windows Media est dans un État non défini.                                                                                                         |
| 1     | PlaylistChanging        | La nouvelle sélection va être chargée.                                                                                                                    |
| 2     | PlaylistLocating        | Le lecteur Windows Media tente de localiser la sélection. La sélection peut être locale (bibliothèque ou métafichier avec une extension de nom de fichier. asx) ou distante. |
| 3     | PlaylistConnecting      | Connexion à la sélection.                                                                                                                            |
| 4     | PlaylistLoading         | La sélection a été trouvée et est maintenant en cours de récupération.                                                                                                    |
| 5     | PlaylistOpening         | La sélection a été récupérée et est maintenant en cours d’analyse et de chargement.                                                                                        |
| 6     | PlaylistOpenNoMedia     | La sélection est ouverte.                                                                                                                                      |
| 7     | PlaylistChanged         | Une nouvelle sélection a été affectée à **currentPlaylist**.                                                                                               |
| 8     | MediaChanging           | Un nouvel élément multimédia est sur le point d’être chargé.                                                                                                                |
| 9     | MediaLocating           | Le lecteur Windows Media recherche l’élément multimédia. Le fichier peut être local ou distant.                                                                      |
| 10    | MediaConnecting         | Connexion au serveur qui contient l’élément multimédia.                                                                                                    |
| 11    | MediaLoading            | L’élément multimédia a été localisé et est maintenant en cours de récupération.                                                                                                |
| 12    | MediaOpening            | L’élément multimédia a été récupéré et est maintenant en cours d’ouverture.                                                                                                 |
| 13    | MediaOpen               | L’élément multimédia est maintenant ouvert.                                                                                                                                |
| 14    | BeginCodecAcquisition   | Démarrage de l’acquisition du codec.                                                                                                                            |
| 15    | EndCodecAcquisition     | L’acquisition du codec est terminée.                                                                                                                         |
| 16    | BeginLicenseAcquisition | Acquisition d’une licence pour lire du contenu protégé par DRM.                                                                                                     |
| 17    | EndLicenseAcquisition   | La licence de lecture de contenu DRM protégé a été acquise.                                                                                               |
| 18    | BeginIndividualization  | Commencez l’individualisation DRM.                                                                                                                           |
| 19    | EndIndividualization    | L’individualisation DRM est terminée.                                                                                                              |
| 20    | MediaWaiting            | En attente d’un élément multimédia.                                                                                                                                |
| 21    | OpeningUnknownURL       | Ouverture d’une URL avec un type inconnu.                                                                                                                    |



 

## <a name="remarks"></a>Notes

Il n’est pas garanti que les États du lecteur Windows Media se produisent dans un ordre particulier. En outre, tous les États ne se produisent pas nécessairement au cours d’une séquence d’événements. Vous ne devez pas écrire du code qui s’appuie sur l’ordre de l’État.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Événement Player. OpenStateChange**](player-player-openstatechange.md)
</dt> </dl>

 

 





