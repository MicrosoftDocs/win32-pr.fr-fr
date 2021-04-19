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
# <a name="wmdm_prop_values_range-structure"></a>Structure de la plage de valeurs WMDM \_ prop \_ \_

La structure de la **\_ plage de \_ valeurs \_ WMDM prop** décrit une plage de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDM_PROP_VALUES_RANGE {
  PROPVARIANT rangeMin;
  PROPVARIANT rangeMax;
  PROPVARIANT rangeStep;
} WMDM_PROP_VALUES_RANGE;
```



## <a name="members"></a>Membres

<dl> <dt>

**rangeMin**
</dt> <dd>

Valeur minimale de la plage.

</dd> <dt>

**rangeMax**
</dt> <dd>

Valeur maximale de la plage.

</dd> <dt>

**rangeStep**
</dt> <dd>

Taille de l’étape dans laquelle les valeurs valides sont incrémentées de la valeur minimale à la valeur maximale. Cela permet de spécifier des valeurs autorisées discrètes dans une plage.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée dans la structure [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) pour décrire une plage de valeurs valides. Une plage de valeurs valides est applicable lorsque \_ l’énumération \_ \_ des valeurs valides de l’énumération prop WMDM \_ \_ est sélectionnée dans l’énumération de [**\_ formulaire WMDM enum \_ prop \_ Valid \_ values \_**](wmdm-enum-prop-valid-values-form.md) .

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

[**\_fonction de format WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**configuration de WMDM \_ prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





