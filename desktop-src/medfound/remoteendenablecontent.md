---
description: 'Version accessible à distance de la méthode IMFContentProtectionManager :: EndEnableContent.'
ms.assetid: aa7a2b3a-5982-4fd8-b5de-7439fc374dfa
title: RemoteEndEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30bab87bc39e930c08b96e1d312932f061f9dd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863414"
---
# <a name="remoteendenablecontent"></a><span data-ttu-id="37e9b-103">RemoteEndEnableContent</span><span class="sxs-lookup"><span data-stu-id="37e9b-103">RemoteEndEnableContent</span></span>

<span data-ttu-id="37e9b-104">Version accessible à distance de la méthode [**IMFContentProtectionManager :: EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="37e9b-104">Remotable version of the [**IMFContentProtectionManager::EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) method.</span></span>

``` syntax
[call_as(EndEnableContent)]
HRESULT RemoteEndEnableContent(
    IUnknown *pResult
);
```

## <a name="remarks"></a><span data-ttu-id="37e9b-105">Notes</span><span class="sxs-lookup"><span data-stu-id="37e9b-105">Remarks</span></span>

<span data-ttu-id="37e9b-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="37e9b-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="37e9b-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="37e9b-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="37e9b-108">Si [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="37e9b-108">If [**EndEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-endenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="37e9b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="37e9b-109">Requirements</span></span>



| <span data-ttu-id="37e9b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="37e9b-110">Requirement</span></span> | <span data-ttu-id="37e9b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="37e9b-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37e9b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37e9b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="37e9b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37e9b-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="37e9b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="37e9b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="37e9b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="37e9b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="37e9b-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="37e9b-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="37e9b-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37e9b-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="37e9b-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="37e9b-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="37e9b-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="37e9b-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="37e9b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37e9b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37e9b-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="37e9b-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




