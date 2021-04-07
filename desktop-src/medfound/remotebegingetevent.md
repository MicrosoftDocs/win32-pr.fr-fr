---
description: 'Version accessible à distance de la méthode IMFMediaEventGenerator :: BeginGetEvent.'
ms.assetid: 96a16fd3-10bc-4cd9-967a-ceb92e26ccc8
title: RemoteBeginGetEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d728653df99baf0e816c53d8d22d7720c9aefac9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863417"
---
# <a name="remotebegingetevent"></a><span data-ttu-id="f099c-103">RemoteBeginGetEvent</span><span class="sxs-lookup"><span data-stu-id="f099c-103">RemoteBeginGetEvent</span></span>

<span data-ttu-id="f099c-104">Version accessible à distance de la méthode [**IMFMediaEventGenerator :: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) .</span><span class="sxs-lookup"><span data-stu-id="f099c-104">Remotable version of the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method.</span></span>

``` syntax
[call_as(BeginGetEvent)]
HRESULT RemoteBeginGetEvent(
    IMFRemoteAsyncCallback* pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="f099c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="f099c-105">Remarks</span></span>

<span data-ttu-id="f099c-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="f099c-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="f099c-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="f099c-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="f099c-108">Si [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="f099c-108">If [**BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="f099c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f099c-109">Requirements</span></span>



| <span data-ttu-id="f099c-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f099c-110">Requirement</span></span> | <span data-ttu-id="f099c-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="f099c-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f099c-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f099c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f099c-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="f099c-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="f099c-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f099c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f099c-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="f099c-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="f099c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="f099c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f099c-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f099c-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="f099c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f099c-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="f099c-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f099c-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="f099c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f099c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f099c-121">**IMFMediaEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="f099c-121">**IMFMediaEventGenerator**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)
</dt> </dl>

 

 




