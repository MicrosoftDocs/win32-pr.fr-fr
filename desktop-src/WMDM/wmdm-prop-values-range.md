---
title: Structure WMDM_PROP_VALUES_RANGE
description: La \_ \_ \_ structure de la plage de valeurs WMDM prop décrit une plage de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.
ms.assetid: fb823a66-cc9c-4632-a4f0-03c7255c3ccb
keywords:
- Structure de WMDM_PROP_VALUES_RANGE Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_RANGE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba82a1067db97e93fff2845e69e89f978548b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523899"
---
# <a name="wmdm_prop_values_range-structure"></a><span data-ttu-id="df25d-104">Structure de la plage de valeurs WMDM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="df25d-104">WMDM\_PROP\_VALUES\_RANGE structure</span></span>

<span data-ttu-id="df25d-105">La structure de la **\_ plage de \_ valeurs \_ WMDM prop** décrit une plage de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="df25d-105">The **WMDM\_PROP\_VALUES\_RANGE** structure describes a range of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="df25d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df25d-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a><span data-ttu-id="df25d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="df25d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="df25d-108">**rangeMin**</span><span class="sxs-lookup"><span data-stu-id="df25d-108">**rangeMin**</span></span>
</dt> <dd>

<span data-ttu-id="df25d-109">Valeur minimale de la plage.</span><span class="sxs-lookup"><span data-stu-id="df25d-109">Minimum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="df25d-110">**rangeMax**</span><span class="sxs-lookup"><span data-stu-id="df25d-110">**rangeMax**</span></span>
</dt> <dd>

<span data-ttu-id="df25d-111">Valeur maximale de la plage.</span><span class="sxs-lookup"><span data-stu-id="df25d-111">Maximum value in the range.</span></span>

</dd> <dt>

<span data-ttu-id="df25d-112">**rangeStep**</span><span class="sxs-lookup"><span data-stu-id="df25d-112">**rangeStep**</span></span>
</dt> <dd>

<span data-ttu-id="df25d-113">Taille de l’étape dans laquelle les valeurs valides sont incrémentées de la valeur minimale à la valeur maximale.</span><span class="sxs-lookup"><span data-stu-id="df25d-113">The step size in which valid values increment from the minimum value to the maximum value.</span></span> <span data-ttu-id="df25d-114">Cela permet de spécifier des valeurs autorisées discrètes dans une plage.</span><span class="sxs-lookup"><span data-stu-id="df25d-114">This permits specifying discrete permissible values in a range.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="df25d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="df25d-115">Remarks</span></span>

<span data-ttu-id="df25d-116">Cette structure est utilisée dans la structure [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) pour décrire une plage de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="df25d-116">This structure is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to describe a range of valid values.</span></span> <span data-ttu-id="df25d-117">Une plage de valeurs valides est applicable lorsque \_ l’énumération \_ \_ des valeurs valides de l’énumération prop WMDM \_ \_ est sélectionnée dans l’énumération de [**\_ formulaire WMDM enum \_ prop \_ Valid \_ values \_**](wmdm-enum-prop-valid-values-form.md) .</span><span class="sxs-lookup"><span data-stu-id="df25d-117">A range of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="df25d-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="df25d-118">Requirements</span></span>



| <span data-ttu-id="df25d-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="df25d-119">Requirement</span></span> | <span data-ttu-id="df25d-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="df25d-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="df25d-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="df25d-121">Header</span></span><br/> | <dl> <span data-ttu-id="df25d-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="df25d-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df25d-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="df25d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df25d-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="df25d-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="df25d-125">**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="df25d-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="df25d-126">**\_fonction de format WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="df25d-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="df25d-127">**configuration de WMDM \_ prop \_**</span><span class="sxs-lookup"><span data-stu-id="df25d-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="df25d-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="df25d-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="df25d-129">**\_ \_ énumération des valeurs prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="df25d-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="df25d-130">**Structures**</span><span class="sxs-lookup"><span data-stu-id="df25d-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





