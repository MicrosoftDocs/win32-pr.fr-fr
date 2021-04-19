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
# <a name="wmdm_enum_prop_valid_values_form-enumeration"></a>\_ \_ \_ Énumération des valeurs valides du prop WMDM \_ enum \_

Le type d’énumération de **\_ \_ \_ \_ \_ formulaire des valeurs valides du prop enum WMDM** décrit les formes possibles des valeurs valides pour une propriété.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum _WMDM_ENUM_PROP_VALID_VALUES_FORM { 
  WMDM_ENUM_PROP_VALID_VALUES_ANY,
  WMDM_ENUM_PROP_VALID_VALUES_RANGE,
  WMDM_ENUM_PROP_VALID_VALUES_ENUM
} WMDM_ENUM_PROP_VALID_VALUES_FORM;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ANY"></span><span id="wmdm_enum_prop_valid_values_any"></span>**WMDM \_ enum \_ prop \_ valeurs valides \_ \_ any**
</dt> <dd>

Toutes les valeurs sont valides.

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_RANGE"></span><span id="wmdm_enum_prop_valid_values_range"></span>**\_plage de \_ \_ valeurs valides de \_ l’énumération WMDM \_**
</dt> <dd>

Les valeurs valides sont exprimées sous la forme d’une plage. Pour plus d’informations, consultez la structure de la [**\_ plage de \_ valeurs \_ WMDM prop**](wmdm-prop-values-range.md) .

</dd> <dt>

<span id="WMDM_ENUM_PROP_VALID_VALUES_ENUM"></span><span id="wmdm_enum_prop_valid_values_enum"></span>**\_ \_ \_ énumération des valeurs valides de \_ l’énumération WMDM \_**
</dt> <dd>

Les valeurs valides sont un jeu énuméré. Pour plus d’informations, consultez [**WMDM \_ prop \_ values \_**](wmdm-prop-values-enum.md) , structure Enum.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée dans la structure [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md) pour spécifier la forme de valeurs valides pour une propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMDM. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Types énumération**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**\_fonction de format WMDM \_**](wmdm-format-capability.md)
</dt> <dt>

[**configuration de WMDM \_ prop \_**](wmdm-prop-config.md)
</dt> <dt>

[**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)
</dt> <dt>

[**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md)
</dt> </dl>

 

 





