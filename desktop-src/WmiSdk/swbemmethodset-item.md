---
description: La méthode Item de l’objet SWbemMethodSet retourne un objet nommé SWbemMethod à partir de la collection.
ms.assetid: 4c1bbecc-b38b-4869-9c8c-b9321536b23e
ms.tgt_platform: multiple
title: SWbemMethodSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet.Item
- ISWbemMethodSet.Item
- ISWbemMethodSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 89d20dc652189abe3354f5d1b51c03279d3f74c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521491"
---
# <a name="swbemmethodsetitem-method"></a><span data-ttu-id="7a103-103">SWbemMethodSet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="7a103-103">SWbemMethodSet.Item method</span></span>

<span data-ttu-id="7a103-104">La méthode **Item** de l’objet [**SWbemMethodSet**](swbemmethodset.md) retourne un objet nommé [**SWbemMethod**](swbemmethod.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="7a103-104">The **Item** method of the [**SWbemMethodSet**](swbemmethodset.md) object returns a named [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span>

<span data-ttu-id="7a103-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7a103-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7a103-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7a103-106">Syntax</span></span>


```VB
objMethod = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="7a103-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7a103-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a103-108">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7a103-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a103-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="7a103-109">Required.</span></span> <span data-ttu-id="7a103-110">Nom de la méthode à récupérer.</span><span class="sxs-lookup"><span data-stu-id="7a103-110">Name of the method to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="7a103-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="7a103-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7a103-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="7a103-112">Reserved.</span></span> <span data-ttu-id="7a103-113">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="7a103-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a103-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7a103-114">Return value</span></span>

<span data-ttu-id="7a103-115">En cas de réussite, l’objet [**SWbemMethod**](swbemmethod.md) demandé retourne.</span><span class="sxs-lookup"><span data-stu-id="7a103-115">If successful, the requested [**SWbemMethod**](swbemmethod.md) object returns.</span></span>

## <a name="error-codes"></a><span data-ttu-id="7a103-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="7a103-116">Error codes</span></span>

<span data-ttu-id="7a103-117">À la fin de la méthode **Item** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="7a103-117">Upon completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="7a103-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="7a103-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="7a103-119">Le paramètre *IFlags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7a103-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="7a103-120">**wbemErrFailed** -2147749894</span><span class="sxs-lookup"><span data-stu-id="7a103-120">**wbemErrFailed** - 2147749894</span></span>
</dt> <dd>

<span data-ttu-id="7a103-121">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7a103-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="7a103-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="7a103-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="7a103-123">La méthode spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="7a103-123">The specified method does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7a103-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7a103-124">Requirements</span></span>



| <span data-ttu-id="7a103-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7a103-125">Requirement</span></span> | <span data-ttu-id="7a103-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="7a103-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a103-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a103-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7a103-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a103-128">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a103-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7a103-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7a103-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a103-130">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a103-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="7a103-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a103-132"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a103-132"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7a103-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7a103-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="7a103-134"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7a103-134"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7a103-135">DLL</span><span class="sxs-lookup"><span data-stu-id="7a103-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a103-136"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a103-136"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a103-137">CLSID</span><span class="sxs-lookup"><span data-stu-id="7a103-137">CLSID</span></span><br/>                    | <span data-ttu-id="7a103-138">CLSID \_ SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="7a103-138">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="7a103-139">IID</span><span class="sxs-lookup"><span data-stu-id="7a103-139">IID</span></span><br/>                      | <span data-ttu-id="7a103-140">IID \_ ISWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="7a103-140">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="7a103-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a103-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a103-142">**SWbemMethodSet**</span><span class="sxs-lookup"><span data-stu-id="7a103-142">**SWbemMethodSet**</span></span>](swbemmethodset.md)
</dt> <dt>

[<span data-ttu-id="7a103-143">**SWbemMethod**</span><span class="sxs-lookup"><span data-stu-id="7a103-143">**SWbemMethod**</span></span>](swbemmethod.md)
</dt> </dl>

 

 




