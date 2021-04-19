---
description: La \_ méthode CompareTo de l’objet SWbemLastError compare deux objets SWbemObject. Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre iFlags.
ms.assetid: 541510e4-ef8d-4436-966f-19c5df422281
ms.tgt_platform: multiple
title: Méthode SWbemLastError.CompareTo_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
- ISWbemLastError.CompareTo_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c24eb6e57e81c6c44922b2d6643be65198951ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524564"
---
# <a name="swbemlasterrorcompareto_-method"></a><span data-ttu-id="d72c9-104">SWbemLastError. CompareTo, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="d72c9-104">SWbemLastError.CompareTo\_ method</span></span>

<span data-ttu-id="d72c9-105">La **méthode \_ CompareTo** de l’objet [**SWbemLastError**](swbemlasterror.md) compare deux objets [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d72c9-105">The **CompareTo\_** method of the [**SWbemLastError**](swbemlasterror.md) object compares two [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="d72c9-106">Cette comparaison est soumise à certaines contraintes basées sur les valeurs spécifiées dans le paramètre *IFlags* .</span><span class="sxs-lookup"><span data-stu-id="d72c9-106">This comparison is subject to certain constraints based on the values specified in the *iFlags* parameter.</span></span>

<span data-ttu-id="d72c9-107">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d72c9-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d72c9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d72c9-108">Syntax</span></span>


```VB
bAreEqual = .CompareTo_( _
  ByVal objwbemObject, _
  [ ByVal iFlags ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d72c9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d72c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d72c9-110">*objwbemObject* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d72c9-110">*objwbemObject* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d72c9-111">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d72c9-111">Required.</span></span> <span data-ttu-id="d72c9-112">Objet de classe [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="d72c9-112">An [**SWbemObject**](swbemobject.md) class object.</span></span> <span data-ttu-id="d72c9-113">Ce paramètre est l’objet avec lequel le premier objet est comparé.</span><span class="sxs-lookup"><span data-stu-id="d72c9-113">This parameter is the object with which the first object is compared.</span></span> <span data-ttu-id="d72c9-114">L’objet doit être une instance **SWbemObject** valide.</span><span class="sxs-lookup"><span data-stu-id="d72c9-114">The object must be a valid **SWbemObject** instance.</span></span>

</dd> <dt>

<span data-ttu-id="d72c9-115">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d72c9-115">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d72c9-116">Entier qui spécifie des indicateurs supplémentaires pour l’opération.</span><span class="sxs-lookup"><span data-stu-id="d72c9-116">An integer that specifies additional flags to the operation.</span></span> <span data-ttu-id="d72c9-117">Ce paramètre spécifie les caractéristiques d’objet à prendre en compte lorsque les comparaisons d’objets sont effectuées.</span><span class="sxs-lookup"><span data-stu-id="d72c9-117">This parameter specifies the object characteristics to consider when object comparisons are made.</span></span> <span data-ttu-id="d72c9-118">Vous pouvez utiliser **wbemComparisonFlagIncludeAll** pour prendre en compte toutes les fonctionnalités (par défaut) ou n’importe quelle combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d72c9-118">You can use **wbemComparisonFlagIncludeAll** to consider all features (default) or any combination of the following values.</span></span>

<dt>

<span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>

<span data-ttu-id="d72c9-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>wbemComparisonFlagIncludeAll \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d72c9-119"><span id="wbemComparisonFlagIncludeAll"></span><span id="wbemcomparisonflagincludeall"></span><span id="WBEMCOMPARISONFLAGINCLUDEALL"></span>\*\*\*\*wbemComparisonFlagIncludeAll\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-120">Fait en sorte que toutes les propriétés, qualificateurs et versions soient comparés.</span><span class="sxs-lookup"><span data-stu-id="d72c9-120">Causes all properties, qualifiers, and flavors to be compared.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>

<span data-ttu-id="d72c9-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>wbemComparisonFlagIgnoreQualifiers \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="d72c9-121"><span id="wbemComparisonFlagIgnoreQualifiers"></span><span id="wbemcomparisonflagignorequalifiers"></span><span id="WBEMCOMPARISONFLAGIGNOREQUALIFIERS"></span>\*\*\*\*wbemComparisonFlagIgnoreQualifiers\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-122">Fait en sorte que tous les qualificateurs (y compris la **clé** et le **dynamique**) soient ignorés en comparaison.</span><span class="sxs-lookup"><span data-stu-id="d72c9-122">Causes all qualifiers (including **Key** and **Dynamic**) to be ignored in comparison.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>

<span data-ttu-id="d72c9-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>wbemComparisonFlagIgnoreObjectSource \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="d72c9-123"><span id="wbemComparisonFlagIgnoreObjectSource"></span><span id="wbemcomparisonflagignoreobjectsource"></span><span id="WBEMCOMPARISONFLAGIGNOREOBJECTSOURCE"></span>\*\*\*\*wbemComparisonFlagIgnoreObjectSource\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-124">Fait en sorte que la source des objets, à savoir le serveur et l’espace de noms dont ils proviennent, soit ignorée par rapport aux autres objets.</span><span class="sxs-lookup"><span data-stu-id="d72c9-124">Causes the source of the objects, namely the server and the namespace they came from, to be ignored in comparison to other objects.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>

<span data-ttu-id="d72c9-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>wbemComparisonFlagIgnoreDefaultValues \* \* \* \* (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="d72c9-125"><span id="wbemComparisonFlagIgnoreDefaultValues"></span><span id="wbemcomparisonflagignoredefaultvalues"></span><span id="WBEMCOMPARISONFLAGIGNOREDEFAULTVALUES"></span>\*\*\*\*wbemComparisonFlagIgnoreDefaultValues\*\*\*\* (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-126">Entraîne l’ignorance des valeurs par défaut des propriétés.</span><span class="sxs-lookup"><span data-stu-id="d72c9-126">Causes the default values of properties to be ignored.</span></span> <span data-ttu-id="d72c9-127">Cet indicateur est significatif uniquement lors de la comparaison de classes.</span><span class="sxs-lookup"><span data-stu-id="d72c9-127">This flag is only meaningful when comparing classes.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>

<span data-ttu-id="d72c9-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>wbemComparisonFlagIgnoreClass \* \* \* \* (8 (0x8))</span><span class="sxs-lookup"><span data-stu-id="d72c9-128"><span id="wbemComparisonFlagIgnoreClass"></span><span id="wbemcomparisonflagignoreclass"></span><span id="WBEMCOMPARISONFLAGIGNORECLASS"></span>\*\*\*\*wbemComparisonFlagIgnoreClass\*\*\*\* (8 (0x8))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-129">Indique au système de supposer que les objets comparés sont des instances de la même classe.</span><span class="sxs-lookup"><span data-stu-id="d72c9-129">Instructs the system to assume that the objects being compared are instances of the same class.</span></span> <span data-ttu-id="d72c9-130">Par conséquent, cet indicateur ne compare que les informations relatives à l’instance.</span><span class="sxs-lookup"><span data-stu-id="d72c9-130">Consequently, this flag compares instance-related information only.</span></span> <span data-ttu-id="d72c9-131">Utilisez cet indicateur pour optimiser les performances.</span><span class="sxs-lookup"><span data-stu-id="d72c9-131">Use this flag to optimize performance.</span></span> <span data-ttu-id="d72c9-132">Si les objets ne sont pas de la même classe, les résultats sont non définis.</span><span class="sxs-lookup"><span data-stu-id="d72c9-132">If the objects are not of the same class, the results are undefined.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>

<span data-ttu-id="d72c9-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>wbemComparisonFlagIgnoreCase \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="d72c9-133"><span id="wbemComparisonFlagIgnoreCase"></span><span id="wbemcomparisonflagignorecase"></span><span id="WBEMCOMPARISONFLAGIGNORECASE"></span>\*\*\*\*wbemComparisonFlagIgnoreCase\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-134">Fait en sorte que les valeurs de chaîne soient comparées sans respect de la casse.</span><span class="sxs-lookup"><span data-stu-id="d72c9-134">Causes string values to be compared in a case-insensitive manner.</span></span> <span data-ttu-id="d72c9-135">Cela s’applique à la fois aux chaînes et aux valeurs de qualificateur.</span><span class="sxs-lookup"><span data-stu-id="d72c9-135">This applies both to strings and to qualifier values.</span></span> <span data-ttu-id="d72c9-136">Les noms de propriétés et de qualificateurs sont toujours comparés sans distinction minuscules/majuscules, que cet indicateur soit spécifié ou non.</span><span class="sxs-lookup"><span data-stu-id="d72c9-136">Property and qualifier names are always compared in a case-insensitive manner whether this flag is specified or not.</span></span>

</dd> <dt>

<span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>

<span data-ttu-id="d72c9-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>wbemComparisonFlagIgnoreFlavor \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="d72c9-137"><span id="wbemComparisonFlagIgnoreFlavor"></span><span id="wbemcomparisonflagignoreflavor"></span><span id="WBEMCOMPARISONFLAGIGNOREFLAVOR"></span>\*\*\*\*wbemComparisonFlagIgnoreFlavor\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="d72c9-138">Fait en sorte que les versions de qualificateur soient ignorées.</span><span class="sxs-lookup"><span data-stu-id="d72c9-138">Causes qualifier flavors to be ignored.</span></span> <span data-ttu-id="d72c9-139">Cet indicateur tient compte des valeurs de qualificateur, mais ignore les distinctions de version telles que les règles de propagation et les restrictions de substitution.</span><span class="sxs-lookup"><span data-stu-id="d72c9-139">This flag still takes qualifier values into account, but ignores flavor distinctions such as propagation rules and override restrictions.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d72c9-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d72c9-140">Return value</span></span>

<span data-ttu-id="d72c9-141">La **méthode \_ CompareTo** retourne la valeur booléenne **true** si les objets correspondent ; sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="d72c9-141">The **CompareTo\_** method returns the Boolean value **TRUE** if the objects match; otherwise, it returns **FALSE**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d72c9-142">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="d72c9-142">Error codes</span></span>

<span data-ttu-id="d72c9-143">À la fin de la **méthode \_ CompareTo** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="d72c9-143">Upon the completion of the **CompareTo\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d72c9-144">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d72c9-144">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d72c9-145">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d72c9-145">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d72c9-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d72c9-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d72c9-147">Un paramètre spécifié n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d72c9-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d72c9-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d72c9-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d72c9-149">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="d72c9-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d72c9-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d72c9-150">Requirements</span></span>



| <span data-ttu-id="d72c9-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d72c9-151">Requirement</span></span> | <span data-ttu-id="d72c9-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="d72c9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d72c9-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d72c9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="d72c9-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d72c9-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d72c9-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d72c9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="d72c9-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d72c9-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d72c9-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="d72c9-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="d72c9-158"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d72c9-158"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d72c9-159">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d72c9-159">Type library</span></span><br/>             | <dl> <span data-ttu-id="d72c9-160"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d72c9-160"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d72c9-161">DLL</span><span class="sxs-lookup"><span data-stu-id="d72c9-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d72c9-162"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d72c9-162"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d72c9-163">CLSID</span><span class="sxs-lookup"><span data-stu-id="d72c9-163">CLSID</span></span><br/>                    | <span data-ttu-id="d72c9-164">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="d72c9-164">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="d72c9-165">IID</span><span class="sxs-lookup"><span data-stu-id="d72c9-165">IID</span></span><br/>                      | <span data-ttu-id="d72c9-166">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="d72c9-166">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="d72c9-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d72c9-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d72c9-168">**SWbemLastError**</span><span class="sxs-lookup"><span data-stu-id="d72c9-168">**SWbemLastError**</span></span>](swbemlasterror.md)
</dt> <dt>

[<span data-ttu-id="d72c9-169">**M**</span><span class="sxs-lookup"><span data-stu-id="d72c9-169">**SWbemObject**</span></span>](swbemobject.md)
</dt> </dl>

 

 




