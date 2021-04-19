---
description: .
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: Gestion et maintenance des images de déploiement (DISM, Deployment Image Servicing and Management)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 734ac9fae497eeb61d706a228fc1ffc6ea4da264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541239"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="4cea6-103">Gestion et maintenance des images de déploiement (DISM, Deployment Image Servicing and Management)</span><span class="sxs-lookup"><span data-stu-id="4cea6-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="4cea6-104">Plateformes affectées</span><span class="sxs-lookup"><span data-stu-id="4cea6-104">Affected Platforms</span></span>

<span data-ttu-id="4cea6-105">**Clients** -Windows Vista SP1 et versions ultérieures \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="4cea6-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="4cea6-106">**Serveurs** -windows Server 2008 RTM et versions ultérieures \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4cea6-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="4cea6-107">Description</span><span class="sxs-lookup"><span data-stu-id="4cea6-107">Description</span></span>

<span data-ttu-id="4cea6-108">L’outil gestion et maintenance des images de déploiement (DISM) remplace les outils pkgmgr, PEImg et IntlConfg en cours de mise hors service dans Windows 7.</span><span class="sxs-lookup"><span data-stu-id="4cea6-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="4cea6-109">DISM fournit un outil centralisé unique pour effectuer toutes les fonctions de ces trois outils de manière plus efficace et standardisée, ce qui élimine la source de nombreuses frustrations rencontrées par les utilisateurs actuels de ces outils.</span><span class="sxs-lookup"><span data-stu-id="4cea6-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="4cea6-110">DISM comprend un shim pour Windows Vista SP1 et versions ultérieures, ainsi que pour Windows Server 2008 RTM et versions ultérieures, qui redirige les appels pkgmgr des applications héritées s’exécutant sur Windows 7 vers DISM.</span><span class="sxs-lookup"><span data-stu-id="4cea6-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="4cea6-111">Si l’application s’exécute sur l’un des systèmes d’exploitation pris en charge, le shim achemine l’appel à Pkgmgr.</span><span class="sxs-lookup"><span data-stu-id="4cea6-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="4cea6-112">Il n’existe aucun shim pour les applications héritées qui appellent PEImg ou IntlConfg.</span><span class="sxs-lookup"><span data-stu-id="4cea6-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="4cea6-113">Utilisation</span><span class="sxs-lookup"><span data-stu-id="4cea6-113">Usage</span></span>

<span data-ttu-id="4cea6-114">DISM est transparent pour les utilisateurs finaux de pkgmgr sur les plateformes prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4cea6-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="4cea6-115">Toutefois, si une application appelle PEImg ou IntlConfg à partir de Windows 7, l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="4cea6-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="4cea6-116">Mettez à jour tous les scripts qui appellent pkgmgr, PEImg ou IntlConfg pour appeler DISM à la place.</span><span class="sxs-lookup"><span data-stu-id="4cea6-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="4cea6-117">Il est important d’inclure la mise à jour des scripts pkgmgr dans le cadre de cet effort, car le shim qui fournit la compatibilité descendante pour pkgmgr sera supprimé dans les versions ultérieures des systèmes d’exploitation Windows.</span><span class="sxs-lookup"><span data-stu-id="4cea6-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="4cea6-118">Vérifiez que les appels à DISM ont remplacé les appels à pkgmgr, PEImg et IntlConfg, et que l’opération s’exécute correctement.</span><span class="sxs-lookup"><span data-stu-id="4cea6-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4cea6-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4cea6-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4cea6-120">[Gestion et maintenance des images de déploiement (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="4cea6-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
