---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: EndUnregisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 8767a145-07b9-4427-9446-cee25e9074fa
title: RemoteEndUnregisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd1131fcd920e306bc6d5f2954c283d41d61310f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524294"
---
# <a name="remoteendunregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="a39ff-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="a39ff-103">RemoteEndUnregisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="a39ff-104">Version accessible à distance de la méthode [**IMFWorkQueueServices :: EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="a39ff-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndUnregisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="a39ff-105">Notes</span><span class="sxs-lookup"><span data-stu-id="a39ff-105">Remarks</span></span>

<span data-ttu-id="a39ff-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="a39ff-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="a39ff-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="a39ff-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="a39ff-108">Si [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="a39ff-108">If [**EndUnregisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="a39ff-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a39ff-109">Requirements</span></span>



| <span data-ttu-id="a39ff-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a39ff-110">Requirement</span></span> | <span data-ttu-id="a39ff-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="a39ff-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a39ff-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a39ff-112">Minimum supported client</span></span><br/> | <span data-ttu-id="a39ff-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a39ff-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="a39ff-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a39ff-114">Minimum supported server</span></span><br/> | <span data-ttu-id="a39ff-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a39ff-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a39ff-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="a39ff-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="a39ff-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a39ff-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="a39ff-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a39ff-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="a39ff-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a39ff-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="a39ff-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a39ff-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a39ff-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="a39ff-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




