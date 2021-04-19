---
title: Structure WMDM_PROP_VALUES_ENUM
description: La \_ \_ \_ structure d’énumération de valeurs WMDM prop contient un ensemble énuméré de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.
ms.assetid: 8094f3c0-a7ed-4e63-8503-aaac3fd9c012
keywords:
- Structure de WMDM_PROP_VALUES_ENUM Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_PROP_VALUES_ENUM
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1c70088d57189dd36d360bc8910a15717d964ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520816"
---
# <a name="wmdm_prop_values_enum-structure"></a><span data-ttu-id="9f2b0-104">WMDM \_ prop \_ Values, \_ structure enum</span><span class="sxs-lookup"><span data-stu-id="9f2b0-104">WMDM\_PROP\_VALUES\_ENUM structure</span></span>

<span data-ttu-id="9f2b0-105">La structure d' **\_ \_ \_ énumération de valeurs WMDM prop** contient un ensemble énuméré de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-105">The **WMDM\_PROP\_VALUES\_ENUM** structure contains an enumerated set of valid values for a particular property in a particular property configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2b0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f2b0-106">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a><span data-ttu-id="9f2b0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="9f2b0-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="9f2b0-108">**cEnumValues**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-108">**cEnumValues**</span></span>
</dt> <dd>

<span data-ttu-id="9f2b0-109">Nombre de valeurs énumérées.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-109">Count of enumerated values.</span></span>

</dd> <dt>

<span data-ttu-id="9f2b0-110">**pValues**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-110">**pValues**</span></span>
</dt> <dd>

<span data-ttu-id="9f2b0-111">Pointeur vers un tableau de valeurs.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-111">Pointer to an array of values.</span></span> <span data-ttu-id="9f2b0-112">La taille du tableau est égale à la valeur de **cEnumValues**.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-112">The size of the array is equal to the value of **cEnumValues**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f2b0-113">Notes</span><span class="sxs-lookup"><span data-stu-id="9f2b0-113">Remarks</span></span>

<span data-ttu-id="9f2b0-114">Cette structure est utilisée dans la structure **WMDM \_ prop \_ desc** pour décrire un ensemble énuméré de valeurs valides.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-114">This structure is used in the **WMDM\_PROP\_DESC** structure to describe an enumerated set of valid values.</span></span> <span data-ttu-id="9f2b0-115">Un ensemble énuméré de valeurs valides est applicable lorsque l’énumération des \_ \_ valeurs valides de l’énumération prop WMDM \_ \_ \_ est sélectionnée dans l’énumération de **\_ formulaire WMDM enum \_ prop \_ Valid \_ values \_** .</span><span class="sxs-lookup"><span data-stu-id="9f2b0-115">An enumerated set of valid values is applicable when WMDM\_ENUM\_PROP\_VALID\_VALUES\_ENUM is selected from the **WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM** enumeration.</span></span>

<span data-ttu-id="9f2b0-116">L’appelant est tenu de libérer la mémoire utilisée par **pValues**.</span><span class="sxs-lookup"><span data-stu-id="9f2b0-116">The caller is required to free the memory used by **pValues**.</span></span> <span data-ttu-id="9f2b0-117">Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="9f2b0-117">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9f2b0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f2b0-118">Requirements</span></span>



| <span data-ttu-id="9f2b0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f2b0-119">Requirement</span></span> | <span data-ttu-id="9f2b0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f2b0-120">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2b0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f2b0-121">Header</span></span><br/> | <dl> <span data-ttu-id="9f2b0-122"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f2b0-122"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2b0-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f2b0-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2b0-124">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-124">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="9f2b0-125">**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-125">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="9f2b0-126">**\_fonction de format WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-126">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="9f2b0-127">**configuration de WMDM \_ prop \_**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-127">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="9f2b0-128">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-128">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="9f2b0-129">**plage de valeurs de WMDM \_ prop \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-129">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="9f2b0-130">**Structures**</span><span class="sxs-lookup"><span data-stu-id="9f2b0-130">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





