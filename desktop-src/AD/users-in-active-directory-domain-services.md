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
ms.openlocfilehash: a8eab1633577906557639a65bc0f24e3bcfc0221f4fdf19602bfa7807a352a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182533"
---
# <a name="users-in-active-directory-domain-services"></a>Utilisateurs dans Active Directory Domain Services

Active Directory Domain Services comprend un service d’annuaire qui stocke le domaine, l’utilisateur, le groupe d’utilisateurs et les données de sécurité.

Sur Windows NT 4,0 et versions antérieures, vous pouvez utiliser des fonctions telles que [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd), [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum), [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel), etc., pour gérer les utilisateurs, les groupes d’utilisateurs et d’autres éléments réseau. sur Windows 2000 et versions ultérieures de Windows, ADSI fournit un accès uniforme et sécurisé à ces éléments et à leurs propriétés. N’oubliez pas que l’interface ADSI fournit un fournisseur Windows NT 4,0 qui vous permet d’utiliser ADSI pour gérer des utilisateurs, des groupes d’utilisateurs et des ordinateurs sur des systèmes Windows NT 4,0. il existe également des fournisseurs pour Windows server 2008 Enterprise (installation server Core), microsoft Exchange 5,5, microsoft Internet Information Server (IIS), novell Services d’annuaire NetWare (NDS) (NDS) et novell NetWare 3. Autrement dit, un ensemble unique de méthodes standardisées pour gérer les utilisateurs et les groupes d’utilisateurs pour Windows NT, NDS et NetWare 3.

en outre, Windows 2000 est un répertoire à plusieurs maîtres. Autrement dit, les modifications apportées à des utilisateurs, des groupes d’utilisateurs et d’autres données stockées dans l’annuaire peuvent être effectuées sur n’importe quel contrôleur de domaine. sur Windows 2000, vous n’êtes pas obligé de localiser le contrôleur de domaine principal (pdc) et de modifier les utilisateurs et les groupes d’utilisateurs sur le contrôleur de domaine principal.

Windows 2000 introduit également un nouvel espace de noms hiérarchique au sein d’un domaine appelé unité d’organisation (uo). Une unité d’organisation peut contenir des ordinateurs, des utilisateurs, des groupes d’utilisateurs et d’autres objets réseau. En règle générale, une unité d’organisation est utilisée dans le but de regrouper des éléments à des fins administratives, telles que la délégation des droits d’administration et l’affectation de stratégies au groupe en tant qu’unité unique.

Les domaines, les unités d’organisation, les utilisateurs, les groupes d’utilisateurs, les ordinateurs et d’autres éléments réseau sont stockés sous forme d’objets dans Active Directory Domain Services. dans Windows version 2000 et les versions ultérieures de Windows, vous ajoutez toujours des utilisateurs, des groupes d’utilisateurs et des ordinateurs à un domaine. Toutefois, vous avez maintenant la possibilité d’ajouter ces objets à un conteneur d’UO ou à tout autre type de conteneur que l’objet que vous souhaitez ajouter définit dans l’attribut **possSuperiors** de son objet **classSchema** . Il s’agit d’un attribut sur l’objet **classSchema** d’un objet et cet attribut limite les types d’objets qui peuvent contenir cet objet.

 

 