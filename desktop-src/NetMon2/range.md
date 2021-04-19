---
description: La structure RANGE définit une plage de valeurs de propriété valides.
ms.assetid: 7bd14410-f5c1-487b-8776-405567991e5a
title: Structure de plage (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RANGE
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: bf465636f315e60e43350bb370e2002b8a96e635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524614"
---
# <a name="range-structure"></a><span data-ttu-id="3ec26-103">Structure de plage</span><span class="sxs-lookup"><span data-stu-id="3ec26-103">RANGE structure</span></span>

<span data-ttu-id="3ec26-104">La structure **Range** définit une plage de valeurs de propriété valides.</span><span class="sxs-lookup"><span data-stu-id="3ec26-104">The **RANGE** structure defines a range of valid property values.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ec26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3ec26-105">Syntax</span></span>


```C++
typedef struct range {
  DWORD MinValue;
  DWORD MaxValue;
} RANGE, *LPRANGE;
```



## <a name="members"></a><span data-ttu-id="3ec26-106">Membres</span><span class="sxs-lookup"><span data-stu-id="3ec26-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="3ec26-107">**MinValue**</span><span class="sxs-lookup"><span data-stu-id="3ec26-107">**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="3ec26-108">Valeur la plus basse possible dans une plage.</span><span class="sxs-lookup"><span data-stu-id="3ec26-108">Lowest possible value in a range.</span></span>

</dd> <dt>

<span data-ttu-id="3ec26-109">**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="3ec26-109">**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="3ec26-110">Valeur la plus élevée possible dans une plage.</span><span class="sxs-lookup"><span data-stu-id="3ec26-110">Highest possible value in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3ec26-111">Notes</span><span class="sxs-lookup"><span data-stu-id="3ec26-111">Remarks</span></span>

<span data-ttu-id="3ec26-112">La structure **Range** est utilisée pour spécifier une plage de nombres valide pour une propriété de protocole.</span><span class="sxs-lookup"><span data-stu-id="3ec26-112">The **RANGE** structure is used to specify a valid range of numbers for a protocol property.</span></span> <span data-ttu-id="3ec26-113">Si le membre **DataQualifier** de la structure **PropertyInfo** a la valeur **prop \_ Qualys \_ Range**, le membre **lpRange** de la structure [PropertyInfo](propertyinfo.md) doit fournir un pointeur vers une structure **Range** .</span><span class="sxs-lookup"><span data-stu-id="3ec26-113">If the **DataQualifier** member of the **PROPERTYINFO** structure is set to **PROP\_QUAL\_RANGE**, the **lpRange** member of the [PROPERTYINFO](propertyinfo.md) structure must provide a pointer to a **RANGE** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ec26-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3ec26-114">Requirements</span></span>



| <span data-ttu-id="3ec26-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3ec26-115">Requirement</span></span> | <span data-ttu-id="3ec26-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ec26-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ec26-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec26-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3ec26-118">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec26-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3ec26-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3ec26-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3ec26-120">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3ec26-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3ec26-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="3ec26-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ec26-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ec26-122"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ec26-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3ec26-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ec26-124">PROPERTYINFO</span><span class="sxs-lookup"><span data-stu-id="3ec26-124">PROPERTYINFO</span></span>](propertyinfo.md)
</dt> </dl>

 

 




