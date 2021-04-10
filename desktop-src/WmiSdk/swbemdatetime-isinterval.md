---
description: Valeur booléenne qui indique si un champ dans une valeur DateTime CIM doit être interprété comme un intervalle.
ms.assetid: ba5fcf17-7c26-4960-9da9-e380d90e5f3e
ms.tgt_platform: multiple
title: SWbemDateTime. IsInterval, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.IsInterval
- ISWbemDateTime.IsInterval
- ISWbemDateTime.get_IsInterval
- ISWbemDateTime.put_IsInterval
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 468ea16de4f1206a9a15c58c2c7891df8afd4c19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210734"
---
# <a name="swbemdatetimeisinterval-property"></a><span data-ttu-id="58bc8-103">SWbemDateTime. IsInterval, propriété</span><span class="sxs-lookup"><span data-stu-id="58bc8-103">SWbemDateTime.IsInterval property</span></span>

<span data-ttu-id="58bc8-104">La propriété **IsInterval** de l’objet [**SWbemDateTime**](swbemdatetime.md) est une valeur booléenne qui indique si un champ d’une valeur DateTime CIM doit être interprété comme un intervalle.</span><span class="sxs-lookup"><span data-stu-id="58bc8-104">The **IsInterval** property of the [**SWbemDateTime**](swbemdatetime.md) object is a Boolean value that indicates whether any field in a CIM datetime value should be interpreted as an interval.</span></span>

<span data-ttu-id="58bc8-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="58bc8-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="58bc8-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="58bc8-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="58bc8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58bc8-107">Syntax</span></span>


```VB
SWbemDateTime.IsInterval As boolean
```



## <a name="property-value"></a><span data-ttu-id="58bc8-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="58bc8-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="58bc8-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="58bc8-109">Examples</span></span>

<span data-ttu-id="58bc8-110">Pour obtenir des exemples d’utilisation de l’objet [**SWbemDateTime**](swbemdatetime.md) pour convertir des valeurs DateTime CIM vers et à partir du format **fileTime** ou du format de **\_ Date VT** , consultez [tâches WMI : dates et heures](wmi-tasks--dates-and-times.md).</span><span class="sxs-lookup"><span data-stu-id="58bc8-110">For examples of using the [**SWbemDateTime**](swbemdatetime.md) object to convert CIM datetime values to and from either the **FILETIME** format or the **VT\_DATE** format, see [WMI Tasks: Dates and Times](wmi-tasks--dates-and-times.md).</span></span> <span data-ttu-id="58bc8-111">Pour obtenir une description du format DateTime CIM, consultez [format de date et d’heure](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="58bc8-111">For a description of the CIM datetime format, see [Date and Time Format](date-and-time-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="58bc8-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="58bc8-112">Requirements</span></span>



| <span data-ttu-id="58bc8-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="58bc8-113">Requirement</span></span> | <span data-ttu-id="58bc8-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="58bc8-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="58bc8-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58bc8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="58bc8-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58bc8-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="58bc8-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="58bc8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="58bc8-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="58bc8-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="58bc8-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="58bc8-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="58bc8-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="58bc8-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="58bc8-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="58bc8-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="58bc8-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="58bc8-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="58bc8-123">DLL</span><span class="sxs-lookup"><span data-stu-id="58bc8-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="58bc8-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="58bc8-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="58bc8-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="58bc8-125">CLSID</span></span><br/>                    | <span data-ttu-id="58bc8-126">CLSID \_ SWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="58bc8-126">CLSID\_SWbemDateTime</span></span><br/>                                                         |
| <span data-ttu-id="58bc8-127">IID</span><span class="sxs-lookup"><span data-stu-id="58bc8-127">IID</span></span><br/>                      | <span data-ttu-id="58bc8-128">IID \_ ISWbemDateTime</span><span class="sxs-lookup"><span data-stu-id="58bc8-128">IID\_ISWbemDateTime</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="58bc8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="58bc8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58bc8-130">**SWbemDateTime**</span><span class="sxs-lookup"><span data-stu-id="58bc8-130">**SWbemDateTime**</span></span>](swbemdatetime.md)
</dt> <dt>

[<span data-ttu-id="58bc8-131">Format de date et d’heure</span><span class="sxs-lookup"><span data-stu-id="58bc8-131">Date and Time Format</span></span>](date-and-time-format.md)
</dt> </dl>

 

 




