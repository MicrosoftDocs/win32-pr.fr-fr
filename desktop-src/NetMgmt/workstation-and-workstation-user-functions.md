---
title: Fonctions utilisateur de station de travail et de station de travail
description: Les fonctions de station de travail de gestion de réseau effectuent des tâches d’administration sur une station de travail locale ou distante.
ms.assetid: cc400f43-297b-4ff4-8353-b268839c48b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd445746bca51abaa0cd72877bdf03dd4d00d338
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509873"
---
# <a name="workstation-and-workstation-user-functions"></a>Fonctions utilisateur de station de travail et de station de travail

Les fonctions de station de travail de gestion de réseau effectuent des tâches d’administration sur une station de travail locale ou distante. Seul un utilisateur ou une application ayant l’appartenance à un groupe d’administrateurs, sur un serveur local ou distant, peut effectuer des tâches d’administration sur une station de travail pour contrôler son fonctionnement, son accès utilisateur et son partage de ressources. Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

Les fonctions de station de travail sont répertoriées ci-dessous.



| Fonction                                   | Description                                                             |
|--------------------------------------------|-------------------------------------------------------------------------|
| [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo) | Retourne des informations sur les éléments de configuration d’une station de travail. |
| [**NetWkstaSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstasetinfo) | Configure une station de travail.                                               |



 

Les fonctions de station de travail permettent d’accéder à deux types discrets d’informations sur les stations de travail :

-   Informations système
-   Informations spécifiques à la plateforme

Dans chaque type, les données sont classées par accès de sécurité. Les données accessibles à l’invité sont un sous-ensemble des données accessibles par l’utilisateur, qui est à son tour un sous-ensemble des données accessibles par l’administrateur.

Les informations de station de travail sont disponibles aux niveaux suivants :

-   [**WKSTA \_ INFO \_ 100**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_100)
-   [**WKSTA \_ INFO \_ 101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_101)
-   [**WKSTA \_ INFO \_ 102**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_info_102)

Les fonctions utilisateur de la station de travail de gestion du réseau permettent d’accéder à des informations spécifiques à l’utilisateur. Les informations spécifiques à l’utilisateur sont séparées des informations de la station de travail, car il peut y avoir plusieurs utilisateurs sur une station de travail.

Les fonctions utilisateur de station de travail sont répertoriées ci-dessous.



| Fonction                                           | Description                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------------------|
| [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)       | Répertorie des informations sur tous les utilisateurs actuellement connectés à la station de travail.           |
| [**NetWkstaUserGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausergetinfo) | Retourne des informations sur un utilisateur actuellement connecté.                             |
| [**NetWkstaUserSetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstausersetinfo) | Définit les informations spécifiques à l’utilisateur pour les éléments de configuration d’une station de travail. |



 

Les informations utilisateur de station de travail sont disponibles aux niveaux suivants :

-   [**\_Informations utilisateur \_ wksta \_ 0**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_0)
-   [**\_Informations utilisateur \_ wksta \_ 1**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1)
-   [**\_Informations utilisateur \_ wksta \_ 1101**](/windows/desktop/api/Lmwksta/ns-lmwksta-wksta_user_info_1101)

 

 