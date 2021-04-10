---
title: Constantes TS_IAS_ (Textstor. h)
description: Les \_ \_ constantes TS IAS \ sont utilisées comme indicateurs de champ de bits pour contrôler l’insertion de texte ou d’objets incorporés au niveau d’une sélection ou d’un point d’insertion.
ms.assetid: 58e0d13c-d90c-41d2-bd93-4eba5fe0a69a
topic_type:
- apiref
api_name:
- TS_IAS_NOQUERY
- TS_IAS_QUERYONLY
api_location:
- Textstor.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d59584295567c586ebd8db7e5f63366fd8272f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103816"
---
# <a name="ts_ias_-constants"></a><span data-ttu-id="12260-103">\_ \_ \* CONSTANTEs IAS TS</span><span class="sxs-lookup"><span data-stu-id="12260-103">TS\_IAS\_\* Constants</span></span>

<span data-ttu-id="12260-104">Les \_ constantes d’IAS TS \_ \* sont utilisées en tant qu’indicateurs de champ de champ pour contrôler l’insertion de texte ou d’objets incorporés au niveau d’une sélection ou d’un point d’insertion.</span><span class="sxs-lookup"><span data-stu-id="12260-104">The TS\_IAS\_\* constants are used as bitfield flags to control insertion of text or embedded objects at a selection or insertion point.</span></span>



| <span data-ttu-id="12260-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="12260-105">Constant/value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="12260-106">Description</span><span class="sxs-lookup"><span data-stu-id="12260-106">Description</span></span>                                                                                                                                   |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TS_IAS_NOQUERY"></span><span id="ts_ias_noquery"></span><dl> <span data-ttu-id="12260-107"><dt>**TS \_ \_NOQUERY IAS**</dt> <dt>(0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="12260-107"><dt>**TS\_IAS\_NOQUERY**</dt> <dt>( 0x1 )</dt></span></span> </dl>       | <span data-ttu-id="12260-108">Le texte est inséré et le pointeur de plage a la valeur **null** lors de la fermeture.</span><span class="sxs-lookup"><span data-stu-id="12260-108">Text is inserted and the range pointer is set to **NULL** upon exit.</span></span> <span data-ttu-id="12260-109">Ne peut pas être combiné avec l' \_ indicateur QUERYONLY de l’IAS TS \_ .</span><span class="sxs-lookup"><span data-stu-id="12260-109">Cannot be combined with the TS\_IAS\_QUERYONLY flag.</span></span><br/>          |
| <span id="TS_IAS_QUERYONLY"></span><span id="ts_ias_queryonly"></span><dl> <span data-ttu-id="12260-110"><dt>**TS \_ \_QUERYONLY IAS**</dt> <dt>(0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="12260-110"><dt>**TS\_IAS\_QUERYONLY**</dt> <dt>( 0x2 )</dt></span></span> </dl> | <span data-ttu-id="12260-111">N’effectuez pas l’insertion.</span><span class="sxs-lookup"><span data-stu-id="12260-111">Do not perform the insertion.</span></span> <span data-ttu-id="12260-112">L’appelant requiert la définition du pointeur de plage.</span><span class="sxs-lookup"><span data-stu-id="12260-112">Caller only requires the range pointer to be set.</span></span> <span data-ttu-id="12260-113">Ne peut pas être combiné avec \_ l' \_ indicateur noquery IAS TS.</span><span class="sxs-lookup"><span data-stu-id="12260-113">Cannot be combined with the TS\_IAS\_NOQUERY flag.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="12260-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="12260-114">Requirements</span></span>



| <span data-ttu-id="12260-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="12260-115">Requirement</span></span> | <span data-ttu-id="12260-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="12260-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="12260-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12260-117">Minimum supported client</span></span><br/> | <span data-ttu-id="12260-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12260-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="12260-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="12260-119">Minimum supported server</span></span><br/> | <span data-ttu-id="12260-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="12260-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="12260-121">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="12260-121">Redistributable</span></span><br/>          | <span data-ttu-id="12260-122">TSF 1,0 sur Windows 2000 professionnel</span><span class="sxs-lookup"><span data-stu-id="12260-122">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                         |
| <span data-ttu-id="12260-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="12260-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="12260-124"><dt>Textstor. h</dt></span><span class="sxs-lookup"><span data-stu-id="12260-124"><dt>Textstor.h</dt></span></span> </dl>   |
| <span data-ttu-id="12260-125">MIDL</span><span class="sxs-lookup"><span data-stu-id="12260-125">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12260-126"><dt>Textstor. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12260-126"><dt>Textstor.idl</dt></span></span> </dl> |



 

 





