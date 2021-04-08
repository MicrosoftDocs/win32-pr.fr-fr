---
title: Agent de système d’annuaire
description: L’agent de système d’annuaire (DSA) est un ensemble de services et de processus qui s’exécutent sur chaque contrôleur de domaine et qui permet d’accéder au magasin de données.
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- Active Directory de l’agent de système d’annuaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842094"
---
# <a name="directory-system-agent"></a>Agent de système d’annuaire

L' [*agent de système d’annuaire*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) est un ensemble de services et de processus qui s’exécutent sur chaque contrôleur de domaine et qui permet d’accéder au magasin de données. Le magasin de données est le magasin physique des données de répertoire situées sur un disque dur. Dans Active Directory Domain Services, le DSA fait partie du sous-système de l’autorité de système locale (LSA). Les clients accèdent au répertoire à l’aide de l’un des mécanismes suivants pris en charge par le DSA :

-   Les clients LDAP se connectent au DSA à l’aide du protocole LDAP (Lightweight Directory Access Protocol). Active Directory Domain Services prennent en charge LDAP 3,0, défini par RFC 3377 et LDAP 2,0, défini par RFC 1777. Les clients Windows utilisent LDAP 3,0 pour se connecter au DSA.
-   Les clients MAPI tels que Microsoft Exchange Server se connectent au DSA à l’aide de l’interface d’appel de procédure distante MAPI.
-   Les DSA de Active Directory Domain Services se connectent les uns aux autres pour effectuer la réplication à l’aide d’une interface d’appel de procédure distante propriétaire.

 

 