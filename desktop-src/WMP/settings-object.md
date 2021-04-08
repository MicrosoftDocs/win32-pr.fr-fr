---
title: Settings (objet) (kit de développement logiciel Windows Media Player)
description: L’objet Settings permet de modifier différents paramètres du lecteur Windows Media à l’aide des propriétés et méthodes suivantes.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objet paramètres lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/12/2019
ms.locfileid: "103841626"
---
# <a name="settings-object"></a>Settings (objet)

L’objet **Settings** permet de modifier différents paramètres du lecteur Windows Media à l’aide des propriétés et méthodes suivantes.

L’objet **Settings** prend en charge les propriétés suivantes.



| Propriété                                                  | Description                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Démarrage automatique](settings-autostart.md)                       | Spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.                           |
| [équilibrée](settings-balance.md)                           | Spécifie ou récupère le solde stéréo actuel.                                                                               |
| [baseURL](settings-baseurl.md)                           | Spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans des fichiers multimédias. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | Récupère l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans le lecteur Windows Media.                          |
| [defaultFrame](settings-defaultframe.md)                 | Spécifie ou récupère le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **commande** .                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.                                        |
| [isAvailable](settings-isavailable.md)                   | Récupère une valeur indiquant si un type d’informations spécifié est disponible ou si une action spécifiée peut être exécutée.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Récupère une valeur indiquant les droits actuellement accordés pour l’accès à la bibliothèque.                                                    |
| [muette](settings-mute.md)                                 | Spécifie ou récupère une valeur indiquant si l’audio est muet.                                                                |
| [playCount](settings-playcount.md)                       | Spécifie ou récupère le nombre de fois qu’un élément multimédia doit être lu.                                                               |
| [évaluation](settings-rate.md)                                 | Spécifie ou récupère la vitesse de lecture actuelle.                                                                                |
| [volume](settings-volume.md)                             | Spécifie ou récupère le volume actuel.                                                                                       |



 

L’objet **Settings** prend en charge les méthodes suivantes.



| Méthode                                                            | Description                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Détermine si le mode de boucle ou le mode de lecture aléatoire est actif. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Demande un niveau d’accès spécifié à la bibliothèque.        |
| [setMode](settings-setmode.md)                                   | Définit le mode de boucle ou le mode de lecture aléatoire (actif ou inactif).   |



 

L’objet **Settings** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                        |
|-----------------------------|---------------------------------|
| [Lecteur](player-object.md) | [settings](player-settings.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




