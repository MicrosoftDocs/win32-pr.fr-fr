---
title: Constantes TS_SD_ (Textstor. h)
description: Les \_ \_ constantes TS SD \ décrivent les États de documents dynamiques utilisés par une application au moment de l’exécution.
ms.assetid: fb673e42-bee7-484e-872a-d709d5ca12f2
topic_type:
- apiref
api_name:
- TS_SD_READONLY
- TS_SD_LOADING
- TS_SD_MASKALL
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 565bc97b9fa2d1474f1ba36cd8137e63125541e5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512791"
---
# <a name="ts_sd_-constants"></a><span data-ttu-id="bf723-103">\_ \_ \* Constantes TS DP</span><span class="sxs-lookup"><span data-stu-id="bf723-103">TS\_SD\_\* Constants</span></span>

<span data-ttu-id="bf723-104">Les \_ \_ \* constantes TS SD décrivent les États de documents dynamiques utilisés par une application au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="bf723-104">The TS\_SD\_\* constants describe dynamic document states used by an application at runtime.</span></span>



| <span data-ttu-id="bf723-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="bf723-105">Constant/value</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="bf723-106">Description</span><span class="sxs-lookup"><span data-stu-id="bf723-106">Description</span></span>                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span id="TS_SD_READONLY"></span><span id="ts_sd_readonly"></span><dl> <span data-ttu-id="bf723-107"><dt>**TS \_ SD \_ ReadOnly**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bf723-107"><dt>**TS\_SD\_READONLY**</dt> <dt>( 0x1 )</dt></span></span> </dl>                              | <span data-ttu-id="bf723-108">Le document est en lecture seule et ne peut pas être modifié.</span><span class="sxs-lookup"><span data-stu-id="bf723-108">The document is read-only and cannot be modified.</span></span><br/> |
| <span id="TS_SD_LOADING"></span><span id="ts_sd_loading"></span><dl> <span data-ttu-id="bf723-109"><dt>**TS \_ \_Chargement SD**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="bf723-109"><dt>**TS\_SD\_LOADING**</dt> <dt>( 0x2 )</dt></span></span> </dl>                                 | <span data-ttu-id="bf723-110">Le document est en cours de chargement et peut être incomplet.</span><span class="sxs-lookup"><span data-stu-id="bf723-110">The document is loading and might be incomplete.</span></span><br/>  |
| <span id="TS_SD_MASKALL"></span><span id="ts_sd_maskall"></span><dl> <span data-ttu-id="bf723-111"><dt>**TS \_ SD \_ MASKALL**</dt> (chargement SD TS en <dt> \_ \_ lecture seule TS \| \_ \_ )</dt></span><span class="sxs-lookup"><span data-stu-id="bf723-111"><dt>**TS\_SD\_MASKALL**</dt> <dt>( TS\_SD\_READONLY \| TS\_SD\_LOADING )</dt></span></span> </dl> | <span data-ttu-id="bf723-112">Le document est à la fois en lecture seule et en cours de chargement.</span><span class="sxs-lookup"><span data-stu-id="bf723-112">The document is both read-only and loading.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="bf723-113">Notes</span><span class="sxs-lookup"><span data-stu-id="bf723-113">Remarks</span></span>

<span data-ttu-id="bf723-114">Le membre **dwDynamicFlags** de la structure d' [ \_ État TS](/windows/desktop/api/Textstor/ns-textstor-ts_status) utilise ces constantes.</span><span class="sxs-lookup"><span data-stu-id="bf723-114">The **dwDynamicFlags** member of the [TS\_STATUS](/windows/desktop/api/Textstor/ns-textstor-ts_status) structure uses these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf723-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf723-115">Requirements</span></span>



| <span data-ttu-id="bf723-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf723-116">Requirement</span></span> | <span data-ttu-id="bf723-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf723-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf723-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf723-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bf723-119">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf723-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bf723-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf723-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bf723-121">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf723-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bf723-122">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bf723-122">Redistributable</span></span><br/>          | <span data-ttu-id="bf723-123">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="bf723-123">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="bf723-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf723-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf723-125"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf723-125"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf723-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="bf723-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf723-127"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf723-127"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf723-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf723-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf723-129">\_statut TS</span><span class="sxs-lookup"><span data-stu-id="bf723-129">TS\_STATUS</span></span>](/windows/desktop/api/Textstor/ns-textstor-ts_status)
</dt> <dt>

[<span data-ttu-id="bf723-130">\_ \_ \* Constantes TF SD</span><span class="sxs-lookup"><span data-stu-id="bf723-130">TF\_SD\_\* Constants</span></span>](tf-sd--constants.md)
</dt> </dl>

 

 





