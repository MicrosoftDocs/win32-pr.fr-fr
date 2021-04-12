---
description: Demande de données de pile des appels.
MS-HAID: vspixengine.ICallStackRequest
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Interface ICallStackRequest
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 08976720-C403-4609-BDB4-6250CA6EBC9C
api_name:
- ICallStackRequest
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbbcd1a7874cbab5c9914eee36a37b991c7f6b06
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109270"
---
# <a name="span-idvspixengineicallstackrequestspanicallstackrequest-interface"></a><span data-ttu-id="6248d-103"><span id="vspixengine.icallstackrequest"></span>Interface ICallStackRequest</span><span class="sxs-lookup"><span data-stu-id="6248d-103"><span id="vspixengine.icallstackrequest"></span>ICallStackRequest interface</span></span>

<span data-ttu-id="6248d-104">Demande de données de pile des appels.</span><span class="sxs-lookup"><span data-stu-id="6248d-104">Request for callstack data.</span></span>

## <a name="members"></a><span data-ttu-id="6248d-105">Membres</span><span class="sxs-lookup"><span data-stu-id="6248d-105">Members</span></span>

<span data-ttu-id="6248d-106">L’interface **ICallStackRequest** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="6248d-106">The **ICallStackRequest** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6248d-107">**ICallStackRequest** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="6248d-107">**ICallStackRequest** also has these types of members:</span></span>

-   [<span data-ttu-id="6248d-108">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6248d-108">Methods</span></span>](#methods)

### <a name="span-idmethodsspanmethods"></a><span data-ttu-id="6248d-109"><span id="methods"></span>Méthodes</span><span class="sxs-lookup"><span data-stu-id="6248d-109"><span id="methods"></span>Methods</span></span>

<span data-ttu-id="6248d-110">L’interface **ICallStackRequest** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="6248d-110">The **ICallStackRequest** interface has these methods.</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><thead><tr class="header"><th style="text-align: left;"><span data-ttu-id="6248d-111">Méthode</span><span class="sxs-lookup"><span data-stu-id="6248d-111">Method</span></span></th><th style="text-align: left;"><span data-ttu-id="6248d-112">Description</span><span class="sxs-lookup"><span data-stu-id="6248d-112">Description</span></span></th></tr></thead><tbody><tr class="odd"><td style="text-align: left;"><span data-ttu-id="6248d-113"><a href="/windows/desktop/direct3dtools/icallstackrequest-requestasync-eventid-icallstackcallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span><span class="sxs-lookup"><span data-stu-id="6248d-113"><a href="/windows/desktop/direct3dtools/icallstackrequest-requestasync-eventid-icallstackcallback-ptr-dword-dword"><strong>RequestAsync</strong></a></span></span></td><td style="text-align: left;"><p><span data-ttu-id="6248d-114">Requête asynchrone pour obtenir les adresses RVA de la pile des appels (adresses virtuelles relatives) de l’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="6248d-114">An asynchronous request to get the call stack RVAs (relative virtual addresses) of the specified event.</span></span></p></td></tr></tbody></table>

 

## <a name="requirements"></a><span data-ttu-id="6248d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6248d-115">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="6248d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6248d-116">Header</span></span></p></td><td><span data-ttu-id="6248d-117">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="6248d-117">Vspixengine.h</span></span></td></tr></tbody></table>

 

 
