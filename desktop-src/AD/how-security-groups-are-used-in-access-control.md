---
title: Utilisation des groupes de sécurité dans les Access Control
description: L’identificateur de sécurité (SID) est l’identificateur d’objet de l’utilisateur ou du groupe de sécurité lorsque l’utilisateur ou le groupe est utilisé à des fins de sécurité.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Utilisation des groupes de sécurité dans les Access Control
- contrôle d’accès, groupes de sécurité utilisés dans
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512019"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Utilisation des groupes de sécurité dans les Access Control

L’identificateur de sécurité (SID) est l’identificateur d’objet de l’utilisateur ou du groupe de sécurité lorsque l’utilisateur ou le groupe est utilisé à des fins de sécurité. Le nom de l’utilisateur ou du groupe n’est pas utilisé en tant qu’identificateur unique dans le système. Le SID est stocké dans l’attribut **objectSID** des objets utilisateur et groupe de sécurité. Le serveur Active Directory génère l' **objectSID** lorsque l’utilisateur ou le groupe est créé. Le système garantit que les SID sont uniques dans une forêt. N’oubliez pas que l' **objectGUID** est l’identificateur unique d’un utilisateur, d’un groupe ou d’un autre objet annuaire. Le SID change si un utilisateur ou un groupe est déplacé vers un autre domaine. l' **objectGUID** reste le même.

Lorsqu’un utilisateur ou un groupe a l’autorisation d’accéder à une ressource, telle qu’une imprimante ou un partage de fichiers, le SID de l’utilisateur ou du groupe est ajouté à l’entrée de contrôle d’accès (ACE) définissant l’autorisation accordée dans la liste de contrôle d’accès discrétionnaire (DACL) de la ressource. Dans Active Directory Domain Services, chaque objet a un attribut **ntSecurityDescriptor** qui stocke une liste DACL définissant l’accès à cet objet ou aux attributs particuliers sur cet objet. Pour plus d’informations sur la définition du contrôle d’accès sur des objets dans Active Directory Domain Services, consultez [contrôle de l’accès aux objets dans Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Lorsqu’un utilisateur se connecte à un domaine Windows 2000, le système d’exploitation génère un jeton d’accès. Ce jeton d’accès est utilisé pour déterminer les ressources auxquelles l’utilisateur peut accéder. Le jeton d’accès utilisateur contient les données suivantes :

-   SID de l’utilisateur.
-   SID de tous les groupes de sécurité globaux et universels dont l’utilisateur est membre.
-   SID de tous les groupes de sécurité globaux et universels imbriqués.

Chaque processus exécuté pour le compte de cet utilisateur dispose d’une copie de ce jeton d’accès.

Lorsque l’utilisateur tente d’accéder à des ressources sur un ordinateur, le service par le biais duquel l’utilisateur accède à la ressource empruntera l’identité de l’utilisateur en créant un nouveau jeton d’accès basé sur le jeton d’accès créé au moment de l’ouverture de session de l’utilisateur. Ce nouveau jeton d’accès contient également les SID suivants :

-   Sid pour tous les groupes locaux de domaine dans le domaine cible dont l’utilisateur est membre.
-   Sid pour tous les groupes locaux de l’ordinateur sur l’ordinateur cible dont l’utilisateur est membre.

Le service utilise ce nouveau jeton d’accès pour évaluer l’accès à la ressource. Si un SID dans le jeton d’accès apparaît dans des ACE dans la liste DACL, le service accorde à l’utilisateur les autorisations spécifiées dans ces entrées de du texte.

 

 




