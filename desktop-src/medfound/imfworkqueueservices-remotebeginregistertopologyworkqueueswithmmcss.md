---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: BeginRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 1ea258c9-1f7f-4324-a17a-d044a4864ea4
title: RemoteBeginRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448008c29e34574263f04ebbc7dee54d60b6f4ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526241"
---
# <a name="remotebeginregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="d4f69-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="d4f69-103">RemoteBeginRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="d4f69-104">Version accessible à distance de la méthode [**IMFWorkQueueServices :: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="d4f69-104">Remotable version of the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(BeginRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteBeginRegisterTopologyWorkQueuesWithMMCSS(
    IMFRemoteAsyncCallback *pCallback
); 
```

## <a name="remarks"></a><span data-ttu-id="d4f69-105">Notes</span><span class="sxs-lookup"><span data-stu-id="d4f69-105">Remarks</span></span>

<span data-ttu-id="d4f69-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="d4f69-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="d4f69-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="d4f69-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="d4f69-108">Si [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="d4f69-108">If [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4f69-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4f69-109">Requirements</span></span>



| <span data-ttu-id="d4f69-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4f69-110">Requirement</span></span> | <span data-ttu-id="d4f69-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4f69-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4f69-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4f69-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d4f69-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4f69-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d4f69-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4f69-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d4f69-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4f69-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d4f69-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4f69-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4f69-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d4f69-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="d4f69-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d4f69-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="d4f69-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4f69-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d4f69-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4f69-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4f69-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="d4f69-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




