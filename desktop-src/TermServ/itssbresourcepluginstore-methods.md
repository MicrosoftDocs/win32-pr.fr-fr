---
title: Méthodes ITsSbResourcePluginStore
description: L’interface ITsSbResourcePluginStore expose les méthodes suivantes.
ms.assetid: D3D59244-E319-47C8-A931-72679C11AC40
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c56d403bc681152a5076d6c219790b452bd749d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840290"
---
# <a name="itssbresourcepluginstore-methods"></a><span data-ttu-id="3fd4d-103">Méthodes ITsSbResourcePluginStore</span><span class="sxs-lookup"><span data-stu-id="3fd4d-103">ITsSbResourcePluginStore Methods</span></span>

<span data-ttu-id="3fd4d-104">L’interface [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="3fd4d-104">The [**ITsSbResourcePluginStore**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore) interface exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3fd4d-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="3fd4d-105">In this section</span></span>

-   [<span data-ttu-id="3fd4d-106">**Méthode AcquireTargetLock**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-106">**AcquireTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-acquiretargetlock)
-   [<span data-ttu-id="3fd4d-107">**Méthode AddEnvironmentToStore**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-107">**AddEnvironmentToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addenvironmenttostore)
-   [<span data-ttu-id="3fd4d-108">**Méthode AddSessionToStore**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-108">**AddSessionToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addsessiontostore)
-   [<span data-ttu-id="3fd4d-109">**Méthode AddTargetToStore**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-109">**AddTargetToStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-addtargettostore)
-   [<span data-ttu-id="3fd4d-110">**Méthode DeleteTarget**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-110">**DeleteTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-deletetarget)
-   [<span data-ttu-id="3fd4d-111">**Méthode EnumerateEnvironments**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-111">**EnumerateEnvironments method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumerateenvironments)
-   [<span data-ttu-id="3fd4d-112">**Méthode EnumerateFarms**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-112">**EnumerateFarms method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratefarms)
-   [<span data-ttu-id="3fd4d-113">**Méthode EnumerateSessions**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-113">**EnumerateSessions method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratesessions)
-   [<span data-ttu-id="3fd4d-114">**Méthode EnumerateTargets**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-114">**EnumerateTargets method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-enumeratetargets)
-   [<span data-ttu-id="3fd4d-115">**Méthode GetFarmProperty**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-115">**GetFarmProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getfarmproperty)
-   [<span data-ttu-id="3fd4d-116">**Méthode GetServerState**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-116">**GetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-getserverstate)
-   [<span data-ttu-id="3fd4d-117">**Méthode QueryEnvironment**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-117">**QueryEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-queryenvironment)
-   [<span data-ttu-id="3fd4d-118">**Méthode QuerySessionBySessionId**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-118">**QuerySessionBySessionId method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querysessionbysessionid)
-   [<span data-ttu-id="3fd4d-119">**Méthode QueryTarget**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-119">**QueryTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-querytarget)
-   [<span data-ttu-id="3fd4d-120">**Méthode ReleaseTargetLock**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-120">**ReleaseTargetLock method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-releasetargetlock)
-   [<span data-ttu-id="3fd4d-121">**Méthode RemoveEnvironmentFromStore**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-121">**RemoveEnvironmentFromStore method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-removeenvironmentfromstore)
-   [<span data-ttu-id="3fd4d-122">**Méthode SaveEnvironment**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-122">**SaveEnvironment method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-saveenvironment)
-   [<span data-ttu-id="3fd4d-123">**Méthode SaveSession**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-123">**SaveSession method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savesession)
-   [<span data-ttu-id="3fd4d-124">**Méthode SaveTarget**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-124">**SaveTarget method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-savetarget)
-   [<span data-ttu-id="3fd4d-125">**Méthode SetEnvironmentProperty**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-125">**SetEnvironmentProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentproperty)
-   [<span data-ttu-id="3fd4d-126">**Méthode SetEnvironmentPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-126">**SetEnvironmentPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setenvironmentpropertywithversioncheck)
-   [<span data-ttu-id="3fd4d-127">**Méthode SetServerDrainMode**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-127">**SetServerDrainMode method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverdrainmode)
-   [<span data-ttu-id="3fd4d-128">**Méthode SetServerWaitingToStart**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-128">**SetServerWaitingToStart method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setserverwaitingtostart)
-   [<span data-ttu-id="3fd4d-129">**Méthode SetSessionState**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-129">**SetSessionState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-setsessionstate)
-   [<span data-ttu-id="3fd4d-130">**Méthode SetTargetProperty**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-130">**SetTargetProperty method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetproperty)
-   [<span data-ttu-id="3fd4d-131">**Méthode SetTargetPropertyWithVersionCheck**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-131">**SetTargetPropertyWithVersionCheck method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetpropertywithversioncheck)
-   [<span data-ttu-id="3fd4d-132">**Méthode SetTargetState**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-132">**SetTargetState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-settargetstate)
-   [<span data-ttu-id="3fd4d-133">**Méthode TestAndSetServerState**</span><span class="sxs-lookup"><span data-stu-id="3fd4d-133">**TestAndSetServerState method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbresourcepluginstore-testandsetserverstate)

 

 




