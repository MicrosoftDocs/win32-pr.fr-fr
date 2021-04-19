---
description: 'Version accessible à distance de la méthode IMFContentProtectionManager :: BeginEnableContent.'
ms.assetid: d06f752f-3f9a-4c7c-9c49-c886a675fe3a
title: RemoteBeginEnableContent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a9bc4a445ec07a7e9678a9d0a193311554f855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518364"
---
# <a name="remotebeginenablecontent"></a><span data-ttu-id="4463a-103">RemoteBeginEnableContent</span><span class="sxs-lookup"><span data-stu-id="4463a-103">RemoteBeginEnableContent</span></span>

<span data-ttu-id="4463a-104">Version accessible à distance de la méthode [**IMFContentProtectionManager :: BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) .</span><span class="sxs-lookup"><span data-stu-id="4463a-104">Remotable version of the [**IMFContentProtectionManager::BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) method.</span></span>

``` syntax
[call_as(BeginEnableContent)]
HRESULT RemoteBeginEnableContent(
    REFCLSID clsidType,
    BYTE *pbData,
    DWORD cbData,
    IMFRemoteAsyncCallback *pCallback
);
```

## <a name="remarks"></a><span data-ttu-id="4463a-105">Notes</span><span class="sxs-lookup"><span data-stu-id="4463a-105">Remarks</span></span>

<span data-ttu-id="4463a-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4463a-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="4463a-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="4463a-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="4463a-108">Si [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="4463a-108">If [**BeginEnableContent**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentprotectionmanager-beginenablecontent) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="4463a-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4463a-109">Requirements</span></span>



| <span data-ttu-id="4463a-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4463a-110">Requirement</span></span> | <span data-ttu-id="4463a-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4463a-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4463a-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4463a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4463a-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4463a-113">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="4463a-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4463a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4463a-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4463a-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="4463a-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4463a-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4463a-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4463a-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="4463a-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4463a-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="4463a-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4463a-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4463a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4463a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4463a-121">**IMFContentProtectionManager**</span><span class="sxs-lookup"><span data-stu-id="4463a-121">**IMFContentProtectionManager**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager)
</dt> </dl>

 

 




