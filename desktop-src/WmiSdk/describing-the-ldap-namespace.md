---
description: Lorsque vous vous connectez à distance à un serveur Active Directory autre que celui qui se trouve dans votre domaine actuel, vous devez spécifier le nom d’un ordinateur qui est déjà membre du domaine appartenant au Active Directory souhaité.
ms.assetid: f1478b9d-4a92-4340-8721-1f443eb6ace2
ms.tgt_platform: multiple
title: Description de l’espace de noms LDAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe1f27c3e2ebc48a0dfa14563822e34bc06d6223
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034998"
---
# <a name="describing-the-ldap-namespace"></a><span data-ttu-id="d0cee-103">Description de l’espace de noms LDAP</span><span class="sxs-lookup"><span data-stu-id="d0cee-103">Describing the LDAP Namespace</span></span>

<span data-ttu-id="d0cee-104">Lorsque vous vous connectez à distance à un serveur Active Directory autre que celui qui se trouve dans votre domaine actuel, vous devez spécifier le nom d’un ordinateur qui est déjà membre du domaine appartenant au Active Directory souhaité.</span><span class="sxs-lookup"><span data-stu-id="d0cee-104">When connecting remotely to an Active Directory server other than the one in your current domain, you must specify the name of a computer that is already a member of the domain belonging to the Active Directory you want.</span></span>

<span data-ttu-id="d0cee-105">Pour vous connecter à distance à un ordinateur qui est déjà membre du domaine appartenant au serveur Active Directory, tapez la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="d0cee-105">To remotely connect to a computer that is already a member of the domain belonging to the Active Directory server, type the following command.</span></span>

<span data-ttu-id="d0cee-106">**\\\\\\ \\ Protocole LDAP de répertoire racine ordinateur_distant \\**</span><span class="sxs-lookup"><span data-stu-id="d0cee-106">**\\\\RemoteComputer\\root\\directory\\LDAP**</span></span>

<span data-ttu-id="d0cee-107">Cet exemple montre que deux parties composent un nom d’espace de noms qualifié complet.</span><span class="sxs-lookup"><span data-stu-id="d0cee-107">This example shows that there are two parts that make up a fully qualified namespace name.</span></span> <span data-ttu-id="d0cee-108">La première partie ( \\ \\ ordinateur_distant) représente l’ordinateur qui est déjà membre du domaine appartenant au serveur Active Directory de votre choix.</span><span class="sxs-lookup"><span data-stu-id="d0cee-108">The first part (\\\\RemoteComputer) represents the computer that is already a member of the domain belonging to the Active Directory server you want.</span></span> <span data-ttu-id="d0cee-109">La deuxième partie ( \\ \\ répertoire racine \\ LDAP) représente le schéma Active Directory dans le fournisseur de services d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="d0cee-109">The second part (\\root\\directory\\LDAP) represents the Active Directory schema in the Directory Services Provider.</span></span>

> [!Note]  
> <span data-ttu-id="d0cee-110">Pour plus d’informations sur la prise en charge et l’installation de ce composant sur un système d’exploitation spécifique, consultez [disponibilité du système d’exploitation des composants WMI](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="d0cee-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

 

 



