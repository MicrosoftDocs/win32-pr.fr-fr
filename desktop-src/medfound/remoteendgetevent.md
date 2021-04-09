---
description: 'Version accessible à distance de la méthode IMFMediaEventGenerator :: EndGetEvent.'
ms.assetid: 5b793760-546c-43d4-8251-d89d8d7152ad
title: RemoteEndGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3c4a5fe87dddf5fc1d256d61d8c863c2f1d9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753884"
---
# <a name="remoteendgetevent"></a><span data-ttu-id="5e5da-103">RemoteEndGetEvent</span><span class="sxs-lookup"><span data-stu-id="5e5da-103">RemoteEndGetEvent</span></span>

<span data-ttu-id="5e5da-104">Version accessible à distance de la méthode [**IMFMediaEventGenerator :: EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) .</span><span class="sxs-lookup"><span data-stu-id="5e5da-104">Remotable version of the [**IMFMediaEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) method.</span></span>

``` syntax
[call_as(EndGetEvent)]
HRESULT RemoteEndGetEvent(
    IUnknown *pResult,
    DWORD *pcbEvent,
    BYTE **ppbEvent
);
```

## <a name="remarks"></a><span data-ttu-id="5e5da-105">Notes</span><span class="sxs-lookup"><span data-stu-id="5e5da-105">Remarks</span></span>

<span data-ttu-id="5e5da-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="5e5da-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="5e5da-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="5e5da-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="5e5da-108">Si [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="5e5da-108">If [**EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5da-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e5da-109">Requirements</span></span>



| <span data-ttu-id="5e5da-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e5da-110">Requirement</span></span> | <span data-ttu-id="5e5da-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e5da-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5da-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e5da-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5da-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e5da-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="5e5da-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5e5da-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5da-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="5e5da-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="5e5da-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e5da-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e5da-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5da-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="5e5da-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5e5da-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e5da-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e5da-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="5e5da-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e5da-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e5da-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="5e5da-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




