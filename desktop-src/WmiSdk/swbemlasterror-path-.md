---
description: La \_ propriété Path de l’objet SWbemLastError retourne un objet SWbemObjectPath qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours. Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.
ms.assetid: 5472e463-54cb-4ba2-8c00-08b70013e38d
ms.tgt_platform: multiple
title: SWbemLastError.Path_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.Path_
- ISWbemLastError.Path_
- ISWbemLastError.get_Path_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c979fd76ffb4ee97f62362d53fac4151de17bae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034726"
---
# <a name="swbemlasterrorpath_-property"></a><span data-ttu-id="c4230-104">SWbemLastError. Path, \_ propriété</span><span class="sxs-lookup"><span data-stu-id="c4230-104">SWbemLastError.Path\_ property</span></span>

<span data-ttu-id="c4230-105">La **propriété \_ path** de l’objet [**SWbemLastError**](swbemlasterror.md) retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance en cours.</span><span class="sxs-lookup"><span data-stu-id="c4230-105">The **Path\_** property of the [**SWbemLastError**](swbemlasterror.md) object returns an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span> <span data-ttu-id="c4230-106">Cette propriété peut être passée en tant que paramètre aux méthodes qui requièrent un chemin d’accès d’objet.</span><span class="sxs-lookup"><span data-stu-id="c4230-106">This property can be passed as a parameter to methods that require an object path.</span></span>

<span data-ttu-id="c4230-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c4230-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="c4230-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c4230-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4230-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c4230-109">Syntax</span></span>


```VB
SWbemLastError.Path_ As Object
```



## <a name="property-value"></a><span data-ttu-id="c4230-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c4230-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="c4230-111">Notes</span><span class="sxs-lookup"><span data-stu-id="c4230-111">Remarks</span></span>

<span data-ttu-id="c4230-112">Seule la propriété de [**classe**](swbemobjectpath-class.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée peut être modifiée.</span><span class="sxs-lookup"><span data-stu-id="c4230-112">Only the [**Class**](swbemobjectpath-class.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance can be modified.</span></span> <span data-ttu-id="c4230-113">Si vous essayez de modifier une autre propriété ou si vous essayez d’appeler les méthodes [**SetAsClass**](swbemobjectpath-setasclass.md) ou [**SetAsSingleton**](swbemobjectpath-setassingleton.md) , vous recevez une erreur de **wbemErrReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="c4230-113">If you try to modify any other property, or try to call the [**SetAsClass**](swbemobjectpath-setasclass.md) or [**SetAsSingleton**](swbemobjectpath-setassingleton.md) methods, you get an error of **wbemErrReadOnly**.</span></span>

<span data-ttu-id="c4230-114">Pour cette raison, vous ne pouvez pas modifier l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui est la valeur de la propriété [**Keys**](swbemobjectpath-keys.md) de l’instance [**SWbemObjectPath**](swbemobjectpath.md) retournée.</span><span class="sxs-lookup"><span data-stu-id="c4230-114">Because of this, you cannot modify the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that is the value of the [**Keys**](swbemobjectpath-keys.md) property of the returned [**SWbemObjectPath**](swbemobjectpath.md) instance.</span></span> <span data-ttu-id="c4230-115">Si vous essayez d’appeler les méthodes [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md)ou [**DeleteAll**](swbemnamedvalueset-deleteall.md) sur cette valeur, vous recevez une erreur **wbemErrReadOnly** .</span><span class="sxs-lookup"><span data-stu-id="c4230-115">If you try to call the [**Add**](swbemnamedvalueset-add.md), [**Remove**](swbemnamedvalueset-remove.md), or [**DeleteAll**](swbemnamedvalueset-deleteall.md) methods on this value, you get a **wbemErrReadOnly** error.</span></span> <span data-ttu-id="c4230-116">En outre, vous ne pouvez pas modifier les [**SWbemNamedValue**](swbemnamedvalue.md) obtenus à partir de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c4230-116">Furthermore, you cannot modify any [**SWbemNamedValue**](swbemnamedvalue.md) obtained from this collection.</span></span> <span data-ttu-id="c4230-117">Les tentatives de modification de la propriété [**value**](swbemnamedvalue-value.md) retournent le même code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c4230-117">Attempts to modify the [**Value**](swbemnamedvalue-value.md) property return the same error code.</span></span>

<span data-ttu-id="c4230-118">Toutefois, si vous appelez [**SWbemObject. Clone \_**](swbemobject-clone-.md) pour créer une copie, la propriété [**path \_**](swbemobject-path-.md) de la copie est entièrement modifiable.</span><span class="sxs-lookup"><span data-stu-id="c4230-118">However, if you call [**SWbemObject.Clone\_**](swbemobject-clone-.md) to create a copy, the [**Path\_**](swbemobject-path-.md) property of the copy is fully modifiable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4230-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c4230-119">Requirements</span></span>



| <span data-ttu-id="c4230-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c4230-120">Requirement</span></span> | <span data-ttu-id="c4230-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="c4230-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4230-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4230-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c4230-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4230-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4230-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c4230-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c4230-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4230-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4230-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c4230-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4230-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c4230-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4230-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="c4230-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4230-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4230-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4230-130">DLL</span><span class="sxs-lookup"><span data-stu-id="c4230-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4230-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4230-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4230-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="c4230-132">CLSID</span></span><br/>                    | <span data-ttu-id="c4230-133">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="c4230-133">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="c4230-134">IID</span><span class="sxs-lookup"><span data-stu-id="c4230-134">IID</span></span><br/>                      | <span data-ttu-id="c4230-135">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="c4230-135">IID\_ISWbemLastError</span></span><br/>                                                         |



 

 




