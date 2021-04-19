---
description: 'Version accessible à distance de la méthode IMFSourceResolver :: BeginCreateObjectFromByteStream.'
ms.assetid: 960b5c51-b9b1-4956-a270-abfb7eedd482
title: RemoteBeginCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2cf089f0b80e83373c36731de4bd9a36d8835b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106538862"
---
# <a name="remotebegincreateobjectfrombytestream"></a><span data-ttu-id="01f0b-103">RemoteBeginCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="01f0b-103">RemoteBeginCreateObjectFromByteStream</span></span>

<span data-ttu-id="01f0b-104">Version accessible à distance de la méthode [**IMFSourceResolver :: BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="01f0b-104">Remotable version of the [**IMFSourceResolver::BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(BeginCreateObjectFromByteStream)]
HRESULT RemoteBeginCreateObjectFromByteStream(
    IMFByteStream* pByteStream,
    LPCWSTR pwszURL,
    IPropertyStore *pProps,
    DWORD dwFlags,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="01f0b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="01f0b-105">Remarks</span></span>

<span data-ttu-id="01f0b-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="01f0b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="01f0b-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="01f0b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="01f0b-108">Si [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="01f0b-108">If [**BeginCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-begincreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="01f0b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="01f0b-109">Requirements</span></span>



| <span data-ttu-id="01f0b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="01f0b-110">Requirement</span></span> | <span data-ttu-id="01f0b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="01f0b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01f0b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f0b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="01f0b-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="01f0b-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="01f0b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="01f0b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="01f0b-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="01f0b-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="01f0b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="01f0b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="01f0b-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="01f0b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="01f0b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="01f0b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="01f0b-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="01f0b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="01f0b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01f0b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01f0b-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="01f0b-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




