---
title: Structure WMDM_PROP_CONFIG
description: La \_ structure WMDM prop \_ config décrit un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge par l’appareil pour un format particulier. Cette structure contient un certain nombre de descriptions de propriété dans un tableau \_ de \_ structures WMDM prop DESC.
ms.assetid: cf116861-e31d-4561-b262-e271888afc24
keywords:
- Structure de WMDM_PROP_CONFIG Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_PROP_CONFIG
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b19314b2f012d25fa2d97b44b9dc7524f9e3355
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523461"
---
# <a name="wmdm_prop_config-structure"></a><span data-ttu-id="9684d-105">Structure de configuration de WMDM \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="9684d-105">WMDM\_PROP\_CONFIG structure</span></span>

<span data-ttu-id="9684d-106">La structure **WMDM \_ prop \_ config** décrit un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge par l’appareil pour un format particulier.</span><span class="sxs-lookup"><span data-stu-id="9684d-106">The **WMDM\_PROP\_CONFIG** structure describes a set of compatible property values across all the properties supported by the device for a particular format.</span></span> <span data-ttu-id="9684d-107">Cette structure contient un certain nombre de descriptions de propriété dans un tableau de structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) .</span><span class="sxs-lookup"><span data-stu-id="9684d-107">This structure contains a number of property descriptions in an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="9684d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9684d-108">Syntax</span></span>


```C++
typedef struct _WMDM_PROP_CONFIG {
  UINT           nPreference;
  UINT           nPropDesc;
  WMDM_PROP_DESC *pPropDesc;
} WMDM_PROP_CONFIG;
```



## <a name="members"></a><span data-ttu-id="9684d-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9684d-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="9684d-110">**nPreference**</span><span class="sxs-lookup"><span data-stu-id="9684d-110">**nPreference**</span></span>
</dt> <dd>

<span data-ttu-id="9684d-111">Niveau de préférence de l’appareil pour cette configuration.</span><span class="sxs-lookup"><span data-stu-id="9684d-111">Device's level of preference for this configuration.</span></span> <span data-ttu-id="9684d-112">La valeur la plus faible indique la configuration la plus préférée.</span><span class="sxs-lookup"><span data-stu-id="9684d-112">The lowest value indicates the most preferred configuration.</span></span>

</dd> <dt>

<span data-ttu-id="9684d-113">**nPropDesc**</span><span class="sxs-lookup"><span data-stu-id="9684d-113">**nPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="9684d-114">Nombre de descriptions de propriétés contenues dans cette configuration.</span><span class="sxs-lookup"><span data-stu-id="9684d-114">Number of property descriptions contained in this configuration.</span></span> <span data-ttu-id="9684d-115">Il existe une seule Description de propriété pour chaque propriété prise en charge pour le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="9684d-115">There is a single property description for each property supported for the specified format.</span></span>

</dd> <dt>

<span data-ttu-id="9684d-116">**pPropDesc**</span><span class="sxs-lookup"><span data-stu-id="9684d-116">**pPropDesc**</span></span>
</dt> <dd>

<span data-ttu-id="9684d-117">Pointeur vers un tableau de structures [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) contenant des descriptions de propriété.</span><span class="sxs-lookup"><span data-stu-id="9684d-117">Pointer to an array of [**WMDM\_PROP\_DESC**](wmdm-prop-desc.md) structures containing property descriptions.</span></span> <span data-ttu-id="9684d-118">La taille du tableau est égale à la valeur de **nPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="9684d-118">The size of the array is equal to the value of **nPropDesc**.</span></span> <span data-ttu-id="9684d-119">L’application doit libérer cette mémoire lorsqu’elle est terminée.</span><span class="sxs-lookup"><span data-stu-id="9684d-119">The application must free this memory when finished with it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9684d-120">Notes</span><span class="sxs-lookup"><span data-stu-id="9684d-120">Remarks</span></span>

<span data-ttu-id="9684d-121">La structure de [**\_ \_ capacité de format WMDM**](wmdm-format-capability.md) retournée par [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) pour un format particulier est constituée d’un certain nombre de configurations de propriétés.</span><span class="sxs-lookup"><span data-stu-id="9684d-121">The [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md) structure returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) for a particular format consists of a number of property configurations.</span></span> <span data-ttu-id="9684d-122">**WMDM \_ Les \_** structures de configuration prop décrivent ces configurations.</span><span class="sxs-lookup"><span data-stu-id="9684d-122">**WMDM\_PROP\_CONFIG** structures describe those configurations.</span></span>

<span data-ttu-id="9684d-123">Une configuration de propriété décrit des valeurs pour toutes les propriétés prises en charge pour un format donné.</span><span class="sxs-lookup"><span data-stu-id="9684d-123">A property configuration describes values for all the properties supported for a given format.</span></span> <span data-ttu-id="9684d-124">Les valeurs de différentes propriétés dans une configuration unique sont compatibles les unes avec les autres.</span><span class="sxs-lookup"><span data-stu-id="9684d-124">The values of different properties in a single configuration are compatible with each other.</span></span> <span data-ttu-id="9684d-125">Par exemple, pour un fichier audio, une configuration inclut des valeurs valides de taux d’échantillonnage et des valeurs valides de la vitesse de transmission, de telle sorte que toutes les combinaisons de ces taux d’échantillonnage et de bits peuvent être lues sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9684d-125">For example, for an audio file, a configuration will include valid values of sample rate and valid values of the bit rate such that all combinations of these sample and bit rates can be played on the device.</span></span>

<span data-ttu-id="9684d-126">L’appelant est tenu de libérer la mémoire utilisée par **pPropDesc**.</span><span class="sxs-lookup"><span data-stu-id="9684d-126">The caller is required to free the memory used by **pPropDesc**.</span></span> <span data-ttu-id="9684d-127">Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).</span><span class="sxs-lookup"><span data-stu-id="9684d-127">For an example of how to do this, see [**WMDM\_FORMAT\_CAPABILITY**](wmdm-format-capability.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9684d-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9684d-128">Requirements</span></span>



| <span data-ttu-id="9684d-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9684d-129">Requirement</span></span> | <span data-ttu-id="9684d-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="9684d-130">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9684d-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="9684d-131">Header</span></span><br/> | <dl> <span data-ttu-id="9684d-132"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9684d-132"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9684d-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9684d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9684d-134">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="9684d-134">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="9684d-135">**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9684d-135">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="9684d-136">**\_fonction de format WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9684d-136">**WMDM\_FORMAT\_CAPABILITY**</span></span>](wmdm-format-capability.md)
</dt> <dt>

[<span data-ttu-id="9684d-137">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="9684d-137">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="9684d-138">**\_ \_ énumération des valeurs prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="9684d-138">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="9684d-139">**plage de valeurs de WMDM \_ prop \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9684d-139">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="9684d-140">**Structures**</span><span class="sxs-lookup"><span data-stu-id="9684d-140">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





