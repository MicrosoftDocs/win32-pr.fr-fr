---
description: La méthode Add de l’objet SWbemQualifierSet ajoute un objet SWbemQualifier à la collection SWbemQualifierSet. Si un qualificateur portant le même nom existe déjà dans la collection, il est remplacé.
ms.assetid: 8f4c4da2-4890-4515-a3dc-76d154dae43c
ms.tgt_platform: multiple
title: Méthode SWbemQualifierSet. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet.Add
- ISWbemQualifierSet.Add
- ISWbemQualifierSet.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: bbbef15ccc45aeba5b7e3c03f6cb9448cfe03ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320657"
---
# <a name="swbemqualifiersetadd-method"></a><span data-ttu-id="81173-104">SWbemQualifierSet. Add, méthode</span><span class="sxs-lookup"><span data-stu-id="81173-104">SWbemQualifierSet.Add method</span></span>

<span data-ttu-id="81173-105">La méthode **Add** de l’objet [**SWbemQualifierSet**](swbemqualifierset.md) ajoute un objet [**SWbemQualifier**](swbemqualifier.md) à la collection **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="81173-105">The **Add** method of the [**SWbemQualifierSet**](swbemqualifierset.md) object adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span> <span data-ttu-id="81173-106">Si un qualificateur portant le même nom existe déjà dans la collection, il est remplacé.</span><span class="sxs-lookup"><span data-stu-id="81173-106">If a qualifier with the same name already exists in the collection, it is replaced.</span></span>

<span data-ttu-id="81173-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="81173-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="81173-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="81173-108">Syntax</span></span>


```VB
objQualifier = .Add( _
  ByVal strName, _
  ByVal varVal, _
  [ ByVal bPropagatesToSubclasses ], _
  [ ByVal bPropagatesToInstances ], _
  [ ByVal bOverridable ], _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="81173-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="81173-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="81173-110">*strName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81173-110">*strName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81173-111">Required.</span></span> <span data-ttu-id="81173-112">Nom du nouveau qualificateur.</span><span class="sxs-lookup"><span data-stu-id="81173-112">Name of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="81173-113">*varVal* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="81173-113">*varVal* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="81173-114">Required.</span></span> <span data-ttu-id="81173-115">Valeur de type Variant du nouveau qualificateur.</span><span class="sxs-lookup"><span data-stu-id="81173-115">Variant value of the new qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="81173-116">*bPropagatesToSubclasses* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="81173-116">*bPropagatesToSubclasses* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-117">Valeur booléenne qui indique si ce nouveau qualificateur est propagé aux sous-classes.</span><span class="sxs-lookup"><span data-stu-id="81173-117">Boolean value that indicates if this new qualifier is propagated to subclasses.</span></span> <span data-ttu-id="81173-118">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="81173-118">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="81173-119">*bPropagatesToInstances* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="81173-119">*bPropagatesToInstances* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-120">Valeur booléenne qui indique si ce nouveau qualificateur est propagé aux instances.</span><span class="sxs-lookup"><span data-stu-id="81173-120">Boolean value that indicates if this new qualifier is propagated to instances.</span></span> <span data-ttu-id="81173-121">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="81173-121">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="81173-122">*bOverridable* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="81173-122">*bOverridable* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-123">Valeur booléenne qui indique si ce qualificateur peut être substitué lorsqu’il est propagé.</span><span class="sxs-lookup"><span data-stu-id="81173-123">Boolean value that indicates if this qualifier can be overridden when propagated.</span></span> <span data-ttu-id="81173-124">La valeur par défaut est **true**.</span><span class="sxs-lookup"><span data-stu-id="81173-124">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="81173-125">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="81173-125">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="81173-126">Réservé.</span><span class="sxs-lookup"><span data-stu-id="81173-126">Reserved.</span></span> <span data-ttu-id="81173-127">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="81173-127">The default value is 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="81173-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="81173-128">Return value</span></span>

<span data-ttu-id="81173-129">En cas de réussite, cette méthode retourne un objet [**SWbemQualifier**](swbemqualifier.md) qui représente le nouveau qualificateur.</span><span class="sxs-lookup"><span data-stu-id="81173-129">If successful, this method returns an [**SWbemQualifier**](swbemqualifier.md) object that represents the new qualifier.</span></span> <span data-ttu-id="81173-130">Dans le cas contraire, un objet **null** est retourné.</span><span class="sxs-lookup"><span data-stu-id="81173-130">Otherwise, a **null** object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="81173-131">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="81173-131">Error codes</span></span>

<span data-ttu-id="81173-132">Une fois la méthode **Add** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="81173-132">After completion of the **Add** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="81173-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="81173-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="81173-134">Le paramètre *IFlags* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="81173-134">The *iFlags* parameter was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="81173-135">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="81173-135">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="81173-136">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="81173-136">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="81173-137">**wbemErrCannotBeKey** -2147749919 (0x8004101F)</span><span class="sxs-lookup"><span data-stu-id="81173-137">**wbemErrCannotBeKey** - 2147749919 (0x8004101F)</span></span>
</dt> <dd>

<span data-ttu-id="81173-138">Tentative non autorisée de spécifier un qualificateur de **clé** sur une propriété qui ne peut pas être une clé.</span><span class="sxs-lookup"><span data-stu-id="81173-138">There was an illegal attempt to specify a **Key** qualifier on a property that cannot be a key.</span></span> <span data-ttu-id="81173-139">Les clés sont spécifiées dans la définition de classe pour un objet et ne peuvent pas être modifiées au niveau de l'instance.</span><span class="sxs-lookup"><span data-stu-id="81173-139">The keys are specified in the class definition for an object and cannot be altered on a per-instance basis.</span></span>

</dd> <dt>

<span data-ttu-id="81173-140">**wbemErrInvalidQualifierType** -2147749929 (0x80041029)</span><span class="sxs-lookup"><span data-stu-id="81173-140">**wbemErrInvalidQualifierType** - 2147749929 (0x80041029)</span></span>
</dt> <dd>

<span data-ttu-id="81173-141">Le paramètre *varVal* n’est pas un type de qualificateur légal.</span><span class="sxs-lookup"><span data-stu-id="81173-141">The *varVal* parameter is not of a legal qualifier type.</span></span>

</dd> <dt>

<span data-ttu-id="81173-142">**wbemErrOverrideNotAllowed** -2147749914 (0x8004101A)</span><span class="sxs-lookup"><span data-stu-id="81173-142">**wbemErrOverrideNotAllowed** - 2147749914 (0x8004101A)</span></span>
</dt> <dd>

<span data-ttu-id="81173-143">Il n’est pas possible d’effectuer l’opération **SWbemQualifierSet. Add** sur ce qualificateur, car l’objet propriétaire n’autorise pas les remplacements.</span><span class="sxs-lookup"><span data-stu-id="81173-143">It is not possible to perform the **SWbemQualifierSet.Add** operation on this qualifier because the owning object does not permit overrides.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="81173-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="81173-144">Requirements</span></span>



| <span data-ttu-id="81173-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="81173-145">Requirement</span></span> | <span data-ttu-id="81173-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="81173-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="81173-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81173-147">Minimum supported client</span></span><br/> | <span data-ttu-id="81173-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="81173-148">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="81173-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="81173-149">Minimum supported server</span></span><br/> | <span data-ttu-id="81173-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="81173-150">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="81173-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="81173-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="81173-152"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="81173-152"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="81173-153">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="81173-153">Type library</span></span><br/>             | <dl> <span data-ttu-id="81173-154"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="81173-154"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="81173-155">DLL</span><span class="sxs-lookup"><span data-stu-id="81173-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="81173-156"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="81173-156"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="81173-157">CLSID</span><span class="sxs-lookup"><span data-stu-id="81173-157">CLSID</span></span><br/>                    | <span data-ttu-id="81173-158">CLSID \_ SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="81173-158">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="81173-159">IID</span><span class="sxs-lookup"><span data-stu-id="81173-159">IID</span></span><br/>                      | <span data-ttu-id="81173-160">IID \_ ISWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="81173-160">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="81173-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="81173-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81173-162">**SWbemQualifierSet**</span><span class="sxs-lookup"><span data-stu-id="81173-162">**SWbemQualifierSet**</span></span>](swbemqualifierset.md)
</dt> <dt>

[<span data-ttu-id="81173-163">**SWbemQualifierSet. Remove**</span><span class="sxs-lookup"><span data-stu-id="81173-163">**SWbemQualifierSet.Remove**</span></span>](swbemqualifierset-remove.md)
</dt> </dl>

 

 




