---
description: Demande de retour de la liste des événements dans un frame.
MS-HAID: vspixengine.IFrameEventsRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface IFrameEventsRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E171A94C-012F-4296-B1EC-2E814F977565
api_name:
- IFrameEventsRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: a66c098c8808eadcf31d39d76a48b6185871aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103950082"
---
# <a name="span-idvspixengineiframeeventsrequestspaniframeeventsrequest-interface"></a><span data-ttu-id="ba502-103"><span id="vspixengine.iframeeventsrequest"></span>Interface IFrameEventsRequest</span><span class="sxs-lookup"><span data-stu-id="ba502-103"><span id="vspixengine.iframeeventsrequest"></span>IFrameEventsRequest interface</span></span>

<span data-ttu-id="ba502-104">Demande de retour de la liste des événements dans un frame.</span><span class="sxs-lookup"><span data-stu-id="ba502-104">Request for returning the list of events in a frame.</span></span>

## <a name="members"></a><span data-ttu-id="ba502-105">Membres</span><span class="sxs-lookup"><span data-stu-id="ba502-105">Members</span></span>

<span data-ttu-id="ba502-106">L’interface **IFrameEventsRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ba502-106">The **IFrameEventsRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ba502-107">**IFrameEventsRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ba502-107">**IFrameEventsRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="ba502-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba502-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="ba502-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="ba502-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="ba502-110">L’interface **IFrameEventsRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ba502-110">The **IFrameEventsRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="ba502-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="ba502-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="ba502-112">Description</span><span class="sxs-lookup"><span data-stu-id="ba502-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="ba502-113"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestasync-dword-dword-dword-arr-iframeeventscallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba502-113"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestasync-dword-dword-dword-arr-iframeeventscallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ba502-114">Demande asynchrone pour obtenir des informations spécifiées sur un frame spécifié unique.</span><span class="sxs-lookup"><span data-stu-id="ba502-114">An asynchronous request to get specified information about a single specified frame.</span></span></p></td></tr><tr class="even"><td style="text-align: left;"><span data-ttu-id="ba502-115"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestsupportedcolumnsasync-iframeeventscallback-ptr-dword"><strong>RequestSupportedColumnsAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="ba502-115"><a href="/windows/desktop/direct3dtools/iframeeventsrequest-requestsupportedcolumnsasync-iframeeventscallback-ptr-dword"><strong>RequestSupportedColumnsAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="ba502-116">Demande asynchrone pour obtenir des informations sur les colonnes (champs) prises en charge par ce type de demande d’événements de frame.</span><span class="sxs-lookup"><span data-stu-id="ba502-116">An asynchronous request to get information about what columns (fields) this frame events request type supports.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="ba502-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba502-117">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="ba502-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba502-118">Header</span></span></p></td><td><span data-ttu-id="ba502-119">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="ba502-119">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
