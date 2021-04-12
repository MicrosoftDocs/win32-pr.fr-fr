---
description: 'Version accessible à distance de IMFWorkQueueServicesEX :: BeginRegisterPlatformWorkQueueWithMMCSSEx.'
ms.assetid: 75af7ce6-9b74-4d61-b7f2-5d07538f91cf
title: RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9d519d13f1e23927f1d34a18d5c5f860e007881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210369"
---
# <a name="remotebeginregisterplatformworkqueuewithmmcssex"></a><span data-ttu-id="8ce67-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span><span class="sxs-lookup"><span data-stu-id="8ce67-103">RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx</span></span>

<span data-ttu-id="8ce67-104">Version accessible à distance de [**IMFWorkQueueServicesEX :: BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span><span class="sxs-lookup"><span data-stu-id="8ce67-104">Remotable version of [**IMFWorkQueueServicesEX::BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex).</span></span>

``` syntax
[call_as(BeginRegisterPlatformWorkQueueWithMMCSSEx)]
HRESULT RemoteBeginRegisterPlatformWorkQueueWithMMCSSEx(
    DWORD dwPlatformWorkQueue,
    LPCWSTR wszClass,
    DWORD dwTaskId, 
    LONG lPriority,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="8ce67-105">Notes</span><span class="sxs-lookup"><span data-stu-id="8ce67-105">Remarks</span></span>

<span data-ttu-id="8ce67-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="8ce67-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="8ce67-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="8ce67-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="8ce67-108">Si [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="8ce67-108">If [**BeginRegisterPlatformWorkQueueWithMMCSSEx**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservicesex-beginregisterplatformworkqueuewithmmcssex) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce67-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8ce67-109">Requirements</span></span>



| <span data-ttu-id="8ce67-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8ce67-110">Requirement</span></span> | <span data-ttu-id="8ce67-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="8ce67-111">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce67-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ce67-112">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce67-113">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ce67-113">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="8ce67-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8ce67-114">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce67-115">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8ce67-115">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="8ce67-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="8ce67-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ce67-117"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8ce67-117"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce67-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8ce67-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ce67-119">**IMFWorkQueueServicesEx**</span><span class="sxs-lookup"><span data-stu-id="8ce67-119">**IMFWorkQueueServicesEx**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservicesex)
</dt> </dl>

 

 




