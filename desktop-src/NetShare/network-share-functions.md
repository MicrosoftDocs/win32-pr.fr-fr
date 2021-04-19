---
description: Les fonctions de partage réseau contrôlent les ressources partagées. Une ressource partagée est une ressource locale sur un serveur (par exemple, un répertoire de disque, un périphérique d’impression ou un canal nommé) accessible par les utilisateurs et les applications sur le réseau.
ms.assetid: 14886bb0-e597-4728-a64f-bc16e82874da
title: Fonctions de partage réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 640dc877c9b482cb8ebdcef0d36e6dff562fcd8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517792"
---
# <a name="network-share-functions"></a><span data-ttu-id="3ccf4-104">Fonctions de partage réseau</span><span class="sxs-lookup"><span data-stu-id="3ccf4-104">Network Share Functions</span></span>

<span data-ttu-id="3ccf4-105">Les fonctions de partage réseau contrôlent les ressources partagées.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-105">The network share functions control shared resources.</span></span> <span data-ttu-id="3ccf4-106">Une ressource partagée est une ressource locale sur un serveur (par exemple, un répertoire de disque, un périphérique d’impression ou un canal nommé) accessible par les utilisateurs et les applications sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-106">A shared resource is a local resource on a server (for example, a disk directory, print device, or named pipe) that can be accessed by users and applications on the network.</span></span>

<span data-ttu-id="3ccf4-107">Les fonctions de partage sont répertoriées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-107">The share functions are listed following.</span></span>



| <span data-ttu-id="3ccf4-108">Fonction</span><span class="sxs-lookup"><span data-stu-id="3ccf4-108">Function</span></span>                                   | <span data-ttu-id="3ccf4-109">Description</span><span class="sxs-lookup"><span data-stu-id="3ccf4-109">Description</span></span>                                                          |
|--------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="3ccf4-110">**NetShareAdd**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-110">**NetShareAdd**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd)         | <span data-ttu-id="3ccf4-111">Partage une ressource sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-111">Shares a resource on a server.</span></span>                                       |
| [<span data-ttu-id="3ccf4-112">**NetShareCheck**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-112">**NetShareCheck**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharecheck)     | <span data-ttu-id="3ccf4-113">Demande si un serveur partage un appareil.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-113">Queries whether a server is sharing a device.</span></span>                        |
| [<span data-ttu-id="3ccf4-114">**NetShareDel**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-114">**NetShareDel**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharedel)         | <span data-ttu-id="3ccf4-115">Supprime un nom de partage de la liste des ressources partagées d’un serveur.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-115">Deletes a share name from a server's list of shared resources.</span></span>       |
| [<span data-ttu-id="3ccf4-116">**NetShareEnum**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-116">**NetShareEnum**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netshareenum)       | <span data-ttu-id="3ccf4-117">Récupère des informations de partage sur chaque ressource partagée sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-117">Retrieves share information about each shared resource on a server.</span></span>  |
| [<span data-ttu-id="3ccf4-118">**NetShareGetInfo**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-118">**NetShareGetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharegetinfo) | <span data-ttu-id="3ccf4-119">Récupère des informations sur une ressource partagée spécifiée sur un serveur.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-119">Retrieves information about a specified shared resource on a server.</span></span> |
| [<span data-ttu-id="3ccf4-120">**NetShareSetInfo**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-120">**NetShareSetInfo**</span></span>](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo) | <span data-ttu-id="3ccf4-121">Définit les paramètres d’une ressource partagée.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-121">Sets a shared resource's parameters.</span></span>                                 |



 

<span data-ttu-id="3ccf4-122">La fonction [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) permet à un utilisateur ou une application de partager une ressource d’un type spécifique à l’aide du nom de partage spécifié.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-122">The [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) function allows a user or application to share a resource of a specific type using the specified share name.</span></span> <span data-ttu-id="3ccf4-123">La fonction **NetShareAdd** requiert le nom de partage et le nom de l’appareil local pour partager la ressource.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-123">The **NetShareAdd** function requires the share name and local device name to share the resource.</span></span> <span data-ttu-id="3ccf4-124">Un utilisateur ou une application doit avoir un compte sur le serveur pour accéder à la ressource.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-124">A user or application must have an account on the server to access the resource.</span></span>

<span data-ttu-id="3ccf4-125">Vous pouvez également spécifier un descripteur de sécurité à associer à un partage.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-125">You can also specify a security descriptor to be associated with a share.</span></span> <span data-ttu-id="3ccf4-126">Les descripteurs de sécurité spécifient les utilisateurs autorisés à accéder aux fichiers via le partage, ainsi que le type d’accès.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-126">Security descriptors specify which users are allowed to access files through the share, and with what type of access.</span></span> <span data-ttu-id="3ccf4-127">Spécifiez [**un \_ descripteur de sécurité**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) avec le niveau d’informations [**share \_ info \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) lors de l’appel de [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) ou [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span><span class="sxs-lookup"><span data-stu-id="3ccf4-127">Specify a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) with the [**SHARE\_INFO\_502**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502) information level when calling [**NetShareAdd**](/windows/desktop/api/Lmshare/nf-lmshare-netshareadd) or [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo).</span></span> <span data-ttu-id="3ccf4-128">**NetShareSetInfo** prend en charge le niveau d’informations [**share \_ info \_ 1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) .</span><span class="sxs-lookup"><span data-stu-id="3ccf4-128">**NetShareSetInfo** supports the [**SHARE\_INFO\_1501**](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501) information level.</span></span> <span data-ttu-id="3ccf4-129">Pour plus d’informations sur les descripteurs de sécurité, consultez [Access Control](/windows/desktop/SecAuthZ/access-control).</span><span class="sxs-lookup"><span data-stu-id="3ccf4-129">For more information about security descriptors, see [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

<span data-ttu-id="3ccf4-130">Les fonctions de gestion de réseau utilisent les noms de partage spéciaux suivants pour la communication interprocessus (IPC) et l’administration à distance du serveur :</span><span class="sxs-lookup"><span data-stu-id="3ccf4-130">The network management functions use the following special share names for interprocess communication (IPC) and remote administration of the server:</span></span>

-   <span data-ttu-id="3ccf4-131">IPC $, réservé à la communication entre processus</span><span class="sxs-lookup"><span data-stu-id="3ccf4-131">IPC$, reserved for interprocess communication</span></span>
-   <span data-ttu-id="3ccf4-132">ADMIN $, réservé à l’administration à distance</span><span class="sxs-lookup"><span data-stu-id="3ccf4-132">ADMIN$, reserved for remote administration</span></span>
-   <span data-ttu-id="3ccf4-133">$, B $, C $ (et d’autres noms de disque local suivis d’un signe dollar), affectés aux périphériques de disque local</span><span class="sxs-lookup"><span data-stu-id="3ccf4-133">A$, B$, C$ (and other local disk names followed by a dollar sign), assigned to local disk devices</span></span>

<span data-ttu-id="3ccf4-134">Pour répertorier toutes les connexions établies avec une ressource partagée sur un serveur, ou pour répertorier toutes les connexions établies à partir d’un ordinateur particulier, appelez la fonction [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) .</span><span class="sxs-lookup"><span data-stu-id="3ccf4-134">To list all connections made to a shared resource on a server, or to list all connections established from a particular computer, call the [**NetConnectionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netconnectionenum) function.</span></span> <span data-ttu-id="3ccf4-135">Vous pouvez appeler **NetConnectionEnum** sur les niveaux d’information [**Connection \_ info \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) et [**Connection \_ info \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) .</span><span class="sxs-lookup"><span data-stu-id="3ccf4-135">You can call **NetConnectionEnum** at the [**CONNECTION\_INFO\_0**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_0) and [**CONNECTION\_INFO\_1**](/windows/desktop/api/Lmshare/ns-lmshare-connection_info_1) information levels.</span></span>

<span data-ttu-id="3ccf4-136">Les fonctions de partage sont disponibles aux niveaux d’informations suivants :</span><span class="sxs-lookup"><span data-stu-id="3ccf4-136">Share functions are available at the following information levels:</span></span>

<dl>

[<span data-ttu-id="3ccf4-137">**Informations de partage \_ \_ 0**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-137">**SHARE\_INFO\_0**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_0)  
[<span data-ttu-id="3ccf4-138">**Informations de partage \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-138">**SHARE\_INFO\_1**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1)  
[<span data-ttu-id="3ccf4-139">**Informations de partage \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-139">**SHARE\_INFO\_2**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_2)  
[<span data-ttu-id="3ccf4-140">**PARTAGER des \_ informations \_ 501**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-140">**SHARE\_INFO\_501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_501)  
[<span data-ttu-id="3ccf4-141">**PARTAGER des \_ informations \_ 502**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-141">**SHARE\_INFO\_502**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_502)  
[<span data-ttu-id="3ccf4-142">**PARTAGER des \_ informations \_ 1005**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-142">**SHARE\_INFO\_1005**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1005)  
</dl>

<span data-ttu-id="3ccf4-143">Les niveaux d’informations suivants sont valides uniquement pour [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span><span class="sxs-lookup"><span data-stu-id="3ccf4-143">The following information levels are valid only for [**NetShareSetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsharesetinfo):</span></span>

<dl>

[<span data-ttu-id="3ccf4-144">**PARTAGER des \_ informations \_ 1004**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-144">**SHARE\_INFO\_1004**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1004)  
[<span data-ttu-id="3ccf4-145">**PARTAGER des \_ informations \_ 1006**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-145">**SHARE\_INFO\_1006**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1006)  
[<span data-ttu-id="3ccf4-146">**PARTAGER des \_ informations \_ 1501**</span><span class="sxs-lookup"><span data-stu-id="3ccf4-146">**SHARE\_INFO\_1501**</span></span>](/windows/desktop/api/Lmshare/ns-lmshare-share_info_1501)  
</dl>

<span data-ttu-id="3ccf4-147">Si vous programmez pour Active Directory, vous pourrez peut-être appeler certaines méthodes d’interface de service d’Active Directory (ADSI) pour obtenir les mêmes fonctionnalités que celles que vous pouvez obtenir en appelant les fonctions de partage de gestion de réseau.</span><span class="sxs-lookup"><span data-stu-id="3ccf4-147">If you are programming for Active Directory, you may be able to call certain Active Directory Service Interface (ADSI) methods to achieve the same functionality you can achieve by calling the network management share functions.</span></span> <span data-ttu-id="3ccf4-148">Pour plus d’informations, consultez [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span><span class="sxs-lookup"><span data-stu-id="3ccf4-148">For more information, see [**IADsFileShare**](/windows/desktop/api/iads/nn-iads-iadsfileshare).</span></span>

 

 
