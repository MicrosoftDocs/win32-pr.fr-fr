---
description: La méthode Item de l’objet SWbemQualifierSet retourne un objet nommé SWbemQualifier à partir de la collection. Il s’agit de la méthode par défaut de cet objet.
ms.assetid: 5ed3a336-c06f-446d-85d4-243daddc82a5
ms.tgt_platform: multiple
title: SWbemQualifierSet. Item, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Item
- ISWbemQualifierSet.Item
- ISWbemQualifierSet.Item
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 9c89ff554b049e6730a64ebf7e5f017fc8a5652f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868573"
---
# <a name="swbemqualifiersetitem-method"></a><span data-ttu-id="e16db-104">SWbemQualifierSet. Item, méthode</span><span class="sxs-lookup"><span data-stu-id="e16db-104">SWbemQualifierSet.Item method</span></span>

<span data-ttu-id="e16db-105">La méthode **Item** de l’objet [**SWbemQualifierSet**](swbemqualifierset.md) retourne un objet nommé [**SWbemQualifier**](swbemqualifier.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="e16db-105">The **Item** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span> <span data-ttu-id="e16db-106">Il s’agit de la méthode par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="e16db-106">This is the default method of this object.</span></span>

<span data-ttu-id="e16db-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="e16db-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e16db-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e16db-108">Syntax</span></span>


```VB
objQualifier = .Item( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="e16db-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e16db-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e16db-110">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e16db-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e16db-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="e16db-111">Required.</span></span> <span data-ttu-id="e16db-112">Nom du qualificateur à récupérer.</span><span class="sxs-lookup"><span data-stu-id="e16db-112">Name of the qualifier to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e16db-113">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="e16db-113">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="e16db-114">Réservé.</span><span class="sxs-lookup"><span data-stu-id="e16db-114">Reserved.</span></span> <span data-ttu-id="e16db-115">La valeur par défaut est 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="e16db-115">The default value is 0 (zero).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e16db-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e16db-116">Return value</span></span>

<span data-ttu-id="e16db-117">En cas de réussite, l’objet [**SWbemQualifier**](swbemqualifier.md) demandé est retourné.</span><span class="sxs-lookup"><span data-stu-id="e16db-117">If successful, the requested [**SWbemQualifier**](swbemqualifier.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e16db-118">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="e16db-118">Error codes</span></span>

<span data-ttu-id="e16db-119">Une fois la méthode **Item** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="e16db-119">After completion of the **Item** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="e16db-120">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="e16db-120">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="e16db-121">Le paramètre *IFlags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="e16db-121">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e16db-122">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="e16db-122">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="e16db-123">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="e16db-123">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="e16db-124">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="e16db-124">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="e16db-125">Le qualificateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="e16db-125">Specified qualifier does not exist.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e16db-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e16db-126">Requirements</span></span>



| <span data-ttu-id="e16db-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e16db-127">Requirement</span></span> | <span data-ttu-id="e16db-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="e16db-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e16db-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e16db-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e16db-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e16db-130">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e16db-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e16db-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e16db-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e16db-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e16db-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e16db-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e16db-134"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="e16db-134"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="e16db-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="e16db-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="e16db-136"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e16db-136"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e16db-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e16db-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e16db-138"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e16db-138"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="e16db-139">CLSID</span><span class="sxs-lookup"><span data-stu-id="e16db-139">CLSID</span></span><br/>                    | <span data-ttu-id="e16db-140">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="e16db-140">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="e16db-141">IID</span><span class="sxs-lookup"><span data-stu-id="e16db-141">IID</span></span><br/>                      | <span data-ttu-id="e16db-142">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="e16db-142">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="e16db-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e16db-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e16db-144">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="e16db-144">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="e16db-145">**SWbemQualifier**</span><span class="sxs-lookup"><span data-stu-id="e16db-145">**SWbemQualifier**</span></span>](swbemqualifier.md)
</dt> </dl>

 

 




