---
description: 'Version accessible à distance de la méthode IMFSourceResolver :: EndCreateObjectFromURL.'
ms.assetid: 42764869-9cbc-4f41-a3af-f2d869db9f99
title: RemoteEndCreateObjectFromURL (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26fff650dca012b58dc6fd46b26f13b1c2ac3c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517551"
---
# <a name="remoteendcreateobjectfromurl"></a><span data-ttu-id="259f3-103">RemoteEndCreateObjectFromURL</span><span class="sxs-lookup"><span data-stu-id="259f3-103">RemoteEndCreateObjectFromURL</span></span>

<span data-ttu-id="259f3-104">Version accessible à distance de la méthode [**IMFSourceResolver :: EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) .</span><span class="sxs-lookup"><span data-stu-id="259f3-104">Remotable version of the [**IMFSourceResolver::EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) method.</span></span>

``` syntax
[call_as(EndCreateObjectFromURL)]
HRESULT RemoteEndCreateObjectFromURL(
    IUnknown *pResult,
    MF_OBJECT_TYPE *pObjectType,
    IUnknown **ppObject
);
```

## <a name="remarks"></a><span data-ttu-id="259f3-105">Notes</span><span class="sxs-lookup"><span data-stu-id="259f3-105">Remarks</span></span>

<span data-ttu-id="259f3-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="259f3-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="259f3-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="259f3-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="259f3-108">Si [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="259f3-108">If [**EndCreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-endcreateobjectfromurl) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="259f3-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="259f3-109">Requirements</span></span>



| <span data-ttu-id="259f3-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="259f3-110">Requirement</span></span> | <span data-ttu-id="259f3-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="259f3-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="259f3-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="259f3-112">Minimum supported client</span></span><br/> | <span data-ttu-id="259f3-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="259f3-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="259f3-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="259f3-114">Minimum supported server</span></span><br/> | <span data-ttu-id="259f3-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="259f3-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="259f3-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="259f3-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="259f3-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="259f3-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="259f3-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="259f3-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="259f3-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="259f3-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="259f3-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="259f3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="259f3-121">**IMFSourceResolver**</span><span class="sxs-lookup"><span data-stu-id="259f3-121">**IMFSourceResolver**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> </dl>

 

 




