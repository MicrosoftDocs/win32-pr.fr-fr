---
description: L’interface IStats fournit les méthodes que vous utilisez pour connecter un NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau. Cette interface génère des statistiques sans frames.
ms.assetid: 57cfcdd6-f16c-4a1c-b2ba-ce98f0576862
title: Interface IStats (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: b64816589e3d4d0a2e3ace7be5c895e3d2cf22f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545797"
---
# <a name="istats-interface"></a><span data-ttu-id="554d9-104">Interface IStats</span><span class="sxs-lookup"><span data-stu-id="554d9-104">IStats interface</span></span>

<span data-ttu-id="554d9-105">L’interface **IStats** fournit les méthodes que vous utilisez pour connecter un NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="554d9-105">The **IStats** interface provides the methods you use to connect an NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="554d9-106">Cette interface génère des statistiques sans frames.</span><span class="sxs-lookup"><span data-stu-id="554d9-106">This interface generates statistics without frames.</span></span>

## <a name="members"></a><span data-ttu-id="554d9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="554d9-107">Members</span></span>

<span data-ttu-id="554d9-108">L’interface **IStats** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="554d9-108">The **IStats** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="554d9-109">**IStats** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="554d9-109">**IStats** also has these types of members:</span></span>

-   [<span data-ttu-id="554d9-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="554d9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="554d9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="554d9-111">Methods</span></span>

<span data-ttu-id="554d9-112">L’interface **IStats** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="554d9-112">The **IStats** interface has these methods.</span></span>



| <span data-ttu-id="554d9-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="554d9-113">Method</span></span>                                                                | <span data-ttu-id="554d9-114">Description</span><span class="sxs-lookup"><span data-stu-id="554d9-114">Description</span></span>                                                                                                                                               |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="554d9-115">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="554d9-115">**Configure**</span></span>](istats-configure.md)                                 | <span data-ttu-id="554d9-116">Configure le déclencheur, la correspondance de modèle et la taille de mémoire tampon du fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="554d9-116">Configures the trigger, pattern match, and buffer size of the capture file.</span></span><br/>                                                                    |
| [<span data-ttu-id="554d9-117">**Se connecter**</span><span class="sxs-lookup"><span data-stu-id="554d9-117">**Connect**</span></span>](istats-connect.md)                                     | <span data-ttu-id="554d9-118">Connecte le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="554d9-118">Connects the NPP to the network.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="554d9-119">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="554d9-119">**Disconnect**</span></span>](istats-disconnect.md)                               | <span data-ttu-id="554d9-120">Déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="554d9-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="554d9-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="554d9-121">**GetControlState**</span></span>](istats-getcontrolstate.md)                     | <span data-ttu-id="554d9-122">Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="554d9-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                        |
| [<span data-ttu-id="554d9-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="554d9-123">**GetConversationStatistics**</span></span>](istats-getconversationstatistics.md) | <span data-ttu-id="554d9-124">Récupère les informations de [*session*](s.md) et de [*station*](s.md) relatives à la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="554d9-124">Retrieves [*session*](s.md) and [*station information*](s.md) about the current capture.</span></span><br/> |
| [<span data-ttu-id="554d9-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="554d9-125">**GetTotalStatistics**</span></span>](istats-gettotalstatistics.md)               | <span data-ttu-id="554d9-126">Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="554d9-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                                |
| [<span data-ttu-id="554d9-127">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="554d9-127">**Pause**</span></span>](istats-pause.md)                                         | <span data-ttu-id="554d9-128">Arrête temporairement la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="554d9-128">Temporarily stops the current capture.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="554d9-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="554d9-129">**QueryStations**</span></span>](istats-querystations.md)                         | <span data-ttu-id="554d9-130">Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="554d9-130">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                                                  |
| [<span data-ttu-id="554d9-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="554d9-131">**QueryStatus**</span></span>](istats-querystatus.md)                             | <span data-ttu-id="554d9-132">Récupère l’état du NPP.</span><span class="sxs-lookup"><span data-stu-id="554d9-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                               |
| [<span data-ttu-id="554d9-133">**Sort**</span><span class="sxs-lookup"><span data-stu-id="554d9-133">**Resume**</span></span>](istats-resume.md)                                       | <span data-ttu-id="554d9-134">Redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="554d9-134">Restarts a paused capture.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="554d9-135">**Activer**</span><span class="sxs-lookup"><span data-stu-id="554d9-135">**Start**</span></span>](istats-start.md)                                         | <span data-ttu-id="554d9-136">Démarre la capture.</span><span class="sxs-lookup"><span data-stu-id="554d9-136">Starts the capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="554d9-137">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="554d9-137">**Stop**</span></span>](istats-stop.md)                                           | <span data-ttu-id="554d9-138">Arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="554d9-138">Stops the current capture.</span></span><br/>                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="554d9-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="554d9-139">Requirements</span></span>



| <span data-ttu-id="554d9-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="554d9-140">Requirement</span></span> | <span data-ttu-id="554d9-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="554d9-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="554d9-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="554d9-142">Minimum supported client</span></span><br/> | <span data-ttu-id="554d9-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="554d9-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="554d9-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="554d9-144">Minimum supported server</span></span><br/> | <span data-ttu-id="554d9-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="554d9-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="554d9-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="554d9-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="554d9-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="554d9-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="554d9-148">DLL</span><span class="sxs-lookup"><span data-stu-id="554d9-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="554d9-149"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="554d9-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

