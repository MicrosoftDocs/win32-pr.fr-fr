---
description: Interface pour la communication à distance des données relatives à un vsglog.
MS-HAID: vspixengine.IPeerToPeerEngine
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IPeerToPeerEngine
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C6C4783F-ED46-47C2-98BB-C618897F8FF8
api_name:
- IPeerToPeerEngine
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 899e5eea28ffb769e082b2e0bd7bc165889b2d37
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517381"
---
# <a name="span-idvspixengineipeertopeerenginespanipeertopeerengine-interface"></a><span data-ttu-id="5984d-103"><span id="vspixengine.ipeertopeerengine"></span>Interface IPeerToPeerEngine</span><span class="sxs-lookup"><span data-stu-id="5984d-103"><span id="vspixengine.ipeertopeerengine"></span>IPeerToPeerEngine interface</span></span>

<span data-ttu-id="5984d-104">Interface pour la communication à distance des données relatives à un vsglog.</span><span class="sxs-lookup"><span data-stu-id="5984d-104">Interface for remote communicating data about a vsglog.</span></span>

## <a name="members"></a><span data-ttu-id="5984d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5984d-105">Members</span></span>

<span data-ttu-id="5984d-106">L’interface **IPeerToPeerEngine** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="5984d-106">The **IPeerToPeerEngine** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="5984d-107">**IPeerToPeerEngine** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5984d-107">**IPeerToPeerEngine** also has these types of members:</span></span>

-   [<span data-ttu-id="5984d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="5984d-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="5984d-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="5984d-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="5984d-110">L’interface **IPeerToPeerEngine** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="5984d-110">The **IPeerToPeerEngine** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="5984d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="5984d-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="5984d-112">Description</span><span class="sxs-lookup"><span data-stu-id="5984d-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5984d-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="5984d-113"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-cancelsetplaybackendpoint"><strong>CancelSetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5984d-114">Annule une demande précédente pour configurer une connexion à distance.</span><span class="sxs-lookup"><span data-stu-id="5984d-114">Cancels a previous request to set up a remote connection.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="5984d-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="5984d-115"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-getplaybackendpoint-bool-bstr-ptr-bstr-ptr-remotingversion-ptr"><strong>GetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5984d-116">Obtient l’adresse de point de terminaison d’un moteur distant.</span><span class="sxs-lookup"><span data-stu-id="5984d-116">Gets the endpoint address of a remote engine.</span></span></p></td></tr><tr class="odd"><td style="text-align: left;"><span data-ttu-id="5984d-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span><span class="sxs-lookup"><span data-stu-id="5984d-117"><a href="/windows/desktop/direct3dtools/ipeertopeerengine-setplaybackendpoint-bool-bstr-bstr-remotingversion"><strong>SetPlaybackEndpoint</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="5984d-118">Définit l’adresse de point de terminaison utilisée pour se connecter à un moteur distant.</span><span class="sxs-lookup"><span data-stu-id="5984d-118">Sets the endpoint address used to connect to a remote engine.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="5984d-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5984d-119">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="5984d-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="5984d-120">Header</span></span></p></td><td><span data-ttu-id="5984d-121">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="5984d-121">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
