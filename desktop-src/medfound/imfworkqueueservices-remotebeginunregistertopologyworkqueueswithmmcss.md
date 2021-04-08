---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: BeginUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1a168462-400d-46c9-a489-7b861770469f
title: RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f52f82c55d692a2e1d9160c7a619338d82956ea0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866190"
---
# <a name="remotebeginunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="6729a-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="6729a-103">RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="6729a-104">Version accessible à distance de la méthode [**IMFWorkQueueServices :: BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="6729a-104">Remotable version of the [**IMFWorkQueueServices::BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginUnregisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="6729a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="6729a-105">Remarks</span></span>

<span data-ttu-id="6729a-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="6729a-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="6729a-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="6729a-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="6729a-108">Si [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="6729a-108">If [**BeginUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="6729a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6729a-109">Requirements</span></span>



| <span data-ttu-id="6729a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6729a-110">Requirement</span></span> | <span data-ttu-id="6729a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="6729a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6729a-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6729a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6729a-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6729a-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6729a-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6729a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6729a-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6729a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6729a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="6729a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6729a-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6729a-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="6729a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6729a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="6729a-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6729a-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="6729a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6729a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6729a-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="6729a-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




