---
description: La \_ propriété Properties de l’objet SWbemObject retourne un objet SWbemPropertySet qui est une collection des propriétés de l’instance ou de la classe actuelle. Cette propriété est en lecture seule.
ms.assetid: 8dd49678-47e7-4c6b-ab12-42532065eaf2
ms.tgt_platform: multiple
title: SWbemObject.Properties_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Properties_
- ISWbemObject.Properties_
- ISWbemObject.get_Properties_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2b215abb7a0ca466c8a93fe20f20518f8d7b2ec8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527804"
---
# <a name="swbemobjectproperties_-property"></a><span data-ttu-id="0d9a9-104">Propriété SWbemObject. Properties \_</span><span class="sxs-lookup"><span data-stu-id="0d9a9-104">SWbemObject.Properties\_ property</span></span>

<span data-ttu-id="0d9a9-105">La **propriété \_ Properties** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemPropertySet**](swbempropertyset.md) qui est une collection des propriétés de l’instance ou de la classe actuelle.</span><span class="sxs-lookup"><span data-stu-id="0d9a9-105">The **Properties\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemPropertySet**](swbempropertyset.md) object that is a collection of the properties for the current class or instance.</span></span> <span data-ttu-id="0d9a9-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0d9a9-106">This property is read-only.</span></span>

<span data-ttu-id="0d9a9-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0d9a9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="0d9a9-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0d9a9-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d9a9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0d9a9-109">Syntax</span></span>


```VB
SWbemObject.Properties_ As Object
```



## <a name="property-value"></a><span data-ttu-id="0d9a9-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0d9a9-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="0d9a9-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="0d9a9-111">Examples</span></span>

<span data-ttu-id="0d9a9-112">L’exemple de code PowerShell [générer des scripts de classe WMI](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell dans la Galerie TechNet utilise la \_ propriété Properties pour générer un script pour chacune des classes WMI qui répertorient le nom de la classe WMI et les propriétés.</span><span class="sxs-lookup"><span data-stu-id="0d9a9-112">The [Generate Powershell WMI Class Scripts](https://Gallery.TechNet.Microsoft.Com/b435aa68-a1df-4f62-af05-1f504f683146) PowerShell code example on TechNet Gallery uses the Properties\_ property to generate a script for each of the WMI classes that will list the WMI class name and the properties.</span></span>

<span data-ttu-id="0d9a9-113">Le code suivant, tiré de la [liste de toutes les propriétés d’un](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) exemple de code VBScript de classe WMI sur la Galerie TechNet, répertorie les propriétés d’une classe WMI spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0d9a9-113">The following code, taken from the [List All the Properties for a WMI Class](https://Gallery.TechNet.Microsoft.Com/0f66f392-05b6-4431-b596-9379124d7a32) VBScript code example on TechNet Gallery, Lists the properties for a specified WMI class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Properties" 
WScript.Echo "------------------------------" 
  
For Each objClassProperty In objClass.Properties_ 
    WScript.Echo objClassProperty.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="0d9a9-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0d9a9-114">Requirements</span></span>



| <span data-ttu-id="0d9a9-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0d9a9-115">Requirement</span></span> | <span data-ttu-id="0d9a9-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="0d9a9-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d9a9-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9a9-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d9a9-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0d9a9-118">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0d9a9-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d9a9-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d9a9-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0d9a9-120">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0d9a9-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="0d9a9-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d9a9-122"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d9a9-122"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d9a9-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0d9a9-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="0d9a9-124"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0d9a9-124"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0d9a9-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0d9a9-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d9a9-126"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d9a9-126"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0d9a9-127">CLSID</span><span class="sxs-lookup"><span data-stu-id="0d9a9-127">CLSID</span></span><br/>                    | <span data-ttu-id="0d9a9-128">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="0d9a9-128">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="0d9a9-129">IID</span><span class="sxs-lookup"><span data-stu-id="0d9a9-129">IID</span></span><br/>                      | <span data-ttu-id="0d9a9-130">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="0d9a9-130">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




