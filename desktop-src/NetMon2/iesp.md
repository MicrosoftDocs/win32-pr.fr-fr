---
description: L’interface IESP fournit les méthodes qui connectent le NPP au réseau, capture le trafic réseau dans un fichier de capture, récupère les statistiques et déconnecte le NPP du réseau.
ms.assetid: e483f501-4928-4bfd-b212-e100f2b8f64f
title: Interface IESP (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 1a7400bb9a16e6ece5f5f26fe95a0398a7d45e19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112802"
---
# <a name="iesp-interface"></a><span data-ttu-id="5e8b7-103">Interface IESP</span><span class="sxs-lookup"><span data-stu-id="5e8b7-103">IESP interface</span></span>

<span data-ttu-id="5e8b7-104">L’interface **IESP** fournit les méthodes qui connectent le NPP au réseau, capture le trafic réseau dans un fichier de capture, récupère les statistiques et déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-104">The **IESP** interface provides the methods that connect the NPP to the network, capture network traffic to a capture file, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="5e8b7-105">Cette interface est principalement utilisée lorsque vous devez collecter des [*statistiques de conversation*](c.md) réseau dans un format de fichier ESP propriétaire.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-105">This interface is used primarily when you need to collect network [*conversation statistics*](c.md) in a proprietary ESP file format.</span></span>

## <a name="members"></a><span data-ttu-id="5e8b7-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5e8b7-106">Members</span></span>

<span data-ttu-id="5e8b7-107">L’interface **IESP** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5e8b7-107">The **IESP** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5e8b7-108">**IESP** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5e8b7-108">**IESP** also has these types of members:</span></span>

-   [<span data-ttu-id="5e8b7-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e8b7-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="5e8b7-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5e8b7-110">Methods</span></span>

<span data-ttu-id="5e8b7-111">L’interface **IESP** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-111">The **IESP** interface has these methods.</span></span>



| <span data-ttu-id="5e8b7-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="5e8b7-112">Method</span></span>                                          | <span data-ttu-id="5e8b7-113">Description</span><span class="sxs-lookup"><span data-stu-id="5e8b7-113">Description</span></span>                                                                                                                        |
|:------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e8b7-114">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-114">**Configure**</span></span>](iesp-configure.md)             | <span data-ttu-id="5e8b7-115">Envoie les informations de configuration d’une capture</span><span class="sxs-lookup"><span data-stu-id="5e8b7-115">Submits configuration information for a capture</span></span><br/>                                                                         |
| [<span data-ttu-id="5e8b7-116">**Se connecter**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-116">**Connect**</span></span>](iesp-connect.md)                 | <span data-ttu-id="5e8b7-117">Connecte le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-117">Connects the NPP to the network.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5e8b7-118">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-118">**Disconnect**</span></span>](iesp-disconnect.md)           | <span data-ttu-id="5e8b7-119">Déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-119">Disconnects the NPP from the network.</span></span><br/>                                                                                   |
| [<span data-ttu-id="5e8b7-120">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-120">**GetControlState**</span></span>](iesp-getcontrolstate.md) | <span data-ttu-id="5e8b7-121">Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-121">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/> |
| [<span data-ttu-id="5e8b7-122">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-122">**Pause**</span></span>](iesp-pause.md)                     | <span data-ttu-id="5e8b7-123">Arrête temporairement la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-123">Temporarily stops the current capture.</span></span><br/>                                                                                  |
| [<span data-ttu-id="5e8b7-124">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-124">**QueryStations**</span></span>](iesp-querystations.md)     | <span data-ttu-id="5e8b7-125">Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-125">Retrieves a list of all computers that are using Network Monitor to capture data on a subnet.</span></span><br/>                           |
| [<span data-ttu-id="5e8b7-126">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-126">**QueryStatus**</span></span>](iesp-querystatus.md)         | <span data-ttu-id="5e8b7-127">Récupère l’état du NPP.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-127">Retrieves the status of the NPP.</span></span><br/>                                                                                        |
| [<span data-ttu-id="5e8b7-128">**Sort**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-128">**Resume**</span></span>](iesp-resume.md)                   | <span data-ttu-id="5e8b7-129">Reprend une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-129">Resumes a paused capture.</span></span><br/>                                                                                               |
| [<span data-ttu-id="5e8b7-130">**Activer**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-130">**Start**</span></span>](iesp-start.md)                     | <span data-ttu-id="5e8b7-131">Démarre la capture et crée le fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-131">Starts the capture and creates the capture file.</span></span><br/>                                                                        |
| [<span data-ttu-id="5e8b7-132">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="5e8b7-132">**Stop**</span></span>](iesp-stop.md)                       | <span data-ttu-id="5e8b7-133">Arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="5e8b7-133">Stops the current capture.</span></span><br/>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="5e8b7-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e8b7-134">Requirements</span></span>



| <span data-ttu-id="5e8b7-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e8b7-135">Requirement</span></span> | <span data-ttu-id="5e8b7-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e8b7-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e8b7-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e8b7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5e8b7-138">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e8b7-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="5e8b7-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e8b7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5e8b7-140">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5e8b7-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="5e8b7-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e8b7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e8b7-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e8b7-142"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="5e8b7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="5e8b7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e8b7-144"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e8b7-144"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

