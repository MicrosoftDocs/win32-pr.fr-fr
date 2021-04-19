---
description: Contient un groupe de tableaux ANDEXP évalués comme homologues.
ms.assetid: 14fa568c-9535-4415-923d-7e93ba4d2e80
title: Structure d’EXPRESSION (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPRESSION
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b6565c294c0d8e0a7a277769404cb8b1b206380e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513356"
---
# <a name="expression-structure"></a><span data-ttu-id="b03a5-103">Structure de l’EXPRESSION</span><span class="sxs-lookup"><span data-stu-id="b03a5-103">EXPRESSION structure</span></span>

<span data-ttu-id="b03a5-104">La structure d' **expression** contient un groupe de tableaux **ANDEXP** évalués comme pairs dans des expressions and logiques, qui ont le format</span><span class="sxs-lookup"><span data-stu-id="b03a5-104">The **EXPRESSION** structure contains a group of **ANDEXP** arrays evaluated as peers in logical AND expressions, which have the format</span></span>

<span data-ttu-id="b03a5-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span><span class="sxs-lookup"><span data-stu-id="b03a5-105">(ANDEXP 1 && ANDEXP 2 && ANDEXP 3).</span></span>

## <a name="syntax"></a><span data-ttu-id="b03a5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b03a5-106">Syntax</span></span>


```C++
typedef struct _EXPRESSION {
  DWORD  nAndExps;
  ANDEXP AndExp[MAX_PATTERNS];
} EXPRESSION, *LPEXPRESSION;
```



## <a name="members"></a><span data-ttu-id="b03a5-107">Membres</span><span class="sxs-lookup"><span data-stu-id="b03a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b03a5-108">**nAndExps**</span><span class="sxs-lookup"><span data-stu-id="b03a5-108">**nAndExps**</span></span>
</dt> <dd>

<span data-ttu-id="b03a5-109">Nombre de modèles **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="b03a5-109">Number of **ANDEXP** patterns.</span></span>

</dd> <dt>

<span data-ttu-id="b03a5-110">**AndExp**</span><span class="sxs-lookup"><span data-stu-id="b03a5-110">**AndExp**</span></span>
</dt> <dd>

<span data-ttu-id="b03a5-111">Tableau de modèles **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="b03a5-111">Array of **ANDEXP** patterns.</span></span> <span data-ttu-id="b03a5-112">Le filtre de capture réorganise toutes les lignes de ce tableau en instructions AND logiques.</span><span class="sxs-lookup"><span data-stu-id="b03a5-112">The capture filter arranges all rows of this array as logical AND statements.</span></span> <span data-ttu-id="b03a5-113">N’oubliez pas que chaque structure d’EXPRESSION peut contenir un maximum de quatre modèles **ANDEXP** .</span><span class="sxs-lookup"><span data-stu-id="b03a5-113">Be aware that each EXPRESSION structure can contain a maximum of four **ANDEXP** patterns.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b03a5-114">Notes</span><span class="sxs-lookup"><span data-stu-id="b03a5-114">Remarks</span></span>

<span data-ttu-id="b03a5-115">Pour plus d’informations sur l’implémentation de cette structure dans le cadre d’un filtre de capture, consultez [filtres de capture](capture-filters.md).</span><span class="sxs-lookup"><span data-stu-id="b03a5-115">For more information about implementing this structure as part of a capture filter, see [Capture Filters](capture-filters.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b03a5-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b03a5-116">Requirements</span></span>



| <span data-ttu-id="b03a5-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b03a5-117">Requirement</span></span> | <span data-ttu-id="b03a5-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="b03a5-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b03a5-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b03a5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b03a5-120">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b03a5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b03a5-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b03a5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b03a5-122">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b03a5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b03a5-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="b03a5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b03a5-124"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b03a5-124"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b03a5-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b03a5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b03a5-126">ANDEXP</span><span class="sxs-lookup"><span data-stu-id="b03a5-126">ANDEXP</span></span>](andexp.md)
</dt> <dt>

[<span data-ttu-id="b03a5-127">CAPTUREFILTER</span><span class="sxs-lookup"><span data-stu-id="b03a5-127">CAPTUREFILTER</span></span>](capturefilter.md)
</dt> </dl>

 

 




