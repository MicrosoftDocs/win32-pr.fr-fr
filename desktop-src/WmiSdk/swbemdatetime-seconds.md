---
description: Obtient ou définit une valeur qui représente le composant « secondes » de la valeur DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: SWbemDateTime. seconds, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0ef4ef15f13bf3d8dfc9272b2a3b734c3678f8e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524975"
---
# <a name="swbemdatetimeseconds-property"></a><span data-ttu-id="fdf80-103">SWbemDateTime. seconds, propriété</span><span class="sxs-lookup"><span data-stu-id="fdf80-103">SWbemDateTime.Seconds property</span></span>

<span data-ttu-id="fdf80-104">La propriété **seconds** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit une valeur qui représente le composant « secondes » de la valeur DateTime.</span><span class="sxs-lookup"><span data-stu-id="fdf80-104">The **Seconds** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets a value that represents the seconds component of the datetime value.</span></span>

<span data-ttu-id="fdf80-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="fdf80-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="fdf80-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="fdf80-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdf80-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fdf80-107">Syntax</span></span>


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a><span data-ttu-id="fdf80-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="fdf80-108">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="fdf80-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="fdf80-109">Error codes</span></span>

<span data-ttu-id="fdf80-110">Une fois que vous avez obtenu ou défini la propriété **seconds** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fdf80-110">After you get or set the **Seconds** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="fdf80-111">**wbemErrValueOutOfRange** -2147749931 (0x8004102B)</span><span class="sxs-lookup"><span data-stu-id="fdf80-111">**wbemErrValueOutOfRange** - 2147749931 (0x8004102B)</span></span>
</dt> <dd>

<span data-ttu-id="fdf80-112">La valeur n’était pas comprise dans la plage comprise entre 0 et 59.</span><span class="sxs-lookup"><span data-stu-id="fdf80-112">The value was not in the range of 0 through 59.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fdf80-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fdf80-113">Remarks</span></span>

<span data-ttu-id="fdf80-114">La propriété **SWbemDateTime. seconds** peut contenir une valeur incorrecte si la propriété [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) a été définie sur 1.</span><span class="sxs-lookup"><span data-stu-id="fdf80-114">The **SWbemDateTime.Seconds** property may contain an incorrect value if the [**SWbemDateTime.Minutes**](swbemdatetime-minutes.md) property has been set to 1.</span></span> <span data-ttu-id="fdf80-115">Elle contient une valeur qui est décalée d’une seconde en raison d’une erreur d’arrondi qui se produit lorsqu’une valeur [**DateTime**](datetime.md) CIM est convertie en valeur de **\_ Date VT** .</span><span class="sxs-lookup"><span data-stu-id="fdf80-115">It contains a value that is offset by one second because of a rounding error that occurs when a CIM [**DATETIME**](datetime.md) value is translated to a **VT\_DATE** value.</span></span> <span data-ttu-id="fdf80-116">Si la propriété **minutes** est définie sur 0 (zéro) à la place, la propriété **seconds** retourne la valeur correcte.</span><span class="sxs-lookup"><span data-stu-id="fdf80-116">If the **Minutes** property is set to 0 (zero) instead, then the **Seconds** property returns the correct value.</span></span>

## <a name="examples"></a><span data-ttu-id="fdf80-117">Exemples</span><span class="sxs-lookup"><span data-stu-id="fdf80-117">Examples</span></span>

<span data-ttu-id="fdf80-118">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="fdf80-118">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="fdf80-119">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="fdf80-119">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdf80-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fdf80-120">Requirements</span></span>



| <span data-ttu-id="fdf80-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fdf80-121">Requirement</span></span> | <span data-ttu-id="fdf80-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="fdf80-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fdf80-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdf80-123">Minimum supported client</span></span><br/> | <span data-ttu-id="fdf80-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fdf80-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fdf80-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fdf80-125">Minimum supported server</span></span><br/> | <span data-ttu-id="fdf80-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fdf80-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fdf80-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fdf80-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="fdf80-128"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdf80-128"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fdf80-129">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="fdf80-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="fdf80-130"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fdf80-130"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fdf80-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fdf80-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fdf80-132"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fdf80-132"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="fdf80-133">CLSID</span><span class="sxs-lookup"><span data-stu-id="fdf80-133">CLSID</span></span><br/>                    | <span data-ttu-id="fdf80-134">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="fdf80-134">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="fdf80-135">IID</span><span class="sxs-lookup"><span data-stu-id="fdf80-135">IID</span></span><br/>                      | <span data-ttu-id="fdf80-136">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="fdf80-136">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="fdf80-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fdf80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdf80-138">**SWbemDateTime.SecondsSpecified**</span><span class="sxs-lookup"><span data-stu-id="fdf80-138">**SWbemDateTime.SecondsSpecified**</span></span>](swbemdatetime-secondsspecified.md)
</dt> <dt>

[<span data-ttu-id="fdf80-139">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="fdf80-139">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="fdf80-140">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="fdf80-140">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

