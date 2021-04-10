---
description: La méthode Item de l’objet SWbemPropertySet obtient un SWbemProperty nommé de la collection. Il s’agit de la méthode par défaut pour cet objet.
ms.assetid: 72025676-01dd-4fd7-b000-de6b09ecc6dc
ms.tgt_platform: multiple
title: SWbemPropertySet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Item
- ISWbemPropertySet.Item
- ISWbemPropertySet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d4dcbbbcb8b5225af038bf71e67c3a14260942
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210540"
---
# <a name="swbempropertysetitem-method"></a><span data-ttu-id="991ed-104">SWbemPropertySet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="991ed-104">SWbemPropertySet.Item method</span></span>

<span data-ttu-id="991ed-105">La méthode **Item** de l’objet [**SWbemPropertySet**](swbempropertyset.md) obtient un [**SWbemProperty**](swbemproperty.md) nommé de la collection.</span><span class="sxs-lookup"><span data-stu-id="991ed-105">The **Item** method of the [**SWbemPropertySet**](swbempropertyset.md) object gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="991ed-106">Il s’agit de la méthode par défaut pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="991ed-106">This is the default method for this object.</span></span>

<span data-ttu-id="991ed-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="991ed-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="991ed-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="991ed-108">Syntax</span></span>


```VB
objProperty = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="991ed-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="991ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="991ed-110">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="991ed-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="991ed-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="991ed-111">Required.</span></span> <span data-ttu-id="991ed-112">Nom de la propriété à récupérer.</span><span class="sxs-lookup"><span data-stu-id="991ed-112">Name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="991ed-113">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="991ed-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="991ed-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="991ed-114">Reserved.</span></span> <span data-ttu-id="991ed-115">Cette valeur doit être égale à zéro si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="991ed-115">This value must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="991ed-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="991ed-116">Return value</span></span>

<span data-ttu-id="991ed-117">En cas de réussite, l’objet [**SWbemProperty**](swbemproperty.md) demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="991ed-117">If successful, the requested [**SWbemProperty**](swbemproperty.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="991ed-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="991ed-118">Error codes</span></span>

<span data-ttu-id="991ed-119">À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="991ed-119">After the completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="991ed-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="991ed-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="991ed-121">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="991ed-121">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="991ed-122">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="991ed-122">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="991ed-123">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="991ed-123">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="991ed-124">**wbemErrOutOfMemory** -2147749896</span><span class="sxs-lookup"><span data-stu-id="991ed-124">**wbemErrOutOfMemory** - 2147749896</span></span>
</dt> <dd>

<span data-ttu-id="991ed-125">Mémoire insuffisante pour l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="991ed-125">Not enough memory for this method to execute.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="991ed-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="991ed-126">Requirements</span></span>



| <span data-ttu-id="991ed-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="991ed-127">Requirement</span></span> | <span data-ttu-id="991ed-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="991ed-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="991ed-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="991ed-129">Minimum supported client</span></span><br/> | <span data-ttu-id="991ed-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="991ed-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="991ed-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="991ed-131">Minimum supported server</span></span><br/> | <span data-ttu-id="991ed-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="991ed-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="991ed-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="991ed-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="991ed-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="991ed-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="991ed-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="991ed-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="991ed-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="991ed-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="991ed-137">DLL</span><span class="sxs-lookup"><span data-stu-id="991ed-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="991ed-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="991ed-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="991ed-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="991ed-139">CLSID</span></span><br/>                    | <span data-ttu-id="991ed-140">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="991ed-140">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="991ed-141">IID</span><span class="sxs-lookup"><span data-stu-id="991ed-141">IID</span></span><br/>                      | <span data-ttu-id="991ed-142">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="991ed-142">IID\_ISWbemPropertySet</span></span><br/>                                                       |



 

 




