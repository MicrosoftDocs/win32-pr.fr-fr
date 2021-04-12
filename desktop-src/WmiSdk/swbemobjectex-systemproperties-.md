---
description: Retourne un objet SWbemPropertySet qui contient la collection de propriétés système WMI qui s’appliquent à l’objet.
ms.assetid: e95c325a-8851-4f55-a99d-4346d064e308
ms.tgt_platform: multiple
title: SWbemObjectEx.SystemProperties_ propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectEx.SystemProperties_
- ISWbemObjectEx.SystemProperties_
- ISWbemObjectEx.get_SystemProperties_
- ISWbemObjectEx.put_SystemProperties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cf8b7e15536c0d4e3116f0583662b3cd0b7d0887
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210416"
---
# <a name="swbemobjectexsystemproperties_-property"></a><span data-ttu-id="3579c-103">SWbemObjectEx.Sys\_ propriété temProperties</span><span class="sxs-lookup"><span data-stu-id="3579c-103">SWbemObjectEx.SystemProperties\_ property</span></span>

<span data-ttu-id="3579c-104">La **propriété \_ SystemProperties** de l’objet [**SWbemObjectEx**](swbemobjectex.md) retourne un objet [**SWbemPropertySet**](swbempropertyset.md) qui contient la collection de [Propriétés système WMI](wmi-system-properties.md) qui s’appliquent à l’objet.</span><span class="sxs-lookup"><span data-stu-id="3579c-104">The **SystemProperties\_** property of the [**SWbemObjectEx**](swbemobjectex.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that contains the collection of [WMI System Properties](wmi-system-properties.md) that apply to the object.</span></span>

<span data-ttu-id="3579c-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="3579c-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="3579c-106">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3579c-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3579c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3579c-107">Syntax</span></span>


```VB
SWbemObjectEx.SystemProperties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="3579c-108">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3579c-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="3579c-109">Exemples</span><span class="sxs-lookup"><span data-stu-id="3579c-109">Examples</span></span>

<span data-ttu-id="3579c-110">L’exemple de code suivant récupère les valeurs de propriété pour la \_ classe de processus Win32.</span><span class="sxs-lookup"><span data-stu-id="3579c-110">The following code sample retrieves the property values for the Win32\_Process class.</span></span>


```VB
Set objWmi = GetObject ("winmgmts:root\cimv2")
Set objClass = objWmi.Get("Win32_Process")

' SWbemObjectEx.SystemProperties_ returns 
' an SWbemPropertySet object that contains the collection
' of sytem properties for Win32_Process class

For Each objProperty In objClass.SystemProperties_

    WScript.Echo vbCrLf & objProperty.Name & ":"

    ' Have to take into account that
    ' __Derivation is an array

    If Not objProperty.IsArray Then
        WScript.Echo vbTab & objProperty.Value
    Else
        For Each strValue In objProperty.Value
            WScript.Echo vbTab & strValue
        Next
    End If

Next
```



## <a name="requirements"></a><span data-ttu-id="3579c-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3579c-111">Requirements</span></span>



| <span data-ttu-id="3579c-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3579c-112">Requirement</span></span> | <span data-ttu-id="3579c-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="3579c-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3579c-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3579c-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3579c-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3579c-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3579c-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3579c-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3579c-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3579c-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3579c-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="3579c-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3579c-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3579c-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3579c-120">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3579c-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="3579c-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3579c-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3579c-122">DLL</span><span class="sxs-lookup"><span data-stu-id="3579c-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3579c-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3579c-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3579c-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="3579c-124">CLSID</span></span><br/>                    | <span data-ttu-id="3579c-125">CLSID \_ SWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="3579c-125">CLSID\_SWbemObjectEx</span></span><br/>                                                         |
| <span data-ttu-id="3579c-126">IID</span><span class="sxs-lookup"><span data-stu-id="3579c-126">IID</span></span><br/>                      | <span data-ttu-id="3579c-127">IID \_ ISWbemObjectEx</span><span class="sxs-lookup"><span data-stu-id="3579c-127">IID\_ISWbemObjectEx</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="3579c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3579c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3579c-129">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="3579c-129">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> </dl>

 

 




