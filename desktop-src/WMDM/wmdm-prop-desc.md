---
title: Structure WMDM_PROP_DESC
description: La \_ structure WMDM prop \_ desc décrit les valeurs valides d’une propriété dans une configuration de propriété particulière.
ms.assetid: e4766e1e-6c1b-4a2d-ad2e-c07035ca2be2
keywords:
- Structure de WMDM_PROP_DESC Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_PROP_DESC
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98f6ea406a3d48d0ed65098d66721fcadbb98411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533316"
---
# <a name="wmdm_prop_desc-structure"></a><span data-ttu-id="7491e-104">WMDM \_ prop \_ desc (structure)</span><span class="sxs-lookup"><span data-stu-id="7491e-104">WMDM\_PROP\_DESC structure</span></span>

<span data-ttu-id="7491e-105">La structure **WMDM \_ prop \_ desc** décrit les valeurs valides d’une propriété dans une configuration de propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="7491e-105">The **WMDM\_PROP\_DESC** structure describes valid values of a property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="7491e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7491e-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_DESC {
  LPWSTR                           pwszPropName;
  WMDM_ENUM_PROP_VALID_VALUES_FORM ValidValuesForm;
  union  {
    WMDM_PROP_VALUES_RANGE ValidValuesRange;
    WMDM_PROP_VALUES_ENUM  EnumeratedValidValues;
  } ValidValues;
} WMDM_PROP_DESC;
```



## <a name="members"></a><span data-ttu-id="7491e-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7491e-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7491e-108">**pwszPropName**</span><span class="sxs-lookup"><span data-stu-id="7491e-108">**pwszPropName**</span></span>
</dt> <dd>

<span data-ttu-id="7491e-109">Nom de la propriété.</span><span class="sxs-lookup"><span data-stu-id="7491e-109">Name of the property.</span></span> <span data-ttu-id="7491e-110">L’application doit libérer cette mémoire une fois qu’elle a fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="7491e-110">The application must free this memory when it is done using it.</span></span>

</dd> <dt>

<span data-ttu-id="7491e-111">**ValidValuesForm**</span><span class="sxs-lookup"><span data-stu-id="7491e-111">**ValidValuesForm**</span></span>
</dt> <dd>

<span data-ttu-id="7491e-112">Une valeur d’énumération de [**\_ \_ \_ valeurs valides \_ \_ de WMDM enum prop**](wmdm-enum-prop-valid-values-form.md) décrivant le type de valeurs, par exemple une plage ou une liste.</span><span class="sxs-lookup"><span data-stu-id="7491e-112">An [**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**](wmdm-enum-prop-valid-values-form.md) enumeration value describing the type of values, such as a range or list.</span></span> <span data-ttu-id="7491e-113">La valeur de cette énumération détermine la variable membre qui est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7491e-113">The value of this enumeration determines which member variable is used.</span></span>

</dd> <dt>

<span data-ttu-id="7491e-114">**ValidValues**</span><span class="sxs-lookup"><span data-stu-id="7491e-114">**ValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="7491e-115">Contient les valeurs valides de la propriété dans une configuration de propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="7491e-115">Holds the valid values of the property in a particular property configuration.</span></span> <span data-ttu-id="7491e-116">Ce membre contient l’un des trois éléments suivants : la valeur d’énumération WMDM \_ enum \_ prop \_ valeurs valides \_ \_ any ; le membre **ValidValuesRange**; ou le membre **EnumeratedValidValues**.</span><span class="sxs-lookup"><span data-stu-id="7491e-116">This member holds one of three items: the enumeration value WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY; the member **ValidValuesRange**; or the member **EnumeratedValidValues**.</span></span> <span data-ttu-id="7491e-117">La valeur ou le membre est indiqué par **ValidValuesForm**.</span><span class="sxs-lookup"><span data-stu-id="7491e-117">The value or member is indicated by **ValidValuesForm**.</span></span>

<dl> <dt>

<span data-ttu-id="7491e-118">**ValidValuesRange**</span><span class="sxs-lookup"><span data-stu-id="7491e-118">**ValidValuesRange**</span></span>
</dt> <dd>

<span data-ttu-id="7491e-119">Structure de la [**\_ plage de \_ valeurs \_ WMDM prop**](wmdm-prop-values-range.md) contenant une plage de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="7491e-119">A [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure containing a range of valid values.</span></span> <span data-ttu-id="7491e-120">Cela est présent uniquement lorsque **ValidValuesForm** est défini sur WMDM \_ enum \_ prop \_ valeurs valides \_ \_ Range.</span><span class="sxs-lookup"><span data-stu-id="7491e-120">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE.</span></span> <span data-ttu-id="7491e-121">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7491e-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="7491e-122">**EnumeratedValidValues**</span><span class="sxs-lookup"><span data-stu-id="7491e-122">**EnumeratedValidValues**</span></span>
</dt> <dd>

<span data-ttu-id="7491e-123">Structure [**d' \_ \_ \_ énumération de valeurs WMDM prop**](wmdm-prop-values-enum.md) contenant un ensemble énuméré de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="7491e-123">A [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure containing an enumerated set of valid values.</span></span> <span data-ttu-id="7491e-124">Cela est présent uniquement lorsque **ValidValuesForm** est défini sur WMDM \_ enum \_ prop \_ valeurs valides \_ \_ enum.</span><span class="sxs-lookup"><span data-stu-id="7491e-124">This is present only when **ValidValuesForm** is set to WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM.</span></span> <span data-ttu-id="7491e-125">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="7491e-125">See Remarks.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7491e-126">Notes</span><span class="sxs-lookup"><span data-stu-id="7491e-126">Remarks</span></span>

<span data-ttu-id="7491e-127">La structure **WMDM \_ prop \_ desc** contient une description de propriété qui se compose d’un nom de propriété et de ses valeurs valides dans une configuration particulière.</span><span class="sxs-lookup"><span data-stu-id="7491e-127">The **WMDM\_PROP\_DESC** structure contains a property description that consists of a property name and its valid values in a particular configuration.</span></span>

<span data-ttu-id="7491e-128">L’appelant est tenu de libérer la mémoire utilisée par **ValidValuesRange** ou **EnumeratedValues**.</span><span class="sxs-lookup"><span data-stu-id="7491e-128">The caller is required to free the memory used by **ValidValuesRange** or **EnumeratedValues**.</span></span> <span data-ttu-id="7491e-129">Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="7491e-129">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7491e-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7491e-130">Requirements</span></span>



| <span data-ttu-id="7491e-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7491e-131">Requirement</span></span> | <span data-ttu-id="7491e-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="7491e-132">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7491e-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="7491e-133">Header</span></span><br/> | <dl> <span data-ttu-id="7491e-134"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7491e-134"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7491e-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7491e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7491e-136">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="7491e-136">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="7491e-137">**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="7491e-137">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="7491e-138">**\_fonction de format WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="7491e-138">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="7491e-139">**configuration de WMDM \_ prop \_**</span><span class="sxs-lookup"><span data-stu-id="7491e-139">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="7491e-140">**\_ \_ énumération des valeurs prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="7491e-140">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="7491e-141">**plage de valeurs de WMDM \_ prop \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7491e-141">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="7491e-142">**Structures**</span><span class="sxs-lookup"><span data-stu-id="7491e-142">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





