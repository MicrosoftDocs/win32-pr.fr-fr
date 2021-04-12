---
description: Obtient ou définit une valeur qui représente le composant « heures » de la valeur DateTime.
ms.assetid: 83f084fa-57a5-4467-acea-7e19de82a91f
ms.tgt_platform: multiple
title: SWbemDateTime. hours, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Hours
- ISWbemDateTime.Hours
- ISWbemDateTime.get_Hours
- ISWbemDateTime.put_Hours
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 27edb3c209e2e95ae7aff20930d260f8f6d44427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210199"
---
# <a name="swbemdatetimehours-property"></a><span data-ttu-id="bf288-103">SWbemDateTime. hours, propriété</span><span class="sxs-lookup"><span data-stu-id="bf288-103">SWbemDateTime.Hours property</span></span>

<span data-ttu-id="bf288-104">La propriété **hours** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant hours de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="bf288-104">The **Hours** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the hours component of the datetime value.</span></span>

<span data-ttu-id="bf288-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bf288-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bf288-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bf288-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf288-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf288-107">Syntax</span></span>


```VB
SWbemDateTime.Hours As Long
```



## <a name="property-value"></a><span data-ttu-id="bf288-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bf288-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="bf288-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="bf288-109">Error codes</span></span>

<span data-ttu-id="bf288-110">Une fois que vous avez obtenu ou défini la propriété **hours** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="bf288-110">After you get or set the **Hours** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="bf288-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="bf288-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="bf288-112">La valeur n’est pas comprise dans la plage comprise entre 0 et 23.</span><span class="sxs-lookup"><span data-stu-id="bf288-112">The value was not in the range of 0 through 23.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="bf288-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="bf288-113">Examples</span></span>

<span data-ttu-id="bf288-114">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="bf288-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="bf288-115">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="bf288-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf288-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf288-116">Requirements</span></span>



| <span data-ttu-id="bf288-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf288-117">Requirement</span></span> | <span data-ttu-id="bf288-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf288-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf288-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf288-119">Minimum supported client</span></span><br/> | <span data-ttu-id="bf288-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf288-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf288-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf288-121">Minimum supported server</span></span><br/> | <span data-ttu-id="bf288-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf288-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf288-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf288-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf288-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf288-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf288-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bf288-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf288-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf288-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf288-127">DLL</span><span class="sxs-lookup"><span data-stu-id="bf288-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf288-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf288-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf288-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf288-129">CLSID</span></span><br/>                    | <span data-ttu-id="bf288-130">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bf288-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="bf288-131">IID</span><span class="sxs-lookup"><span data-stu-id="bf288-131">IID</span></span><br/>                      | <span data-ttu-id="bf288-132">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bf288-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bf288-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf288-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf288-134">**SWbemDateTime.HoursSpecified**</span><span class="sxs-lookup"><span data-stu-id="bf288-134">**SWbemDateTime.HoursSpecified**</span></span>](swbemdatetime-hoursspecified.md)
</dt> <dt>

[<span data-ttu-id="bf288-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bf288-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bf288-136">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="bf288-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

