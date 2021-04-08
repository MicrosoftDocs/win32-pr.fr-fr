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
# <a name="directory-system-agent"></a><span data-ttu-id="e5895-104">Agent de système d’annuaire</span><span class="sxs-lookup"><span data-stu-id="e5895-104">Directory System Agent</span></span>

<span data-ttu-id="e5895-105">L' [*agent de système d’annuaire*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) est un ensemble de services et de processus qui s’exécutent sur chaque contrôleur de domaine et qui permet d’accéder au magasin de données.</span><span class="sxs-lookup"><span data-stu-id="e5895-105">The [*directory system agent*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) is a collection of services and processes that run on each domain controller and provides access to the data store.</span></span> <span data-ttu-id="e5895-106">Le magasin de données est le magasin physique des données de répertoire situées sur un disque dur.</span><span class="sxs-lookup"><span data-stu-id="e5895-106">The data store is the physical store of directory data located on a hard disk.</span></span> <span data-ttu-id="e5895-107">Dans Active Directory Domain Services, le DSA fait partie du sous-système de l’autorité de système locale (LSA).</span><span class="sxs-lookup"><span data-stu-id="e5895-107">In Active Directory Domain Services, the DSA is part of the local system authority (LSA) subsystem.</span></span> <span data-ttu-id="e5895-108">Les clients accèdent au répertoire à l’aide de l’un des mécanismes suivants pris en charge par le DSA :</span><span class="sxs-lookup"><span data-stu-id="e5895-108">Clients access the directory using one of the following mechanisms supported by the DSA:</span></span>

-   <span data-ttu-id="e5895-109">Les clients LDAP se connectent au DSA à l’aide du protocole LDAP (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="e5895-109">LDAP clients connect to the DSA using the Lightweight Directory Access Protocol (LDAP).</span></span> <span data-ttu-id="e5895-110">Active Directory Domain Services prennent en charge LDAP 3,0, défini par RFC 3377 et LDAP 2,0, défini par RFC 1777.</span><span class="sxs-lookup"><span data-stu-id="e5895-110">Active Directory Domain Services support LDAP 3.0, defined by RFC 3377, and LDAP 2.0, defined by RFC 1777.</span></span> <span data-ttu-id="e5895-111">Les clients Windows utilisent LDAP 3,0 pour se connecter au DSA.</span><span class="sxs-lookup"><span data-stu-id="e5895-111">Windows clients use LDAP 3.0 to connect to the DSA.</span></span>
-   <span data-ttu-id="e5895-112">Les clients MAPI tels que Microsoft Exchange Server se connectent au DSA à l’aide de l’interface d’appel de procédure distante MAPI.</span><span class="sxs-lookup"><span data-stu-id="e5895-112">MAPI clients such as Microsoft Exchange Server connect to the DSA using the MAPI remote procedure call interface.</span></span>
-   <span data-ttu-id="e5895-113">Les DSA de Active Directory Domain Services se connectent les uns aux autres pour effectuer la réplication à l’aide d’une interface d’appel de procédure distante propriétaire.</span><span class="sxs-lookup"><span data-stu-id="e5895-113">The DSAs in Active Directory Domain Services connect to each other to perform replication using a proprietary remote procedure call interface.</span></span>

 

 