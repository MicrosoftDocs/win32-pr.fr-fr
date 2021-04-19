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
# <a name="wpdattributeform-enumeration"></a><span data-ttu-id="38e77-103">Énumération WpdAttributeForm</span><span class="sxs-lookup"><span data-stu-id="38e77-103">WpdAttributeForm enumeration</span></span>

<span data-ttu-id="38e77-104">Le type d’énumération **WpdAttributeForm** décrit la façon dont une propriété stocke ses valeurs.</span><span class="sxs-lookup"><span data-stu-id="38e77-104">The **WpdAttributeForm** enumeration type describes how a property stores its values.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e77-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="38e77-105">Syntax</span></span>


```C++
typedef enum WpdAttributeForm { 
  WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PROPERTY_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER   = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="38e77-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="38e77-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="38e77-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**\_formulaire d’attribut de propriété wpd \_ \_ \_ non spécifié**</span><span class="sxs-lookup"><span data-stu-id="38e77-107"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_property_attribute_form_unspecified"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="38e77-108">Le formulaire des données de la propriété n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="38e77-108">The form of the property's data is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="38e77-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**\_plage de \_ formulaire des attributs de propriété wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38e77-109"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_property_attribute_form_range"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="38e77-110">La valeur est exprimée sous la forme d’une plage de valeurs, avec un minimum et un maximum.</span><span class="sxs-lookup"><span data-stu-id="38e77-110">The value is expressed as a range of values, with a minimum and a maximum.</span></span>

</dd> <dt>

<span data-ttu-id="38e77-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**\_ \_ \_ énumération de formulaire d’attribut de propriété wpd \_**</span><span class="sxs-lookup"><span data-stu-id="38e77-111"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_property_attribute_form_enumeration"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="38e77-112">La propriété possède une série de valeurs individuelles.</span><span class="sxs-lookup"><span data-stu-id="38e77-112">The property has a series of individual values.</span></span>

</dd> <dt>

<span data-ttu-id="38e77-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**\_ \_ \_ expression régulière de formulaire \_ de l’attribut de propriété \_ wpd**</span><span class="sxs-lookup"><span data-stu-id="38e77-113"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_property_attribute_form_regular_expression"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="38e77-114">La valeur de la propriété est une expression régulière, et non une expression littérale.</span><span class="sxs-lookup"><span data-stu-id="38e77-114">The property value is a regular expression, not a literal expression.</span></span>

</dd> <dt>

<span data-ttu-id="38e77-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**\_formulaire d’attribut de propriété wpd \_ \_ \_ OJBECT \_ identificateur**</span><span class="sxs-lookup"><span data-stu-id="38e77-115"><span id="WPD_PROPERTY_ATTRIBUTE_FORM_OJBECT_IDENTIFIER"></span><span id="wpd_property_attribute_form_ojbect_identifier"></span>**WPD\_PROPERTY\_ATTRIBUTE\_FORM\_OJBECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="38e77-116">La valeur de propriété représente un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="38e77-116">The property value represents an object identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38e77-117">Notes</span><span class="sxs-lookup"><span data-stu-id="38e77-117">Remarks</span></span>

<span data-ttu-id="38e77-118">Cette énumération est utilisée par la propriété de [ \_ formulaire d' \_ attribut \_ de propriété wpd](attributes.md) pour décrire le mode de stockage des données d’une propriété.</span><span class="sxs-lookup"><span data-stu-id="38e77-118">This enumeration is used by the [WPD\_PROPERTY\_ATTRIBUTE\_FORM](attributes.md) property to describe how a property's data is stored.</span></span>

## <a name="requirements"></a><span data-ttu-id="38e77-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="38e77-119">Requirements</span></span>



| <span data-ttu-id="38e77-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="38e77-120">Requirement</span></span> | <span data-ttu-id="38e77-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="38e77-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="38e77-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="38e77-122">Header</span></span><br/> | <dl> <span data-ttu-id="38e77-123"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="38e77-123"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e77-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="38e77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e77-125">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="38e77-125">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




