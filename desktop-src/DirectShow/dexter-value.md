---
description: Identifie une propriété qui doit être définie sur une transition ou un effet, ainsi que le nombre de valeurs distinctes que la propriété suppose sur la durée de la transition ou de l’effet.
ms.assetid: 3b1c35cf-f1f7-4f2c-8d94-1aaae4116833
title: Structure DEXTER_VALUE (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DEXTER_VALUE
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 930b828e1b715cfcb53275192ed76a7df7d116ec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532667"
---
# <a name="dexter_value-structure"></a><span data-ttu-id="0d268-103">Structure de valeur DEXTERity \_</span><span class="sxs-lookup"><span data-stu-id="0d268-103">DEXTER\_VALUE structure</span></span>

> [!Note]  
> <span data-ttu-id="0d268-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="0d268-104">\[Deprecated.</span></span> <span data-ttu-id="0d268-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0d268-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="0d268-106">Identifie une propriété qui doit être définie sur une transition ou un effet, ainsi que le nombre de valeurs distinctes que la propriété suppose sur la durée de la transition ou de l’effet.</span><span class="sxs-lookup"><span data-stu-id="0d268-106">Identifies a property that is to be set on a transition or effect, along with the number of distinct values that the property assumes over the duration of the transition or effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d268-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d268-107">Syntax</span></span>


```C++
typedef struct {
  VARIANT        v;
  REFERENCE_TIME rt;
  DWORD          dwInterp;
} DEXTER_VALUE;
```



## <a name="members"></a><span data-ttu-id="0d268-108">Membres</span><span class="sxs-lookup"><span data-stu-id="0d268-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d268-109">**v**</span><span class="sxs-lookup"><span data-stu-id="0d268-109">**v**</span></span>
</dt> <dd>

<span data-ttu-id="0d268-110">Valeur de la propriété.</span><span class="sxs-lookup"><span data-stu-id="0d268-110">Value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="0d268-111">**rt**</span><span class="sxs-lookup"><span data-stu-id="0d268-111">**rt**</span></span>
</dt> <dd>

<span data-ttu-id="0d268-112">Heure à laquelle la propriété assume la valeur, par rapport au début de la transition ou de l’effet.</span><span class="sxs-lookup"><span data-stu-id="0d268-112">Time at which the property assumes the value, relative to the start of the transition or effect.</span></span>

</dd> <dt>

<span data-ttu-id="0d268-113">**dwInterp**</span><span class="sxs-lookup"><span data-stu-id="0d268-113">**dwInterp**</span></span>
</dt> <dd>

<span data-ttu-id="0d268-114">Indicateur qui spécifie la façon dont la propriété progresse de la valeur précédente à cette valeur.</span><span class="sxs-lookup"><span data-stu-id="0d268-114">Flag indicating how the property progresses from the previous value to this value.</span></span> <span data-ttu-id="0d268-115">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d268-115">Must be one of the following:</span></span>



| <span data-ttu-id="0d268-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d268-116">Value</span></span>                                                                                                                                                                           | <span data-ttu-id="0d268-117">Signification</span><span class="sxs-lookup"><span data-stu-id="0d268-117">Meaning</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="DEXTERF_JUMP"></span><span id="dexterf_jump"></span><dl> <span data-ttu-id="0d268-118"><dt>**DEXTERF \_ saut**</dt></span><span class="sxs-lookup"><span data-stu-id="0d268-118"><dt>**DEXTERF\_JUMP**</dt></span></span> </dl>                      | <span data-ttu-id="0d268-119">La propriété passe instantanément à la nouvelle valeur à l’heure spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0d268-119">The property jumps instantly to the new value at the specified time.</span></span><br/>     |
| <span id="DEXTERF_INTERPOLATE"></span><span id="dexterf_interpolate"></span><dl> <span data-ttu-id="0d268-120"><dt>**\_interpolation DEXTERF**</dt></span><span class="sxs-lookup"><span data-stu-id="0d268-120"><dt>**DEXTERF\_INTERPOLATE**</dt></span></span> </dl> | <span data-ttu-id="0d268-121">La propriété est interpolée de façon linéaire dans le temps à partir de la valeur précédente.</span><span class="sxs-lookup"><span data-stu-id="0d268-121">The property is interpolated linearly over time from the previous value.</span></span><br/> |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d268-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d268-122">Requirements</span></span>



| <span data-ttu-id="0d268-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d268-123">Requirement</span></span> | <span data-ttu-id="0d268-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d268-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d268-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d268-125">Header</span></span><br/> | <dl> <span data-ttu-id="0d268-126"><dt>Qedit. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d268-126"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d268-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0d268-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d268-128">**IPropertySetter**</span><span class="sxs-lookup"><span data-stu-id="0d268-128">**IPropertySetter**</span></span>](ipropertysetter.md)
</dt> <dt>

[<span data-ttu-id="0d268-129">**\_paramètre Dexter**</span><span class="sxs-lookup"><span data-stu-id="0d268-129">**DEXTER\_PARAM**</span></span>](dexter-param.md)
</dt> </dl>

 

 




