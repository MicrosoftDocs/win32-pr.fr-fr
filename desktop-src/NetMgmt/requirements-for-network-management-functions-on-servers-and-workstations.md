---
title: Configuration requise pour les fonctions de gestion de réseau sur les serveurs et les stations de travail
description: Si vous appelez l’une des fonctions de gestion de réseau décrites dans cette rubrique sur un serveur ou une station de travail, les différentes exigences d’accès s’appliquent aux requêtes d’informations et aux mises à jour d’informations.
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842641"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>Configuration requise pour les fonctions de gestion de réseau sur les serveurs et les stations de travail

Si vous appelez l’une des fonctions de gestion de réseau décrites dans cette rubrique sur un serveur ou une station de travail, les différentes exigences d’accès s’appliquent aux requêtes d’informations et aux mises à jour d’informations.

## <a name="queries"></a>Requêtes

Si vous appelez l’une des fonctions suivantes pour exécuter une requête sur un serveur ou une station de travail, par défaut, tous les utilisateurs authentifiés peuvent lire et énumérer les informations.

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (niveaux 1 et 2 uniquement)
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (niveaux 2 et 502 uniquement)
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

Vous trouverez ci-dessous des informations supplémentaires sur l’accès anonyme lors de la lecture et de l’énumération des informations.

**Windows Server 2003 et Windows XP :** L’accès anonyme aux informations est possible si le paramètre de stratégie EveryoneIncludesAnonymous autorise l’accès anonyme.

**Windows 2000 :** L’accès anonyme aux objets sécurisables est possible si le paramètre de stratégie RestrictAnonymous autorise l’accès anonyme. Vous pouvez restreindre l’accès anonyme en affectant la valeur 1 à la clé suivante dans le registre.

**HKEY \_ Paramètre \_ \\ CurrentControlSet du \\ \\ contrôle CurrentControlSet \\ du système de l’ordinateur local** \\  = 1

Pour plus d’informations, reportez-vous à l’article suivant de la base de connaissances Microsoft :

ID d’ARTICLE : [Q246261](https://support.microsoft.com/kb/246261)

TITLE : utilisation de la valeur de Registre RestrictAnonymous.

## <a name="updates"></a>Mises à jour

Par défaut, seuls les administrateurs et les utilisateurs avec pouvoir peuvent écrire des informations.

Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control), [privilèges](/windows/desktop/SecAuthZ/privileges)et [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects). Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).

 

 