---
description: 'Version accessible à distance de la méthode IMFSourceResolver :: EndCreateObjectFromByteStream.'
ms.assetid: 6e4e9ace-e18a-45df-b20c-28e352fcdee7
title: RemoteEndCreateObjectFromByteStream (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba53b7d22ed79cb97edba034dc4c61d9aa27fa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114034"
---
# <a name="remoteendcreateobjectfrombytestream"></a><span data-ttu-id="33abf-103">RemoteEndCreateObjectFromByteStream</span><span class="sxs-lookup"><span data-stu-id="33abf-103">RemoteEndCreateObjectFromByteStream</span></span>

<span data-ttu-id="33abf-104">Version accessible à distance de la méthode [**IMFSourceResolver :: EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) .</span><span class="sxs-lookup"><span data-stu-id="33abf-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromByteStream)]
HRESULT RemoteEndCreateObjectFromByteStream(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="33abf-105">Notes</span><span class="sxs-lookup"><span data-stu-id="33abf-105">Remarks</span></span>

<span data-ttu-id="33abf-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="33abf-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="33abf-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="33abf-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="33abf-108">Si [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="33abf-108">If [**EndCreateObjectFromByteStream**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfrombytestream) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="33abf-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33abf-109">Requirements</span></span>



| <span data-ttu-id="33abf-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33abf-110">Requirement</span></span> | <span data-ttu-id="33abf-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="33abf-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33abf-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33abf-112">Minimum supported client</span></span><br/> | <span data-ttu-id="33abf-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="33abf-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="33abf-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="33abf-114">Minimum supported server</span></span><br/> | <span data-ttu-id="33abf-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="33abf-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="33abf-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="33abf-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="33abf-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33abf-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="33abf-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="33abf-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="33abf-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33abf-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="33abf-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33abf-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33abf-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="33abf-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




