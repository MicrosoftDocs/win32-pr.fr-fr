---
description: La méthode Add de l’objet SWbemNamedValueSet ajoute un objet SWbemNamedValue à la collection. Si un élément existe déjà dans la collection avec le même nom, le nouvel élément le remplace.
ms.assetid: 471b23f5-6c53-40e2-a2a9-0798044c9dfb
ms.tgt_platform: multiple
title: Méthode SWbemNamedValueSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
- ISWbemNamedValueSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3aa1a3a982d7621c910a5afca95b26db1dd5f4d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528480"
---
# <a name="swbemnamedvaluesetadd-method"></a><span data-ttu-id="6f193-104">SWbemNamedValueSet. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="6f193-104">SWbemNamedValueSet.Add method</span></span>

<span data-ttu-id="6f193-105">La méthode **Add** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) ajoute un objet [**SWbemNamedValue**](swbemnamedvalue.md) à la collection.</span><span class="sxs-lookup"><span data-stu-id="6f193-105">The **Add** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object adds an [**SWbemNamedValue**](swbemnamedvalue.md) object to the collection.</span></span> <span data-ttu-id="6f193-106">Si un élément existe déjà dans la collection avec le même nom, le nouvel élément le remplace.</span><span class="sxs-lookup"><span data-stu-id="6f193-106">If an element already exists in the collection with the same name, the new element replaces it.</span></span>

<span data-ttu-id="6f193-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f193-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f193-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f193-108">Syntax</span></span>


```VB
objNamedValue = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6f193-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f193-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f193-110">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f193-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f193-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6f193-111">Required.</span></span> <span data-ttu-id="6f193-112">Nom de la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="6f193-112">Name of the new value.</span></span>

</dd> <dt>

<span data-ttu-id="6f193-113">*varVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6f193-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f193-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="6f193-114">Required.</span></span> <span data-ttu-id="6f193-115">Variant qui représente la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="6f193-115">Variant that represents the new value.</span></span>

</dd> <dt>

<span data-ttu-id="6f193-116">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="6f193-116">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f193-117">Réservé et doit avoir la valeur zéro si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6f193-117">Reserved and must be set to zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f193-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6f193-118">Return value</span></span>

<span data-ttu-id="6f193-119">En cas de réussite, cette méthode retourne l’objet [**SWbemNamedValue**](swbemnamedvalue.md) nouvellement modifié ou nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="6f193-119">If successful, this method returns the newly modified or newly created [**SWbemNamedValue**](swbemnamedvalue.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f193-120">Notes</span><span class="sxs-lookup"><span data-stu-id="6f193-120">Remarks</span></span>

<span data-ttu-id="6f193-121">Pour obtenir des exemples d’ajout et de récupération de valeurs nommées, consultez [**SWbemNamedValue. Value**](swbemnamedvalue-value.md).</span><span class="sxs-lookup"><span data-stu-id="6f193-121">For examples of adding and retrieving named values, see [**SWbemNamedValue.Value**](swbemnamedvalue-value.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f193-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6f193-122">Requirements</span></span>



| <span data-ttu-id="6f193-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6f193-123">Requirement</span></span> | <span data-ttu-id="6f193-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6f193-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f193-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f193-125">Minimum supported client</span></span><br/> | <span data-ttu-id="6f193-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f193-126">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f193-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6f193-127">Minimum supported server</span></span><br/> | <span data-ttu-id="6f193-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f193-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f193-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="6f193-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f193-130"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f193-130"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f193-131">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="6f193-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f193-132"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f193-132"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f193-133">DLL</span><span class="sxs-lookup"><span data-stu-id="6f193-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f193-134"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f193-134"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f193-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f193-135">CLSID</span></span><br/>                    | <span data-ttu-id="6f193-136">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6f193-136">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="6f193-137">IID</span><span class="sxs-lookup"><span data-stu-id="6f193-137">IID</span></span><br/>                      | <span data-ttu-id="6f193-138">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="6f193-138">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="6f193-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6f193-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f193-140">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="6f193-140">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




