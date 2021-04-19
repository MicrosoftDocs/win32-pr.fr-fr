---
description: Valeur booléenne qui indique si le composant de temps UTC (Universal Coordinated Time) dans la valeur DateTime CIM contient un intervalle ou une valeur générique.
ms.assetid: 9cb04351-294b-48ba-8d1c-2f28cb9ce463
ms.tgt_platform: multiple
title: SWbemDateTime. UTCSpecified, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTCSpecified
- ISWbemDateTime.UTCSpecified
- ISWbemDateTime.get_UTCSpecified
- ISWbemDateTime.put_UTCSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e2ada5bbbfa68e6cb63c0e060d6c3a12c0f771a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530089"
---
# <a name="swbemdatetimeutcspecified-property"></a><span data-ttu-id="c00cd-103">SWbemDateTime. UTCSpecified, propriété</span><span class="sxs-lookup"><span data-stu-id="c00cd-103">SWbemDateTime.UTCSpecified property</span></span>

<span data-ttu-id="c00cd-104">La propriété **UTCSpecified** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si le composant de l’heure UTC (Universal Coordinated Time) de la valeur DateTime CIM contient un intervalle ou une valeur générique.</span><span class="sxs-lookup"><span data-stu-id="c00cd-104">The **UTCSpecified** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether the Universal Coordinated Time (UTC) component in the CIM datetime value contains an interval or a wildcard value.</span></span> <span data-ttu-id="c00cd-105">Si **UTCSpecified** a la valeur **true** et que [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**, [**SWbemDateTime. UTC**](swbemdatetime-utc.md) contient une valeur [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="c00cd-105">If **UTCSpecified** is **TRUE** and [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**, then [**SWbemDateTime.UTC**](swbemdatetime-utc.md) contains a [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="c00cd-106">Une valeur **DateTime** qui contient un intervalle ne peut pas être convertie au format de **\_ Date VT** ou **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="c00cd-106">A **DATETIME** value that contains an interval cannot be converted into either the **VT\_DATE** format or the **FILETIME** format.</span></span> <span data-ttu-id="c00cd-107">Si **UTCSpecified** a la **valeur false** et que **IsInterval** a la **valeur true**, **SWbemDateTime. UTC** contient un intervalle.</span><span class="sxs-lookup"><span data-stu-id="c00cd-107">If **UTCSpecified** is **FALSE** and **IsInterval** is **TRUE**, then **SWbemDateTime.UTC** contains an interval.</span></span>

<span data-ttu-id="c00cd-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c00cd-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c00cd-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c00cd-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c00cd-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c00cd-110">Syntax</span></span>


```VB
SWbemDateTime.UTCSpecified As Boolean
```



## <a name="property-value"></a><span data-ttu-id="c00cd-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c00cd-111">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="c00cd-112">Exemples</span><span class="sxs-lookup"><span data-stu-id="c00cd-112">Examples</span></span>

<span data-ttu-id="c00cd-113">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="c00cd-113">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="c00cd-114">Pour obtenir une description du format DateTime CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="c00cd-114">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c00cd-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c00cd-115">Requirements</span></span>



| <span data-ttu-id="c00cd-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c00cd-116">Requirement</span></span> | <span data-ttu-id="c00cd-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c00cd-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c00cd-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00cd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c00cd-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c00cd-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c00cd-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c00cd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c00cd-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c00cd-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c00cd-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="c00cd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="c00cd-123"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c00cd-123"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c00cd-124">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c00cd-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="c00cd-125"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c00cd-125"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c00cd-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c00cd-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c00cd-127"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c00cd-127"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c00cd-128">CLSID</span><span class="sxs-lookup"><span data-stu-id="c00cd-128">CLSID</span></span><br/>                    | <span data-ttu-id="c00cd-129">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c00cd-129">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="c00cd-130">IID</span><span class="sxs-lookup"><span data-stu-id="c00cd-130">IID</span></span><br/>                      | <span data-ttu-id="c00cd-131">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="c00cd-131">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c00cd-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c00cd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c00cd-133">**SWbemDateTime. UTC**</span><span class="sxs-lookup"><span data-stu-id="c00cd-133">**SWbemDateTime.UTC**</span></span>](swbemdatetime-utc.md)
</dt> <dt>

[<span data-ttu-id="c00cd-134">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="c00cd-134">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="c00cd-135">Date/heure</span><span class="sxs-lookup"><span data-stu-id="c00cd-135">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




