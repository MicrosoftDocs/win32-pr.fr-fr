---
title: Constantes TS_LF_ (Textstor. h)
description: Les \_ \_ constantes TS LF \ spécifient le type de verrou de document.
ms.assetid: f0bb6ef9-a8fc-4331-9210-6c5ba1721a73
topic_type:
- apiref
api_name:
- TS_LF_SYNC
- TS_LF_READ
- TS_LF_READWRITE
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6240511fd95e91a7f22477f631178dfab528f1e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106509696"
---
# <a name="ts_lf_-constants"></a><span data-ttu-id="5f9bf-103">\_ \_ \* Constantes TS LF</span><span class="sxs-lookup"><span data-stu-id="5f9bf-103">TS\_LF\_\* Constants</span></span>

<span data-ttu-id="5f9bf-104">Les \_ \_ \* constantes TS LF spécifient le type de verrou de document.</span><span class="sxs-lookup"><span data-stu-id="5f9bf-104">The TS\_LF\_\* constants specify the type of document lock.</span></span>



| <span data-ttu-id="5f9bf-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="5f9bf-105">Constant/value</span></span>                                                                                                                                                                                                                    | <span data-ttu-id="5f9bf-106">Description</span><span class="sxs-lookup"><span data-stu-id="5f9bf-106">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span id="TS_LF_SYNC"></span><span id="ts_lf_sync"></span><dl> <span data-ttu-id="5f9bf-107"><dt>**TS \_ \_Synchronisation LF**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5f9bf-107"><dt>**TS\_LF\_SYNC**</dt> <dt>( 0x1 )</dt></span></span> </dl>                | <span data-ttu-id="5f9bf-108">Le document a un verrou synchrone si cet indicateur est combiné avec d’autres indicateurs.</span><span class="sxs-lookup"><span data-stu-id="5f9bf-108">The document has a synchronous-lock if this flag is combined with other flags.</span></span><br/> |
| <span id="TS_LF_READ"></span><span id="ts_lf_read"></span><dl> <span data-ttu-id="5f9bf-109"><dt>**TS \_ \_Lecture LF**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="5f9bf-109"><dt>**TS\_LF\_READ**</dt> <dt>( 0x2 )</dt></span></span> </dl>                | <span data-ttu-id="5f9bf-110">Le document a un verrou en lecture seule et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="5f9bf-110">The document has a read-only lock and cannot be modified.</span></span><br/>                      |
| <span id="TS_LF_READWRITE"></span><span id="ts_lf_readwrite"></span><dl> <span data-ttu-id="5f9bf-111"><dt>**TS \_ LF \_ ReadWrite**</dt> <dt>(0x6)</dt></span><span class="sxs-lookup"><span data-stu-id="5f9bf-111"><dt>**TS\_LF\_READWRITE**</dt> <dt>( 0x6 )</dt></span></span> </dl> | <span data-ttu-id="5f9bf-112">Le document a un verrou en lecture/écriture et peut être modifié.</span><span class="sxs-lookup"><span data-stu-id="5f9bf-112">The document has a read/write lock and can be modified.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="5f9bf-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5f9bf-113">Requirements</span></span>



| <span data-ttu-id="5f9bf-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5f9bf-114">Requirement</span></span> | <span data-ttu-id="5f9bf-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="5f9bf-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f9bf-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f9bf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5f9bf-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f9bf-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5f9bf-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5f9bf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5f9bf-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5f9bf-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5f9bf-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="5f9bf-120">Redistributable</span></span><br/>          | <span data-ttu-id="5f9bf-121">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="5f9bf-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="5f9bf-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="5f9bf-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5f9bf-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="5f9bf-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="5f9bf-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="5f9bf-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5f9bf-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5f9bf-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f9bf-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f9bf-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f9bf-127">Verrous de document</span><span class="sxs-lookup"><span data-stu-id="5f9bf-127">Document Locks</span></span>](document-locks.md)
</dt> <dt>

[<span data-ttu-id="5f9bf-128">ITextStoreACP :: RequestLock</span><span class="sxs-lookup"><span data-stu-id="5f9bf-128">ITextStoreACP::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-requestlock)
</dt> <dt>

[<span data-ttu-id="5f9bf-129">ITextStoreACPSink :: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="5f9bf-129">ITextStoreACPSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacpsink-onlockgranted)
</dt> <dt>

[<span data-ttu-id="5f9bf-130">ITextStoreAnchor :: RequestLock</span><span class="sxs-lookup"><span data-stu-id="5f9bf-130">ITextStoreAnchor::RequestLock</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-requestlock)
</dt> <dt>

[<span data-ttu-id="5f9bf-131">ITextStoreAnchorSink :: OnLockGranted</span><span class="sxs-lookup"><span data-stu-id="5f9bf-131">ITextStoreAnchorSink::OnLockGranted</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchorsink-onlockgranted)
</dt> </dl>

 

 





