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
# <a name="wpdparameterattributeform-enumeration"></a><span data-ttu-id="57767-103">Énumération WpdParameterAttributeForm</span><span class="sxs-lookup"><span data-stu-id="57767-103">WpdParameterAttributeForm enumeration</span></span>

<span data-ttu-id="57767-104">Le type d’énumération [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) décrit comment un paramètre (méthode ou événement) stocke sa valeur.</span><span class="sxs-lookup"><span data-stu-id="57767-104">The [**WpdParameterAttributeForm**](/previous-versions/windows/hardware/drivers/ff597895(v=vs.85)) enumeration type describes how a (method or event) parameter stores its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="57767-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57767-105">Syntax</span></span>


```C++
typedef enum tagWpdParameterAttributeForm { 
  WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED         = 0,
  WPD_PARAMETER_ATTRIBUTE_FORM_RANGE               = 1,
  WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION         = 2,
  WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION  = 3,
  WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER        = 4
} WpdParameterAttributeForm;
```



## <a name="constants"></a><span data-ttu-id="57767-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="57767-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="57767-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**\_formulaire d’attribut de paramètre wpd \_ \_ \_ non spécifié**</span><span class="sxs-lookup"><span data-stu-id="57767-107"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_UNSPECIFIED"></span><span id="wpd_parameter_attribute_form_unspecified"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_UNSPECIFIED**</span></span>
</dt> <dd>

<span data-ttu-id="57767-108">Le format du paramètre n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="57767-108">The form of the parameter is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="57767-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**\_plage de \_ formulaire d’attribut de paramètre wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57767-109"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_RANGE"></span><span id="wpd_parameter_attribute_form_range"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_RANGE**</span></span>
</dt> <dd>

<span data-ttu-id="57767-110">Le paramètre spécifie une plage.</span><span class="sxs-lookup"><span data-stu-id="57767-110">The parameter specifies a range.</span></span>

</dd> <dt>

<span data-ttu-id="57767-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**\_ \_ \_ énumération de formulaire d’attribut de paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="57767-111"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_ENUMERATION"></span><span id="wpd_parameter_attribute_form_enumeration"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_ENUMERATION**</span></span>
</dt> <dd>

<span data-ttu-id="57767-112">Le paramètre est une énumération.</span><span class="sxs-lookup"><span data-stu-id="57767-112">The parameter is an enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="57767-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**\_ \_ \_ expression régulière de formulaire d’attribut \_ de paramètre wpd \_**</span><span class="sxs-lookup"><span data-stu-id="57767-113"><span id="WPD_PARAMETER_ATTRIBUTE_FORM_REGULAR_EXPRESSION"></span><span id="wpd_parameter_attribute_form_regular_expression"></span>**WPD\_PARAMETER\_ATTRIBUTE\_FORM\_REGULAR\_EXPRESSION**</span></span>
</dt> <dd>

<span data-ttu-id="57767-114">Le paramètre est une expression régulière.</span><span class="sxs-lookup"><span data-stu-id="57767-114">The parameter is a regular expression.</span></span>

</dd> <dt>

<span data-ttu-id="57767-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**\_identificateur d' \_ objet d’attribut de paramètre wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="57767-115"><span id="WPD_PARAMETER_ATTRIBUTE_OBJECT_IDENTIFIER"></span><span id="wpd_parameter_attribute_object_identifier"></span>**WPD\_PARAMETER\_ATTRIBUTE\_OBJECT\_IDENTIFIER**</span></span>
</dt> <dd>

<span data-ttu-id="57767-116">Le paramètre est un identificateur d’objet.</span><span class="sxs-lookup"><span data-stu-id="57767-116">The parameter is an object identifier.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="57767-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="57767-117">Requirements</span></span>



| <span data-ttu-id="57767-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="57767-118">Requirement</span></span> | <span data-ttu-id="57767-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="57767-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="57767-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="57767-120">Header</span></span><br/> | <dl> <span data-ttu-id="57767-121"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="57767-121"><dt>PortableDevice.h</dt></span></span> </dl> |



 

