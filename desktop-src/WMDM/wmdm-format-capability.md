---
title: Structure WMDM_FORMAT_CAPABILITY
description: La \_ \_ structure de capacité du format WMDM décrit les fonctionnalités d’un appareil pour un format particulier.
ms.assetid: 9672173D-B11E-4DCB-BCAE-38B94FCC8B99
keywords:
- Structure de WMDM_FORMAT_CAPABILITY Windows Media Gestionnaire de périphériques
topic_type:
- apiref
api_name:
- WMDM_FORMAT_CAPABILITY
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14f8dbdd81aff63a819624cdb1c778cb9bec712b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528005"
---
# <a name="wmdm_format_capability-structure"></a><span data-ttu-id="cc041-104">Structure de la \_ capacité de format WMDM \_</span><span class="sxs-lookup"><span data-stu-id="cc041-104">WMDM\_FORMAT\_CAPABILITY structure</span></span>

<span data-ttu-id="cc041-105">La structure de **\_ \_ capacité du format WMDM** décrit les fonctionnalités d’un appareil pour un format particulier.</span><span class="sxs-lookup"><span data-stu-id="cc041-105">The **WMDM\_FORMAT\_CAPABILITY** structure describes the capabilities of a device for a particular format.</span></span> <span data-ttu-id="cc041-106">Cette structure contient un ensemble de configurations de propriétés dans un tableau de structures de configuration **WMDM \_ prop \_** .</span><span class="sxs-lookup"><span data-stu-id="cc041-106">This structure contains a set of property configurations in an array of **WMDM\_PROP\_CONFIG** structures.</span></span> <span data-ttu-id="cc041-107">Chaque configuration de propriété représente un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge pour un format donné.</span><span class="sxs-lookup"><span data-stu-id="cc041-107">Each property configuration represents a set of compatible property values across all the properties supported for a given format.</span></span> <span data-ttu-id="cc041-108">L’application peut récupérer cette structure en appelant la méthode **IWMDMDevice3 :: GetFormatCapability** et en passant le code de format.</span><span class="sxs-lookup"><span data-stu-id="cc041-108">The application can get this structure by calling the **IWMDMDevice3::GetFormatCapability** method and passing in the format code.</span></span> <span data-ttu-id="cc041-109">Pour obtenir la liste des codes de format, consultez [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).</span><span class="sxs-lookup"><span data-stu-id="cc041-109">For a list of format codes, see [**WMDM\_FORMATCODE**](wmdm-formatcode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cc041-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc041-110">Syntax</span></span>


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a><span data-ttu-id="cc041-111">Membres</span><span class="sxs-lookup"><span data-stu-id="cc041-111">Members</span></span>

<dl> <dt>

<span data-ttu-id="cc041-112">**nPropConfig**</span><span class="sxs-lookup"><span data-stu-id="cc041-112">**nPropConfig**</span></span>
</dt> <dd>

<span data-ttu-id="cc041-113">Nombre de configurations de propriétés dans le tableau **pConfigs** .</span><span class="sxs-lookup"><span data-stu-id="cc041-113">Number of property configurations in the **pConfigs** array.</span></span>

</dd> <dt>

<span data-ttu-id="cc041-114">**pConfigs**</span><span class="sxs-lookup"><span data-stu-id="cc041-114">**pConfigs**</span></span>
</dt> <dd>

<span data-ttu-id="cc041-115">Pointeur vers un tableau de structures de [**\_ \_ configuration prop WMDM**](wmdm-prop-config.md) .</span><span class="sxs-lookup"><span data-stu-id="cc041-115">Pointer to an array of [**WMDM\_PROP\_CONFIG**](wmdm-prop-config.md) structures.</span></span> <span data-ttu-id="cc041-116">La taille du tableau est égale à la valeur de **nPropConfig**.</span><span class="sxs-lookup"><span data-stu-id="cc041-116">The size of array is equal to the value of **nPropConfig**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc041-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cc041-117">Remarks</span></span>

<span data-ttu-id="cc041-118">La structure de **\_ \_ capacité de format WMDM** fournit un mécanisme flexible pour exprimer les fonctionnalités de l’appareil pour un format particulier.</span><span class="sxs-lookup"><span data-stu-id="cc041-118">The **WMDM\_FORMAT\_CAPABILITY** structure provides a flexible mechanism to express the capabilities of the device for a particular format.</span></span>

<span data-ttu-id="cc041-119">Si le contenu est destiné à être rendu par l’appareil (par exemple, un fichier audio à lire par le périphérique), les propriétés du contenu doivent correspondre à l’une des configurations de propriété retournées par [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) dans la structure de **\_ \_ capacité du format WMDM** .</span><span class="sxs-lookup"><span data-stu-id="cc041-119">If the content is meant to be rendered by the device (for example, an audio file to be played by the device), the properties of the content must match one of the property configurations returned by [**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) in the **WMDM\_FORMAT\_CAPABILITY** structure.</span></span> <span data-ttu-id="cc041-120">Par exemple, pour un fichier audio, la vitesse de transmission et la fréquence d’échantillonnage doivent correspondre à l’une des configurations de propriété retournées.</span><span class="sxs-lookup"><span data-stu-id="cc041-120">For example, for an audio file, the bit rate and sample rate must satisfy one of the property configurations returned.</span></span>

<span data-ttu-id="cc041-121">L’appelant est responsable de la libération de la mémoire allouée pour cette structure.</span><span class="sxs-lookup"><span data-stu-id="cc041-121">The caller is responsible for freeing the memory allocated for this structure.</span></span> <span data-ttu-id="cc041-122">La fonction suivante montre comment effacer une structure **de \_ \_ capacité de format WMDM** .</span><span class="sxs-lookup"><span data-stu-id="cc041-122">The following function demonstrates how to clear a **WMDM\_FORMAT\_CAPABILITY** structure.</span></span>


```C++
void FreeFormatCapability(WMDM_FORMAT_CAPABILITY formatCap)
{
    // Loop through all configurations.
    for (UINT i=0; i < formatCap.nPropConfig; i++) 
    {
        // Loop through all descriptions of a configuration and delete
        // the values particular to that description type.
        for (UINT j=0; j < formatCap.pConfigs[i].nPropDesc; j++) 
        {
            switch (formatCap.pConfigs[i].pPropDesc[j].ValidValuesForm)
            {
                case WMDM_ENUM_PROP_VALID_VALUES_ENUM:
                    for (UINT k=0; k < formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.cEnumValues; k++)
                    {
                        PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues[k]));
                    }
                    CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].ValidValues.EnumeratedValidValues.pValues);
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_RANGE:
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMin));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeMax));
                    PropVariantClear (&(formatCap.pConfigs[i].pPropDesc[j].ValidValues.ValidValuesRange.rangeStep));
                    break;
                case WMDM_ENUM_PROP_VALID_VALUES_ANY:
                    // No dynamically allocated memory for this value.
                default:
                    break;
            }

            // Free the memory for the description name.
            CoTaskMemFree(formatCap.pConfigs[i].pPropDesc[j].pwszPropName);
        }
        // Free the memory holding the array of description items for this configuration.
        CoTaskMemFree(formatCap.pConfigs[i].pPropDesc);
    }

    // Free the memory pointing to the array of configurations.
    CoTaskMemFree(formatCap.pConfigs);
    formatCap.nPropConfig = 0;
}
```



## <a name="requirements"></a><span data-ttu-id="cc041-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc041-123">Requirements</span></span>



| <span data-ttu-id="cc041-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc041-124">Requirement</span></span> | <span data-ttu-id="cc041-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc041-125">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cc041-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="cc041-126">Header</span></span><br/> | <dl> <span data-ttu-id="cc041-127"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cc041-127"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc041-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc041-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc041-129">**IWMDMDevice3::GetFormatCapability**</span><span class="sxs-lookup"><span data-stu-id="cc041-129">**IWMDMDevice3::GetFormatCapability**</span></span>](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[<span data-ttu-id="cc041-130">**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="cc041-130">**WMDM\_ENUM\_PROP\_VALID\_VALUES\_FORM**</span></span>](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[<span data-ttu-id="cc041-131">**configuration de WMDM \_ prop \_**</span><span class="sxs-lookup"><span data-stu-id="cc041-131">**WMDM\_PROP\_CONFIG**</span></span>](wmdm-prop-config.md)
</dt> <dt>

[<span data-ttu-id="cc041-132">**WMDM \_ prop \_ desc**</span><span class="sxs-lookup"><span data-stu-id="cc041-132">**WMDM\_PROP\_DESC**</span></span>](wmdm-prop-desc.md)
</dt> <dt>

[<span data-ttu-id="cc041-133">**\_ \_ énumération des valeurs prop WMDM \_**</span><span class="sxs-lookup"><span data-stu-id="cc041-133">**WMDM\_PROP\_VALUES\_ENUM**</span></span>](wmdm-prop-values-enum.md)
</dt> <dt>

[<span data-ttu-id="cc041-134">**plage de valeurs de WMDM \_ prop \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cc041-134">**WMDM\_PROP\_VALUES\_RANGE**</span></span>](wmdm-prop-values-range.md)
</dt> <dt>

[<span data-ttu-id="cc041-135">**Structures**</span><span class="sxs-lookup"><span data-stu-id="cc041-135">**Structures**</span></span>](structures.md)
</dt> </dl>

 

 





