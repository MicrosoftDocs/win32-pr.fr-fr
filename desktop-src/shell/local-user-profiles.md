---
description: Le système crée automatiquement un profil utilisateur local pour chaque utilisateur quand l’utilisateur ouvre une session sur l’ordinateur pour la première fois. Le système conserve automatiquement les paramètres de l’environnement de travail de chaque utilisateur dans un profil utilisateur sur l’ordinateur local.
title: Profils utilisateur locaux
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0e6c060e-025e-4d00-9b92-4f3b7bf66dda
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ba330189b11875198ce40ffdb9dd34925e3adc4b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127226873"
---
# <a name="local-user-profiles"></a>Profils utilisateur locaux

la sécurité Windows nécessite un profil utilisateur pour chaque compte d’utilisateur sur un ordinateur. Le système crée automatiquement un *profil utilisateur local* pour chaque utilisateur quand l’utilisateur ouvre une session sur l’ordinateur pour la première fois. Le système conserve automatiquement les paramètres de l’environnement de travail de chaque utilisateur dans un profil utilisateur sur l’ordinateur local.

Windows Vista et versions ultérieures : les profils utilisateur sont gérés via l’élément **comptes d’utilisateur** du panneau de configuration.

Windows 2000 et Windows XP : pour copier ou supprimer un profil utilisateur, sélectionnez **système** dans le panneau de configuration, puis l’onglet **avancé** , puis le bouton **Paramètres** dans la zone **profil utilisateur** .

Le profil de l’utilisateur n’est pas chargé automatiquement lorsque l’utilisateur a ouvert une session à l’aide de la fonction [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Pour charger un profil utilisateur par programme, utilisez la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Pour décharger un profil utilisateur chargé par **LoadUserProfile**, appelez la fonction [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
