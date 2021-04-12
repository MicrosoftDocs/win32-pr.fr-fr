---
title: Administration du compte d’utilisateur RAS
description: Un serveur RAS Windows NT 4,0 utilise une base de données de comptes d’utilisateur qui contient des informations sur un ensemble de comptes d’utilisateur.
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 521d090fc16e7d731525b79493119f3c604e043c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315383"
---
# <a name="ras-user-account-administration"></a>Administration du compte d’utilisateur RAS

Un serveur RAS Windows NT 4,0 utilise une base de données de comptes d’utilisateur qui contient des informations sur un ensemble de comptes d’utilisateur. Les informations incluent les privilèges RAS d’un utilisateur, qui sont un ensemble d’indicateurs binaires qui déterminent comment le serveur RAS répond quand l’utilisateur appelle pour se connecter. Les fonctions d’administration du serveur RAS vous permettent de localiser la base de données des comptes d’utilisateur et d’obtenir et de définir les privilèges RAS pour les comptes d’utilisateur.

Un serveur RAS Windows NT 4,0 peut faire partie d’un domaine Windows NT/Windows 2000, ou il peut s’agir d’un serveur ou d’une station de travail Windows NT autonome qui ne fait pas partie d’un domaine. Pour un serveur qui fait partie d’un domaine, la base de données de comptes d’utilisateur est stockée sur le serveur qui est le contrôleur de domaine principal (PDC). Un serveur autonome stocke sa propre base de données de compte d’utilisateur local. Pour obtenir le nom du serveur qui stocke la base de données de comptes d’utilisateur utilisée par un serveur RAS spécifié, vous pouvez appeler la fonction [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) . Vous pouvez ensuite utiliser le nom du serveur de comptes d’utilisateur dans un appel à la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) pour énumérer les utilisateurs dans une base de données de comptes d’utilisateur. Vous pouvez également utiliser le nom du serveur dans les appels aux fonctions [**RasAdminUserGetInfo**](rasadminusergetinfo.md) et [**RasAdminUserSetInfo**](rasadminusersetinfo.md) pour obtenir et définir les privilèges RAS pour un compte d’utilisateur spécifié.

Les fonctions [**RasAdminUserGetInfo**](rasadminusergetinfo.md) et [**RasAdminUserSetInfo**](rasadminusersetinfo.md) utilisent la structure de l' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) pour spécifier les privilèges RAS d’un utilisateur et le numéro de téléphone de rappel. Les privilèges RAS indiquent les informations suivantes :

-   Si l’utilisateur peut établir une connexion à distance au serveur ou au domaine auquel le serveur appartient.
-   Si l’utilisateur peut établir une connexion par le biais d’un rappel, dans lequel le serveur RAS se bloque, puis rappelle à l’utilisateur d’établir la connexion.

Chaque compte d’utilisateur spécifie l’un des indicateurs suivants pour indiquer le privilège de rappel de l’utilisateur.



| Valeur                      | Signification                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ Nocallback        | Le serveur RAS ne rappellera pas l’utilisateur pour établir une connexion.                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | Lorsque l’utilisateur appelle, le serveur RAS se bloque et appelle un numéro de téléphone de rappel prédéfini stocké dans la base de données des comptes d’utilisateur. Le membre **szPhoneNumber** de la structure de l' [**\_ utilisateur RAS \_ 0**](ras-user-0-str.md) contient le numéro de téléphone de l’utilisateur appelant. |
| RASPRIV \_ CallerSetCallback | Lorsque l’utilisateur appelle, le serveur RAS offre la possibilité de spécifier un numéro de téléphone à rappeler. L’utilisateur peut également choisir de se connecter immédiatement sans rappel. Le membre **szPhoneNumber** contient un nombre par défaut que l’utilisateur peut remplacer.      |



 

 

 