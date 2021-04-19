---
description: Valeur booléenne qui indique si le composant « jour » dans la valeur DATETIME CIM contient un intervalle ou une valeur générique.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: SWbemDateTime. DaySpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f295d33940f36212fde4fe821af8d5df24d4f75f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527388"
---
# <a name="swbemdatetimedayspecified-property"></a><span data-ttu-id="74e88-103">SWbemDateTime. DaySpecified, propriété</span><span class="sxs-lookup"><span data-stu-id="74e88-103">SWbemDateTime.DaySpecified property</span></span>

<span data-ttu-id="74e88-104">La propriété **DaySpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant Day de la valeur [**DateTime**](datetime.md) CIM contient un intervalle ou une valeur générique.</span><span class="sxs-lookup"><span data-stu-id="74e88-104">The **DaySpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the day component in the CIM [**DATETIME**](datetime.md) value contains an interval or a wildcard value.</span></span> <span data-ttu-id="74e88-105">Si **DaySpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. Day**](swbemdatetime-day.md) contient une valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="74e88-105">If **DaySpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Day**](swbemdatetime-day.md) contains a datetime value.</span></span> <span data-ttu-id="74e88-106">Une valeur [**DateTime**](datetime.md) qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="74e88-106">A [**DATETIME**](datetime.md) value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="74e88-107">Si **DaySpecified** a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. Day** contient un intervalle.</span><span class="sxs-lookup"><span data-stu-id="74e88-107">If **DaySpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Day** contains an interval.</span></span>

<span data-ttu-id="74e88-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="74e88-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="74e88-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="74e88-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="74e88-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="74e88-110">Syntax</span></span>


```VB
SWbemDateTime.DaySpecified As BOOLEAN
```



## <a name="property-value"></a><span data-ttu-id="74e88-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="74e88-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="74e88-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="74e88-112">Examples</span></span>

<span data-ttu-id="74e88-113">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="74e88-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="74e88-114">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="74e88-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="74e88-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74e88-115">Requirements</span></span>



| <span data-ttu-id="74e88-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74e88-116">Requirement</span></span> | <span data-ttu-id="74e88-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="74e88-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="74e88-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74e88-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74e88-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="74e88-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="74e88-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74e88-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74e88-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="74e88-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="74e88-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="74e88-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="74e88-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="74e88-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="74e88-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="74e88-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="74e88-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="74e88-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="74e88-126">DLL</span><span class="sxs-lookup"><span data-stu-id="74e88-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="74e88-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74e88-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="74e88-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="74e88-128">CLSID</span></span><br/>                    | <span data-ttu-id="74e88-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="74e88-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="74e88-130">IID</span><span class="sxs-lookup"><span data-stu-id="74e88-130">IID</span></span><br/>                      | <span data-ttu-id="74e88-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="74e88-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="74e88-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74e88-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74e88-133">**SWbemDateTime. jour**</span><span class="sxs-lookup"><span data-stu-id="74e88-133">**SWbemDateTime.Day**</span></span>](swbemdatetime-day.md)
</dt> <dt>

[<span data-ttu-id="74e88-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="74e88-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="74e88-135">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="74e88-135">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




