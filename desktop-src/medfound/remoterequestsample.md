---
description: 'Version accessible à distance de la méthode IMFMediaStream :: RequestSample.'
ms.assetid: 05ed4de0-fe5c-4183-8f1d-55d5a27e436a
title: RemoteRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c8b06f0501de9cc041bf5776adb5e17e59a8c17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521451"
---
# <a name="remoterequestsample"></a><span data-ttu-id="109be-103">RemoteRequestSample</span><span class="sxs-lookup"><span data-stu-id="109be-103">RemoteRequestSample</span></span>

<span data-ttu-id="109be-104">Version accessible à distance de la méthode [**IMFMediaStream :: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="109be-104">Remotable version of the [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) method.</span></span>

``` syntax
[call_as(RequestSample)]
HRESULT RemoteRequestSample();
```

## <a name="remarks"></a><span data-ttu-id="109be-105">Notes</span><span class="sxs-lookup"><span data-stu-id="109be-105">Remarks</span></span>

<span data-ttu-id="109be-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="109be-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="109be-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="109be-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="109be-108">Si [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="109be-108">If [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="109be-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="109be-109">Requirements</span></span>



| <span data-ttu-id="109be-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="109be-110">Requirement</span></span> | <span data-ttu-id="109be-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="109be-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="109be-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="109be-112">Minimum supported client</span></span><br/> | <span data-ttu-id="109be-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="109be-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="109be-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="109be-114">Minimum supported server</span></span><br/> | <span data-ttu-id="109be-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="109be-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="109be-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="109be-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="109be-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="109be-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="109be-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="109be-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="109be-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="109be-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="109be-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="109be-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="109be-121">**IMFMediaStream**</span><span class="sxs-lookup"><span data-stu-id="109be-121">**IMFMediaStream**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)
</dt> </dl>

 

 




