---
description: 'Version accessible à distance de la méthode IMFMediaSource :: CreatePresentationDescriptor.'
ms.assetid: 9ad6793e-32ca-471b-8639-41098b3e8216
title: RemoteCreatePresentationDescriptor (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c02d78c1febe8c1a82ae3e91c50e06c750bcfef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114366"
---
# <a name="remotecreatepresentationdescriptor"></a><span data-ttu-id="4d0d9-103">RemoteCreatePresentationDescriptor</span><span class="sxs-lookup"><span data-stu-id="4d0d9-103">RemoteCreatePresentationDescriptor</span></span>

<span data-ttu-id="4d0d9-104">Version accessible à distance de la méthode [**IMFMediaSource :: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) .</span><span class="sxs-lookup"><span data-stu-id="4d0d9-104">Remotable version of the [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) method.</span></span>

``` syntax
[call_as(CreatePresentationDescriptor)]
HRESULT RemoteCreatePresentationDescriptor(
    DWORD *pcbPD,
    BYTE **pbPD,
    IMFPresentationDescriptor **ppRemotePD
);
```

## <a name="remarks"></a><span data-ttu-id="4d0d9-105">Notes</span><span class="sxs-lookup"><span data-stu-id="4d0d9-105">Remarks</span></span>

<span data-ttu-id="4d0d9-106">Les applications ne peuvent pas appeler cette méthode directement, et les objets n’implémentent pas cette méthode.</span><span class="sxs-lookup"><span data-stu-id="4d0d9-106">Applications cannot call this method directly, and objects do not implement this method.</span></span> <span data-ttu-id="4d0d9-107">La méthode n’apparaît pas dans le vtable pour l’interface.</span><span class="sxs-lookup"><span data-stu-id="4d0d9-107">The method does not appear in the vtable for the interface.</span></span> <span data-ttu-id="4d0d9-108">Si [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) est appelé à travers les limites de processus, la dll de proxy/stub de Media Foundation traduit l’appel en appel à la méthode distante, puis la traduit en retour.</span><span class="sxs-lookup"><span data-stu-id="4d0d9-108">If [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) is called across process boundaries, the Media Foundation proxy/stub DLL translates the call into a call to the remote method and then translates it back.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d0d9-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d0d9-109">Requirements</span></span>



| <span data-ttu-id="4d0d9-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4d0d9-110">Requirement</span></span> | <span data-ttu-id="4d0d9-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d0d9-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d0d9-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d0d9-112">Minimum supported client</span></span><br/> | <span data-ttu-id="4d0d9-113">Applications de bureau Windows Vista- \[ \| applications UWP\]</span><span class="sxs-lookup"><span data-stu-id="4d0d9-113">Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                                                    |
| <span data-ttu-id="4d0d9-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4d0d9-114">Minimum supported server</span></span><br/> | <span data-ttu-id="4d0d9-115">Applications de bureau Windows Server 2008 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="4d0d9-115">Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/>                                              |
| <span data-ttu-id="4d0d9-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="4d0d9-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="4d0d9-117"><dt>Mfobjects. h (inclure Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4d0d9-117"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |
| <span data-ttu-id="4d0d9-118">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4d0d9-118">Library</span></span><br/>                  | <dl> <span data-ttu-id="4d0d9-119"><dt>Mfuuid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4d0d9-119"><dt>Mfuuid.lib</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="4d0d9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4d0d9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d0d9-121">**IMFMediaSource**</span><span class="sxs-lookup"><span data-stu-id="4d0d9-121">**IMFMediaSource**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
</dt> </dl>

 

 




