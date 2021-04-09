---
description: Spécifie le type d’unité contenu dans un IMFSample dans une \_ collection de ForwardedDecodeUnits MFSampleExtension.
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: Énumération MF_CUSTOM_DECODE_UNIT_TYPE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 406f6b3f6b93ced212ccf06910b69761ac0dfd9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201991"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a><span data-ttu-id="42876-103">\_ \_ \_ Énumération de type d’unité de décodage personnalisé MF \_</span><span class="sxs-lookup"><span data-stu-id="42876-103">MF\_CUSTOM\_DECODE\_UNIT\_TYPE enumeration</span></span>

<span data-ttu-id="42876-104">Spécifie le type d’unité contenu dans un [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) dans une collection de [ \_ ForwardedDecodeUnits MFSampleExtension](mfsampleextension-forwardeddecodeunits.md) .</span><span class="sxs-lookup"><span data-stu-id="42876-104">Specifies the type of unit contained in an [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) in a [MFSampleExtension\_ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) collection.</span></span>

## <a name="members"></a><span data-ttu-id="42876-105">Membres</span><span class="sxs-lookup"><span data-stu-id="42876-105">Members</span></span>



| <span data-ttu-id="42876-106">Membre</span><span class="sxs-lookup"><span data-stu-id="42876-106">Member</span></span>                    | <span data-ttu-id="42876-107">Description</span><span class="sxs-lookup"><span data-stu-id="42876-107">Description</span></span>                                                             | <span data-ttu-id="42876-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="42876-108">Value</span></span> |
|---------------------------|-------------------------------------------------------------------------|-------|
| <span data-ttu-id="42876-109">**\_unité de décodage MF \_ \_ nal**</span><span class="sxs-lookup"><span data-stu-id="42876-109">**MF\_DECODE\_UNIT\_NAL**</span></span> | <span data-ttu-id="42876-110">Le type d’unité est l’unité de la couche d’abstraction de réseau (NALU).</span><span class="sxs-lookup"><span data-stu-id="42876-110">The unit type is network abstraction layer unit (NALU).</span></span> <br/>     | <span data-ttu-id="42876-111">0</span><span class="sxs-lookup"><span data-stu-id="42876-111">0</span></span>     |
| <span data-ttu-id="42876-112">**\_SEI unité de décodage MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42876-112">**MF\_DECODE\_UNIT\_SEI**</span></span> | <span data-ttu-id="42876-113">Le type d’unité est informations supplémentaires sur l’amélioration (SEI).</span><span class="sxs-lookup"><span data-stu-id="42876-113">The unit type is Supplemental Enhancement Information (SEI).</span></span><br/> | <span data-ttu-id="42876-114">1</span><span class="sxs-lookup"><span data-stu-id="42876-114">1</span></span>     |



## <a name="remarks"></a><span data-ttu-id="42876-115">Notes</span><span class="sxs-lookup"><span data-stu-id="42876-115">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="42876-116">Spécifications</span><span class="sxs-lookup"><span data-stu-id="42876-116">Requirements</span></span>



| <span data-ttu-id="42876-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42876-117">Requirement</span></span> | <span data-ttu-id="42876-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="42876-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="42876-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42876-119">Minimum supported client</span></span><br/> | <span data-ttu-id="42876-120">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42876-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="42876-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42876-121">Minimum supported server</span></span><br/> | <span data-ttu-id="42876-122">Applications de bureau Windows Server 2016 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42876-122">Windows Server 2016 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="42876-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="42876-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="42876-124"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="42876-124"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




