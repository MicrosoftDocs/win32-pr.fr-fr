---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: EndUnregisterPlatformWorkQueueWithMMCSS.'
ms.assetid: 92eef511-0af0-4146-ac81-7dfa4a649016
title: RemoteEndUnregisterPlatformWorkQueueWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a03f8cdc1bfdded539c8143c3fa50c6bafb54de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868030"
---
# <a name="remoteendunregisterplatformworkqueuewithmmcss"></a><span data-ttu-id="779aa-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="779aa-103">RemoteEndUnregisterPlatformWorkQueueWithMMCSS</span></span>

<span data-ttu-id="779aa-104">Version accessible à distance de la méthode [**IMFWorkQueueServices :: EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="779aa-104">Remotable version of the [**IMFWorkQueueServices::EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) method.</span></span>

``` syntax
[call_as(EndUnregisterPlatformWorkQueueWithMMCSS)]
HRESULT RemoteEndUnregisterPlatformWorkQueueWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="779aa-105">Notes</span><span class="sxs-lookup"><span data-stu-id="779aa-105">Remarks</span></span>

<span data-ttu-id="779aa-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="779aa-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="779aa-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="779aa-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="779aa-108">Si [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="779aa-108">If [**EndUnregisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endunregisterplatformworkqueuewithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="779aa-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="779aa-109">Requirements</span></span>



| <span data-ttu-id="779aa-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="779aa-110">Requirement</span></span> | <span data-ttu-id="779aa-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="779aa-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779aa-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779aa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="779aa-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779aa-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="779aa-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="779aa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="779aa-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="779aa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="779aa-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="779aa-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="779aa-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="779aa-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="779aa-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="779aa-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="779aa-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="779aa-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="779aa-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="779aa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="779aa-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="779aa-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




