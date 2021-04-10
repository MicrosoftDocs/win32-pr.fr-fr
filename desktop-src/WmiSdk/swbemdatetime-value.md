---
description: Obtient ou définit la date CIM brute au format DMTF (Distributed Management Task Force).
ms.assetid: 426a60d5-c364-406e-8346-049a13d59c7f
ms.tgt_platform: multiple
title: SWbemDateTime. Value, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Value
- ISWbemDateTime.Value
- ISWbemDateTime.get_Value
- ISWbemDateTime.put_Value
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2ecb3a42a865559ba9b3c3e5fbec7302f975fa0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114875"
---
# <a name="swbemdatetimevalue-property"></a><span data-ttu-id="d99b2-103">SWbemDateTime. Value (propriété)</span><span class="sxs-lookup"><span data-stu-id="d99b2-103">SWbemDateTime.Value property</span></span>

<span data-ttu-id="d99b2-104">La propriété **value** de l’objet [**SWbemDateTime**](swbemdatetime.md) obtient ou définit la date brute CIM au format DMTF (Distributed Management Task Force).</span><span class="sxs-lookup"><span data-stu-id="d99b2-104">The **Value** property of the [**SWbemDateTime**](swbemdatetime.md) object gets or sets the raw CIM date in the DMTF (Distributed Management Task Force) format.</span></span> <span data-ttu-id="d99b2-105">Le format DMTF est une représentation sous forme de chaîne de la valeur [**DateTime**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="d99b2-105">The DMTF format is a string representation of the [**DATETIME**](datetime.md) value.</span></span> <span data-ttu-id="d99b2-106">Il s’agit de la propriété par défaut pour les objets **SWbemDateTime** .</span><span class="sxs-lookup"><span data-stu-id="d99b2-106">This property is the default property for **SWbemDateTime** objects.</span></span> <span data-ttu-id="d99b2-107">La valeur par défaut de la propriété **value** est 00000101000000.000000 + 000.</span><span class="sxs-lookup"><span data-stu-id="d99b2-107">The **Value** property has a default value of 00000101000000.000000+000.</span></span>

<span data-ttu-id="d99b2-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d99b2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="d99b2-109">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="d99b2-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d99b2-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d99b2-110">Syntax</span></span>


```VB
SWbemDateTime.Value As String
```



## <a name="property-value"></a><span data-ttu-id="d99b2-111">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="d99b2-111">Property value</span></span>

## <a name="error-codes"></a><span data-ttu-id="d99b2-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d99b2-112">Error codes</span></span>

<span data-ttu-id="d99b2-113">Une fois que vous avez obtenu ou défini la propriété **valeur** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir le code d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d99b2-113">After you get or set the **Value** property, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain the error code below.</span></span>

<dl> <dt>

<span data-ttu-id="d99b2-114">**wbemErrInvalidSyntax** -2147749921 (0x80041021)</span><span class="sxs-lookup"><span data-stu-id="d99b2-114">**wbemErrInvalidSyntax** - 2147749921 (0x80041021)</span></span>
</dt> <dd>

<span data-ttu-id="d99b2-115">Le format de *strValue* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d99b2-115">The format of *strValue* is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d99b2-116">Exemples</span><span class="sxs-lookup"><span data-stu-id="d99b2-116">Examples</span></span>

<span data-ttu-id="d99b2-117">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs [**DateTime**](datetime.md) CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="d99b2-117">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM [**DATETIME**](datetime.md) values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="d99b2-118">Pour obtenir une description du format **DateTime** CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="d99b2-118">For a description of the CIM **DATETIME** format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d99b2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d99b2-119">Requirements</span></span>



| <span data-ttu-id="d99b2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d99b2-120">Requirement</span></span> | <span data-ttu-id="d99b2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d99b2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d99b2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d99b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d99b2-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d99b2-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d99b2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d99b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d99b2-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d99b2-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d99b2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="d99b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d99b2-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d99b2-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d99b2-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d99b2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="d99b2-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d99b2-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d99b2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="d99b2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d99b2-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d99b2-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d99b2-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="d99b2-132">CLSID</span></span><br/>                    | <span data-ttu-id="d99b2-133">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="d99b2-133">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="d99b2-134">IID</span><span class="sxs-lookup"><span data-stu-id="d99b2-134">IID</span></span><br/>                      | <span data-ttu-id="d99b2-135">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="d99b2-135">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d99b2-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d99b2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d99b2-137">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="d99b2-137">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="d99b2-138">**Date/heure**</span><span class="sxs-lookup"><span data-stu-id="d99b2-138">**DATETIME**</span></span>](datetime.md)
</dt> </dl>

 

