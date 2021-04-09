---
title: Constantes TF_SD_ (msctf. h)
description: Les \_ \_ constantes TF SD \ décrivent l’état du document.
ms.assetid: 953d39cd-8af1-4c86-8fb8-8b8ec917c631
topic_type:
- apiref
api_name:
- TF_SD_READONLY
- TF_SD_LOADING
api_location:
- Msctf.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 12ed0d68c8a8afd9299b908eb81a04a31fbd3d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103013"
---
# <a name="tf_sd_-constants"></a><span data-ttu-id="6783d-103">\_ \_ \* Constantes TF SD</span><span class="sxs-lookup"><span data-stu-id="6783d-103">TF\_SD\_\* Constants</span></span>

<span data-ttu-id="6783d-104">Les \_ \_ \* constantes TF SD décrivent l’état du document.</span><span class="sxs-lookup"><span data-stu-id="6783d-104">The TF\_SD\_\* constants describe the document status.</span></span>



| <span data-ttu-id="6783d-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="6783d-105">Constant/value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="6783d-106">Description</span><span class="sxs-lookup"><span data-stu-id="6783d-106">Description</span></span>                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TF_SD_READONLY"></span><span id="tf_sd_readonly"></span><dl> <span data-ttu-id="6783d-107"><dt>**Tf \_ SD \_ ReadOnly**</dt> <dt>(TS \_ SD \_ ReadOnly)</dt></span><span class="sxs-lookup"><span data-stu-id="6783d-107"><dt>**TF\_SD\_READONLY**</dt> <dt>( TS\_SD\_READONLY )</dt></span></span> </dl> | <span data-ttu-id="6783d-108">Le document est en lecture seule et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="6783d-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TF_SD_LOADING"></span><span id="tf_sd_loading"></span><dl> <span data-ttu-id="6783d-109"><dt>**Tf \_ \_chargement SD**</dt> <dt>( \_ chargement SD TS \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="6783d-109"><dt>**TF\_SD\_LOADING**</dt> <dt>( TS\_SD\_LOADING )</dt></span></span> </dl>     | <span data-ttu-id="6783d-110">Le document est en cours de chargement et peut être incomplet.</span><span class="sxs-lookup"><span data-stu-id="6783d-110">The document is loading and can be incomplete.</span></span><br/>    |



## <a name="remarks"></a><span data-ttu-id="6783d-111">Notes</span><span class="sxs-lookup"><span data-stu-id="6783d-111">Remarks</span></span>

<span data-ttu-id="6783d-112">Le membre **dwDynamicFlags** de la structure d' [ \_ État TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) utilise ces constantes.</span><span class="sxs-lookup"><span data-stu-id="6783d-112">The **dwDynamicFlags** member of the [TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85)) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="6783d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6783d-113">Requirements</span></span>



| <span data-ttu-id="6783d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6783d-114">Requirement</span></span> | <span data-ttu-id="6783d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6783d-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6783d-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6783d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6783d-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6783d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6783d-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6783d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6783d-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6783d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6783d-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="6783d-120">Redistributable</span></span><br/>          | <span data-ttu-id="6783d-121">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="6783d-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="6783d-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="6783d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6783d-123"><dt>Msctf. h</dt></span><span class="sxs-lookup"><span data-stu-id="6783d-123"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="6783d-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="6783d-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6783d-125"><dt>Msctf. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6783d-125"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6783d-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6783d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6783d-127">[\_État TF](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6783d-127">[TF\_STATUS](/previous-versions/windows/desktop/legacy/ms629192(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6783d-128">\_ \_ \* Constantes TS DP</span><span class="sxs-lookup"><span data-stu-id="6783d-128">TS\_SD\_\* Constants</span></span>](ts-sd--constants.md)
</dt> <dt>

[<span data-ttu-id="6783d-129">ITfContextOwner :: GetStatus</span><span class="sxs-lookup"><span data-stu-id="6783d-129">ITfContextOwner::GetStatus</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getstatus)
</dt> <dt>

[<span data-ttu-id="6783d-130">ITfContextOwnerServices :: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="6783d-130">ITfContextOwnerServices::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextownerservices-onstatuschange)
</dt> <dt>

[<span data-ttu-id="6783d-131">ITextStoreACP :: GetStatus</span><span class="sxs-lookup"><span data-stu-id="6783d-131">ITextStoreACP::GetStatus</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getstatus)
</dt> <dt>

[<span data-ttu-id="6783d-132">ITfStatusSunk :: OnStatusChange</span><span class="sxs-lookup"><span data-stu-id="6783d-132">ITfStatusSunk::OnStatusChange</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfstatussink-onstatuschange)
</dt> </dl>

 

