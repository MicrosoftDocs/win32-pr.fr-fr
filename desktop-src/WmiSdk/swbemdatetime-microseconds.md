---
description: Obtient ou définit une valeur qui représente le composant microsecondes de la valeur DateTime.
ms.assetid: b810b781-86a3-4730-8114-44d10454f7c3
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. microsecondrs (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Microseconds
- ISWbemDateTime.Microseconds
- ISWbemDateTime.get_Microseconds
- ISWbemDateTime.put_Microseconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 94213eb70a98be1af8f8404ddece8bf2f07ca807
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320825"
---
# <a name="swbemdatetimemicroseconds-property"></a><span data-ttu-id="00008-103">SWbemDateTime. microsecondes, propriété</span><span class="sxs-lookup"><span data-stu-id="00008-103">SWbemDateTime.Microseconds property</span></span>

<span data-ttu-id="00008-104">La propriété **microsecondes** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant microsecondes de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="00008-104">The **Microseconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the microseconds component of the datetime value.</span></span>

<span data-ttu-id="00008-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="00008-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="00008-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="00008-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="00008-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="00008-107">Syntax</span></span>


```VB
SWbemDateTime.Microseconds As Long
```



## <a name="property-value"></a><span data-ttu-id="00008-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="00008-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="00008-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="00008-109">Error codes</span></span>

<span data-ttu-id="00008-110">Une fois que vous avez obtenu ou défini la propriété **microsecondes** , l’objet **Err** peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="00008-110">After you get or set the **Microseconds** property, the **Err** object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="00008-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="00008-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="00008-112">La valeur n’était pas comprise dans la plage comprise entre 0 et 999999.</span><span class="sxs-lookup"><span data-stu-id="00008-112">The value was not in the range of 0 through 999999.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="00008-113">Exemples</span><span class="sxs-lookup"><span data-stu-id="00008-113">Examples</span></span>

<span data-ttu-id="00008-114">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="00008-114">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="00008-115">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="00008-115">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="00008-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="00008-116">Requirements</span></span>



| <span data-ttu-id="00008-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="00008-117">Requirement</span></span> | <span data-ttu-id="00008-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="00008-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00008-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00008-119">Minimum supported client</span></span><br/> | <span data-ttu-id="00008-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00008-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00008-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="00008-121">Minimum supported server</span></span><br/> | <span data-ttu-id="00008-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00008-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00008-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="00008-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="00008-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="00008-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="00008-125">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="00008-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="00008-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="00008-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="00008-127">DLL</span><span class="sxs-lookup"><span data-stu-id="00008-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00008-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00008-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="00008-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="00008-129">CLSID</span></span><br/>                    | <span data-ttu-id="00008-130">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="00008-130">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="00008-131">IID</span><span class="sxs-lookup"><span data-stu-id="00008-131">IID</span></span><br/>                      | <span data-ttu-id="00008-132">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="00008-132">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="00008-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00008-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00008-134">**SWbemDateTime.MicrosecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="00008-134">**SWbemDateTime.MicrosecondsSpecified**</span></span>](swbemdatetime-microsecondsspecified.md)
</dt> <dt>

[<span data-ttu-id="00008-135">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="00008-135">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="00008-136">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="00008-136">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

 




