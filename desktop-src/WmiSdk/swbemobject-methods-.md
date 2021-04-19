---
description: La propriété Methods \_ de l’objet SWbemObject retourne un objet SWbemMethodSet qui est une collection des méthodes pour l’instance ou la classe actuelle. Cette propriété est en lecture seule.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: SWbemObject.Methods_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521373"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="24aa2-104">SWbemObject. Methods, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="24aa2-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="24aa2-105">La **propriété \_ Methods** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemMethodSet**](swbemmethodset.md) qui est une collection des méthodes pour l’instance ou la classe actuelle.</span><span class="sxs-lookup"><span data-stu-id="24aa2-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="24aa2-106">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24aa2-106">This property is read-only.</span></span>

<span data-ttu-id="24aa2-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="24aa2-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="24aa2-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="24aa2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="24aa2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24aa2-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="24aa2-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="24aa2-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="24aa2-111">Exemples</span><span class="sxs-lookup"><span data-stu-id="24aa2-111">Examples</span></span>

<span data-ttu-id="24aa2-112">L' [exemple de code](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)suivant, tiré de la Galerie TechNet, explique comment répertorier toutes les méthodes d’une classe.</span><span class="sxs-lookup"><span data-stu-id="24aa2-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="24aa2-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24aa2-113">Requirements</span></span>



| <span data-ttu-id="24aa2-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24aa2-114">Requirement</span></span> | <span data-ttu-id="24aa2-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="24aa2-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24aa2-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24aa2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="24aa2-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24aa2-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24aa2-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24aa2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="24aa2-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24aa2-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24aa2-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="24aa2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="24aa2-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="24aa2-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="24aa2-122">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="24aa2-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="24aa2-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24aa2-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24aa2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="24aa2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24aa2-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24aa2-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="24aa2-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="24aa2-126">CLSID</span></span><br/>                    | <span data-ttu-id="24aa2-127">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="24aa2-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="24aa2-128">IID</span><span class="sxs-lookup"><span data-stu-id="24aa2-128">IID</span></span><br/>                      | <span data-ttu-id="24aa2-129">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="24aa2-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




