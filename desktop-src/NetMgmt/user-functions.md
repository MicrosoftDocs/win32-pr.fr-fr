---
title: Fonctions utilisateur
description: Les fonctions utilisateur de gestion de réseau contrôlent le compte d’un utilisateur dans la base de données de sécurité, qui est la base de données du gestionnaire de comptes de sécurité (SAM) ou, dans le cas des contrôleurs de domaine, le Active Directory. Les fonctions utilisateur sont répertoriées ci-dessous.
ms.assetid: cf0e5102-3924-46c0-8124-0aa04e95f48d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c8d7b59ff121c0225f166888b42ef1a731336ed80799cd0593ba38b4fb04ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796815"
---
# <a name="user-functions"></a>Fonctions utilisateur

Les fonctions utilisateur de gestion de réseau contrôlent le compte d’un utilisateur dans la base de données de sécurité, qui est la base de données du gestionnaire de comptes de sécurité (SAM) ou, dans le cas des contrôleurs de domaine, le Active Directory. Les fonctions utilisateur sont répertoriées ci-dessous.



| Fonction                                               | Description                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------|
| [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd)                       | Ajoute un compte d’utilisateur et attribue un mot de passe et un niveau de privilège.     |
| [**NetUserChangePassword**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserchangepassword) | Modifie le mot de passe d’un utilisateur pour un serveur réseau ou un domaine spécifié. |
| [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel)                       | Supprime un compte d’utilisateur du serveur.                             |
| [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)                     | Répertorie tous les comptes d’utilisateur sur un serveur.                                |
| [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)           | Retourne une liste de noms de groupes globaux auxquels appartient un utilisateur.       |
| [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)               | Retourne des informations sur un compte d’utilisateur particulier sur un serveur.    |
| [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups) | Retourne la liste des noms de groupes locaux auxquels appartient un utilisateur.        |
| [**NetUserSetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetgroups)           | Définit les appartenances aux groupes globaux pour un compte d’utilisateur spécifié.         |
| [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo)               | Définit le mot de passe et d’autres éléments d’un compte d’utilisateur.             |



 

Chaque utilisateur ou application qui accède à des ressources réseau doit avoir un compte dans la base de données de sécurité. Les services d’annuaire utilisent ce compte pour vérifier que l’utilisateur ou l’application a l’autorisation de se connecter à une ressource. lorsqu’un utilisateur ou une application demande l’accès à une ressource, le système de sécurité Windows recherche un compte d’utilisateur ou un compte de groupe approprié pour autoriser l’accès.

Une fois que vous avez supprimé un compte d’utilisateur en appelant la fonction [**NetUserDel**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserdel) , l’utilisateur ne peut plus accéder au serveur, sauf en utilisant le compte invité.

Étant donné que le mot de passe d’un utilisateur est confidentiel, il n’est pas retourné par la fonction [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum) ou la fonction [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo) . Le mot de passe est initialement attribué lorsque vous appelez [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd).

Les informations de compte d’utilisateur sont disponibles aux niveaux suivants :

-   [**\_Informations utilisateur \_ 0**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_0)
-   [**\_Informations utilisateur \_ 1**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1)
-   [**\_Informations utilisateur \_ 2**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_2)
-   [**\_Informations utilisateur \_ 3**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_3)
-   [**\_Informations utilisateur \_ 4**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_4)
-   [**\_Informations utilisateur \_ 10**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_10)
-   [**\_Informations utilisateur \_ 11**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_11)
-   [**\_Informations utilisateur \_ 20**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_20)
-   [**\_Informations utilisateur \_ 21**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_21)
-   [**\_Informations utilisateur \_ 22**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_22)
-   [**\_Informations utilisateur \_ 23**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_23)

En outre, les niveaux d’informations suivants sont valides lorsque vous appelez la fonction [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) :

-   [**\_Informations utilisateur \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003)
-   [**\_Informations utilisateur \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005)
-   [**\_Informations utilisateur \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006)
-   [**\_Informations utilisateur \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007)
-   [**\_Informations utilisateur \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008)
-   [**\_Informations utilisateur \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009)
-   [**\_Informations utilisateur \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010)
-   [**\_Informations utilisateur \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011)
-   [**\_Informations utilisateur \_ 1012**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1012)
-   [**\_Informations utilisateur \_ 1014**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1014)
-   [**\_Informations utilisateur \_ 1017**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1017)
-   [**\_Informations utilisateur \_ 1020**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1020)
-   [**\_Informations utilisateur \_ 1024**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1024)
-   [**\_Informations utilisateur \_ 1051**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1051)
-   [**\_Informations utilisateur \_ 1052**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1052)
-   [**\_Informations utilisateur \_ 1053**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1053)

Les fonctions suivantes permettent aux applications de vérifier la conformité des mots de passe.



| Fonction                                                               | Description                                                                                                |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [**NetValidatePasswordPolicyFree**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicyfree) | Libère la mémoire allouée par la fonction [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy) . |
| [**NetValidatePasswordPolicy**](/windows/desktop/api/Lmaccess/nf-lmaccess-netvalidatepasswordpolicy)         | Vérifie que les mots de passe répondent aux exigences de complexité, de vieillissement, de longueur minimale et de réutilisation de l’historique.            |



 

Si vous programmez pour Active Directory, vous pouvez appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions utilisateur de gestion de réseau. Pour plus d’informations, consultez [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) et [**IADsComputer**](/windows/desktop/api/iads/nn-iads-iadscomputer).

 

 