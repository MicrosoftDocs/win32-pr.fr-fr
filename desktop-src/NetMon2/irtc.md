---
description: L’interface IRTC fournit les méthodes utilisées pour connecter le NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau.
ms.assetid: 9252a9ba-2c3e-40b9-b8de-84ef5d4831a7
title: Interface IRTC (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: c937d7d9233b1df063a7cf4a12e57e909145b8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951632"
---
# <a name="irtc-interface"></a><span data-ttu-id="c4bef-103">Interface IRTC</span><span class="sxs-lookup"><span data-stu-id="c4bef-103">IRTC interface</span></span>

<span data-ttu-id="c4bef-104">L’interface **IRTC** fournit les méthodes utilisées pour connecter le NPP au réseau, capturer le trafic réseau, récupérer des statistiques et déconnecter le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="c4bef-104">The **IRTC** interface provides the methods used to connect the NPP to the network, capture network traffic, retrieve statistics, and disconnect the NPP from the network.</span></span> <span data-ttu-id="c4bef-105">**IRTC** obtient une interface aux points d’entrée locaux uniquement, qui sont nécessaires pour effectuer une capture en temps réel.</span><span class="sxs-lookup"><span data-stu-id="c4bef-105">**IRTC** gets an interface to local-only entry points, which are necessary to engage in real-time capture.</span></span> <span data-ttu-id="c4bef-106">Cette interface comprend une méthode qui transmet un rappel au NPP.</span><span class="sxs-lookup"><span data-stu-id="c4bef-106">This interface includes a method that hands off a callback to the NPP.</span></span>

## <a name="members"></a><span data-ttu-id="c4bef-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c4bef-107">Members</span></span>

<span data-ttu-id="c4bef-108">L’interface **IRTC** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4bef-108">The **IRTC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4bef-109">**IRTC** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c4bef-109">**IRTC** also has these types of members:</span></span>

-   [<span data-ttu-id="c4bef-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4bef-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4bef-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c4bef-111">Methods</span></span>

<span data-ttu-id="c4bef-112">L’interface **IRTC** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c4bef-112">The **IRTC** interface has these methods.</span></span>



| <span data-ttu-id="c4bef-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c4bef-113">Method</span></span>                                                              | <span data-ttu-id="c4bef-114">Description</span><span class="sxs-lookup"><span data-stu-id="c4bef-114">Description</span></span>                                                                                                                                             |
|:--------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4bef-115">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="c4bef-115">**Configure**</span></span>](irtc-configure.md)                                 | <span data-ttu-id="c4bef-116">Définit le déclencheur, la correspondance de modèle et la taille de mémoire tampon de la capture.</span><span class="sxs-lookup"><span data-stu-id="c4bef-116">Sets the trigger, pattern match, and buffer size of the capture.</span></span><br/>                                                                             |
| [<span data-ttu-id="c4bef-117">**Se connecter**</span><span class="sxs-lookup"><span data-stu-id="c4bef-117">**Connect**</span></span>](irtc-connect.md)                                     | <span data-ttu-id="c4bef-118">Connecte le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="c4bef-118">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c4bef-119">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="c4bef-119">**Disconnect**</span></span>](irtc-disconnect.md)                               | <span data-ttu-id="c4bef-120">Déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="c4bef-120">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="c4bef-121">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="c4bef-121">**GetControlState**</span></span>](irtc-getcontrolstate.md)                     | <span data-ttu-id="c4bef-122">Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="c4bef-122">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="c4bef-123">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="c4bef-123">**GetConversationStatistics**</span></span>](irtc-getconversationstatistics.md) | <span data-ttu-id="c4bef-124">Récupère les informations de [*session*](s.md) et de [*station*](s.md) pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="c4bef-124">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="c4bef-125">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="c4bef-125">**GetTotalStatistics**</span></span>](irtc-gettotalstatistics.md)               | <span data-ttu-id="c4bef-126">Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c4bef-126">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="c4bef-127">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="c4bef-127">**Pause**</span></span>](irtc-pause.md)                                         | <span data-ttu-id="c4bef-128">Arrête temporairement la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="c4bef-128">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="c4bef-129">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="c4bef-129">**QueryStations**</span></span>](irtc-querystations.md)                         | <span data-ttu-id="c4bef-130">Récupère une liste de tous les ordinateurs d’un sous-réseau qui utilisent Moniteur réseau pour capturer les données réseau.</span><span class="sxs-lookup"><span data-stu-id="c4bef-130">Retrieves a list of all computers on a subnet that are using Network Monitor to capture network data.</span></span><br/>                                        |
| [<span data-ttu-id="c4bef-131">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="c4bef-131">**QueryStatus**</span></span>](irtc-querystatus.md)                             | <span data-ttu-id="c4bef-132">Récupère l’état du NPP.</span><span class="sxs-lookup"><span data-stu-id="c4bef-132">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="c4bef-133">**Sort**</span><span class="sxs-lookup"><span data-stu-id="c4bef-133">**Resume**</span></span>](irtc-resume.md)                                       | <span data-ttu-id="c4bef-134">Redémarre une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="c4bef-134">Restarts a paused capture.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="c4bef-135">**Activer**</span><span class="sxs-lookup"><span data-stu-id="c4bef-135">**Start**</span></span>](irtc-start.md)                                         | <span data-ttu-id="c4bef-136">Démarre une capture.</span><span class="sxs-lookup"><span data-stu-id="c4bef-136">Starts a capture.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="c4bef-137">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="c4bef-137">**Stop**</span></span>](irtc-stop.md)                                           | <span data-ttu-id="c4bef-138">Arrête la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="c4bef-138">Stops the current capture.</span></span><br/>                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="c4bef-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4bef-139">Requirements</span></span>



| <span data-ttu-id="c4bef-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4bef-140">Requirement</span></span> | <span data-ttu-id="c4bef-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4bef-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bef-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4bef-142">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bef-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4bef-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="c4bef-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4bef-144">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bef-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c4bef-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="c4bef-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4bef-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4bef-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4bef-147"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="c4bef-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c4bef-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4bef-149"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4bef-149"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

