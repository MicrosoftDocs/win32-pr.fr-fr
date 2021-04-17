---
description: Convertit une valeur de date et d’heure au format DATETIME CIM au format FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. GetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3f8a8c85cb4c78be578187b1f55afce078fe7bd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485729"
---
# <a name="swbemdatetimegetfiletime-method"></a><span data-ttu-id="9751b-103">Méthode SWbemDateTime. GetFileTime</span><span class="sxs-lookup"><span data-stu-id="9751b-103">SWbemDateTime.GetFileTime method</span></span>

<span data-ttu-id="9751b-104">La méthode **GetFileTime** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une valeur de date et d’heure dans le format [DateTime](datetime.md) CIM au format FILETIME.</span><span class="sxs-lookup"><span data-stu-id="9751b-104">The **GetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date and time value in the CIM [DATETIME](datetime.md) format to the FILETIME format.</span></span>

<span data-ttu-id="9751b-105">Si le paramètre est défini sur **true**, la valeur de retour représente une heure locale pour le client.</span><span class="sxs-lookup"><span data-stu-id="9751b-105">If the parameter is set to **TRUE**, then the return value represents a local time for the client.</span></span> <span data-ttu-id="9751b-106">Dans le cas contraire, la valeur de retour est une heure UTC (Coordinated Universal Time).</span><span class="sxs-lookup"><span data-stu-id="9751b-106">Otherwise, the return value is a Coordinated Universal Time (UTC) time.</span></span> <span data-ttu-id="9751b-107">Une structure [DateTime](datetime.md) **fileTime** est une valeur 64 bits qui représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="9751b-107">A **FILETIME** [DATETIME](datetime.md) structure is a 64-bit value that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="9751b-108">Windows Management Instrumentation (WMI) traite les valeurs **fileTime** comme des représentations sous forme de chaîne de nombres 64 bits non signés.</span><span class="sxs-lookup"><span data-stu-id="9751b-108">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="9751b-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="9751b-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9751b-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9751b-110">Syntax</span></span>


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a><span data-ttu-id="9751b-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9751b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9751b-112">*bIsLocaL* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="9751b-112">*bIsLocaL* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="9751b-113">Indique si la valeur retournée est interprétée comme heure locale.</span><span class="sxs-lookup"><span data-stu-id="9751b-113">Indicates whether the returned value is interpreted as local time.</span></span> <span data-ttu-id="9751b-114">La propriété UTC contient ensuite l’heure locale convertie en décalage UTC (temps universel coordonné) correct.</span><span class="sxs-lookup"><span data-stu-id="9751b-114">The UTC property then contains the local time converted to the correct Coordinated Universal Times (UTC) offset.</span></span> <span data-ttu-id="9751b-115">Si la valeur est **false**, la valeur est interprétée comme étant UTC avec un décalage de zéro (0).</span><span class="sxs-lookup"><span data-stu-id="9751b-115">If the value is **FALSE**, then the value is interpreted as UTC with a zero (0) offset.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9751b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9751b-116">Return value</span></span>

<span data-ttu-id="9751b-117">Date et heure au format **fileTime** .</span><span class="sxs-lookup"><span data-stu-id="9751b-117">The date and time in the **FILETIME** format.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9751b-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="9751b-118">Error codes</span></span>

<span data-ttu-id="9751b-119">À la fin de la méthode **GetFileTime** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="9751b-119">After completing the **GetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="9751b-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="9751b-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="9751b-121">L'appel a échoué.</span><span class="sxs-lookup"><span data-stu-id="9751b-121">The call failed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9751b-122">Notes</span><span class="sxs-lookup"><span data-stu-id="9751b-122">Remarks</span></span>

<span data-ttu-id="9751b-123">**VT \_** Les valeurs de date et **fileTime** ne peuvent pas contenir de champs génériques.</span><span class="sxs-lookup"><span data-stu-id="9751b-123">**VT\_DATE** and **FILETIME** values cannot contain wildcard fields.</span></span>

<span data-ttu-id="9751b-124">La méthode **GetFileTime** échoue (wbemErrFailed) si l’une des propriétés suivantes a la **valeur false**:</span><span class="sxs-lookup"><span data-stu-id="9751b-124">The **GetFileTime** method fails (wbemErrFailed) if any of the following properties are **FALSE**:</span></span>

-   [<span data-ttu-id="9751b-125">**YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-125">**YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
-   [<span data-ttu-id="9751b-126">**MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-126">**MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
-   [<span data-ttu-id="9751b-127">**DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-127">**DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
-   [<span data-ttu-id="9751b-128">**HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-128">**HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
-   [<span data-ttu-id="9751b-129">**MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-129">**MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
-   [<span data-ttu-id="9751b-130">**SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-130">**SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
-   [<span data-ttu-id="9751b-131">**MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-131">**MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
-   [<span data-ttu-id="9751b-132">**UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="9751b-132">**UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)

<span data-ttu-id="9751b-133">En cas de retour réussi de [**SetFileTime**](swbemdatetime-setfiletime.md), toutes ces propriétés ont la valeur **true**.</span><span class="sxs-lookup"><span data-stu-id="9751b-133">On a successful return from [**SetFileTime**](swbemdatetime-setfiletime.md), all of these properties are set to **TRUE**.</span></span>

## <a name="examples"></a><span data-ttu-id="9751b-134">Exemples</span><span class="sxs-lookup"><span data-stu-id="9751b-134">Examples</span></span>

<span data-ttu-id="9751b-135">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="9751b-135">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="9751b-136">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="9751b-136">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9751b-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9751b-137">Requirements</span></span>



| <span data-ttu-id="9751b-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9751b-138">Requirement</span></span> | <span data-ttu-id="9751b-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="9751b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9751b-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9751b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="9751b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9751b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9751b-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9751b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="9751b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9751b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9751b-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="9751b-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="9751b-145"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9751b-145"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9751b-146">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="9751b-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="9751b-147"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="9751b-147"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="9751b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="9751b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9751b-149"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9751b-149"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="9751b-150">CLSID</span><span class="sxs-lookup"><span data-stu-id="9751b-150">CLSID</span></span><br/>                    | <span data-ttu-id="9751b-151">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="9751b-151">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="9751b-152">IID</span><span class="sxs-lookup"><span data-stu-id="9751b-152">IID</span></span><br/>                      | <span data-ttu-id="9751b-153">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="9751b-153">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="9751b-154">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9751b-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9751b-155">**SWbemDateTime. getVarDate,**</span><span class="sxs-lookup"><span data-stu-id="9751b-155">**SWbemDateTime.GetVarDate**</span></span>](swbemdatetime-getvardate.md)
</dt> <dt>

[<span data-ttu-id="9751b-156">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="9751b-156">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="9751b-157">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="9751b-157">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

