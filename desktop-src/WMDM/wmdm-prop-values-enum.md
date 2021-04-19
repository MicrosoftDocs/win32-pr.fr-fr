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
# <a name="wmdm_prop_values_enum-structure"></a>WMDM \_ prop \_ Values, \_ structure enum

La structure d' **\_ \_ \_ énumération de valeurs WMDM prop** contient un ensemble énuméré de valeurs valides pour une propriété particulière dans une configuration de propriété particulière.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct _WMDM_PROP_VALUES_ENUM {
  UINT        cEnumValues;
  PROPVARIANT *pValues;
} WMDM_PROP_VALUES_ENUM;
```



## <a name="members"></a>Membres

<dl> <dt>

**cEnumValues**
</dt> <dd>

Nombre de valeurs énumérées.

</dd> <dt>

**pValues**
</dt> <dd>

Pointeur vers un tableau de valeurs. La taille du tableau est égale à la valeur de **cEnumValues**.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette structure est utilisée dans la structure **WMDM \_ prop \_ desc** pour décrire un ensemble énuméré de valeurs valides. Un ensemble énuméré de valeurs valides est applicable lorsque l’énumération des \_ \_ valeurs valides de l’énumération prop WMDM \_ \_ \_ est sélectionnée dans l’énumération de **\_ formulaire WMDM enum \_ prop \_ Valid \_ values \_** .

L’appelant est tenu de libérer la mémoire utilisée par **pValues**. Pour obtenir un exemple de la procédure à suivre, consultez [**WMDM \_ format \_ Capability**](wmdm-format-capability.md).

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

[**plage de valeurs de WMDM \_ prop \_ \_**](wmdm-prop-values-range.md)
</dt> <dt>

[**Structures**](structures.md)
</dt> </dl>

 

 





