---
title: Groupes sur les serveurs membres et Windows 2000 professionnel
description: Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, il existe une base de données de sécurité locale.
ms.assetid: 17a651e2-3650-4e12-b17e-badd3d479515
ms.tgt_platform: multiple
keywords:
- Groupes sur les serveurs membres et Windows 2000 Professionnel AD
- groupes Active Directory, groupes sur les serveurs membres et Windows 2000 professionnel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530da03182d05764540a85f1c2529ced5877be5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309282"
---
# <a name="groups-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="d85a9-105">Groupes sur les serveurs membres et Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="d85a9-105">Groups on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="d85a9-106">Sur les serveurs membres et les ordinateurs qui exécutent Windows 2000 professionnel, il existe une base de données de sécurité locale.</span><span class="sxs-lookup"><span data-stu-id="d85a9-106">On member servers and computers running on Windows 2000 Professional, there is a local security database.</span></span> <span data-ttu-id="d85a9-107">Cette base de données de sécurité locale peut contenir ses propres groupes locaux et d’utilisateurs locaux dont l’étendue est uniquement l’ordinateur particulier sur lequel elles sont créées.</span><span class="sxs-lookup"><span data-stu-id="d85a9-107">This local security database can contain its own local user and local groups whose scope is only the particular computer where they are created.</span></span> <span data-ttu-id="d85a9-108">Lors de la gestion de ces types d’utilisateurs et de groupes sur les serveurs membres et les ordinateurs qui exécutent Windows NT Workstation ou Windows 2000 professionnel, utilisez le fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="d85a9-108">When managing these types of users and groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="d85a9-109">Lorsqu’un serveur membre ou un ordinateur exécutant Windows 2000 Professionnel ou Windows 2000 professionnel est membre d’un domaine Windows 2000, les groupes ou les utilisateurs du domaine peuvent être utilisés dans la base de données de sécurité locale pour accorder des droits à ce groupe sur cet ordinateur particulier.</span><span class="sxs-lookup"><span data-stu-id="d85a9-109">When a member server or a computer running on Windows 2000 Professional or Windows 2000 Professional is a member of a Windows 2000 domain, the groups or users in the domain can be used in the local security database to grant rights to that group on that particular computer.</span></span>

<span data-ttu-id="d85a9-110">Lorsque vous gérez des groupes sur un domaine Windows 2000 à l’aide d’ADSI, utilisez le fournisseur LDAP.</span><span class="sxs-lookup"><span data-stu-id="d85a9-110">When managing groups on a Windows 2000 domain using ADSI, use the LDAP provider.</span></span> <span data-ttu-id="d85a9-111">Lorsque vous gérez des groupes sur des serveurs membres et des ordinateurs qui exécutent Windows NT Workstation ou Windows 2000 professionnel, utilisez le fournisseur Winnt.</span><span class="sxs-lookup"><span data-stu-id="d85a9-111">When managing groups on member servers and computers running on Windows NT Workstation or Windows 2000 Professional, use the WinNT provider.</span></span>

<span data-ttu-id="d85a9-112">Vous devez lier au moins une instance à chaque fournisseur : 1) créer une liaison avec le fournisseur LDAP pour récupérer l’ADsPath du groupe ou de l’utilisateur que vous souhaitez ajouter à un groupe dans la base de données locale et 2) créer une liaison avec le fournisseur WinNT pour ajouter cet utilisateur ou ce groupe à un groupe local.</span><span class="sxs-lookup"><span data-stu-id="d85a9-112">You must bind, at least one instance, to each provider: 1) Bind to the LDAP provider to retrieve the ADsPath to the group or user you want to add to a group in the local database and 2) Bind to the WinNT provider to add that user or group to a local group.</span></span>

 

 




