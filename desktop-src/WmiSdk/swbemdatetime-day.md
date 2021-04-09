---
description: Obtient ou définit une valeur qui représente le composant « jour » de la valeur DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: SWbemDateTime. Day, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952859"
---
# <a name="swbemdatetimeday-property"></a><span data-ttu-id="f043e-103">SWbemDateTime. Day, propriété</span><span class="sxs-lookup"><span data-stu-id="f043e-103">SWbemDateTime.Day property</span></span>

<span data-ttu-id="f043e-104">La propriété **Day** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant Day de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="f043e-104">The **Day** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the day component of the datetime value.</span></span> <span data-ttu-id="f043e-105">La valeur doit être comprise entre 1 et 31 si [**IsInterval**](swbemdatetime-isinterval.md) a la valeur **false**.</span><span class="sxs-lookup"><span data-stu-id="f043e-105">The value must be in the range of 1 through 31 if [**IsInterval**](swbemdatetime-isinterval.md) is **FALSE**.</span></span> <span data-ttu-id="f043e-106">Toutefois, la vérification des erreurs n’est pas sensible à la valeur du mois.</span><span class="sxs-lookup"><span data-stu-id="f043e-106">However, error checking is not sensitive to the month value.</span></span> <span data-ttu-id="f043e-107">Par conséquent, la valeur dans la plage de 31 ne retourne pas d’erreur dans les cas où la valeur [**SWbemDateTime. month**](swbemdatetime-month.md) correspond à un mois de moins de 31 jours (février, avril, juin, septembre).</span><span class="sxs-lookup"><span data-stu-id="f043e-107">Thus, the in-range value of 31 will not return an error in the cases where the [**SWbemDateTime.Month**](swbemdatetime-month.md) value is for a month of fewer than 31 days (February, April, June, September, November).</span></span>

<span data-ttu-id="f043e-108">La valeur par défaut pour **Day** est 01.</span><span class="sxs-lookup"><span data-stu-id="f043e-108">The default value for **Day** is 01.</span></span>

<span data-ttu-id="f043e-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="f043e-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="f043e-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="f043e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f043e-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f043e-111">Syntax</span></span>


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a><span data-ttu-id="f043e-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="f043e-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="f043e-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="f043e-113">Error codes</span></span>

<span data-ttu-id="f043e-114">Une fois que vous avez obtenu ou défini la propriété **Day** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="f043e-114">After you get or set the **Day** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="f043e-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="f043e-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="f043e-116">Si [**IsInterval**](swbemdatetime-isinterval.md) a la **valeur true** et que la plage des valeurs correctes est supérieure à 0 à 99999999.</span><span class="sxs-lookup"><span data-stu-id="f043e-116">If [**IsInterval**](swbemdatetime-isinterval.md) is **TRUE** and the range of correct values exceeds 0 through 99999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f043e-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="f043e-117">Examples</span></span>

<span data-ttu-id="f043e-118">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="f043e-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="f043e-119">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="f043e-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f043e-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f043e-120">Requirements</span></span>



| <span data-ttu-id="f043e-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f043e-121">Requirement</span></span> | <span data-ttu-id="f043e-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f043e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f043e-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f043e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f043e-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f043e-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f043e-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f043e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f043e-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f043e-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f043e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="f043e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="f043e-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f043e-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f043e-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="f043e-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="f043e-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f043e-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f043e-131">DLL</span><span class="sxs-lookup"><span data-stu-id="f043e-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f043e-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f043e-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f043e-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="f043e-133">CLSID</span></span><br/>                    | <span data-ttu-id="f043e-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f043e-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="f043e-135">IID</span><span class="sxs-lookup"><span data-stu-id="f043e-135">IID</span></span><br/>                      | <span data-ttu-id="f043e-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="f043e-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="f043e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f043e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f043e-138">**SWbemDateTime.DaySpecified**</span><span class="sxs-lookup"><span data-stu-id="f043e-138">**SWbemDateTime.DaySpecified**</span></span>](swbemdatetime-dayspecified.md)
</dt> <dt>

[<span data-ttu-id="f043e-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="f043e-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="f043e-140">Date/heure</span><span class="sxs-lookup"><span data-stu-id="f043e-140">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

