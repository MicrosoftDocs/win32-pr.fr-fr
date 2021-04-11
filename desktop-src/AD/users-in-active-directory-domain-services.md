---
title: Utilisateurs dans Active Directory Domain Services
description: Active Directory Domain Services comprend un service d’annuaire qui stocke le domaine, l’utilisateur, le groupe d’utilisateurs et les données de sécurité.
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Utilisateurs Active Directory Domain Services Active Directory
- utilisateurs, services de domaine Active Directory
- services de domaine Active Directory, utilisateurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b10ad85f359cab6baf891df03f368f3e7da5974f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "104030975"
---
# <a name="users-in-active-directory-domain-services"></a>Utilisateurs dans Active Directory Domain Services

Active Directory Domain Services comprend un service d’annuaire qui stocke le domaine, l’utilisateur, le groupe d’utilisateurs et les données de sécurité.

Sur Windows NT 4,0 et versions antérieures, vous pouvez utiliser des fonctions telles que [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel), etc., pour gérer les utilisateurs, les groupes d’utilisateurs et d’autres éléments réseau. Sur Windows 2000 et les versions ultérieures de Windows, ADSI fournit un accès uniforme et sécurisé à ces éléments et à leurs propriétés. N’oubliez pas que l’interface ADSI fournit un fournisseur Windows NT 4,0 qui vous permet d’utiliser ADSI pour gérer les utilisateurs, les groupes d’utilisateurs et les ordinateurs sur les systèmes Windows NT 4,0. Il existe également des fournisseurs pour Windows Server 2008 Enterprise (installation Server Core), Microsoft Exchange 5,5, Microsoft Internet Information Server (IIS), Novell Services d’annuaire NetWare (NDS) (NDS) et Novell NetWare 3. Autrement dit, un ensemble unique de méthodes standardisées pour gérer les utilisateurs et les groupes d’utilisateurs pour Windows NT, NDS et NetWare 3.

En outre, Windows 2000 est un répertoire à plusieurs maîtres. Autrement dit, les modifications apportées à des utilisateurs, des groupes d’utilisateurs et d’autres données stockées dans l’annuaire peuvent être effectuées sur n’importe quel contrôleur de domaine. Sur Windows 2000, vous n’êtes pas obligé de localiser le contrôleur de domaine principal (PDC) et de modifier les utilisateurs et les groupes d’utilisateurs sur le contrôleur de domaine principal.

Windows 2000 introduit également un nouvel espace de noms hiérarchique au sein d’un domaine appelé unité d’organisation (UO). Une unité d’organisation peut contenir des ordinateurs, des utilisateurs, des groupes d’utilisateurs et d’autres objets réseau. En règle générale, une unité d’organisation est utilisée dans le but de regrouper des éléments à des fins administratives, telles que la délégation des droits d’administration et l’affectation de stratégies au groupe en tant qu’unité unique.

Les domaines, les unités d’organisation, les utilisateurs, les groupes d’utilisateurs, les ordinateurs et d’autres éléments réseau sont stockés sous forme d’objets dans Active Directory Domain Services. Dans Windows 2000 et les versions ultérieures de Windows, vous ajoutez toujours des utilisateurs, des groupes d’utilisateurs et des ordinateurs à un domaine. Toutefois, vous avez maintenant la possibilité d’ajouter ces objets à un conteneur d’UO ou à tout autre type de conteneur que l’objet que vous souhaitez ajouter définit dans l’attribut **possSuperiors** de son objet **classSchema** . Il s’agit d’un attribut sur l’objet **classSchema** d’un objet et cet attribut limite les types d’objets qui peuvent contenir cet objet.

 

 