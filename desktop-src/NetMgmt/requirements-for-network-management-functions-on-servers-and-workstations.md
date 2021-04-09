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
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a><span data-ttu-id="9f7a4-103">Configuration requise pour les fonctions de gestion de réseau sur les serveurs et les stations de travail</span><span class="sxs-lookup"><span data-stu-id="9f7a4-103">Requirements for Network Management Functions on Servers and Workstations</span></span>

<span data-ttu-id="9f7a4-104">Si vous appelez l’une des fonctions de gestion de réseau décrites dans cette rubrique sur un serveur ou une station de travail, les différentes exigences d’accès s’appliquent aux requêtes d’informations et aux mises à jour d’informations.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-104">If you call one of the network management functions listed in this topic on a server or workstation, different access requirements apply to information queries and information updates.</span></span>

## <a name="queries"></a><span data-ttu-id="9f7a4-105">Requêtes</span><span class="sxs-lookup"><span data-stu-id="9f7a4-105">Queries</span></span>

<span data-ttu-id="9f7a4-106">Si vous appelez l’une des fonctions suivantes pour exécuter une requête sur un serveur ou une station de travail, par défaut, tous les utilisateurs authentifiés peuvent lire et énumérer les informations.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-106">If you call one of the following functions to perform a query on a server or workstation, by default, all authenticated users can read and enumerate the information.</span></span>

-   <span data-ttu-id="9f7a4-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-107">[**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum), [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo), [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)</span></span>
-   <span data-ttu-id="9f7a4-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-108">[**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum), [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo), [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)</span></span>
-   [<span data-ttu-id="9f7a4-109">**NetQueryDisplayInformation**</span><span class="sxs-lookup"><span data-stu-id="9f7a4-109">**NetQueryDisplayInformation**</span></span>](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   <span data-ttu-id="9f7a4-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (niveaux 1 et 2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-110">[**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (levels 1 and 2 only)</span></span>
-   <span data-ttu-id="9f7a4-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (niveaux 2 et 502 uniquement)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-111">[**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (levels 2 and 502 only)</span></span>
-   <span data-ttu-id="9f7a4-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-112">[**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum), [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups), [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo), [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups), [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)</span></span>
-   <span data-ttu-id="9f7a4-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-113">[**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo), [**NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)</span></span>

<span data-ttu-id="9f7a4-114">Vous trouverez ci-dessous des informations supplémentaires sur l’accès anonyme lors de la lecture et de l’énumération des informations.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-114">Following is additional information about anonymous access when reading and enumerating information.</span></span>

<span data-ttu-id="9f7a4-115">**Windows Server 2003 et Windows XP :** L’accès anonyme aux informations est possible si le paramètre de stratégie EveryoneIncludesAnonymous autorise l’accès anonyme.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-115">**Windows Server 2003 and Windows XP:** Anonymous access to information is possible if the EveryoneIncludesAnonymous policy setting allows anonymous access.</span></span>

<span data-ttu-id="9f7a4-116">**Windows 2000 :** L’accès anonyme aux objets sécurisables est possible si le paramètre de stratégie RestrictAnonymous autorise l’accès anonyme.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-116">**Windows 2000:** Anonymous access to securable objects is possible if the RestrictAnonymous policy setting allows anonymous access.</span></span> <span data-ttu-id="9f7a4-117">Vous pouvez restreindre l’accès anonyme en affectant la valeur 1 à la clé suivante dans le registre.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-117">You can restrict anonymous access by setting the following key in the registry to the value 1.</span></span>

<span data-ttu-id="9f7a4-118">**HKEY \_ Paramètre \_ \\ CurrentControlSet du \\ \\ contrôle CurrentControlSet \\ du système de l’ordinateur local** \\  = 1</span><span class="sxs-lookup"><span data-stu-id="9f7a4-118">**HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Lsa**\\**RestrictAnonymous** = 1</span></span>

<span data-ttu-id="9f7a4-119">Pour plus d’informations, reportez-vous à l’article suivant de la base de connaissances Microsoft :</span><span class="sxs-lookup"><span data-stu-id="9f7a4-119">For more information, see the following article in the Microsoft Knowledge Base:</span></span>

<span data-ttu-id="9f7a4-120">ID d’ARTICLE : [Q246261](https://support.microsoft.com/kb/246261)</span><span class="sxs-lookup"><span data-stu-id="9f7a4-120">ARTICLE ID: [Q246261](https://support.microsoft.com/kb/246261)</span></span>

<span data-ttu-id="9f7a4-121">TITLE : utilisation de la valeur de Registre RestrictAnonymous.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-121">TITLE: How to use the RestrictAnonymous registry Value.</span></span>

## <a name="updates"></a><span data-ttu-id="9f7a4-122">Mises à jour</span><span class="sxs-lookup"><span data-stu-id="9f7a4-122">Updates</span></span>

<span data-ttu-id="9f7a4-123">Par défaut, seuls les administrateurs et les utilisateurs avec pouvoir peuvent écrire des informations.</span><span class="sxs-lookup"><span data-stu-id="9f7a4-123">By default, only Administrators and Power Users can write information.</span></span>

<span data-ttu-id="9f7a4-124">Pour plus d’informations sur le contrôle de l’accès aux objets sécurisables, consultez [Access Control](/windows/desktop/SecAuthZ/access-control), [privilèges](/windows/desktop/SecAuthZ/privileges)et [objets sécurisables](/windows/desktop/SecAuthZ/securable-objects).</span><span class="sxs-lookup"><span data-stu-id="9f7a4-124">For more information about controlling access to securable objects, see [Access Control](/windows/desktop/SecAuthZ/access-control), [Privileges](/windows/desktop/SecAuthZ/privileges), and [Securable Objects](/windows/desktop/SecAuthZ/securable-objects).</span></span> <span data-ttu-id="9f7a4-125">Pour plus d’informations sur l’appel de fonctions qui requièrent des privilèges d’administrateur, consultez [exécution avec des privilèges spéciaux](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="9f7a4-125">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

 

 