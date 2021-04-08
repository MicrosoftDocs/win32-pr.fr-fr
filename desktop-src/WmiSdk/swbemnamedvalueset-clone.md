---
description: La méthode Clone de l’objet SWbemNamedValueSet retourne un nouvel objet qui est un clone de la collection actuelle.
ms.assetid: 0e7fab2e-8175-45e5-aa70-1109502e2b3f
ms.tgt_platform: multiple
title: Méthode SWbemNamedValueSet. Clone (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
- ISWbemNamedValueSet.Clone
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 17678d36a553c84c008f606c647d7ff1fa9dfadc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103756975"
---
# <a name="swbemnamedvaluesetclone-method"></a><span data-ttu-id="5ca58-103">SWbemNamedValueSet. Clone, méthode</span><span class="sxs-lookup"><span data-stu-id="5ca58-103">SWbemNamedValueSet.Clone method</span></span>

<span data-ttu-id="5ca58-104">La méthode **clone** de l’objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) retourne un nouvel objet qui est un clone de la collection actuelle.</span><span class="sxs-lookup"><span data-stu-id="5ca58-104">The **Clone** method of the [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns a new object that is a clone of the current collection.</span></span>

<span data-ttu-id="5ca58-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="5ca58-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5ca58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ca58-106">Syntax</span></span>


```VB
objwbemNamedValueSet = .Clone( _
)
```



## <a name="parameters"></a><span data-ttu-id="5ca58-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ca58-107">Parameters</span></span>

<span data-ttu-id="5ca58-108">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="5ca58-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ca58-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5ca58-109">Return value</span></span>

<span data-ttu-id="5ca58-110">En cas de réussite, un nouvel objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) retourne.</span><span class="sxs-lookup"><span data-stu-id="5ca58-110">If successful, a new [**SWbemNamedValueSet**](swbemnamedvalueset.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5ca58-111">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="5ca58-111">Error codes</span></span>

<span data-ttu-id="5ca58-112">À la fin de la méthode **clone** , l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="5ca58-112">Upon completion of the **Clone** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="5ca58-113">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="5ca58-113">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="5ca58-114">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5ca58-114">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="5ca58-115">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="5ca58-115">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="5ca58-116">Mémoire insuffisante pour cloner l’objet.</span><span class="sxs-lookup"><span data-stu-id="5ca58-116">Not enough memory to clone the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5ca58-117">Notes</span><span class="sxs-lookup"><span data-stu-id="5ca58-117">Remarks</span></span>

<span data-ttu-id="5ca58-118">Utilisez cette méthode pour dupliquer une collection [**SWbemNamedValueSet**](swbemnamedvalueset.md) .</span><span class="sxs-lookup"><span data-stu-id="5ca58-118">Use this method to duplicate an [**SWbemNamedValueSet**](swbemnamedvalueset.md) collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ca58-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5ca58-119">Requirements</span></span>



| <span data-ttu-id="5ca58-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5ca58-120">Requirement</span></span> | <span data-ttu-id="5ca58-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="5ca58-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca58-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ca58-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca58-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5ca58-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5ca58-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5ca58-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca58-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5ca58-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5ca58-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="5ca58-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca58-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ca58-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ca58-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="5ca58-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="5ca58-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="5ca58-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="5ca58-130">DLL</span><span class="sxs-lookup"><span data-stu-id="5ca58-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca58-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca58-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="5ca58-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="5ca58-132">CLSID</span></span><br/>                    | <span data-ttu-id="5ca58-133">CLSID \_ SWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="5ca58-133">CLSID\_SWbemNamedValueSet</span></span><br/>                                                    |
| <span data-ttu-id="5ca58-134">IID</span><span class="sxs-lookup"><span data-stu-id="5ca58-134">IID</span></span><br/>                      | <span data-ttu-id="5ca58-135">IID \_ ISWbemNamedValueSet</span><span class="sxs-lookup"><span data-stu-id="5ca58-135">IID\_ISWbemNamedValueSet</span></span><br/>                                                     |



## <a name="see-also"></a><span data-ttu-id="5ca58-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5ca58-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca58-137">**SWbemNamedValueSet**</span><span class="sxs-lookup"><span data-stu-id="5ca58-137">**SWbemNamedValueSet**</span></span>](swbemnamedvalueset.md)
</dt> </dl>

 

 




