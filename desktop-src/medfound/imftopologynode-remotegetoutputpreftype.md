---
description: 'Version accessible à distance de la méthode IMFTopologyNode :: GetOutputPrefType.'
ms.assetid: 56fbbf14-0c55-4f98-bcda-7f434cff803c
title: RemoteGetOutputPrefType (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46069add8f9d15a2b3742a083a1cf169a46b969f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518565"
---
# <a name="remotegetoutputpreftype"></a><span data-ttu-id="3ce7c-103">RemoteGetOutputPrefType</span><span class="sxs-lookup"><span data-stu-id="3ce7c-103">RemoteGetOutputPrefType</span></span>

<span data-ttu-id="3ce7c-104">Version accessible à distance de la méthode [**IMFTopologyNode :: GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) .</span><span class="sxs-lookup"><span data-stu-id="3ce7c-104">Remotable version of the [**IMFTopologyNode::GetOutputPrefType**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getoutputpreftype) method.</span></span>

``` syntax
[call_as(GetOutputPrefType)] 
HRESULT RemoteGetOutputPrefType(
    DWORD dwOutputIndex,
    DWORD *pcbData,
    BYTE **ppbData
);
```

## <a name="remarks"></a><span data-ttu-id="3ce7c-105">Notes</span><span class="sxs-lookup"><span data-stu-id="3ce7c-105">Remarks</span></span>

<span data-ttu-id="3ce7c-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="3ce7c-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="3ce7c-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="3ce7c-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="3ce7c-108">Si **GetOutputPrefType** est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="3ce7c-108">If **GetOutputPrefType** is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ce7c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ce7c-109">Requirements</span></span>



| <span data-ttu-id="3ce7c-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ce7c-110">Requirement</span></span> | <span data-ttu-id="3ce7c-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ce7c-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce7c-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ce7c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3ce7c-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ce7c-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3ce7c-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ce7c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3ce7c-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ce7c-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3ce7c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ce7c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ce7c-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3ce7c-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="3ce7c-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="3ce7c-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="3ce7c-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ce7c-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="3ce7c-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ce7c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ce7c-121">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="3ce7c-121">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




