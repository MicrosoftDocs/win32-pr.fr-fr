---
description: La méthode Remove de l’objet SWbemQualifierSet supprime un qualificateur nommé de la collection.
ms.assetid: 7d386858-efd1-42e6-9176-9cb4bcfc77d0
ms.tgt_platform: multiple
title: SWbemQualifierSet. Remove, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
- ISWbemQualifierSet.Remove
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 39c95f268328bc0cad3f3c0874b633fc36c4f5b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528473"
---
# <a name="swbemqualifiersetremove-method"></a><span data-ttu-id="8cf9f-103">SWbemQualifierSet. Remove, méthode</span><span class="sxs-lookup"><span data-stu-id="8cf9f-103">SWbemQualifierSet.Remove method</span></span>

<span data-ttu-id="8cf9f-104">La méthode **Remove** de l’objet [**SWbemQualifierSet**](swbemqualifierset.md) supprime un qualificateur nommé de la collection.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-104">The **Remove** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object deletes a named qualifier from the collection.</span></span>

<span data-ttu-id="8cf9f-105">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8cf9f-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8cf9f-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cf9f-106">Syntax</span></span>


```VB
SWbemQualifierSet.Remove( _
  ByVal strName, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8cf9f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cf9f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8cf9f-108">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8cf9f-108">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-109">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-109">Required.</span></span> <span data-ttu-id="8cf9f-110">Nom du qualificateur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-110">Name of the qualifier to remove.</span></span>

</dd> <dt>

<span data-ttu-id="8cf9f-111">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="8cf9f-111">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-112">Réservé.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-112">Reserved.</span></span> <span data-ttu-id="8cf9f-113">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-113">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8cf9f-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8cf9f-114">Return value</span></span>

<span data-ttu-id="8cf9f-115">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-115">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8cf9f-116">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="8cf9f-116">Error codes</span></span>

<span data-ttu-id="8cf9f-117">À la fin de la méthode **Remove** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-117">After completion of the **Remove** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8cf9f-118">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8cf9f-118">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-119">Le paramètre *IFlags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-119">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8cf9f-120">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8cf9f-120">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-121">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-121">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8cf9f-122">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="8cf9f-122">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-123">Le qualificateur spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-123">Specified qualifier does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8cf9f-124">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="8cf9f-124">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="8cf9f-125">La suppression de ce qualificateur n’est pas conforme.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-125">Removing this qualifier is illegal.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8cf9f-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8cf9f-126">Remarks</span></span>

<span data-ttu-id="8cf9f-127">Vous ne pouvez pas itérer une collection lors de la suppression d’éléments, car lorsque vous supprimez un élément d’une collection, le pointeur de collection est déplacé vers l’élément suivant.</span><span class="sxs-lookup"><span data-stu-id="8cf9f-127">You cannot iterate a collection while removing items because when you remove an element from a collection, the collection pointer is moved to the next element.</span></span> <span data-ttu-id="8cf9f-128">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="8cf9f-128">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8cf9f-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8cf9f-129">Requirements</span></span>



| <span data-ttu-id="8cf9f-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8cf9f-130">Requirement</span></span> | <span data-ttu-id="8cf9f-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8cf9f-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8cf9f-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cf9f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="8cf9f-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8cf9f-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8cf9f-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8cf9f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="8cf9f-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8cf9f-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8cf9f-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="8cf9f-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="8cf9f-137"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8cf9f-137"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8cf9f-138">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8cf9f-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="8cf9f-139"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8cf9f-139"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8cf9f-140">DLL</span><span class="sxs-lookup"><span data-stu-id="8cf9f-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8cf9f-141"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8cf9f-141"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8cf9f-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="8cf9f-142">CLSID</span></span><br/>                    | <span data-ttu-id="8cf9f-143">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="8cf9f-143">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="8cf9f-144">IID</span><span class="sxs-lookup"><span data-stu-id="8cf9f-144">IID</span></span><br/>                      | <span data-ttu-id="8cf9f-145">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="8cf9f-145">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="8cf9f-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8cf9f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8cf9f-147">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="8cf9f-147">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="8cf9f-148">**SWbemQualifierSet. Add**</span><span class="sxs-lookup"><span data-stu-id="8cf9f-148">**SWbemQualifierSet.Add**</span></span>](swbemqualifierset-add.md)
</dt> </dl>

 

 




