---
description: Obtient ou définit une valeur qui représente le composant « mois » de la valeur DateTime.
ms.assetid: 05818f0a-7e15-4ddd-a6a7-9d16ae82cd3c
ms.tgt_platform: multiple
title: Propriété SWbemDateTime. month (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Month
- ISWbemDateTime.Month
- ISWbemDateTime.get_Month
- ISWbemDateTime.put_Month
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 73769d73cffc5b9731cfd55785e2fa087182b33b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521998"
---
# <a name="swbemdatetimemonth-property"></a><span data-ttu-id="bf1b1-103">SWbemDateTime. month (propriété)</span><span class="sxs-lookup"><span data-stu-id="bf1b1-103">SWbemDateTime.Month property</span></span>

<span data-ttu-id="bf1b1-104">La propriété **Month** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant Month de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="bf1b1-104">The **Month** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the month component of the datetime value.</span></span> <span data-ttu-id="bf1b1-105">Le nombre doit être compris entre 01 et 12, ou l’erreur **wbemValueOutOfRange** est retournée.</span><span class="sxs-lookup"><span data-stu-id="bf1b1-105">The number must be in the range of 01 through 12 or the error **wbemValueOutOfRange** is returned.</span></span>

<span data-ttu-id="bf1b1-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="bf1b1-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="bf1b1-107">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="bf1b1-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf1b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf1b1-108">Syntax</span></span>


```VB
SWbemDateTime.Month As Long
```



## <a name="property-value"></a><span data-ttu-id="bf1b1-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="bf1b1-109">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="bf1b1-110">Exemples</span><span class="sxs-lookup"><span data-stu-id="bf1b1-110">Examples</span></span>

<span data-ttu-id="bf1b1-111">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="bf1b1-111">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="bf1b1-112">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="bf1b1-112">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf1b1-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf1b1-113">Requirements</span></span>



| <span data-ttu-id="bf1b1-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf1b1-114">Requirement</span></span> | <span data-ttu-id="bf1b1-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf1b1-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf1b1-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf1b1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="bf1b1-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf1b1-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bf1b1-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf1b1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="bf1b1-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf1b1-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bf1b1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf1b1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf1b1-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf1b1-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf1b1-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="bf1b1-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf1b1-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="bf1b1-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="bf1b1-124">DLL</span><span class="sxs-lookup"><span data-stu-id="bf1b1-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf1b1-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf1b1-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="bf1b1-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="bf1b1-126">CLSID</span></span><br/>                    | <span data-ttu-id="bf1b1-127">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bf1b1-127">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="bf1b1-128">IID</span><span class="sxs-lookup"><span data-stu-id="bf1b1-128">IID</span></span><br/>                      | <span data-ttu-id="bf1b1-129">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="bf1b1-129">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="bf1b1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bf1b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf1b1-131">**SWbemDateTime.MonthSpecified**</span><span class="sxs-lookup"><span data-stu-id="bf1b1-131">**SWbemDateTime.MonthSpecified**</span></span>](swbemdatetime-monthspecified.md)
</dt> <dt>

[<span data-ttu-id="bf1b1-132">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="bf1b1-132">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="bf1b1-133">Date/heure</span><span class="sxs-lookup"><span data-stu-id="bf1b1-133">DATETIME</span></span>](datetime.md)
</dt> </dl>

 

 




