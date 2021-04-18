---
description: Rappel pour retourner la liste des événements dans un frame.
MS-HAID: vspixengine.IFrameEventsCallback
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameEventsCallback
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: F40DD5DC-E78E-41F3-9D25-4D7CAE27DE45
api_name:
- IFrameEventsCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 98815681db182c99a86c05c1ea22eaad41526438
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106519188"
---
# <a name="span-idvspixengineiframeeventscallbackspaniframeeventscallback-interface"></a><span data-ttu-id="8c50b-103"><span id="vspixengine.iframeeventscallback"></span>Interface IFrameEventsCallback</span><span class="sxs-lookup"><span data-stu-id="8c50b-103"><span id="vspixengine.iframeeventscallback"></span>IFrameEventsCallback interface</span></span>

<span data-ttu-id="8c50b-104">Rappel pour retourner la liste des événements dans un frame.</span><span class="sxs-lookup"><span data-stu-id="8c50b-104">Callback to return the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="8c50b-105">Membres</span><span class="sxs-lookup"><span data-stu-id="8c50b-105">Members</span></span>

<span data-ttu-id="8c50b-106">L’interface **IFrameEventsCallback** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8c50b-106">The **IFrameEventsCallback** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8c50b-107">**IFrameEventsCallback** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8c50b-107">**IFrameEventsCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="8c50b-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8c50b-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="8c50b-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="8c50b-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="8c50b-110">L’interface **IFrameEventsCallback** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8c50b-110">The **IFrameEventsCallback** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="8c50b-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="8c50b-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="8c50b-112">Description</span><span class="sxs-lookup"><span data-stu-id="8c50b-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="8c50b-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span><span class="sxs-lookup"><span data-stu-id="8c50b-113"><a href="/windows/desktop/direct3dtools/iframeeventscallback-getsupportedeventcolumns-dword-eventcolumnid-arr-bstr-arr"><strong>GetSupportedEventColumns</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8c50b-114">Obtient des informations sur les colonnes (types de données d’événement) prises en charge par la liste d’événements.</span><span class="sxs-lookup"><span data-stu-id="8c50b-114">Gets information about which columns (types of event data) are supported by the event list.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="8c50b-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span><span class="sxs-lookup"><span data-stu-id="8c50b-115"><a href="/windows/desktop/direct3dtools/iframeeventscallback-resultcallback-dword-dword-dword-dword-variant-arr"><strong>ResultCallback</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="8c50b-116">Fonction de rappel utilisée pour informer l’hôte d’informations sur les événements dans la liste des événements.</span><span class="sxs-lookup"><span data-stu-id="8c50b-116">A callback function used to notify the host of information about events in the event list.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="8c50b-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8c50b-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="8c50b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="8c50b-118">Header</span></span></p></td><td><span data-ttu-id="8c50b-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="8c50b-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
