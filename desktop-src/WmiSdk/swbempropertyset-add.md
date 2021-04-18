---
description: La méthode Add de l’objet SWbemPropertySet ajoute un objet SWbemProperty à la collection SWbemPropertySet. Si une propriété du même nom existe déjà dans la collection, son contenu est remplacé par la nouvelle définition.
ms.assetid: 52a5f964-3d53-441b-9a58-650afdc5b1b9
ms.tgt_platform: multiple
title: Méthode SWbemPropertySet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet.Add
- ISWbemPropertySet.Add
- ISWbemPropertySet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1ad5b40d31d162b287bdb1a387cd0602e0be1ce6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526930"
---
# <a name="swbempropertysetadd-method"></a><span data-ttu-id="eb758-104">SWbemPropertySet. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="eb758-104">SWbemPropertySet.Add method</span></span>

<span data-ttu-id="eb758-105">La méthode **Add** de l’objet [**SWbemPropertySet**](swbempropertyset.md) ajoute un objet [**SWbemProperty**](swbemproperty.md) à la collection **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="eb758-105">The **Add** method of the [**SWbemPropertySet**](swbempropertyset.md) object adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span> <span data-ttu-id="eb758-106">Si une propriété du même nom existe déjà dans la collection, son contenu est remplacé par la nouvelle définition.</span><span class="sxs-lookup"><span data-stu-id="eb758-106">If a property with the same name already exists in the collection, its contents are replaced with the new definition.</span></span>

> [!Note]  
> <span data-ttu-id="eb758-107">La valeur de la propriété ajoutée est **null** (non assigné) après cette opération.</span><span class="sxs-lookup"><span data-stu-id="eb758-107">The value of the added property is **NULL** (unassigned) after this operation.</span></span> <span data-ttu-id="eb758-108">Pour définir ou modifier la valeur d’une propriété WMI, vous devez définir la propriété [**value**](swbemdatetime-value.md) de l’objet [**SWbemProperty**](swbemproperty.md) retourné.</span><span class="sxs-lookup"><span data-stu-id="eb758-108">To set or change the value of a WMI property, you must set the [**Value**](swbemdatetime-value.md) property of the returned [**SWbemProperty**](swbemproperty.md) object.</span></span>

 

<span data-ttu-id="eb758-109">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="eb758-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb758-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb758-110">Syntax</span></span>


```VB
objProperty = .Add( _
  ByVal strName, _
  ByVal iCIMType, _
  [ ByVal bIsArray ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="eb758-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb758-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb758-112">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb758-112">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb758-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eb758-113">Required.</span></span> <span data-ttu-id="eb758-114">Nom de la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="eb758-114">Name of the new property.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-115">*iCIMType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="eb758-115">*iCIMType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eb758-116">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="eb758-116">Required.</span></span> <span data-ttu-id="eb758-117">Entier qui représente le qualificateur **CimType** de la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="eb758-117">An integer that represents the **CIMType** qualifier of the new property.</span></span> <span data-ttu-id="eb758-118">Consultez [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) pour obtenir la liste avec les qualificateurs **CimType** et leurs valeurs.</span><span class="sxs-lookup"><span data-stu-id="eb758-118">See [**WbemCimTypeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum) for the list with the **CIMType** qualifiers and their values.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-119">*bIsArray* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb758-119">*bIsArray* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb758-120">Spécifie si la propriété est un type tableau.</span><span class="sxs-lookup"><span data-stu-id="eb758-120">Specifies whether the property is an array type.</span></span> <span data-ttu-id="eb758-121">La valeur par défaut de ce paramètre est **false**.</span><span class="sxs-lookup"><span data-stu-id="eb758-121">The default value for this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-122">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="eb758-122">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb758-123">Réservé et doit être égal à zéro s’il est spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb758-123">Reserved and must be zero if specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb758-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="eb758-124">Return value</span></span>

<span data-ttu-id="eb758-125">En cas de réussite, cette méthode retourne un objet [**SWbemProperty**](swbemproperty.md) qui représente la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="eb758-125">If successful, this method returns an [**SWbemProperty**](swbemproperty.md) object that represents the new property.</span></span> <span data-ttu-id="eb758-126">Dans le cas contraire, un objet **null** est retourné.</span><span class="sxs-lookup"><span data-stu-id="eb758-126">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="eb758-127">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="eb758-127">Error codes</span></span>

<span data-ttu-id="eb758-128">Une fois la méthode **Add** terminée, l’objet **Err** peut contenir l’un des codes d’erreur ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="eb758-128">After completion of the **Add** method, the **Err** object may contain one of the error codes below.</span></span>

<dl> <dt>

<span data-ttu-id="eb758-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="eb758-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="eb758-130">Échec non spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb758-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-131">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="eb758-131">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="eb758-132">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="eb758-132">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-133">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="eb758-133">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="eb758-134">Mémoire insuffisante pour l’exécution de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="eb758-134">Not enough memory for this method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="eb758-135">**wbemErrInvalidPropertyType** -2147749930</span><span class="sxs-lookup"><span data-stu-id="eb758-135">**wbemErrInvalidPropertyType** - 2147749930</span></span>
</dt> <dd>

<span data-ttu-id="eb758-136">Le qualificateur **CimType** n’est pas reconnu.</span><span class="sxs-lookup"><span data-stu-id="eb758-136">The **CIMType** qualifier is not recognized.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="eb758-137">Exemples</span><span class="sxs-lookup"><span data-stu-id="eb758-137">Examples</span></span>

<span data-ttu-id="eb758-138">Pour obtenir un exemple de code qui utilise cette méthode, consultez la rubrique [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="eb758-138">For a code example that uses this method, see the [**SWbemPropertySet**](swbempropertyset.md) topic.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb758-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eb758-139">Requirements</span></span>



| <span data-ttu-id="eb758-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eb758-140">Requirement</span></span> | <span data-ttu-id="eb758-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="eb758-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb758-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb758-142">Minimum supported client</span></span><br/> | <span data-ttu-id="eb758-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb758-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb758-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="eb758-144">Minimum supported server</span></span><br/> | <span data-ttu-id="eb758-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb758-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb758-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="eb758-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb758-147"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb758-147"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb758-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="eb758-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="eb758-149"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="eb758-149"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="eb758-150">DLL</span><span class="sxs-lookup"><span data-stu-id="eb758-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb758-151"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb758-151"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="eb758-152">CLSID</span><span class="sxs-lookup"><span data-stu-id="eb758-152">CLSID</span></span><br/>                    | <span data-ttu-id="eb758-153">CLSID \_ SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="eb758-153">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="eb758-154">IID</span><span class="sxs-lookup"><span data-stu-id="eb758-154">IID</span></span><br/>                      | <span data-ttu-id="eb758-155">IID \_ ISWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="eb758-155">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="eb758-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb758-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb758-157">**SWbemPropertySet**</span><span class="sxs-lookup"><span data-stu-id="eb758-157">**SWbemPropertySet**</span></span>](swbempropertyset.md)
</dt> <dt>

[<span data-ttu-id="eb758-158">**SWbemPropertySet. Remove**</span><span class="sxs-lookup"><span data-stu-id="eb758-158">**SWbemPropertySet.Remove**</span></span>](swbempropertyset-remove.md)
</dt> <dt>

[<span data-ttu-id="eb758-159">**SWbemProperty. Value**</span><span class="sxs-lookup"><span data-stu-id="eb758-159">**SWbemProperty.Value**</span></span>](swbemproperty-value.md)
</dt> </dl>

 

 




