---
description: Obtient ou définit une valeur qui représente le composant « minutes » de la valeur DateTime.
ms.assetid: a52a66c2-f7ab-48d0-bdee-a07984ed3bc2
ms.tgt_platform: multiple
title: SWbemDateTime. minutes, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Minutes
- ISWbemDateTime.Minutes
- ISWbemDateTime.get_Minutes
- ISWbemDateTime.put_Minutes
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cce55d731916d0e8180de1bde495566d4ed22c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106539740"
---
# <a name="swbemdatetimeminutes-property"></a><span data-ttu-id="ec063-103">SWbemDateTime. minutes, propriété</span><span class="sxs-lookup"><span data-stu-id="ec063-103">SWbemDateTime.Minutes property</span></span>

<span data-ttu-id="ec063-104">La propriété **minutes** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant « minutes » de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="ec063-104">The **Minutes** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the minutes component of the datetime value.</span></span>

<span data-ttu-id="ec063-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ec063-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="ec063-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="ec063-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec063-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec063-107">Syntax</span></span>


```VB
SWbemDateTime.Minutes As Long
```



## <a name="property-value"></a><span data-ttu-id="ec063-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="ec063-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="ec063-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="ec063-109">Error codes</span></span>

<span data-ttu-id="ec063-110">Une fois que vous avez obtenu ou défini la propriété **minutes** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="ec063-110">After you get or set the **Minutes** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="ec063-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="ec063-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="ec063-112">La valeur n’était pas comprise dans la plage comprise entre 0 et 59.</span><span class="sxs-lookup"><span data-stu-id="ec063-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec063-113">Notes</span><span class="sxs-lookup"><span data-stu-id="ec063-113">Remarks</span></span>

<span data-ttu-id="ec063-114">Si la propriété **SWbemDateTime. minutes** est définie sur 1, la propriété [**SWbemDateTime. seconds**](swbemdatetime-seconds.md) contient une valeur qui est décalée d’une seconde une erreur d’arrondi qui se produit lorsqu’une valeur **DateTime** CIM est convertie en valeur de **\_ Date VT** .</span><span class="sxs-lookup"><span data-stu-id="ec063-114">If the **SWbemDateTime.Minutes** property is set to 1, then the [**SWbemDateTime.Seconds**](swbemdatetime-seconds.md) property contains a value that is offset by one second a rounding error that occurs when a CIM **datetime** value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="ec063-115">Si la propriété **minutes** est définie sur 0, la propriété **seconds** retourne la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="ec063-115">If the **Minutes** property is set to 0 instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="ec063-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="ec063-116">Examples</span></span>

<span data-ttu-id="ec063-117">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="ec063-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="ec063-118">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="ec063-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ec063-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ec063-119">Requirements</span></span>



| <span data-ttu-id="ec063-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ec063-120">Requirement</span></span> | <span data-ttu-id="ec063-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ec063-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec063-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec063-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ec063-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec063-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec063-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ec063-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ec063-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec063-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec063-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ec063-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ec063-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ec063-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ec063-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="ec063-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="ec063-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ec063-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ec063-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ec063-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec063-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec063-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ec063-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="ec063-132">CLSID</span></span><br/>                    | <span data-ttu-id="ec063-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="ec063-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="ec063-134">IID</span><span class="sxs-lookup"><span data-stu-id="ec063-134">IID</span></span><br/>                      | <span data-ttu-id="ec063-135">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="ec063-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="ec063-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec063-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec063-137">**SWbemDateTime.MinutesSpecified**</span><span class="sxs-lookup"><span data-stu-id="ec063-137">**SWbemDateTime.MinutesSpecified**</span></span>](swbemdatetime-minutesspecified.md)
</dt> <dt>

[<span data-ttu-id="ec063-138">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="ec063-138">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="ec063-139">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="ec063-139">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

