---
description: Valeur booléenne qui indique si le composant « mois » dans la valeur DateTime CIM contient un intervalle ou une valeur générique.
ms.assetid: 12dd94de-24be-4b13-bde5-2fc28be94efa
ms.tgt_platform: multiple
title: SWbemDateTime. MonthSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MonthSpecified
- ISWbemDateTime.MonthSpecified
- ISWbemDateTime.get_MonthSpecified
- ISWbemDateTime.put_MonthSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 52b44444a5810577289353778c2c00b1ebfb80fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524566"
---
# <a name="swbemdatetimemonthspecified-property"></a><span data-ttu-id="db6b7-103">SWbemDateTime. MonthSpecified, propriété</span><span class="sxs-lookup"><span data-stu-id="db6b7-103">SWbemDateTime.MonthSpecified property</span></span>

<span data-ttu-id="db6b7-104">La propriété **MonthSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant month dans la valeur DateTime CIM contient un intervalle ou une valeur générique.</span><span class="sxs-lookup"><span data-stu-id="db6b7-104">The **MonthSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the month component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="db6b7-105">Si **MonthSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. month**](swbemdatetime-month.md) contient une valeur de date.</span><span class="sxs-lookup"><span data-stu-id="db6b7-105">If **MonthSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.Month**](swbemdatetime-month.md) contains a date value.</span></span> <span data-ttu-id="db6b7-106">Une valeur DateTime qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="db6b7-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="db6b7-107">Si **MonthSpecified** a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. month** contient un intervalle.</span><span class="sxs-lookup"><span data-stu-id="db6b7-107">If **MonthSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Month** contains an interval.</span></span>

<span data-ttu-id="db6b7-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="db6b7-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="db6b7-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="db6b7-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="db6b7-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="db6b7-110">Syntax</span></span>


```VB
SWbemDateTime.MonthSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="db6b7-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="db6b7-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="db6b7-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="db6b7-112">Examples</span></span>

<span data-ttu-id="db6b7-113">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="db6b7-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="db6b7-114">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="db6b7-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db6b7-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="db6b7-115">Requirements</span></span>



| <span data-ttu-id="db6b7-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="db6b7-116">Requirement</span></span> | <span data-ttu-id="db6b7-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="db6b7-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="db6b7-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6b7-118">Minimum supported client</span></span><br/> | <span data-ttu-id="db6b7-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="db6b7-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="db6b7-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="db6b7-120">Minimum supported server</span></span><br/> | <span data-ttu-id="db6b7-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="db6b7-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="db6b7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="db6b7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="db6b7-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="db6b7-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="db6b7-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="db6b7-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="db6b7-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="db6b7-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="db6b7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="db6b7-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db6b7-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db6b7-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="db6b7-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="db6b7-128">CLSID</span></span><br/>                    | <span data-ttu-id="db6b7-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="db6b7-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="db6b7-130">IID</span><span class="sxs-lookup"><span data-stu-id="db6b7-130">IID</span></span><br/>                      | <span data-ttu-id="db6b7-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="db6b7-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="db6b7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="db6b7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db6b7-133">**SWbemDateTime. mois**</span><span class="sxs-lookup"><span data-stu-id="db6b7-133">**SWbemDateTime.Month**</span></span>](swbemdatetime-month.md)
</dt> <dt>

[<span data-ttu-id="db6b7-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="db6b7-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="db6b7-135">Date/heure</span><span class="sxs-lookup"><span data-stu-id="db6b7-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




