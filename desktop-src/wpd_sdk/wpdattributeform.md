---
description: Le type d’énumération WpdAttributeForm décrit la façon dont une propriété stocke ses valeurs.
ms.assetid: 3ad8d1f9-1b74-4f34-9af5-1acdd588b650
title: Énumération WpdAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 4c70f68dc04adcb454fcc7c5ae301f0dabf60c28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528838"
---
# <a name="wpdattributeform-enumeration"></a>Énumération WpdAttributeForm

Le type d’énumération **WpdAttributeForm** décrit la façon dont une propriété stocke ses valeurs.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_formulaire d’attribut de propriété wpd \_ \_ \_ non spécifié**
</dt> <dd>

Le formulaire des données de la propriété n’est pas spécifié.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_plage de \_ formulaire des attributs de propriété wpd \_ \_**
</dt> <dd>

La valeur est exprimée sous la forme d’une plage de valeurs, avec un minimum et un maximum.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ énumération de formulaire d’attribut de propriété wpd \_**
</dt> <dd>

La propriété possède une série de valeurs individuelles.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expression régulière de formulaire \_ de l’attribut de propriété \_ wpd**
</dt> <dd>

La valeur de la propriété est une expression régulière, et non une expression littérale.

</dd> <dt>

<span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_formulaire d’attribut de propriété wpd \_ \_ \_ OJBECT \_ identificateur**
</dt> <dd>

La valeur de propriété représente un identificateur d’objet.

</dd> </dl>

## <a name="remarks"></a>Notes

Cette énumération est utilisée par la propriété de [ \_ formulaire d' \_ attribut \_ de propriété wpd](attributes.md) pour décrire le mode de stockage des données d’une propriété.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Structures et types énumération**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




