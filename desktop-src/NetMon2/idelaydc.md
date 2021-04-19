---
description: L’interface IDelaydC fournit les méthodes utilisées pour se connecter au réseau, capturer le trafic réseau vers un fichier de capture, récupérer des statistiques et se déconnecter du réseau.
ms.assetid: ab275653-2377-4af6-a810-48515962c88c
title: Interface IDelaydC (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: cb87bc9f821e758b83a1bc3dee5d81a4b1b771d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529704"
---
# <a name="idelaydc-interface"></a><span data-ttu-id="15dca-103">Interface IDelaydC</span><span class="sxs-lookup"><span data-stu-id="15dca-103">IDelaydC interface</span></span>

<span data-ttu-id="15dca-104">L’interface **IDelaydC** fournit les méthodes utilisées pour se connecter au réseau, capturer le trafic réseau vers un fichier de capture, récupérer des statistiques et se déconnecter du réseau.</span><span class="sxs-lookup"><span data-stu-id="15dca-104">The **IDelaydC** interface provides the methods used to connect to the network, capture network traffic to a capture file, retrieve statistics, and disconnect from the network.</span></span>

<span data-ttu-id="15dca-105">Cette interface capture des frames à partir du flux de données réseau, puis copie les frames dans un fichier de capture.</span><span class="sxs-lookup"><span data-stu-id="15dca-105">This interface captures frames from the network data stream and then copies the frames to a capture file.</span></span> <span data-ttu-id="15dca-106">Cette interface est utilisée par les applications Moniteur réseau et NPP.</span><span class="sxs-lookup"><span data-stu-id="15dca-106">This interface is used by Network Monitor and NPP applications.</span></span> <span data-ttu-id="15dca-107">Pour recevoir les données réseau, la carte d’interface réseau ciblée doit prendre en charge le mode de proximité.</span><span class="sxs-lookup"><span data-stu-id="15dca-107">To receive the network data, the targeted NIC must support promiscuous mode.</span></span>

## <a name="members"></a><span data-ttu-id="15dca-108">Membres</span><span class="sxs-lookup"><span data-stu-id="15dca-108">Members</span></span>

<span data-ttu-id="15dca-109">L’interface **IDelaydC** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="15dca-109">The **IDelaydC** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="15dca-110">**IDelaydC** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="15dca-110">**IDelaydC** also has these types of members:</span></span>

-   [<span data-ttu-id="15dca-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="15dca-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="15dca-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="15dca-112">Methods</span></span>

<span data-ttu-id="15dca-113">L’interface **IDelaydC** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="15dca-113">The **IDelaydC** interface has these methods.</span></span>



| <span data-ttu-id="15dca-114">Méthode</span><span class="sxs-lookup"><span data-stu-id="15dca-114">Method</span></span>                                                                  | <span data-ttu-id="15dca-115">Description</span><span class="sxs-lookup"><span data-stu-id="15dca-115">Description</span></span>                                                                                                                                             |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15dca-116">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="15dca-116">**Configure**</span></span>](idelaydc-configure.md)                                 | <span data-ttu-id="15dca-117">Envoie les informations de configuration utilisées pour une capture.</span><span class="sxs-lookup"><span data-stu-id="15dca-117">Submits configuration information used for a capture.</span></span><br/>                                                                                        |
| [<span data-ttu-id="15dca-118">**Se connecter**</span><span class="sxs-lookup"><span data-stu-id="15dca-118">**Connect**</span></span>](idelaydc-connect.md)                                     | <span data-ttu-id="15dca-119">Connecte le NPP au réseau.</span><span class="sxs-lookup"><span data-stu-id="15dca-119">Connects the NPP to the network.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="15dca-120">**Déconnecter**</span><span class="sxs-lookup"><span data-stu-id="15dca-120">**Disconnect**</span></span>](idelaydc-disconnect.md)                               | <span data-ttu-id="15dca-121">Déconnecte le NPP du réseau.</span><span class="sxs-lookup"><span data-stu-id="15dca-121">Disconnects the NPP from the network.</span></span><br/>                                                                                                        |
| [<span data-ttu-id="15dca-122">**GetControlState**</span><span class="sxs-lookup"><span data-stu-id="15dca-122">**GetControlState**</span></span>](idelaydc-getcontrolstate.md)                     | <span data-ttu-id="15dca-123">Récupère l’état de la [*capture*](c.md), qui indique si la capture est en cours d’exécution ou en pause.</span><span class="sxs-lookup"><span data-stu-id="15dca-123">Retrieves the state of the [*capture*](c.md), which indicates if the capture is running or paused.</span></span><br/>                      |
| [<span data-ttu-id="15dca-124">**GetConversationStatistics**</span><span class="sxs-lookup"><span data-stu-id="15dca-124">**GetConversationStatistics**</span></span>](idelaydc-getconversationstatistics.md) | <span data-ttu-id="15dca-125">Récupère les informations de [*session*](s.md) et de [*station*](s.md) pour la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="15dca-125">Retrieves [*session*](s.md) and [*station information*](s.md) for the current capture.</span></span><br/> |
| [<span data-ttu-id="15dca-126">**GetTotalStatistics**</span><span class="sxs-lookup"><span data-stu-id="15dca-126">**GetTotalStatistics**</span></span>](idelaydc-gettotalstatistics.md)               | <span data-ttu-id="15dca-127">Extrait le temps, la mémoire tampon, le pilote et d’autres statistiques réseau à partir de la capture en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="15dca-127">Extracts time, buffer, driver, and other network statistics from the currently running capture.</span></span><br/>                                              |
| [<span data-ttu-id="15dca-128">**Suspendre**</span><span class="sxs-lookup"><span data-stu-id="15dca-128">**Pause**</span></span>](idelaydc-pause.md)                                         | <span data-ttu-id="15dca-129">Arrête temporairement la capture en cours.</span><span class="sxs-lookup"><span data-stu-id="15dca-129">Temporarily stops the current capture.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="15dca-130">**QueryStations**</span><span class="sxs-lookup"><span data-stu-id="15dca-130">**QueryStations**</span></span>](idelaydc-querystations.md)                         | <span data-ttu-id="15dca-131">Récupère une liste de tous les ordinateurs qui utilisent Moniteur réseau pour capturer des données sur un sous-réseau.</span><span class="sxs-lookup"><span data-stu-id="15dca-131">Retrieves a list of all computers that use Network Monitor to capture data on a subnet.</span></span><br/>                                                      |
| [<span data-ttu-id="15dca-132">**QueryStatus**</span><span class="sxs-lookup"><span data-stu-id="15dca-132">**QueryStatus**</span></span>](idelaydc-querystatus.md)                             | <span data-ttu-id="15dca-133">Récupère l’état du NPP.</span><span class="sxs-lookup"><span data-stu-id="15dca-133">Retrieves the status of the NPP.</span></span><br/>                                                                                                             |
| [<span data-ttu-id="15dca-134">**Sort**</span><span class="sxs-lookup"><span data-stu-id="15dca-134">**Resume**</span></span>](idelaydc-resume.md)                                       | <span data-ttu-id="15dca-135">Reprend une capture suspendue.</span><span class="sxs-lookup"><span data-stu-id="15dca-135">Resumes a paused capture.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="15dca-136">**Activer**</span><span class="sxs-lookup"><span data-stu-id="15dca-136">**Start**</span></span>](idelaydc-start.md)                                         | <span data-ttu-id="15dca-137">Démarre une capture et crée le [*fichier de capture*](c.md).</span><span class="sxs-lookup"><span data-stu-id="15dca-137">Starts a capture and creates the [*capture file*](c.md).</span></span><br/>                                                           |
| [<span data-ttu-id="15dca-138">**Erreur**</span><span class="sxs-lookup"><span data-stu-id="15dca-138">**Stop**</span></span>](idelaydc-stop.md)                                           | <span data-ttu-id="15dca-139">Arrête la capture en cours et ferme le [*fichier de capture*](c.md).</span><span class="sxs-lookup"><span data-stu-id="15dca-139">Stops the current capture and closes the [*capture file*](c.md).</span></span><br/>                                                   |



 

## <a name="requirements"></a><span data-ttu-id="15dca-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15dca-140">Requirements</span></span>



| <span data-ttu-id="15dca-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15dca-141">Requirement</span></span> | <span data-ttu-id="15dca-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="15dca-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dca-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15dca-143">Minimum supported client</span></span><br/> | <span data-ttu-id="15dca-144">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15dca-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="15dca-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15dca-145">Minimum supported server</span></span><br/> | <span data-ttu-id="15dca-146">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15dca-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="15dca-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="15dca-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="15dca-148"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="15dca-148"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="15dca-149">DLL</span><span class="sxs-lookup"><span data-stu-id="15dca-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15dca-150"><dt>Ndisnpp.dll ; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15dca-150"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



 

