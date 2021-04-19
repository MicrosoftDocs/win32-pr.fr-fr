---
description: Voici les fonctions COM+.
ms.assetid: fdeb70ff-17ae-4ee4-a8b1-7fffb65ba2b2
title: Fonctions COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f7ce33e729a12c37ff1f2dcef516ab13d9b69a
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2021
ms.locfileid: "106537191"
---
# <a name="com-functions"></a><span data-ttu-id="69dc7-103">Fonctions COM+</span><span class="sxs-lookup"><span data-stu-id="69dc7-103">COM+ Functions</span></span>

<span data-ttu-id="69dc7-104">Voici les fonctions COM+.</span><span class="sxs-lookup"><span data-stu-id="69dc7-104">The following are the COM+ functions.</span></span>



| <span data-ttu-id="69dc7-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="69dc7-105">Function</span></span>                                                                 | <span data-ttu-id="69dc7-106">Description</span><span class="sxs-lookup"><span data-stu-id="69dc7-106">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="69dc7-107">**CoCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="69dc7-107">**CoCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-cocreateactivity)                             | <span data-ttu-id="69dc7-108">Crée une activité, pour exécuter un travail en traitement par lots de type synchrone ou asynchrone, pouvant utiliser des services COM+ sans créer obligatoirement un composant COM+.</span><span class="sxs-lookup"><span data-stu-id="69dc7-108">Creates an activity to do synchronous or asynchronous batch work that can use COM+ services without needing to create a COM+ component.</span></span> |
| [<span data-ttu-id="69dc7-109">**CoEnterServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="69dc7-109">**CoEnterServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coenterservicedomain)                     | <span data-ttu-id="69dc7-110">Permet d’entrer du code qui peut ensuite utiliser des services COM+.</span><span class="sxs-lookup"><span data-stu-id="69dc7-110">Used to enter code that can then use COM+ services.</span></span>                                                                                     |
| [<span data-ttu-id="69dc7-111">**CoGetDefaultContext**</span><span class="sxs-lookup"><span data-stu-id="69dc7-111">**CoGetDefaultContext**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetdefaultcontext)                       | <span data-ttu-id="69dc7-112">Récupère une référence au contexte par défaut du cloisonnement spécifié.</span><span class="sxs-lookup"><span data-stu-id="69dc7-112">Retrieves a reference to the default context of the specified apartment.</span></span>                                                                |
| [<span data-ttu-id="69dc7-113">**CoLeaveServiceDomain**</span><span class="sxs-lookup"><span data-stu-id="69dc7-113">**CoLeaveServiceDomain**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-coleaveservicedomain)                     | <span data-ttu-id="69dc7-114">Utilisé pour conserver le code qui utilise les services COM+.</span><span class="sxs-lookup"><span data-stu-id="69dc7-114">Used to leave code that uses COM+ services.</span></span>                                                                                             |
| <span data-ttu-id="69dc7-115">**ComPlusCompleteCbbSetup**</span><span class="sxs-lookup"><span data-stu-id="69dc7-115">**ComPlusCompleteCbbSetup**</span></span>               | <span data-ttu-id="69dc7-116">Effectue une migration du catalogue sur l’ordinateur de destination.</span><span class="sxs-lookup"><span data-stu-id="69dc7-116">Completes a catalog migration on the destination computer.</span></span>                                                                              |
| <span data-ttu-id="69dc7-117">**GetComPlusPackageInstallStatus**</span><span class="sxs-lookup"><span data-stu-id="69dc7-117">**GetComPlusPackageInstallStatus**</span></span> | <span data-ttu-id="69dc7-118">Indique si le Common Language Runtime (CLR) 64 bits est installé.</span><span class="sxs-lookup"><span data-stu-id="69dc7-118">Indicates whether the 64-bit Common Language Runtime (CLR) is installed.</span></span>                                                                |
| [<span data-ttu-id="69dc7-119">**GetDispenserManager**</span><span class="sxs-lookup"><span data-stu-id="69dc7-119">**GetDispenserManager**</span></span>](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager)                       | <span data-ttu-id="69dc7-120">Récupère l’interface [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) du gestionnaire du distributeur.</span><span class="sxs-lookup"><span data-stu-id="69dc7-120">Retrieves the dispenser manager's [**IDispenserManager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) interface.</span></span>                                             |
| [<span data-ttu-id="69dc7-121">**GetManagedExtensions**</span><span class="sxs-lookup"><span data-stu-id="69dc7-121">**GetManagedExtensions**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getmanagedextensions)                     | <span data-ttu-id="69dc7-122">Détermine si la version installée de COM+ prend en charge les fonctionnalités spéciales fournies pour gérer les composants pris en charge (objets managés).</span><span class="sxs-lookup"><span data-stu-id="69dc7-122">Determines whether the installed version of COM+ supports special features provided to manage serviced components (managed objects).</span></span>    |
| [<span data-ttu-id="69dc7-123">**GetObjectContext**</span><span class="sxs-lookup"><span data-stu-id="69dc7-123">**GetObjectContext**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)                             | <span data-ttu-id="69dc7-124">Récupère une référence au contexte associé à l’objet COM+ actuel.</span><span class="sxs-lookup"><span data-stu-id="69dc7-124">Retrieves a reference to the context that is associated with the current COM+ object.</span></span>                                                   |
| [<span data-ttu-id="69dc7-125">**MTSCreateActivity**</span><span class="sxs-lookup"><span data-stu-id="69dc7-125">**MTSCreateActivity**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-mtscreateactivity)                           | <span data-ttu-id="69dc7-126">Crée une activité dans un thread unique cloisonné pour effectuer un travail en traitement par lots synchrone ou asynchrone.</span><span class="sxs-lookup"><span data-stu-id="69dc7-126">Creates an activity in a single-threaded apartment to do synchronous or asynchronous batch work.</span></span>                                        |
| [<span data-ttu-id="69dc7-127">**RecycleSurrogate**</span><span class="sxs-lookup"><span data-stu-id="69dc7-127">**RecycleSurrogate**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-recyclesurrogate)                             | <span data-ttu-id="69dc7-128">Recycle le processus appelant.</span><span class="sxs-lookup"><span data-stu-id="69dc7-128">Recycles the calling process.</span></span>                                                                                                           |
| [<span data-ttu-id="69dc7-129">**SafeRef**</span><span class="sxs-lookup"><span data-stu-id="69dc7-129">**SafeRef**</span></span>](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)                                               | <span data-ttu-id="69dc7-130">Périmé n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="69dc7-130">Obsolete; do not use.</span></span>                                                                                                                   |



 

 

 



