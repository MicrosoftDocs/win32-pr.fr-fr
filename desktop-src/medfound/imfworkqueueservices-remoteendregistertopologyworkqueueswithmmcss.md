---
description: 'Version accessible à distance de la méthode IMFWorkQueueServices :: EndRegisterTopologyWorkQueuesWithMMCSS.'
ms.assetid: 94dce412-6a72-4ddf-86a3-5176ee1eb6d2
title: RemoteEndRegisterTopologyWorkQueuesWithMMCSS (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3333becfcd7a3c5e2621b628b6435b96af017cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530246"
---
# <a name="remoteendregistertopologyworkqueueswithmmcss"></a><span data-ttu-id="ae21f-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span><span class="sxs-lookup"><span data-stu-id="ae21f-103">RemoteEndRegisterTopologyWorkQueuesWithMMCSS</span></span>

<span data-ttu-id="ae21f-104">Version accessible à distance de la méthode [**IMFWorkQueueServices :: EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) .</span><span class="sxs-lookup"><span data-stu-id="ae21f-104">Remotable version of the [**IMFWorkQueueServices::EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) method.</span></span>

``` syntax
[call_as(EndRegisterTopologyWorkQueuesWithMMCSS)]
HRESULT RemoteEndRegisterTopologyWorkQueuesWithMMCSS(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="ae21f-105">Notes</span><span class="sxs-lookup"><span data-stu-id="ae21f-105">Remarks</span></span>

<span data-ttu-id="ae21f-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ae21f-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="ae21f-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="ae21f-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="ae21f-108">Si [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="ae21f-108">If [**EndRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-endregistertopologyworkqueueswithmmcss) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae21f-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae21f-109">Requirements</span></span>



| <span data-ttu-id="ae21f-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae21f-110">Requirement</span></span> | <span data-ttu-id="ae21f-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae21f-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae21f-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae21f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="ae21f-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae21f-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ae21f-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ae21f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="ae21f-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ae21f-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ae21f-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae21f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="ae21f-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae21f-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="ae21f-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae21f-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="ae21f-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae21f-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ae21f-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae21f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae21f-121">**IMFWorkQueueServices**</span><span class="sxs-lookup"><span data-stu-id="ae21f-121">**IMFWorkQueueServices**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices)
</dt> </dl>

 

 




