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
ms.openlocfilehash: c42c654bc07e6e47e5ead5b374f6cd16b20c2fc3e36433eb68006b1e270c1ca6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004799"
---
# <a name="wmdm_format_capability-structure"></a>Structure de la \_ capacité de format WMDM \_

La structure de **\_ \_ capacité du format WMDM** décrit les fonctionnalités d’un appareil pour un format particulier. Cette structure contient un ensemble de configurations de propriétés dans un tableau de structures de configuration **WMDM \_ prop \_** . Chaque configuration de propriété représente un ensemble de valeurs de propriété compatibles sur toutes les propriétés prises en charge pour un format donné. L’application peut récupérer cette structure en appelant la méthode **IWMDMDevice3 :: GetFormatCapability** et en passant le code de format. Pour obtenir la liste des codes de format, consultez [**WMDM \_ FORMATCODE**](wmdm-formatcode.md).

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDM_FORMAT_CAPABILITY {
  UINT              nPropConfig;
  WMDM_PROP_CONFIG  *pConfigs;
} WMDM_FORMAT_CAPABILITY;
```



## <a name="members"></a>Membres

<dl> <dt>

**nPropConfig**
</dt> <dd>

Nombre de configurations de propriétés dans le tableau **pConfigs** .

</dd> <dt>

**pConfigs**
</dt> <dd>

Pointeur vers un tableau de structures de [**\_ \_ configuration prop WMDM**](wmdm-prop-config.md) . La taille du tableau est égale à la valeur de **nPropConfig**.

</dd> </dl>

## <a name="remarks"></a>Remarques

La structure de **\_ \_ capacité de format WMDM** fournit un mécanisme flexible pour exprimer les fonctionnalités de l’appareil pour un format particulier.

Si le contenu est destiné à être rendu par l’appareil (par exemple, un fichier audio à lire par le périphérique), les propriétés du contenu doivent correspondre à l’une des configurations de propriété retournées par [**IWMDMDevice3 :: GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability) dans la structure de **\_ \_ capacité du format WMDM** . Par exemple, pour un fichier audio, la vitesse de transmission et la fréquence d’échantillonnage doivent correspondre à l’une des configurations de propriété retournées.

L’appelant est responsable de la libération de la mémoire allouée pour cette structure. La fonction suivante montre comment effacer une structure **de \_ \_ capacité de format WMDM** .


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



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_ \_ \_ formulaire valeurs valides \_ de l’énumération WMDM \_**](wmdm-enum-prop-valid-values-form.md)
</dt> <dt>

[**configuration de WMDM \_ prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





