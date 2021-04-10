---
description: La \_ méthode CompareTo de l’objet SWbemObject compare deux objets SWbemObject. Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre iFlags.
ms.assetid: 38813551-2403-4def-ae57-2b17f72cd180
ms.tgt_platform: multiple
title: Méthode SWbemObject.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.CompareTo_
- ISWbemObject.CompareTo_
- ISWbemObject.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f77bf9db9ee864e136ba695051445e543b466e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755013"
---
# <a name="swbemobjectcompareto_-method"></a><span data-ttu-id="99112-104">SWbemObject. CompareTo, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="99112-104">SWbemObject.CompareTo\_ method</span></span>

<span data-ttu-id="99112-105">La **méthode \_ CompareTo** de l’objet [**SWbemObject**](swbemobject.md) compare deux objets **SWbemObject** .</span><span class="sxs-lookup"><span data-stu-id="99112-105">The **CompareTo\_** method of the [**SWbemObject**](swbemobject.md) object compares two **SWbemObject** objects.</span></span> <span data-ttu-id="99112-106">Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="99112-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="99112-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="99112-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="99112-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99112-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="99112-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99112-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99112-110">*objwbemObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="99112-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99112-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="99112-111">Required.</span></span> <span data-ttu-id="99112-112">Ce paramètre est un objet [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="99112-112">This parameter is an [**SWbemObject**](swbemobject.md) object.</span></span> <span data-ttu-id="99112-113">Il s’agit de l’objet avec lequel le premier objet est comparé.</span><span class="sxs-lookup"><span data-stu-id="99112-113">This is the object with which the first object is compared.</span></span> <span data-ttu-id="99112-114">L’objet doit être une instance **SWbemObject** valide.</span><span class="sxs-lookup"><span data-stu-id="99112-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="99112-115">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="99112-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="99112-116">Spécifie les caractéristiques d’objet à prendre en compte lors de la comparaison d’un objet avec d’autres objets.</span><span class="sxs-lookup"><span data-stu-id="99112-116">Specifies the object characteristics to consider when comparing an object with other objects.</span></span> <span data-ttu-id="99112-117">Vous pouvez utiliser **wbemComparisonFlagIncludeAll** pour prendre en compte toutes les fonctionnalités (il s’agit de la valeur par défaut) ou n’importe quelle combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="99112-117">You can use **wbemComparisonFlagIncludeAll** to consider all features (this is the default), or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="99112-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="99112-118"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="99112-119">Compare toutes les propriétés, qualificateurs et versions.</span><span class="sxs-lookup"><span data-stu-id="99112-119">Compares all properties, qualifiers, and flavors.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="99112-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="99112-120"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="99112-121">Fait en sorte que la source des objets, à savoir le serveur et l’espace de noms dont ils proviennent, soit ignorée par rapport aux autres objets.</span><span class="sxs-lookup"><span data-stu-id="99112-121">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="99112-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="99112-122"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="99112-123">Fait en sorte que tous les qualificateurs (y compris la **clé** et le **dynamique**) soient ignorés en comparaison.</span><span class="sxs-lookup"><span data-stu-id="99112-123">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="99112-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="99112-124"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="99112-125">Entraîne l’ignorance des valeurs par défaut des propriétés.</span><span class="sxs-lookup"><span data-stu-id="99112-125">Causes default values of properties to be ignored.</span></span> <span data-ttu-id="99112-126">Cet indicateur est significatif uniquement lors de la comparaison de classes.</span><span class="sxs-lookup"><span data-stu-id="99112-126">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="99112-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="99112-127"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="99112-128">Fait en sorte que les versions de qualificateur soient ignorées.</span><span class="sxs-lookup"><span data-stu-id="99112-128">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="99112-129">Cet indicateur prend en compte les valeurs de qualificateur, mais ignore les distinctions de parfum telles que les règles de propagation et les restrictions de remplacement.</span><span class="sxs-lookup"><span data-stu-id="99112-129">This flag takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="99112-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="99112-130"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="99112-131">Compare les valeurs de chaîne sans respect de la casse.</span><span class="sxs-lookup"><span data-stu-id="99112-131">Compares string values in a case-insensitive manner.</span></span> <span data-ttu-id="99112-132">Cela s’applique à la fois aux chaînes et aux valeurs de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="99112-132">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="99112-133">Les noms de propriétés et de qualificateurs sont toujours comparés sans distinction minuscules/majuscules, que cet indicateur soit spécifié ou non.</span><span class="sxs-lookup"><span data-stu-id="99112-133">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="99112-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="99112-134"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="99112-135">Indique au système de supposer que les objets comparés sont des instances de la même classe.</span><span class="sxs-lookup"><span data-stu-id="99112-135">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="99112-136">Par conséquent, cet indicateur ne compare que les informations relatives à l’instance.</span><span class="sxs-lookup"><span data-stu-id="99112-136">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="99112-137">Utilisez cet indicateur pour optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="99112-137">Use this flag to optimize performance.</span></span> <span data-ttu-id="99112-138">Si les objets ne sont pas de la même classe, les résultats sont non définis.</span><span class="sxs-lookup"><span data-stu-id="99112-138">If the objects are not of the same class, the results are undefined.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99112-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="99112-139">Return value</span></span>

<span data-ttu-id="99112-140">Cette méthode retourne la valeur booléenne **true** si les objets correspondent.</span><span class="sxs-lookup"><span data-stu-id="99112-140">This method returns the Boolean value of **TRUE** if the objects match.</span></span> <span data-ttu-id="99112-141">Elle retourne la **valeur false** si les objets ne correspondent pas.</span><span class="sxs-lookup"><span data-stu-id="99112-141">It returns **FALSE** if the objects do not match.</span></span>

## <a name="error-codes"></a><span data-ttu-id="99112-142">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="99112-142">Error codes</span></span>

<span data-ttu-id="99112-143">Une fois la méthode **CompareTo \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="99112-143">After the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="99112-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="99112-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="99112-145">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="99112-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="99112-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="99112-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="99112-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="99112-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="99112-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="99112-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="99112-149">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="99112-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="99112-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="99112-150">Requirements</span></span>



| <span data-ttu-id="99112-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="99112-151">Requirement</span></span> | <span data-ttu-id="99112-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="99112-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="99112-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99112-153">Minimum supported client</span></span><br/> | <span data-ttu-id="99112-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="99112-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="99112-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="99112-155">Minimum supported server</span></span><br/> | <span data-ttu-id="99112-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="99112-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="99112-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="99112-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="99112-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="99112-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="99112-159">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="99112-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="99112-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="99112-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="99112-161">DLL</span><span class="sxs-lookup"><span data-stu-id="99112-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="99112-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="99112-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="99112-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="99112-163">CLSID</span></span><br/>                    | <span data-ttu-id="99112-164">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="99112-164">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="99112-165">IID</span><span class="sxs-lookup"><span data-stu-id="99112-165">IID</span></span><br/>                      | <span data-ttu-id="99112-166">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="99112-166">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="99112-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="99112-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99112-168">**M**</span><span class="sxs-lookup"><span data-stu-id="99112-168">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




