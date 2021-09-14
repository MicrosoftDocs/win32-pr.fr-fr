---
description: si un ordinateur exécute Windows serveur 2000 ou version ultérieure sur un réseau, les utilisateurs peuvent stocker leurs profils sur le serveur. Ces profils sont appelés profils utilisateur itinérants.
title: Profils utilisateur itinérants
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8af06fdf-be99-4295-8f11-7d7f68e66956
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e3b95374b06c4efc665b231b4c7e1f1d81861dea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235199"
---
# <a name="roaming-user-profiles"></a>Profils utilisateur itinérants

si un ordinateur exécute Windows serveur 2000 ou version ultérieure sur un réseau, les utilisateurs peuvent stocker leurs profils sur le serveur. Ces profils sont appelés *profils utilisateur itinérants*.

Les profils utilisateur itinérants présentent les avantages suivants :

-   Disponibilité automatique des ressources. Le profil unique d’un utilisateur est automatiquement disponible lorsqu’il se connecte à un ordinateur sur le réseau. Les utilisateurs n’ont pas besoin de créer un profil sur chaque ordinateur qu’ils utilisent sur un réseau.
-   Remplacement et sauvegarde de l’ordinateur simplifiés. Lorsque l’ordinateur d’un utilisateur doit être remplacé, il peut être remplacé facilement, car toutes les informations de profil de l’utilisateur sont conservées séparément sur le réseau, indépendamment d’un ordinateur individuel. Lorsque l’utilisateur ouvre une session sur le nouvel ordinateur pour la première fois, la copie sur le serveur du profil de l’utilisateur est copiée sur le nouvel ordinateur.

Le profil de l’utilisateur n’est pas chargé automatiquement lorsque l’utilisateur a ouvert une session à l’aide de la fonction [**LogonUser**](/windows/win32/api/winbase/nf-winbase-logonusera) . Pour charger un profil utilisateur itinérant par programme, utilisez la fonction [**LoadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-loaduserprofilea) . Pour décharger un profil utilisateur itinérant chargé par **LoadUserProfile**, appelez la fonction [**UnloadUserProfile**](/windows/desktop/api/Userenv/nf-userenv-unloaduserprofile) .

 

 
