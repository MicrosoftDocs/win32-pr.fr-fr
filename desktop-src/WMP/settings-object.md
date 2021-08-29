---
title: Paramètres objet (kit de développement logiciel Lecteur Windows Media)
description: l’objet Paramètres fournit un moyen de modifier différents paramètres de Lecteur Windows Media à l’aide des propriétés et méthodes suivantes.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Paramètres Lecteur Windows Media d’objets
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e763a4792530b3ab0809c33277bdf92dc90fe4c0251b3d329b4c3f3f36b55f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002359"
---
# <a name="settings-object"></a>Paramètres Dessin

l’objet **Paramètres** fournit un moyen de modifier différents paramètres de Lecteur Windows Media à l’aide des propriétés et méthodes suivantes.

l’objet **Paramètres** prend en charge les propriétés suivantes.



| Propriété                                                  | Description                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Démarrage automatique](settings-autostart.md)                       | Spécifie ou récupère une valeur indiquant si l’élément multimédia actuel commence à être lu automatiquement.                           |
| [équilibrée](settings-balance.md)                           | Spécifie ou récupère le solde stéréo actuel.                                                                               |
| [baseURL](settings-baseurl.md)                           | Spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec des commandes de script d’URL incorporées dans des fichiers multimédias. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | récupère l’identificateur de paramètres régionaux (LCID) de la langue audio par défaut spécifiée dans Lecteur Windows Media.                          |
| [defaultFrame](settings-defaultframe.md)                 | Spécifie ou récupère le nom du frame utilisé pour afficher une URL qui est reçue dans un événement **commande** .                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Spécifie ou récupère une valeur indiquant si les boîtes de dialogue d’erreur s’affichent automatiquement.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Spécifie ou récupère une valeur indiquant si les événements d’URL doivent lancer un navigateur Web.                                        |
| [isAvailable](settings-isavailable.md)                   | Récupère une valeur indiquant si un type d’informations spécifié est disponible ou si une action spécifiée peut être exécutée.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Récupère une valeur indiquant les droits actuellement accordés pour l’accès à la bibliothèque.                                                    |
| [muette](settings-mute.md)                                 | Spécifie ou récupère une valeur indiquant si l’audio est muet.                                                                |
| [playCount](settings-playcount.md)                       | Spécifie ou récupère le nombre de fois qu’un élément multimédia doit être lu.                                                               |
| [évaluation](settings-rate.md)                                 | Spécifie ou récupère la vitesse de lecture actuelle.                                                                                |
| [volume](settings-volume.md)                             | Spécifie ou récupère le volume actuel.                                                                                       |



 

l’objet **Paramètres** prend en charge les méthodes suivantes.



| Méthode                                                            | Description                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Détermine si le mode de boucle ou le mode de lecture aléatoire est actif. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Demande un niveau d’accès spécifié à la bibliothèque.        |
| [setMode](settings-setmode.md)                                   | Définit le mode de boucle ou le mode de lecture aléatoire (actif ou inactif).   |



 

l’objet **Paramètres** est accessible par le biais de la propriété suivante.



| Object                      | Propriété                        |
|-----------------------------|---------------------------------|
| [Lecteur](player-object.md) | [settings](player-settings.md) |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




