---
description: 'Version accessible à distance de la méthode IMFTopologyNode :: GetInputPrefType.'
ms.assetid: b02cf739-97a9-4bb0-abb1-0da491857c50
title: RemoteGetInputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6461e804d6066b467378742ff02c8e708f5f6714
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752885"
---
# <a name="remotegetinputpreftype"></a><span data-ttu-id="fc470-103">RemoteGetInputPrefType</span><span class="sxs-lookup"><span data-stu-id="fc470-103">RemoteGetInputPrefType</span></span>

<span data-ttu-id="fc470-104">Version accessible à distance de la méthode [**IMFTopologyNode :: GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="fc470-104">Remotable version of the [**IMFTopologyNode::GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) method.</span></span>

``` syntax
[call_as(GetInputPrefType)] 
HRESULT RemoteGetInputPrefType(
    DWORD dwInputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="fc470-105">Notes</span><span class="sxs-lookup"><span data-stu-id="fc470-105">Remarks</span></span>

<span data-ttu-id="fc470-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="fc470-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="fc470-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="fc470-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="fc470-108">Si [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="fc470-108">If [**GetInputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinputpreftype) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc470-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc470-109">Requirements</span></span>



| <span data-ttu-id="fc470-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc470-110">Requirement</span></span> | <span data-ttu-id="fc470-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc470-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc470-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc470-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fc470-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc470-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="fc470-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fc470-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fc470-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fc470-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="fc470-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc470-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc470-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fc470-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="fc470-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc470-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="fc470-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc470-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="fc470-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc470-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc470-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="fc470-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




