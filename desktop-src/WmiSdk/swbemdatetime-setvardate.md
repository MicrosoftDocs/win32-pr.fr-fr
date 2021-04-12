---
description: Convertit une date au \_ format de date VT au format DateTime CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. SetVarDate (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8641bad2c59f100b689c74e23faf727bc80d2f49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320530"
---
# <a name="swbemdatetimesetvardate-method"></a><span data-ttu-id="53463-103">Méthode SWbemDateTime. SetVarDate</span><span class="sxs-lookup"><span data-stu-id="53463-103">SWbemDateTime.SetVarDate method</span></span>

<span data-ttu-id="53463-104">La méthode **SetVarDate** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une date au format de **\_ Date VT** au format [DateTime CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="53463-104">The **SetVarDate** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the **VT\_DATE** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="53463-105">Une valeur de **\_ Date VT** est une valeur datetime variant qui Visual Basic et à l’aide d’ActiveX.</span><span class="sxs-lookup"><span data-stu-id="53463-105">A **VT\_DATE** value is a variant datetime value that Visual Basic and ActiveX use.</span></span>

<span data-ttu-id="53463-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="53463-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="53463-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53463-107">Syntax</span></span>


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="53463-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53463-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53463-109">*Vdate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="53463-109">*vdate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53463-110">Valeur de date de la variante pour définir l’objet.</span><span class="sxs-lookup"><span data-stu-id="53463-110">The variant date value to set the object.</span></span> <span data-ttu-id="53463-111">Ce paramètre doit être au format **de \_ Date VT** .</span><span class="sxs-lookup"><span data-stu-id="53463-111">This parameter must be in the **VT\_DATE** format.</span></span>

</dd> <dt>

<span data-ttu-id="53463-112">*bIsLocal* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="53463-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="53463-113">Si la **valeur est true**, *Vdate* est interprété comme une heure locale et la propriété de temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct.</span><span class="sxs-lookup"><span data-stu-id="53463-113">If **TRUE**, *vdate* is interpreted as a local time, and the Coordinated Universal Time (UTC) property contains the local time that is converted to the correct UTC offset.</span></span> <span data-ttu-id="53463-114">Quand *bIsLocal* a la valeur **false**, *Vdate* est converti directement en valeur UTC avec un décalage de zéro (0).</span><span class="sxs-lookup"><span data-stu-id="53463-114">When *bIsLocal* is **FALSE**, then *vdate* is converted directly into a UTC value with an offset of zero (0).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53463-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53463-115">Return value</span></span>

<span data-ttu-id="53463-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="53463-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="53463-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="53463-117">Error codes</span></span>

<span data-ttu-id="53463-118">À la fin de la méthode **SetVarDate** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="53463-118">After completing the **SetVarDate** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="53463-119">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="53463-119">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="53463-120">Le format de *Vdate* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="53463-120">The format of *vdate* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53463-121">Notes</span><span class="sxs-lookup"><span data-stu-id="53463-121">Remarks</span></span>

<span data-ttu-id="53463-122">Après un appel réussi à **SetVarDate**, la valeur [**DateTime**](datetime.md) est interprétée comme une valeur DateTime absolue au lieu d’un intervalle, et la propriété [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="53463-122">After a successful call to **SetVarDate**, the [**DATETIME**](datetime.md) value is interpreted as an absolute datetime value instead of an interval, and the [**IsInterval**](swbemdatetime-isinterval.md) property is set to **FALSE**.</span></span>

<span data-ttu-id="53463-123">La fonction intrinsèque Visual Basic ou VBScript Function [CDate](/previous-versions//2dt118h2(v=vs.85)) fournit une valeur [**DateTime**](datetime.md) au format de **\_ Date VT** pour l’entrée dans **SetVarDate**.</span><span class="sxs-lookup"><span data-stu-id="53463-123">The intrinsic Visual Basic or VBScript function [CDate](/previous-versions//2dt118h2(v=vs.85)) provides a [**datetime**](datetime.md) value in the **VT\_DATE** format for input to **SetVarDate**.</span></span>

## <a name="examples"></a><span data-ttu-id="53463-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="53463-124">Examples</span></span>

<span data-ttu-id="53463-125">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="53463-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="53463-126">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="53463-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

<span data-ttu-id="53463-127">L’exemple de code VBScript [date to WMI Date-Time format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript de la Galerie TechNet utilise SetVarDate pour convertir une valeur date-heure normale au format date-heure UTC.</span><span class="sxs-lookup"><span data-stu-id="53463-127">The [Convert Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) VBScript code sample in the TechNet Gallery uses SetVarDate to convert a regular date-time value into the UTC date-time format.</span></span>

## <a name="requirements"></a><span data-ttu-id="53463-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53463-128">Requirements</span></span>



| <span data-ttu-id="53463-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53463-129">Requirement</span></span> | <span data-ttu-id="53463-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="53463-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="53463-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53463-131">Minimum supported client</span></span><br/> | <span data-ttu-id="53463-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="53463-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="53463-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53463-133">Minimum supported server</span></span><br/> | <span data-ttu-id="53463-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="53463-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="53463-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="53463-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="53463-136"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="53463-136"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="53463-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="53463-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="53463-138"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="53463-138"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="53463-139">DLL</span><span class="sxs-lookup"><span data-stu-id="53463-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="53463-140"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53463-140"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="53463-141">CLSID</span><span class="sxs-lookup"><span data-stu-id="53463-141">CLSID</span></span><br/>                    | <span data-ttu-id="53463-142">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="53463-142">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="53463-143">IID</span><span class="sxs-lookup"><span data-stu-id="53463-143">IID</span></span><br/>                      | <span data-ttu-id="53463-144">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="53463-144">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="53463-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53463-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53463-146">**SWbemDateTime.SetFileTime**</span><span class="sxs-lookup"><span data-stu-id="53463-146">**SWbemDateTime.SetFileTime**</span></span>](swbemdatetime-setfiletime.md)
</dt> <dt>

[<span data-ttu-id="53463-147">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="53463-147">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="53463-148">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="53463-148">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

