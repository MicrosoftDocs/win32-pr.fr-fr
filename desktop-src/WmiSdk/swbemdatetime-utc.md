---
description: Obtient ou définit la représentation en temps universel coordonné (UTC) de la valeur DateTime.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. UTC (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 80a4c32e47b94289f66999fdbf1f7daf5f9f03cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524565"
---
# <a name="swbemdatetimeutc-property"></a><span data-ttu-id="32d8d-103">SWbemDateTime. UTC, propriété</span><span class="sxs-lookup"><span data-stu-id="32d8d-103">SWbemDateTime.UTC property</span></span>

<span data-ttu-id="32d8d-104">La propriété **UTC** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit la représentation en temps universel coordonné (UTC) de la valeur **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="32d8d-104">The **UTC** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the Coordinated Universal Times (UTC) representation of the **datetime** value.</span></span> <span data-ttu-id="32d8d-105">UTC est l’heure définie par la norme de l’heure du monde.</span><span class="sxs-lookup"><span data-stu-id="32d8d-105">UTC is the time as set by the World Time Standard.</span></span> <span data-ttu-id="32d8d-106">L’heure UTC a remplacé l’heure GMT (Greenwich Mean Time).</span><span class="sxs-lookup"><span data-stu-id="32d8d-106">UTC has replaced Greenwich Mean Time (GMT).</span></span> <span data-ttu-id="32d8d-107">Une valeur UTC avec un décalage égal à zéro est identique à l’heure GMT avec un décalage de zéro.</span><span class="sxs-lookup"><span data-stu-id="32d8d-107">A UTC value with a zero offset is the same as GMT with a zero offset.</span></span> <span data-ttu-id="32d8d-108">Le nombre signé doit être compris entre-720 et 720, ou l’erreur **wbemErrValueOutOfRange** est retournée.</span><span class="sxs-lookup"><span data-stu-id="32d8d-108">The signed number must be in the range of -720 through 720 or the error **wbemErrValueOutOfRange** is returned.</span></span>

<span data-ttu-id="32d8d-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="32d8d-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="32d8d-110">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="32d8d-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32d8d-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32d8d-111">Syntax</span></span>


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a><span data-ttu-id="32d8d-112">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="32d8d-112">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="32d8d-113">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="32d8d-113">Error codes</span></span>

<span data-ttu-id="32d8d-114">Une fois que vous avez obtenu ou défini la propriété **UTC** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="32d8d-114">After you get or set the **UTC** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="32d8d-115">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="32d8d-115">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="32d8d-116">La valeur n’était pas comprise dans la plage comprise entre-720 et 720.</span><span class="sxs-lookup"><span data-stu-id="32d8d-116">The value was not in the range of -720 through 720.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="32d8d-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="32d8d-117">Examples</span></span>

<span data-ttu-id="32d8d-118">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="32d8d-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="32d8d-119">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="32d8d-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="32d8d-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32d8d-120">Requirements</span></span>



| <span data-ttu-id="32d8d-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32d8d-121">Requirement</span></span> | <span data-ttu-id="32d8d-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="32d8d-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32d8d-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32d8d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="32d8d-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32d8d-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="32d8d-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32d8d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="32d8d-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32d8d-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="32d8d-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="32d8d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="32d8d-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="32d8d-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="32d8d-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="32d8d-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="32d8d-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="32d8d-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="32d8d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="32d8d-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32d8d-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32d8d-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="32d8d-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="32d8d-133">CLSID</span></span><br/>                    | <span data-ttu-id="32d8d-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="32d8d-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="32d8d-135">IID</span><span class="sxs-lookup"><span data-stu-id="32d8d-135">IID</span></span><br/>                      | <span data-ttu-id="32d8d-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="32d8d-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="32d8d-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32d8d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32d8d-138">**SWbemDateTime.UTCSpecified**</span><span class="sxs-lookup"><span data-stu-id="32d8d-138">**SWbemDateTime.UTCSpecified**</span></span>](swbemdatetime-utcspecified.md)
</dt> <dt>

[<span data-ttu-id="32d8d-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="32d8d-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="32d8d-140">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="32d8d-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

