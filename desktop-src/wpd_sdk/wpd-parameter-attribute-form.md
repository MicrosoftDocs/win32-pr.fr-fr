---
description: Décrit comment un paramètre (méthode ou événement) stocke sa valeur.
ms.assetid: 066196af-7805-4823-8ab7-cb95c17bba2a
title: Énumération WpdParameterAttributeForm (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WpdParameterAttributeForm
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 528008edbb74d5eda626b9868814ad621e676fa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532550"
---
# <a name="wpdparameterattributeform-enumeration"></a>Énumération WpdParameterAttributeForm

Le type d’énumération [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) décrit comment un paramètre (méthode ou événement) stocke sa valeur.

## <a name="syntax"></a>Syntaxe


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_formulaire d’attribut de paramètre wpd \_ \_ \_ non spécifié**
</dt> <dd>

Le format du paramètre n’est pas spécifié.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_plage de \_ formulaire d’attribut de paramètre wpd \_ \_**
</dt> <dd>

Le paramètre spécifie une plage.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ énumération de formulaire d’attribut de paramètre wpd \_**
</dt> <dd>

Le paramètre est une énumération.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ expression régulière de formulaire d’attribut \_ de paramètre wpd \_**
</dt> <dd>

Le paramètre est une expression régulière.

</dd> <dt>

<span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_identificateur d' \_ objet d’attribut de paramètre wpd \_ \_**
</dt> <dd>

Le paramètre est un identificateur d’objet.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

