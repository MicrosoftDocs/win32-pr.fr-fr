---
title: Constantes GXFPF_ (Textstor. h)
description: GXFPF \_ \ constantes spécifient la position de caractère à retourner en fonction des coordonnées d’écran du point par rapport à un cadre englobant de caractère.
ms.assetid: e69e5a4c-65e6-4d9b-8cb0-962524aa5d39
topic_type:
- apiref
api_name:
- GXFPF_ROUND_NEAREST
- GXFPF_NEAREST
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1d2dfc5ce874a7c4ce5b205c9b92436040aa60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464706"
---
# <a name="gxfpf_-constants"></a><span data-ttu-id="bd5ed-103">\_ \* CONSTANTEs GXFPF</span><span class="sxs-lookup"><span data-stu-id="bd5ed-103">GXFPF\_\* Constants</span></span>

<span data-ttu-id="bd5ed-104">Les \_ \* constantes GXFPF spécifient la position de caractère à retourner en fonction des coordonnées d’écran du point par rapport à un cadre englobant de caractère.</span><span class="sxs-lookup"><span data-stu-id="bd5ed-104">GXFPF\_\* constants specify the character position to return based on the screen coordinates of the point relative to a character bounding box.</span></span>



| <span data-ttu-id="bd5ed-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="bd5ed-105">Constant/value</span></span>                                                                                                                                                                                                                                | <span data-ttu-id="bd5ed-106">Description</span><span class="sxs-lookup"><span data-stu-id="bd5ed-106">Description</span></span>                                                                                                                                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GXFPF_ROUND_NEAREST"></span><span id="gxfpf_round_nearest"></span><dl> <span data-ttu-id="bd5ed-107"><dt>**GXFPF \_ ARRONDI \_ le plus proche**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="bd5ed-107"><dt>**GXFPF\_ROUND\_NEAREST**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="bd5ed-108">Si les coordonnées d’écran du point sont contenues dans un cadre englobant de caractère, la position de caractère retournée est le bord englobant le plus proche des coordonnées d’écran du point.</span><span class="sxs-lookup"><span data-stu-id="bd5ed-108">If the screen coordinates of the point are contained in a character bounding box, the character position returned is the bounding edge closest to the screen coordinates of the point.</span></span><br/> |
| <span id="GXFPF_NEAREST"></span><span id="gxfpf_nearest"></span><dl> <span data-ttu-id="bd5ed-109"><dt>**GXFPF \_ Le plus proche**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="bd5ed-109"><dt>**GXFPF\_NEAREST**</dt> <dt>( 0x2 )</dt></span></span> </dl>                    | <span data-ttu-id="bd5ed-110">Si les coordonnées d’écran du point ne sont pas contenues dans un cadre englobant de caractère, la position de caractère la plus proche est retournée.</span><span class="sxs-lookup"><span data-stu-id="bd5ed-110">If the screen coordinates of the point are not contained in a character bounding box, the closest character position is returned.</span></span><br/>                                                      |



## <a name="remarks"></a><span data-ttu-id="bd5ed-111">Notes</span><span class="sxs-lookup"><span data-stu-id="bd5ed-111">Remarks</span></span>

<span data-ttu-id="bd5ed-112">Les paramètres *dwFlags* des méthodes [ITextStoreACP :: GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) et [ITfContextOwner :: GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) utilisent ces constantes.</span><span class="sxs-lookup"><span data-stu-id="bd5ed-112">The *dwflags* parameters of the [ITextStoreACP::GetACPFromPoint](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint) and [ITfContextOwner::GetACPFromPoint](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint) methods use these constants.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd5ed-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bd5ed-113">Requirements</span></span>



| <span data-ttu-id="bd5ed-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bd5ed-114">Requirement</span></span> | <span data-ttu-id="bd5ed-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bd5ed-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd5ed-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5ed-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bd5ed-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5ed-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="bd5ed-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bd5ed-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bd5ed-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bd5ed-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="bd5ed-120">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="bd5ed-120">Redistributable</span></span><br/>          | <span data-ttu-id="bd5ed-121">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="bd5ed-121">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="bd5ed-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="bd5ed-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd5ed-123"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="bd5ed-123"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="bd5ed-124">MIDL</span><span class="sxs-lookup"><span data-stu-id="bd5ed-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd5ed-125"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd5ed-125"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd5ed-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bd5ed-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd5ed-127">ITextStoreACP :: GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="bd5ed-127">ITextStoreACP::GetACPFromPoint</span></span>](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getacpfrompoint)
</dt> <dt>

[<span data-ttu-id="bd5ed-128">ITfContextOwner::GetACPFromPoint</span><span class="sxs-lookup"><span data-stu-id="bd5ed-128">ITfContextOwner::GetACPFromPoint</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcontextowner-getacpfrompoint)
</dt> </dl>

 

 





