---
description: La structure PATTERNMATCH définit les éléments de modèle utilisés pour évaluer un frame.
ms.assetid: 3ad27197-92da-49e5-bb0e-daf54de6c54c
title: PATTERNMATCH, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PATTERNMATCH
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 286a331f4baeb1dde79a720385c61606835248f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952270"
---
# <a name="patternmatch-structure"></a><span data-ttu-id="a7568-103">PATTERNMATCH, structure</span><span class="sxs-lookup"><span data-stu-id="a7568-103">PATTERNMATCH structure</span></span>

<span data-ttu-id="a7568-104">La structure **PATTERNMATCH** définit les éléments de modèle utilisés pour évaluer un frame.</span><span class="sxs-lookup"><span data-stu-id="a7568-104">The **PATTERNMATCH** structure defines pattern elements used to evaluate a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7568-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7568-105">Syntax</span></span>


```C++
typedef struct _PATTERNMATCH {
  DWORD        Flags;
  BYTE         OffsetBasis;
  GENERIC_PORT Port;
  WORD         Offset;
  WORD         Length;
  BYTE         PatternToMatch[MAX_PATTERN_LENGTH];
} PATTERNMATCH, *LPPATTERNMATCH;
```



## <a name="members"></a><span data-ttu-id="a7568-106">Membres</span><span class="sxs-lookup"><span data-stu-id="a7568-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="a7568-107">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="a7568-107">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-108">Indicateurs de correspondance de modèle :</span><span class="sxs-lookup"><span data-stu-id="a7568-108">Pattern match flags:</span></span>



| <span data-ttu-id="a7568-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7568-109">Value</span></span>                                                                                                                                                                                                                                                                                           | <span data-ttu-id="a7568-110">Signification</span><span class="sxs-lookup"><span data-stu-id="a7568-110">Meaning</span></span>                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="PATTERN_MATCH_FLAGS_NOT"></span><span id="pattern_match_flags_not"></span><dl> <span data-ttu-id="a7568-111"><dt>**Modèle \_ Indicateurs de correspondance \_ \_ non**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-111"><dt>**PATTERN\_MATCH\_FLAGS\_NOT**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="a7568-112">Lorsqu’il est défini, cet indicateur conserve les trames qui n’ont pas le modèle spécifié dans l’emplacement approprié.</span><span class="sxs-lookup"><span data-stu-id="a7568-112">When set, this flag retains frames that lack the specified pattern in the proper spot.</span></span><br/> |
| <span id="PATTERN_MATCH_FLAGS_PORT_SPECIFIED"></span><span id="pattern_match_flags_port_specified"></span><dl> <span data-ttu-id="a7568-113"><dt>**Modèle \_ PORT des indicateurs de correspondance \_ \_ \_ spécifié**</dt> . <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a7568-113"><dt>**PATTERN\_MATCH\_FLAGS\_PORT\_SPECIFIED**</dt> <dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="a7568-114">Recherche une valeur de numéro de port.</span><span class="sxs-lookup"><span data-stu-id="a7568-114">Seeks a port number value.</span></span><br/>                                                             |



 

</dd> <dt>

<span data-ttu-id="a7568-115">**OffsetBasis**</span><span class="sxs-lookup"><span data-stu-id="a7568-115">**OffsetBasis**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-116">Types de décalage, qui peuvent être l’un des suivants :</span><span class="sxs-lookup"><span data-stu-id="a7568-116">Types of offset, which can be one of the following:</span></span>



| <span data-ttu-id="a7568-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7568-117">Value</span></span>                                                                                                                                                                                                                                                       | <span data-ttu-id="a7568-118">Signification</span><span class="sxs-lookup"><span data-stu-id="a7568-118">Meaning</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="OFFSET_BASIS_RELATIVE_TO_FRAME"></span><span id="offset_basis_relative_to_frame"></span><dl> <span data-ttu-id="a7568-119"><dt>**\_base \_ de décalage par rapport \_ au \_ Frame**</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-119"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_FRAME**</dt></span></span> </dl>                                         | <span data-ttu-id="a7568-120">Définit un décalage, en octets, par rapport au début du frame.</span><span class="sxs-lookup"><span data-stu-id="a7568-120">Sets an offset, in bytes, relative to start of the frame.</span></span><br/>                   |
| <span id="OFFSET_BASIS_RELATIVE_TO_EFFECTIVE_PROTOCOL"></span><span id="offset_basis_relative_to_effective_protocol"></span><dl> <span data-ttu-id="a7568-121"><dt>**DÉCALAGE \_ \_ de base par rapport \_ au \_ \_ protocole effectif**</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-121"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_EFFECTIVE\_PROTOCOL**</dt></span></span> </dl> | <span data-ttu-id="a7568-122">Définit un décalage, en octets, par rapport au début du protocole référencé.</span><span class="sxs-lookup"><span data-stu-id="a7568-122">Sets an offset, in bytes, relative to the start of the referenced protocol.</span></span><br/> |
| <span id="OFFSET_BASIS_RELATIVE_TO_IPX"></span><span id="offset_basis_relative_to_ipx"></span><dl> <span data-ttu-id="a7568-123"><dt>**\_base \_ de décalage par rapport \_ à \_ IPX**</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-123"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IPX**</dt></span></span> </dl>                                               | <span data-ttu-id="a7568-124">Définit un décalage, en octets, uniquement par rapport à IPX.</span><span class="sxs-lookup"><span data-stu-id="a7568-124">Sets an offset, in bytes, only relative to IPX.</span></span><br/>                             |
| <span id="OFFSET_BASIS_RELATIVE_TO_IP"></span><span id="offset_basis_relative_to_ip"></span><dl> <span data-ttu-id="a7568-125"><dt>**\_base \_ de décalage par rapport \_ à l' \_ adresse IP**</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-125"><dt>**OFFSET\_BASIS\_RELATIVE\_TO\_IP**</dt></span></span> </dl>                                                  | <span data-ttu-id="a7568-126">Définit un décalage, en octets, uniquement par rapport à l’adresse IP.</span><span class="sxs-lookup"><span data-stu-id="a7568-126">Sets an offset, in bytes, only relative to IP.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="a7568-127">**Port**</span><span class="sxs-lookup"><span data-stu-id="a7568-127">**Port**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-128">Valeur de port, si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="a7568-128">Port value, if specified.</span></span>

</dd> <dt>

<span data-ttu-id="a7568-129">**Offset**</span><span class="sxs-lookup"><span data-stu-id="a7568-129">**Offset**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-130">Décalage, en octets, par rapport à **OffsetBasis**.</span><span class="sxs-lookup"><span data-stu-id="a7568-130">The offset, in bytes, relative to the **OffsetBasis**.</span></span>

</dd> <dt>

<span data-ttu-id="a7568-131">**Durée**</span><span class="sxs-lookup"><span data-stu-id="a7568-131">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-132">Longueur du modèle correspondant.</span><span class="sxs-lookup"><span data-stu-id="a7568-132">Length of the matched pattern.</span></span>

</dd> <dt>

<span data-ttu-id="a7568-133">**PatternToMatch**</span><span class="sxs-lookup"><span data-stu-id="a7568-133">**PatternToMatch**</span></span>
</dt> <dd>

<span data-ttu-id="a7568-134">Modèle à faire correspondre.</span><span class="sxs-lookup"><span data-stu-id="a7568-134">Pattern to match.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a7568-135">Notes</span><span class="sxs-lookup"><span data-stu-id="a7568-135">Remarks</span></span>

<span data-ttu-id="a7568-136">Cette structure est utilisée pour construire un filtre de capture.</span><span class="sxs-lookup"><span data-stu-id="a7568-136">This structure is used to construct a capture filter.</span></span> <span data-ttu-id="a7568-137">Pour plus d’informations sur l’implémentation de cette structure, consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="a7568-137">For more information about implementing this structure, see [Capture Filters](capture-filters.md).</span></span>

<span data-ttu-id="a7568-138">Un filtre de capture peut contenir jusqu’à quatre structures **PATTERNMATCH** .</span><span class="sxs-lookup"><span data-stu-id="a7568-138">A capture filter can contain up to four **PATTERNMATCH** structures.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7568-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7568-139">Requirements</span></span>



| <span data-ttu-id="a7568-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7568-140">Requirement</span></span> | <span data-ttu-id="a7568-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7568-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a7568-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7568-142">Minimum supported client</span></span><br/> | <span data-ttu-id="a7568-143">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7568-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a7568-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7568-144">Minimum supported server</span></span><br/> | <span data-ttu-id="a7568-145">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7568-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a7568-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7568-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7568-147"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7568-147"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7568-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7568-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7568-149">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="a7568-149">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




