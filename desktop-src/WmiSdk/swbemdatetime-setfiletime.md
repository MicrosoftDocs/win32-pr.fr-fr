---
description: Convertit une date au format FILETIME de chaîne au format DateTime CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: Méthode SWbemDateTime. SetFileTime (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114878"
---
# <a name="swbemdatetimesetfiletime-method"></a><span data-ttu-id="f2759-103">Méthode SWbemDateTime. SetFileTime</span><span class="sxs-lookup"><span data-stu-id="f2759-103">SWbemDateTime.SetFileTime method</span></span>

<span data-ttu-id="f2759-104">La méthode **SetFileTime** de l’objet [**SWbemDateTime**](swbemdatetime.md) convertit une date au format **fileTime** de chaîne au format [DateTime CIM](date-and-time-format.md) .</span><span class="sxs-lookup"><span data-stu-id="f2759-104">The **SetFileTime** method of the [**SWbemDateTime**](swbemdatetime.md) object converts a date in the string **FILETIME** format to the [CIM datetime](date-and-time-format.md) format.</span></span>

<span data-ttu-id="f2759-105">Le format **fileTime** est une structure datetime de 64 bits qui représente le nombre d’unités de 100 nanosecondes depuis le début du 1er janvier 1601.</span><span class="sxs-lookup"><span data-stu-id="f2759-105">The **FILETIME** format is a 64-bit datetime structure that represents the number of 100-nanosecond units since the beginning of January 1, 1601.</span></span> <span data-ttu-id="f2759-106">Windows Management Instrumentation (WMI) traite les valeurs **fileTime** comme des représentations sous forme de chaîne de nombres 64 bits non signés.</span><span class="sxs-lookup"><span data-stu-id="f2759-106">Windows Management Instrumentation (WMI) treats **FILETIME** values as string representations of unsigned 64-bit numbers.</span></span>

<span data-ttu-id="f2759-107">Pour plus d’explications sur la syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f2759-107">For the syntax explanation, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2759-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2759-108">Syntax</span></span>


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a><span data-ttu-id="f2759-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2759-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2759-110">*strFileTime* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2759-110">*strFileTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2759-111">Valeur **fileTime** utilisée pour définir l’objet.</span><span class="sxs-lookup"><span data-stu-id="f2759-111">**FILETIME** value used to set the object.</span></span>

</dd> <dt>

<span data-ttu-id="f2759-112">*bIsLocal* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="f2759-112">*bIsLocal* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="f2759-113">Si la **valeur est true**, *strFileTime* est interprété comme une heure locale.</span><span class="sxs-lookup"><span data-stu-id="f2759-113">If **TRUE**, *strFileTime* is interpreted as a local time.</span></span> <span data-ttu-id="f2759-114">La propriété temps universel coordonné (UTC, Universal Time Coordinated) contient l’heure locale convertie en décalage UTC correct.</span><span class="sxs-lookup"><span data-stu-id="f2759-114">The Coordinated Universal Time (UTC) property contains the local time converted to the correct UTC offset.</span></span> <span data-ttu-id="f2759-115">Quand *bIsLocal* a la valeur **false**, *strFileTime* est converti directement en valeur UTC avec un décalage égal à 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="f2759-115">When *bIsLocal* is **FALSE**, then *strFileTime* is converted directly into a UTC value with an offset of 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2759-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2759-116">Return value</span></span>

<span data-ttu-id="f2759-117">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="f2759-117">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="f2759-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f2759-118">Error codes</span></span>

<span data-ttu-id="f2759-119">À la fin de la méthode **SetFileTime** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur figurant dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="f2759-119">After completing the **SetFileTime** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="f2759-120">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="f2759-120">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="f2759-121">Le format de *strFileTime* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="f2759-121">The format of *strFileTime* is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2759-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f2759-122">Remarks</span></span>

<span data-ttu-id="f2759-123">Après un appel réussi à **SetFileTime**, la valeur [**DateTime**](datetime.md) est toujours interprétée comme une valeur absolue (**DateTime**) et [**IsInterval**](swbemdatetime-isinterval.md) est défini sur **false**.</span><span class="sxs-lookup"><span data-stu-id="f2759-123">After a successful call to **SetFileTime**, the [**datetime**](datetime.md) value is always interpreted as an absolute (**datetime**) value, and [**IsInterval**](swbemdatetime-isinterval.md) is set to **FALSE**.</span></span>

## <a name="examples"></a><span data-ttu-id="f2759-124">Exemples</span><span class="sxs-lookup"><span data-stu-id="f2759-124">Examples</span></span>

<span data-ttu-id="f2759-125">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f2759-125">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f2759-126">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f2759-126">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2759-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2759-127">Requirements</span></span>



| <span data-ttu-id="f2759-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2759-128">Requirement</span></span> | <span data-ttu-id="f2759-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2759-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2759-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2759-130">Minimum supported client</span></span><br/> | <span data-ttu-id="f2759-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2759-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f2759-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2759-132">Minimum supported server</span></span><br/> | <span data-ttu-id="f2759-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2759-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f2759-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="f2759-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="f2759-135"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f2759-135"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f2759-136">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f2759-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2759-137"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f2759-137"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f2759-138">DLL</span><span class="sxs-lookup"><span data-stu-id="f2759-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2759-139"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2759-139"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2759-140">CLSID</span><span class="sxs-lookup"><span data-stu-id="f2759-140">CLSID</span></span><br/>                    | <span data-ttu-id="f2759-141">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f2759-141">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f2759-142">IID</span><span class="sxs-lookup"><span data-stu-id="f2759-142">IID</span></span><br/>                      | <span data-ttu-id="f2759-143">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f2759-143">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f2759-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2759-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2759-145">**SWbemDateTime.SetVarDate**</span><span class="sxs-lookup"><span data-stu-id="f2759-145">**SWbemDateTime.SetVarDate**</span></span>](swbemdatetime-setvardate.md)
</dt> <dt>

[<span data-ttu-id="f2759-146">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f2759-146">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f2759-147">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="f2759-147">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

