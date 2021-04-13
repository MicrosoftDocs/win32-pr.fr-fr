---
title: Constantes TS_SHIFT_ (Textstor. h)
description: Les \_ \_ constantes TS Shift \ sont utilisées par l’interface IAnchor pour la manipulation du texte masqué et du comptage des caractères.
ms.assetid: 93329238-f6e8-432e-9167-550a02b33b46
topic_type:
- apiref
api_name:
- TS_SHIFT_COUNT_HIDDEN
- TS_SHIFT_HALT_HIDDEN
- TS_SHIFT_HALT_VISIBLE
- TS_SHIFT_COUNT_ONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f3a11463aea1633079d771bf6a8b333475865e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384695"
---
# <a name="ts_shift_-constants"></a><span data-ttu-id="a161a-103">\_Constantes de décalage TS \_ \*</span><span class="sxs-lookup"><span data-stu-id="a161a-103">TS\_SHIFT\_\* Constants</span></span>

<span data-ttu-id="a161a-104">Les \_ \_ \* constantes de décalage TS sont utilisées par l’interface **IAnchor** pour la manipulation du texte masqué et du comptage de caractères.</span><span class="sxs-lookup"><span data-stu-id="a161a-104">The TS\_Shift\_\* constants are used by the **IAnchor** interface for manipulation of hidden text and character counting.</span></span>



| <span data-ttu-id="a161a-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="a161a-105">Constant/value</span></span>                                                                                                                                                                                                                                       | <span data-ttu-id="a161a-106">Description</span><span class="sxs-lookup"><span data-stu-id="a161a-106">Description</span></span>                                                                                                                                                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_SHIFT_COUNT_HIDDEN"></span><span id="ts_shift_count_hidden"></span><dl> <span data-ttu-id="a161a-107"><dt>**TS \_ Nombre de DÉCALAGEs \_ \_ masqué**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-107"><dt>**TS\_SHIFT\_COUNT\_HIDDEN**</dt> <dt>( 0x1 )</dt></span></span> </dl> | <span data-ttu-id="a161a-108">Spécifie que l’ancre sera déplacée vers la limite de région suivante, y compris la limite d’une zone de texte masqué.</span><span class="sxs-lookup"><span data-stu-id="a161a-108">Specifies that the anchor will be shifted to the next region boundary, including the boundary of a hidden text region.</span></span> <span data-ttu-id="a161a-109">S’il n’est pas défini, le point d’ancrage est déplacé au-delà du texte masqué adjacent jusqu’à ce qu’une région de texte visible soit trouvée.</span><span class="sxs-lookup"><span data-stu-id="a161a-109">If not set, the anchor will be shifted past any adjacent hidden text until a region of visible text is found.</span></span><br/> |
| <span id="TS_SHIFT_HALT_HIDDEN"></span><span id="ts_shift_halt_hidden"></span><dl> <span data-ttu-id="a161a-110"><dt>**TS \_ Arrêt du décalage \_ \_ masqué**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-110"><dt>**TS\_SHIFT\_HALT\_HIDDEN**</dt> <dt>( 0x2 )</dt></span></span> </dl>    | <span data-ttu-id="a161a-111">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a161a-111">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_HALT_VISIBLE"></span><span id="ts_shift_halt_visible"></span><dl> <span data-ttu-id="a161a-112"><dt>**TS \_ Arrêt du décalage \_ \_ visible**</dt> <dt>(0x4)</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-112"><dt>**TS\_SHIFT\_HALT\_VISIBLE**</dt> <dt>( 0x4 )</dt></span></span> </dl> | <span data-ttu-id="a161a-113">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="a161a-113">Not used.</span></span><br/>                                                                                                                                                                                                                            |
| <span id="TS_SHIFT_COUNT_ONLY"></span><span id="ts_shift_count_only"></span><dl> <span data-ttu-id="a161a-114"><dt>**TS \_ Nombre de DÉCALAGEs \_ \_ uniquement**</dt> <dt>(0x8)</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-114"><dt>**TS\_SHIFT\_COUNT\_ONLY**</dt> <dt>( 0x8 )</dt></span></span> </dl>       | <span data-ttu-id="a161a-115">Le point d’ancrage n’est pas décalé.</span><span class="sxs-lookup"><span data-stu-id="a161a-115">The anchor is not shifted.</span></span><br/>                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="a161a-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a161a-116">Requirements</span></span>



| <span data-ttu-id="a161a-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a161a-117">Requirement</span></span> | <span data-ttu-id="a161a-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="a161a-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a161a-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a161a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a161a-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a161a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="a161a-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a161a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a161a-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a161a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a161a-123">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="a161a-123">Redistributable</span></span><br/>          | <span data-ttu-id="a161a-124">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="a161a-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="a161a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="a161a-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a161a-126"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-126"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="a161a-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="a161a-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a161a-128"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a161a-128"><dt>Textstor.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a161a-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a161a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a161a-130">IAnchor::ShiftRegion</span><span class="sxs-lookup"><span data-stu-id="a161a-130">IAnchor::ShiftRegion</span></span>](/windows/desktop/api/Textstor/nf-textstor-ianchor-shiftregion)
</dt> </dl>

 

 





