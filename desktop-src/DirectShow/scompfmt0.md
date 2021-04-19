---
description: Contient des informations de format pour la recompression intelligente.
ms.assetid: 471a7b4a-e639-443b-a30e-870b747e072c
title: SCompFmt0, structure (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SCompFmt0
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: ad5a5277718e8d414d64a86b9c31739cf576736a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532247"
---
# <a name="scompfmt0-structure"></a><span data-ttu-id="7b92d-103">SCompFmt0, structure</span><span class="sxs-lookup"><span data-stu-id="7b92d-103">SCompFmt0 structure</span></span>

> [!Note]  
> <span data-ttu-id="7b92d-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7b92d-104">\[Deprecated.</span></span> <span data-ttu-id="7b92d-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="7b92d-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="7b92d-106">Contient des informations de format pour la recompression intelligente.</span><span class="sxs-lookup"><span data-stu-id="7b92d-106">Contains format information for smart recompression.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b92d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b92d-107">Syntax</span></span>


```C++
typedef struct _SCompFmt0 {
  long          nFormatId;
  AM_MEDIA_TYPE MediaType;
} SCompFmt0;
```



## <a name="members"></a><span data-ttu-id="7b92d-108">Membres</span><span class="sxs-lookup"><span data-stu-id="7b92d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b92d-109">**nFormatId**</span><span class="sxs-lookup"><span data-stu-id="7b92d-109">**nFormatId**</span></span>
</dt> <dd>

<span data-ttu-id="7b92d-110">Réservé doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="7b92d-110">Reserved; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b92d-111">**MediaType**</span><span class="sxs-lookup"><span data-stu-id="7b92d-111">**MediaType**</span></span>
</dt> <dd>

<span data-ttu-id="7b92d-112">[**Am \_ Structure du \_ type de média**](/windows/win32/api/strmif/ns-strmif-am_media_type) qui décrit le format de compression.</span><span class="sxs-lookup"><span data-stu-id="7b92d-112">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that describes the compression format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b92d-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b92d-113">Requirements</span></span>



| <span data-ttu-id="7b92d-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b92d-114">Requirement</span></span> | <span data-ttu-id="7b92d-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b92d-115">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b92d-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b92d-116">Header</span></span><br/> | <dl> <span data-ttu-id="7b92d-117"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b92d-117"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b92d-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b92d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b92d-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="7b92d-119">**IAMTimelineGroup::GetSmartRecompressFormat**</span></span>](iamtimelinegroup-getsmartrecompressformat.md)
</dt> <dt>

[<span data-ttu-id="7b92d-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span><span class="sxs-lookup"><span data-stu-id="7b92d-120">**IAMTimelineGroup::SetSmartRecompressFormat**</span></span>](iamtimelinegroup-setsmartrecompressformat.md)
</dt> </dl>

 

 




