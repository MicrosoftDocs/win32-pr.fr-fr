---
description: Indique si le composant « minutes » de la valeur DateTime CIM contient un intervalle ou une valeur de caractère générique.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: SWbemDateTime. MinutesSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114879"
---
# <a name="swbemdatetimeminutesspecified-property"></a><span data-ttu-id="b1a98-103">SWbemDateTime. MinutesSpecified, propriété</span><span class="sxs-lookup"><span data-stu-id="b1a98-103">SWbemDateTime.MinutesSpecified property</span></span>

<span data-ttu-id="b1a98-104">La propriété **MinutesSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant « minutes » de la valeur DateTime CIM contient un intervalle ou une valeur générique.</span><span class="sxs-lookup"><span data-stu-id="b1a98-104">The **MinutesSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the minutes component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="b1a98-105">Si **MinutesSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false** (indiquant que la valeur DateTime CIM n’a pas de caractère générique), [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) contient une valeur de date.</span><span class="sxs-lookup"><span data-stu-id="b1a98-105">If **MinutesSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE** (indicating that the CIM datetime value has no wildcards), then [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) contains a date value.</span></span> <span data-ttu-id="b1a98-106">Une valeur DateTime qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="b1a98-106">A datetime value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="b1a98-107">Si [**HoursSpecified**](swbemdatetime-hoursspecified.md) a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. minutes** contient un intervalle.</span><span class="sxs-lookup"><span data-stu-id="b1a98-107">If [**HoursSpecified**](swbemdatetime-hoursspecified.md) is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.Minutes** contains an interval.</span></span>

<span data-ttu-id="b1a98-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b1a98-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b1a98-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b1a98-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1a98-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b1a98-110">Syntax</span></span>


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a><span data-ttu-id="b1a98-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b1a98-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="b1a98-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="b1a98-112">Examples</span></span>

<span data-ttu-id="b1a98-113">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="b1a98-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="b1a98-114">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b1a98-114">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b1a98-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b1a98-115">Requirements</span></span>



| <span data-ttu-id="b1a98-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b1a98-116">Requirement</span></span> | <span data-ttu-id="b1a98-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="b1a98-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a98-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a98-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b1a98-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b1a98-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b1a98-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b1a98-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b1a98-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b1a98-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b1a98-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b1a98-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1a98-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1a98-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1a98-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b1a98-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="b1a98-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b1a98-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b1a98-126">DLL</span><span class="sxs-lookup"><span data-stu-id="b1a98-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1a98-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1a98-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b1a98-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="b1a98-128">CLSID</span></span><br/>                    | <span data-ttu-id="b1a98-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="b1a98-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="b1a98-130">IID</span><span class="sxs-lookup"><span data-stu-id="b1a98-130">IID</span></span><br/>                      | <span data-ttu-id="b1a98-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="b1a98-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b1a98-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1a98-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1a98-133">**SWbemDateTime. minutes**</span><span class="sxs-lookup"><span data-stu-id="b1a98-133">**SWbemDateTime.Minutes**</span></span>](swbemdatetime-minutes.md)
</dt> <dt>

[<span data-ttu-id="b1a98-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="b1a98-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="b1a98-135">Date/heure</span><span class="sxs-lookup"><span data-stu-id="b1a98-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




