---
title: Énumération WMDM_ENUM_PROP_VALID_VALUES_FORM
description: Le \_ \_ \_ \_ \_ type d’énumération de formulaire des valeurs valides du prop enum WMDM décrit les formes possibles des valeurs valides pour une propriété.
ms.assetid: 49d174b4-c8a3-4c16-ad21-4b66dcf8088f
keywords:
- WMDM_ENUM_PROP_VALID_VALUES_FORM l’énumération des Gestionnaire de périphériques Windows Media
topic_type:
- apiref
api_name:
- WMDM_ENUM_PROP_VALID_VALUES_FORM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d7db971f359a9cead2aae6083a934086d42c481
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527992"
---
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a><span data-ttu-id="36f98-104">\_ \_ \_ Énumération des valeurs valides du prop WMDM \_ enum \_</span><span class="sxs-lookup"><span data-stu-id="36f98-104">WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM enumeration</span></span>

<span data-ttu-id="36f98-105">Le type d’énumération de **\_ \_ \_ \_ \_ formulaire des valeurs valides du prop enum WMDM** décrit les formes possibles des valeurs valides pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="36f98-105">The **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration type describes possible forms of valid values for a property.</span></span>

## <a name="syntax"></a><span data-ttu-id="36f98-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36f98-106">Syntax</span></span>


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a><span data-ttu-id="36f98-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="36f98-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="36f98-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ enum \_ prop \_ valeurs valides \_ \_ any**</span><span class="sxs-lookup"><span data-stu-id="36f98-108"><span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ANY**</span></span>
</dt> <dd>

<span data-ttu-id="36f98-109">Toutes les valeurs sont valides.</span><span class="sxs-lookup"><span data-stu-id="36f98-109">All values are valid.</span></span>

</dd> <dt>

<span data-ttu-id="36f98-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_plage de \_ \_ valeurs valides de \_ l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-110"><span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="36f98-111">Les valeurs valides sont exprimées sous la forme d’une plage.</span><span class="sxs-lookup"><span data-stu-id="36f98-111">Valid values are expressed as a range.</span></span> <span data-ttu-id="36f98-112">Pour plus d’informations, consultez la structure de la [**\_ plage de \_ valeurs \_ WMDM prop**](wmdm-prop-values-range.md) .</span><span class="sxs-lookup"><span data-stu-id="36f98-112">For detailed information, see the [**WMDM\_PROP\_VALUES\_RANGE**](wmdm-prop-values-range.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="36f98-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_ \_ \_ énumération des valeurs valides de \_ l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-113"><span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM**</span></span>
</dt> <dd>

<span data-ttu-id="36f98-114">Les valeurs valides sont un jeu énuméré.</span><span class="sxs-lookup"><span data-stu-id="36f98-114">Valid values are an enumerated set.</span></span> <span data-ttu-id="36f98-115">Pour plus d’informations, consultez [**WMDM \_ prop \_ values \_**](wmdm-prop-values-enum.md) , structure Enum.</span><span class="sxs-lookup"><span data-stu-id="36f98-115">For detailed information, see the [**WMDM\_PROP\_VALUES\_ENUM**](wmdm-prop-values-enum.md) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="36f98-116">Notes</span><span class="sxs-lookup"><span data-stu-id="36f98-116">Remarks</span></span>

<span data-ttu-id="36f98-117">Cette énumération est utilisée dans la structure [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) pour spécifier la forme de valeurs valides pour une propriété.</span><span class="sxs-lookup"><span data-stu-id="36f98-117">This enumeration is used in the [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structure to specify the form of valid values for a property.</span></span>

## <a name="requirements"></a><span data-ttu-id="36f98-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36f98-118">Requirements</span></span>



| <span data-ttu-id="36f98-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36f98-119">Requirement</span></span> | <span data-ttu-id="36f98-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="36f98-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="36f98-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="36f98-121">Header</span></span><br/> | <dl> <span data-ttu-id="36f98-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36f98-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36f98-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36f98-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36f98-124">**Types énumération**</span><span class="sxs-lookup"><span data-stu-id="36f98-124">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="36f98-125">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="36f98-125">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="36f98-126">**\_fonction de format WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="36f98-127">**configuration de WMDM \_ prop \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="36f98-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="36f98-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="36f98-129">**\_ \_ énumération des valeurs prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-129">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="36f98-130">**plage de valeurs de WMDM \_ prop \_ \_**</span><span class="sxs-lookup"><span data-stu-id="36f98-130">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> </dl>

 

 





