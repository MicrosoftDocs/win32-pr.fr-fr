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
ms.openlocfilehash: cad250745d51f00d3bb0492b6da8d3f9802bf87b78d65f4640324a68caa9ddf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903939"
---
# <a name="wmdm_prop_desc-structure"></a>WMDM \_ prop \_ desc (structure)

La structure **WMDM \_ prop \_ desc** décrit les valeurs valides d’une propriété dans une configuration de propriété particulière.

## <a name="syntax"></a>Syntaxe


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



## <a name="members"></a>Membres

<dl> <dt>

**pwszPropName**
</dt> <dd>

Nom de la propriété. L’application doit libérer cette mémoire une fois qu’elle a fini de l’utiliser.

</dd> <dt>

**ValidValuesForm**
</dt> <dd>

Une valeur d’énumération de [**\_ \_ \_ valeurs valides \_ \_ de WMDM enum prop**](wmdm-enum-prop-valid-values-form.md) décrivant le type de valeurs, par exemple une plage ou une liste. La valeur de cette énumération détermine la variable membre qui est utilisée.

</dd> <dt>

**ValidValues**
</dt> <dd>

Contient les valeurs valides de la propriété dans une configuration de propriété particulière. Ce membre contient l’un des trois éléments suivants : la valeur d’énumération WMDM \_ enum \_ prop \_ valeurs valides \_ \_ any ; le membre **ValidValuesRange**; ou le membre **EnumeratedValidValues**. La valeur ou le membre est indiqué par **ValidValuesForm**.

<dl> <dt>

**ValidValuesRange**
</dt> <dd>

Structure de la [**\_ plage de \_ valeurs \_ WMDM prop**](wmdm-prop-values-range.md) contenant une plage de valeurs valides. Cela est présent uniquement lorsque **ValidValuesForm** est défini sur WMDM \_ enum \_ prop \_ valeurs valides \_ \_ Range. Consultez la section Notes.

</dd> <dt>

**EnumeratedValidValues**
</dt> <dd>

Structure [**d' \_ \_ \_ énumération de valeurs WMDM prop**](wmdm-prop-values-enum.md) contenant un ensemble énuméré de valeurs valides. Cela est présent uniquement lorsque **ValidValuesForm** est défini sur WMDM \_ enum \_ prop \_ valeurs valides \_ \_ enum. Consultez la section Notes.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

La structure **WMDM \_ prop \_ desc** contient une description de propriété qui se compose d’un nom de propriété et de ses valeurs valides dans une configuration particulière.

L’appelant est tenu de libérer la mémoire utilisée par **ValidValuesRange** ou **EnumeratedValues**. Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).

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

[**\_ \_ énumération des valeurs prop WMDM \_**](wmdm-prop-values-enum.md)
</dt> <dt>

[**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





