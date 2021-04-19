---
description: Obtient ou définit une valeur qui représente le composant « année » de la valeur DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. Year (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528274"
---
# <a name="swbemdatetimeyear-property"></a><span data-ttu-id="768a0-103">SWbemDateTime. Year, propriété</span><span class="sxs-lookup"><span data-stu-id="768a0-103">SWbemDateTime.Year property</span></span>

<span data-ttu-id="768a0-104">La propriété **year** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant Year de la valeur [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="768a0-104">The **Year** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the year component of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="768a0-105">La valeur doit être comprise dans la plage 0000-9999 ou l’erreur wbemErrValueOutOfRange est retournée.</span><span class="sxs-lookup"><span data-stu-id="768a0-105">The value must be in the range of 0000 - 9999 or the error wbemErrValueOutOfRange is returned.</span></span>

<span data-ttu-id="768a0-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="768a0-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="768a0-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="768a0-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="768a0-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="768a0-108">Syntax</span></span>


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a><span data-ttu-id="768a0-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="768a0-109">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="768a0-110">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="768a0-110">Error codes</span></span>

<span data-ttu-id="768a0-111">Une fois que vous avez obtenu ou défini la propriété **year** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="768a0-111">After you get or set the **Year** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="768a0-112">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="768a0-112">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="768a0-113">La valeur n’était pas comprise dans la plage de 0000 à 9999.</span><span class="sxs-lookup"><span data-stu-id="768a0-113">The value was not in the range of 0000 through 9999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="768a0-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="768a0-114">Examples</span></span>

<span data-ttu-id="768a0-115">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="768a0-115">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="768a0-116">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="768a0-116">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="768a0-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="768a0-117">Requirements</span></span>



| <span data-ttu-id="768a0-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="768a0-118">Requirement</span></span> | <span data-ttu-id="768a0-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="768a0-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="768a0-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="768a0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="768a0-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="768a0-121">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="768a0-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="768a0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="768a0-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="768a0-123">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="768a0-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="768a0-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="768a0-125"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="768a0-125"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="768a0-126">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="768a0-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="768a0-127"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="768a0-127"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="768a0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="768a0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="768a0-129"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="768a0-129"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="768a0-130">CLSID</span><span class="sxs-lookup"><span data-stu-id="768a0-130">CLSID</span></span><br/>                    | <span data-ttu-id="768a0-131">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="768a0-131">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="768a0-132">IID</span><span class="sxs-lookup"><span data-stu-id="768a0-132">IID</span></span><br/>                      | <span data-ttu-id="768a0-133">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="768a0-133">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="768a0-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="768a0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="768a0-135">**SWbemDateTime.YearSpecified**</span><span class="sxs-lookup"><span data-stu-id="768a0-135">**SWbemDateTime.YearSpecified**</span></span>](swbemdatetime-yearspecified.md)
</dt> <dt>

[<span data-ttu-id="768a0-136">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="768a0-136">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="768a0-137">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="768a0-137">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

