---
description: Les éléments d’API suivants sont utilisés avec les profils utilisateur.
title: Référence des profils utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 86871866-bb90-4287-9640-0a6cd136a800
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4b064eefae4916576cb8ccc6b3dfe058ea4e2e34f960315b74d384194f61ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967829"
---
# <a name="user-profiles-reference"></a>Référence des profils utilisateur

Les éléments d’API suivants sont utilisés avec les profils utilisateur.

## <a name="functions"></a>Fonctions



| Fonction                                                                   | Description                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock)                   | Récupère les variables d’environnement pour l’utilisateur spécifié.                                                   |
| [**CreateProfile**](/windows/desktop/api/Userenv/nf-userenv-createprofile)                                     | Crée un nouveau profil utilisateur. (Windows Vista et versions ultérieures uniquement.)                                                   |
| [**DeleteProfile**](/windows/desktop/api/Userenv/nf-userenv-deleteprofilea)                                     | Supprime le profil utilisateur et tous les paramètres liés à l’utilisateur de l’ordinateur spécifié.                           |
| [**DestroyEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-destroyenvironmentblock)                 | Libère les variables d’environnement créées par la fonction [**CreateEnvironmentBlock**](/windows/desktop/api/Userenv/nf-userenv-createenvironmentblock) . |
| [**ExpandEnvironmentStringsForUser**](/windows/desktop/api/Userenv/nf-userenv-expandenvironmentstringsforusera) | Développe la chaîne source à l’aide du bloc d’environnement établi pour l’utilisateur spécifié.                  |
| [**GetAllUsersProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getallusersprofiledirectorya)         | Récupère le chemin d’accès à la racine du profil tous les utilisateurs.                                                      |
| [**GetDefaultUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getdefaultuserprofiledirectorya)   | Récupère le chemin d’accès à la racine du profil utilisateur par défaut.                                                   |
| [**GetProfilesDirectory**](/windows/desktop/api/Userenv/nf-userenv-getprofilesdirectorya)                       | Récupère le chemin d’accès au répertoire racine dans lequel tous les profils utilisateur sont stockés.                                  |
| [**GetProfileType**](/windows/desktop/api/Userenv/nf-userenv-getprofiletype)                                   | Récupère le type de profil chargé pour l’utilisateur actuel.                                                    |
| [**GetUserProfileDirectory**](/windows/desktop/api/Userenv/nf-userenv-getuserprofiledirectorya)                 | Récupère le chemin d’accès au répertoire racine du profil de l’utilisateur spécifié.                                     |
| [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea)                                 | Charge le profil de l’utilisateur spécifié.                                                                           |
| [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile)                             | Décharge le profil d’un utilisateur qui a été chargé par la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) .          |



 

La fonction [**CreateUserProfileEx**](createuserprofileex.md) n’est pas prise en charge.

## <a name="structures"></a>Structures



| Structure                          | Description                                |
|------------------------------------|--------------------------------------------|
| [**PROFILEINFO**](/windows/desktop/api/Profinfo/ns-profinfo-profileinfoa) | Contient des informations sur un profil utilisateur. |



 

 

 



