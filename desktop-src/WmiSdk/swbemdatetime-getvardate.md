---
description: Convertit une valeur de date et d’heure au format DATETIME CIM au \_ format de date VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. getVarDate, (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524976"
---
# <a name="swbemdatetimegetvardate-method"></a><span data-ttu-id="b6423-103">Méthode SWbemDateTime. getVarDate,</span><span class="sxs-lookup"><span data-stu-id="b6423-103">SWbemDateTime.GetVarDate method</span></span>

<span data-ttu-id="b6423-104">La méthode **getVarDate,** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une valeur de date et d’heure au format [**DateTime**](datetime.md) CIM au format de **\_ Date VT** .</span><span class="sxs-lookup"><span data-stu-id="b6423-104">The **GetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [**DATETIME**](datetime.md) format to the **VT\_DATE** format.</span></span>

<span data-ttu-id="b6423-105">Le format de **\_ Date VT** est une valeur [**DateTime**](datetime.md) de variante Automation que Visual Basic et un ActiveX utilisent.</span><span class="sxs-lookup"><span data-stu-id="b6423-105">The **VT\_DATE** format is an automation variant [**DATETIME**](datetime.md) value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="b6423-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b6423-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b6423-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6423-107">Syntax</span></span>


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="b6423-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b6423-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6423-109">*bIsLocal* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="b6423-109">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b6423-110">Indique si la valeur retournée est interprétée comme heure locale.</span><span class="sxs-lookup"><span data-stu-id="b6423-110">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="b6423-111">La propriété temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct.</span><span class="sxs-lookup"><span data-stu-id="b6423-111">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="b6423-112">Si la valeur est **false**, la valeur est interprétée comme étant UTC avec un décalage de zéro (0).</span><span class="sxs-lookup"><span data-stu-id="b6423-112">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6423-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b6423-113">Return value</span></span>

<span data-ttu-id="b6423-114">Valeur de date et d’heure au format de **\_ Date VT** .</span><span class="sxs-lookup"><span data-stu-id="b6423-114">The date and time value in the **VT\_DATE** format.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6423-115">Notes</span><span class="sxs-lookup"><span data-stu-id="b6423-115">Remarks</span></span>

<span data-ttu-id="b6423-116">**VT \_** Les valeurs de date et **fileTime** ne peuvent pas contenir de champs génériques.</span><span class="sxs-lookup"><span data-stu-id="b6423-116">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="b6423-117">La méthode **getVarDate,** échoue (**wbemErrFailed**) si l’une des propriétés suivantes a la **valeur false**:</span><span class="sxs-lookup"><span data-stu-id="b6423-117">The **GetVarDate** method fails (**wbemErrFailed**) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="b6423-118">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-118">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="b6423-119">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-119">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="b6423-120">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-120">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="b6423-121">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-121">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="b6423-122">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-122">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="b6423-123">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-123">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="b6423-124">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-124">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="b6423-125">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="b6423-125">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="b6423-126">En cas de retour réussi de [**SetVarDate**](swbemdatetime-setvardate.md), toutes ces propriétés ont la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="b6423-126">On successful return from [**SetVarDate**](swbemdatetime-setvardate.md), all of these properties are set to **TRUE**.</span></span>

<span data-ttu-id="b6423-127">Après un appel réussi à [**SetVarDate**](swbemdatetime-setvardate.md), la valeur [**DateTime**](datetime.md) est toujours interprétée comme une valeur **DateTime** absolue au lieu d’un intervalle, et [**IsInterval**](swbemdatetime-isinterval.md) est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="b6423-127">After a successful call to [**SetVarDate**](swbemdatetime-setvardate.md), the [**DATETIME**](datetime.md) value is always interpreted as an absolute **DATETIME** value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

<span data-ttu-id="b6423-128">Si [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **true**, un appel à **getVarDate,** provoque l’erreur **wbemErrFailed** .</span><span class="sxs-lookup"><span data-stu-id="b6423-128">If [**IsInterval**](swbemdatetime-isinterval.md) is set to **TRUE**, then a call to **GetVarDate** results in the **wbemErrFailed** error.</span></span>

<span data-ttu-id="b6423-129">Une perte de précision se produit lorsque vous appelez **getVarDate,**, car les valeurs [DateTime](datetime.md) ont une résolution d’une microseconde (s), et les valeurs de **\_ DATE VT** ont une résolution de 500 millisecondes.</span><span class="sxs-lookup"><span data-stu-id="b6423-129">Some loss of precision occurs when you call **GetVarDate**, because [datetime](datetime.md) values have a one microsecond ( s) resolution, and **VT\_DATE** values have a 500 millisecond resolution.</span></span>

## <a name="examples"></a><span data-ttu-id="b6423-130">Exemples</span><span class="sxs-lookup"><span data-stu-id="b6423-130">Examples</span></span>

<span data-ttu-id="b6423-131">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format de **\_ Date** **fileTime** ou VT, consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="b6423-131">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="b6423-132">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b6423-132">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b6423-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6423-133">Requirements</span></span>



| <span data-ttu-id="b6423-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6423-134">Requirement</span></span> | <span data-ttu-id="b6423-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6423-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6423-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6423-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b6423-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6423-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6423-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b6423-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b6423-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6423-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6423-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6423-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6423-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6423-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b6423-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b6423-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="b6423-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b6423-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b6423-144">DLL</span><span class="sxs-lookup"><span data-stu-id="b6423-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6423-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6423-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b6423-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="b6423-146">CLSID</span></span><br/>                    | <span data-ttu-id="b6423-147">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="b6423-147">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="b6423-148">IID</span><span class="sxs-lookup"><span data-stu-id="b6423-148">IID</span></span><br/>                      | <span data-ttu-id="b6423-149">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="b6423-149">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="b6423-150">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6423-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6423-151">**SWbemDateTime. GetFileTime**</span><span class="sxs-lookup"><span data-stu-id="b6423-151">**SWbemDateTime.GetFileTime**</span></span>](swbemdatetime-getfiletime.md)
</dt> <dt>

[<span data-ttu-id="b6423-152">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="b6423-152">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="b6423-153">Date/heure</span><span class="sxs-lookup"><span data-stu-id="b6423-153">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




