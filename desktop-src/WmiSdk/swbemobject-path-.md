---
description: La \_ propriété Path de l’objet SWbemObject retourne un objet SWbemObjectPath qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours. Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.
ms.assetid: 85a55159-5f10-49b5-bc37-39d7b4dfccd7
ms.tgt_platform: multiple
title: SWbemObject.Path_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Path_
- ISWbemObject.Path_
- ISWbemObject.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 773f6f9bb04aa31290bc351550a45d849d74e06f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203540"
---
# <a name="swbemobjectpath_-property"></a><span data-ttu-id="024ce-104">SWbemObject. Path, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="024ce-104">SWbemObject.Path\_ property</span></span>

<span data-ttu-id="024ce-105">La **propriété \_ path** de l’objet [**SWbemObject**](swbemobject.md) retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours.</span><span class="sxs-lookup"><span data-stu-id="024ce-105">The **Path\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="024ce-106">Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.</span><span class="sxs-lookup"><span data-stu-id="024ce-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="024ce-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="024ce-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="024ce-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="024ce-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="024ce-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="024ce-109">Syntax</span></span>


```VB
SWbemObject.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="024ce-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="024ce-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="024ce-111">Notes</span><span class="sxs-lookup"><span data-stu-id="024ce-111">Remarks</span></span>

<span data-ttu-id="024ce-112">Seule la propriété de [**classe**](swbemobjectpath-class.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="024ce-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="024ce-113">Si vous essayez de modifier une autre propriété ou si vous essayez d’appeler les méthodes [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md), vous obtiendrez une erreur **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="024ce-113">If you try to modify any other property, or try to call the methods [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md), you will get a **wbemErrReadOnly** error.</span></span>

<span data-ttu-id="024ce-114">Pour cette raison, vous ne pouvez pas modifier l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est la valeur de la propriété [**Keys**](swbemobjectpath-keys.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée.</span><span class="sxs-lookup"><span data-stu-id="024ce-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="024ce-115">Si vous essayez d’appeler les méthodes [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) sur cette valeur, vous obtiendrez une erreur wbemErrReadOnly.</span><span class="sxs-lookup"><span data-stu-id="024ce-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you will get a wbemErrReadOnly error.</span></span> <span data-ttu-id="024ce-116">En outre, vous ne pouvez pas modifier les [**SWbemNamedValue**](swbemnamedvalue.md) obtenus à partir de cette collection.</span><span class="sxs-lookup"><span data-stu-id="024ce-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="024ce-117">Les tentatives de modification de la propriété **value** retournent le même code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="024ce-117">Attempts to modify the **Value** property return the same error code.</span></span>

<span data-ttu-id="024ce-118">Toutefois, si vous appelez [**SWbemObject. Clone \_**](swbemobject-clone-.md) pour créer une copie, la propriété [**SWbemObjectPath. Path**](swbemobjectpath-path.md) de la copie est entièrement modifiable.</span><span class="sxs-lookup"><span data-stu-id="024ce-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**SWbemObjectPath.Path**](swbemobjectpath-path.md) property of the copy is fully modifiable.</span></span>

## <a name="examples"></a><span data-ttu-id="024ce-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="024ce-119">Examples</span></span>

<span data-ttu-id="024ce-120">L’exemple de code suivant, tiré de la [liste de toutes les classes WMI cimv2](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) dans la Galerie TechNet, utilise la \_ propriété Path pour répertorier toutes les classes WMI cimv2.</span><span class="sxs-lookup"><span data-stu-id="024ce-120">The following code sample, taken from [List All the WMI cimV2 Classes](https://Gallery.TechNet.Microsoft.Com/5649568b-074e-4f5d-be52-e8b7d8fe4517) in the TechNet Gallery, uses the Path\_ property to list all the WMI cimV2 classes.</span></span>


```VB
strComputer = "." 
Set objWMIService=GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\root\cimv2") 
  
For Each objclass in objWMIService.SubclassesOf() 
    Wscript.Echo objClass.Path_.Class 
Next 
```



## <a name="requirements"></a><span data-ttu-id="024ce-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="024ce-121">Requirements</span></span>



| <span data-ttu-id="024ce-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="024ce-122">Requirement</span></span> | <span data-ttu-id="024ce-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="024ce-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="024ce-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="024ce-124">Minimum supported client</span></span><br/> | <span data-ttu-id="024ce-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="024ce-125">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="024ce-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="024ce-126">Minimum supported server</span></span><br/> | <span data-ttu-id="024ce-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="024ce-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="024ce-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="024ce-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="024ce-129"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="024ce-129"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="024ce-130">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="024ce-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="024ce-131"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="024ce-131"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="024ce-132">DLL</span><span class="sxs-lookup"><span data-stu-id="024ce-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="024ce-133"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="024ce-133"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="024ce-134">CLSID</span><span class="sxs-lookup"><span data-stu-id="024ce-134">CLSID</span></span><br/>                    | <span data-ttu-id="024ce-135">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="024ce-135">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="024ce-136">IID</span><span class="sxs-lookup"><span data-stu-id="024ce-136">IID</span></span><br/>                      | <span data-ttu-id="024ce-137">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="024ce-137">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




