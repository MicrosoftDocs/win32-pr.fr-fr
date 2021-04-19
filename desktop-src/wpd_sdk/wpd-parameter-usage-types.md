---
description: Le \_ \_ \_ type d’énumération des types d’utilisation de paramètre wpd décrit comment un paramètre de méthode est utilisé dans une méthode donnée.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Énumération WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539623"
---
# <a name="wpd_parameter_usage_types-enumeration"></a><span data-ttu-id="1799d-103">\_ \_ Énumération des types d’utilisation des paramètres wpd \_</span><span class="sxs-lookup"><span data-stu-id="1799d-103">WPD\_PARAMETER\_USAGE\_TYPES enumeration</span></span>

<span data-ttu-id="1799d-104">Le type d’énumération des [**\_ types d' \_ utilisation \_ de paramètre wpd**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) décrit comment un paramètre de méthode est utilisé dans une méthode donnée.</span><span class="sxs-lookup"><span data-stu-id="1799d-104">The [**WPD\_PARAMETER\_USAGE\_TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) enumeration type describes how a method parameter is used in a given method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1799d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1799d-105">Syntax</span></span>


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="1799d-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="1799d-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1799d-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_retour de \_ l’utilisation des paramètres wpd \_**</span><span class="sxs-lookup"><span data-stu-id="1799d-107"><span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD\_PARAMETER\_USAGE\_RETURN**</span></span>
</dt> <dd>

<span data-ttu-id="1799d-108">Le paramètre reçoit la valeur de retour, si elle est spécifiée par la méthode.</span><span class="sxs-lookup"><span data-stu-id="1799d-108">The parameter receives the return value, if specified by the method.</span></span>

</dd> <dt>

<span data-ttu-id="1799d-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ utilisation des paramètres wpd \_ dans**</span><span class="sxs-lookup"><span data-stu-id="1799d-109"><span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**WPD\_PARAMETER\_USAGE\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="1799d-110">Le paramètre contient une valeur d’entrée avant l’appel de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1799d-110">The parameter contains an input value before the method is called.</span></span>

</dd> <dt>

<span data-ttu-id="1799d-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**\_utilisation du paramètre wpd \_ \_ out**</span><span class="sxs-lookup"><span data-stu-id="1799d-111"><span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**WPD\_PARAMETER\_USAGE\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="1799d-112">Le paramètre contient une valeur de sortie lorsque la méthode est retournée.</span><span class="sxs-lookup"><span data-stu-id="1799d-112">The parameter contains an output value when the method returns.</span></span>

</dd> <dt>

<span data-ttu-id="1799d-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**\_utilisation du paramètre wpd \_ \_ INOUT**</span><span class="sxs-lookup"><span data-stu-id="1799d-113"><span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**WPD\_PARAMETER\_USAGE\_INOUT**</span></span>
</dt> <dd>

<span data-ttu-id="1799d-114">Le paramètre contient une valeur d’entrée avant que la méthode soit appelée et une valeur de sortie lors de son retour.</span><span class="sxs-lookup"><span data-stu-id="1799d-114">The parameter contains an input value before the method is called and an output value when it returns.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1799d-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1799d-115">Requirements</span></span>



| <span data-ttu-id="1799d-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1799d-116">Requirement</span></span> | <span data-ttu-id="1799d-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1799d-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1799d-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1799d-118">Header</span></span><br/> | <dl> <span data-ttu-id="1799d-119"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="1799d-119"><dt>PortableDevice.h</dt></span></span> </dl> |



 

