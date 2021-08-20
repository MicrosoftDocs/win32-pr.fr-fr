---
description: Un profil utilisateur obligatoire est un type spécial de profil utilisateur itinérant préconfiguré que les administrateurs peuvent utiliser pour spécifier des paramètres pour les utilisateurs.
title: Profils utilisateur obligatoires
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 09616c7f-1cec-48a0-a953-d4ae35fbd2f6
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 748135affd0b6be399242ff171c88a45da3047911f0603f47eccf0a1f0ba0018
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678143"
---
# <a name="mandatory-user-profiles"></a>Profils utilisateur obligatoires

Un profil utilisateur obligatoire est un type spécial de [profil utilisateur itinérant](roaming-user-profiles.md) préconfiguré que les administrateurs peuvent utiliser pour spécifier des paramètres pour les utilisateurs. Avec les profils utilisateur obligatoires, un utilisateur peut modifier son bureau, mais les modifications ne sont pas enregistrées lorsque l’utilisateur se déconnecte. La prochaine fois que l’utilisateur ouvre une session, le profil utilisateur obligatoire créé par l’administrateur est téléchargé. Il existe deux types de profils obligatoires : les profils *obligatoires normaux* et les profils *Super obligatoires* .

Les profils utilisateur deviennent des profils obligatoires lorsque l’administrateur renomme le fichier NTuser. dat (la ruche du registre) sur le serveur en NTuser. Man. L’extension. Man fait en sorte que le profil utilisateur soit un profil en lecture seule.

Les profils utilisateur deviennent *Super obligatoires* lorsque le nom du dossier du chemin d’accès du profil se termine par. Man ; par exemple, le \\ \\ partage de serveur \\ \\ mandatoryprofile. Man \\ .

Les profils utilisateur Super obligatoires sont similaires aux profils obligatoires normaux, à l’exception près que les utilisateurs qui ont des profils Super obligatoires ne peuvent pas ouvrir une session lorsque le serveur qui stocke le profil obligatoire n’est pas disponible. Les utilisateurs avec des profils obligatoires normaux peuvent se connecter avec la copie mise en cache localement du profil obligatoire.

Seuls les administrateurs système peuvent apporter des modifications aux profils utilisateur obligatoires.

 

 



