---
description: La méthode SWbemRefresher. Remove supprime l’objet SWbemRefreshableItem avec l’index spécifié de l’actualisateur.
ms.assetid: db5ac740-e2b3-4667-b511-d750cb092e0f
ms.tgt_platform: multiple
title: SWbemRefresher. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Remove
- ISWbemRefresher.Remove
- ISWbemRefresher.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9504b81ce83a91695765e75e74de374437c188d4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953428"
---
# <a name="swbemrefresherremove-method"></a><span data-ttu-id="06c92-103">SWbemRefresher. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="06c92-103">SWbemRefresher.Remove method</span></span>

<span data-ttu-id="06c92-104">La méthode **SWbemRefresher. Remove** supprime l’objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) avec l’index spécifié de l’actualisateur.</span><span class="sxs-lookup"><span data-stu-id="06c92-104">The **SWbemRefresher.Remove** method removes the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object with the specified index from the refresher.</span></span> <span data-ttu-id="06c92-105">L’objet **SWbemRefreshableItem** peut représenter soit un objet unique, soit un jeu d’objets.</span><span class="sxs-lookup"><span data-stu-id="06c92-105">The **SWbemRefreshableItem** object can represent either a single object or an object set.</span></span>

<span data-ttu-id="06c92-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="06c92-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="06c92-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="06c92-107">Syntax</span></span>


```VB
objRefresher = .Remove( _
  ByVal LIndex, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="06c92-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="06c92-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06c92-109">*LIndex*</span><span class="sxs-lookup"><span data-stu-id="06c92-109">*LIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="06c92-110">Index de l’élément dans l’objet [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="06c92-110">Index of the item in the [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="06c92-111">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06c92-111">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06c92-112">Les indicateurs doivent être définis à T0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="06c92-112">Flags must be set t0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="06c92-113">*objWbemNamedvalueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="06c92-113">*objWbemNamedvalueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06c92-114">Null.</span><span class="sxs-lookup"><span data-stu-id="06c92-114">Null.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06c92-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="06c92-115">Return value</span></span>

<span data-ttu-id="06c92-116">Cette méthode n’a pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="06c92-116">This method has no return values.</span></span>

## <a name="remarks"></a><span data-ttu-id="06c92-117">Notes</span><span class="sxs-lookup"><span data-stu-id="06c92-117">Remarks</span></span>

<span data-ttu-id="06c92-118">**Codes d’erreur** Si l’actualisateur n’a pas d’élément avec l’index spécifié, **wbemErrNotFound** est généré.</span><span class="sxs-lookup"><span data-stu-id="06c92-118">**Error codes** If the refresher has no item with the specified index, **wbemErrNotFound** is generated.</span></span>

## <a name="requirements"></a><span data-ttu-id="06c92-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="06c92-119">Requirements</span></span>



| <span data-ttu-id="06c92-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="06c92-120">Requirement</span></span> | <span data-ttu-id="06c92-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="06c92-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06c92-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c92-122">Minimum supported client</span></span><br/> | <span data-ttu-id="06c92-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="06c92-123">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="06c92-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="06c92-124">Minimum supported server</span></span><br/> | <span data-ttu-id="06c92-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="06c92-125">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="06c92-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="06c92-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="06c92-127"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c92-127"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="06c92-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="06c92-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="06c92-129"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="06c92-129"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="06c92-130">DLL</span><span class="sxs-lookup"><span data-stu-id="06c92-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06c92-131"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06c92-131"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="06c92-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="06c92-132">CLSID</span></span><br/>                    | <span data-ttu-id="06c92-133">CLSID \_ SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="06c92-133">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="06c92-134">IID</span><span class="sxs-lookup"><span data-stu-id="06c92-134">IID</span></span><br/>                      | <span data-ttu-id="06c92-135">IID \_ ISWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="06c92-135">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="06c92-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="06c92-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c92-137">**SWbemRefresher**</span><span class="sxs-lookup"><span data-stu-id="06c92-137">**SWbemRefresher**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




