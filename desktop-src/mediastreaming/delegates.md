---
title: Délégués
description: L’API de diffusion multimédia en continu fournit les fonctions de gestionnaire d’événements suivantes.
ms.assetid: CDE7B829-D0D1-479D-9B35-4445E711AF58
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23fbf0f44a0822fd0c8914833b0696fcb9aacad
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507885"
---
# <a name="delegates"></a><span data-ttu-id="7bb78-103">Délégués</span><span class="sxs-lookup"><span data-stu-id="7bb78-103">Delegates</span></span>

<span data-ttu-id="7bb78-104">L' [API de diffusion multimédia en continu](media-streaming-api-portal.md) fournit les fonctions de gestionnaire d’événements suivantes.</span><span class="sxs-lookup"><span data-stu-id="7bb78-104">The [Media Streaming API](media-streaming-api-portal.md) provides the following event handler functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7bb78-105">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="7bb78-105">In this section</span></span>



| <span data-ttu-id="7bb78-106">Rubrique</span><span class="sxs-lookup"><span data-stu-id="7bb78-106">Topic</span></span>                                                                                   | <span data-ttu-id="7bb78-107">Description</span><span class="sxs-lookup"><span data-stu-id="7bb78-107">Description</span></span>                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb78-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bb78-108">[**ConnectionStatusHandler**](/previous-versions/windows/desktop/legacy/hh828836(v=vs.85))</span></span><br/>                   | <span data-ttu-id="7bb78-109">Représente la fonction qui gérera l’événement [**ConnectionStatusChanged**](connectionstatuschanged.md) qui avertit le client des modifications de l’état de la connexion réseau de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="7bb78-109">Represents the function that will handle the [**ConnectionStatusChanged**](connectionstatuschanged.md) event which notifies the client of changes in the device s network connection status.</span></span><br/>               |
| <span data-ttu-id="7bb78-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bb78-110">[**DeviceControllerFinderHandler**](/previous-versions/windows/desktop/legacy/hh828843(v=vs.85))</span></span><br/>       | <span data-ttu-id="7bb78-111">Représente la fonction qui gérera les événements [**DeviceArrival**](devicearrival.md) et [**DeviceDeparture**](devicedeparture.md) qui informent le client des modifications apportées à la liste des appareils mis en cache.</span><span class="sxs-lookup"><span data-stu-id="7bb78-111">Represents the function that will handle the [**DeviceArrival**](devicearrival.md) and [**DeviceDeparture**](devicedeparture.md) events which notify the client of changes in the list of cached devices.</span></span><br/> |
| <span data-ttu-id="7bb78-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bb78-112">[**RenderingParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh828994(v=vs.85))</span></span><br/> | <span data-ttu-id="7bb78-113">Représente la fonction qui gérera l’événement [**RenderingParametersUpdate**](renderingparametersupdate.md) , qui avertit le client d’une mise à jour de tous les paramètres de contrôle de rendu de la gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="7bb78-113">Represents the function that will handle the [**RenderingParametersUpdate**](renderingparametersupdate.md) event which notifies the client of an update to any of the DMR s rendering control parameters.</span></span><br/>  |
| <span data-ttu-id="7bb78-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7bb78-114">[**TransportParametersUpdateHandler**](/previous-versions/windows/desktop/legacy/hh829007(v=vs.85))</span></span><br/> | <span data-ttu-id="7bb78-115">Représente la fonction qui gérera l’événement [**TransportParametersUpdate**](transportparametersupdate.md) , qui notifie le client d’une mise à jour à l’un des paramètres de transport de la gestion des e/s.</span><span class="sxs-lookup"><span data-stu-id="7bb78-115">Represents the function that will handle the [**TransportParametersUpdate**](transportparametersupdate.md) event which notifies the client of an update to any of the DMR s transport parameters.</span></span><br/>          |



 

 

