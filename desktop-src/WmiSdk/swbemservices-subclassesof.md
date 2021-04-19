---
description: Retourne un objet SWbemObjectSet.
ms.assetid: cfe08956-7215-4e2e-a279-6e86f14e5c27
ms.tgt_platform: multiple
title: SWbemServices. SubclassesOf, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
- ISWbemServices.SubclassesOf
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e8c23dee5ee3f0a1cf5babe37d0ccb6aa0a3ac7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520470"
---
# <a name="swbemservicessubclassesof-method"></a><span data-ttu-id="1e863-103">SWbemServices. SubclassesOf, méthode</span><span class="sxs-lookup"><span data-stu-id="1e863-103">SWbemServices.SubclassesOf method</span></span>

<span data-ttu-id="1e863-104">La méthode **SubclassesOf** de l’objet [**SWbemServices**](swbemservices.md) retourne un objet [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="1e863-104">The **SubclassesOf** method of the [**SWbemServices**](swbemservices.md) object returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="1e863-105">Cet objet est une collection de sous-classes d’une classe spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e863-105">This object is a collection of subclasses of a specified class.</span></span> <span data-ttu-id="1e863-106">Les éléments de la collection retournée peuvent être obtenus à l’aide de méthodes de collection standard.</span><span class="sxs-lookup"><span data-stu-id="1e863-106">Items in the returned collection can be obtained using standard collection methods.</span></span> <span data-ttu-id="1e863-107">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="1e863-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="1e863-108">Cette méthode fonctionne uniquement pour les objets de classe.</span><span class="sxs-lookup"><span data-stu-id="1e863-108">This method only works for class objects.</span></span>

<span data-ttu-id="1e863-109">La méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="1e863-109">The method is called in the semisynchronous mode.</span></span> <span data-ttu-id="1e863-110">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="1e863-110">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="1e863-111">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1e863-111">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1e863-112">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1e863-112">Syntax</span></span>


```VB
objWbemObjectSet = .SubclassesOf( _
  [ ByVal strSuperclass ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="1e863-113">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1e863-113">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e863-114">*strSuperclass* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e863-114">*strSuperclass* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e863-115">Spécifie un nom de classe parente.</span><span class="sxs-lookup"><span data-stu-id="1e863-115">Specifies a parent class name.</span></span> <span data-ttu-id="1e863-116">Seules les sous-classes de cette classe retournent dans l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="1e863-116">Only subclasses of this class return in the enumerator.</span></span> <span data-ttu-id="1e863-117">Si vous laissez ce paramètre vide et si *IFlags* est **wbemQueryFlagShallow**, seules les classes de niveau supérieur sont retournées (c’est-à-dire les classes qui n’ont pas de classe parente).</span><span class="sxs-lookup"><span data-stu-id="1e863-117">If you leave this parameter blank, and if *iFlags* is **wbemQueryFlagShallow**, only the top-level classes are returned (that is, classes that have no parent class).</span></span> <span data-ttu-id="1e863-118">Si ce paramètre est vide et que *IFlags* est **wbemQueryFlagDeep** , toutes les classes de l’espace de noms sont retournées.</span><span class="sxs-lookup"><span data-stu-id="1e863-118">If this parameter is blank and *iFlags* is **wbemQueryFlagDeep** all classes within the namespace are returned.</span></span>

</dd> <dt>

<span data-ttu-id="1e863-119">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e863-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e863-120">Détermine le détail de l’énumération des appels.</span><span class="sxs-lookup"><span data-stu-id="1e863-120">Determines how detailed the call enumerates.</span></span> <span data-ttu-id="1e863-121">Les valeurs par défaut de ce paramètre sont **wbemFlagReturnImmediately** et **wbemQueryFlagDeep**.</span><span class="sxs-lookup"><span data-stu-id="1e863-121">The default values for this parameter are **wbemFlagReturnImmediately** and **wbemQueryFlagDeep**.</span></span> <span data-ttu-id="1e863-122">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="1e863-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>

<span data-ttu-id="1e863-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>wbemQueryFlagShallow \* \* \* \* (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="1e863-123"><span id="wbemQueryFlagShallow"></span><span id="wbemqueryflagshallow"></span><span id="WBEMQUERYFLAGSHALLOW"></span>\*\*\*\*wbemQueryFlagShallow\*\*\*\* (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="1e863-124">Force l’énumération à inclure uniquement les sous-classes immédiates de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e863-124">Forces the enumeration to include only immediate subclasses of the specified parent class.</span></span>

</dd> <dt>

<span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>

<span data-ttu-id="1e863-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>wbemQueryFlagDeep \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1e863-125"><span id="wbemQueryFlagDeep"></span><span id="wbemqueryflagdeep"></span><span id="WBEMQUERYFLAGDEEP"></span>\*\*\*\*wbemQueryFlagDeep\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1e863-126">Valeur par défaut pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="1e863-126">Default for this parameter.</span></span> <span data-ttu-id="1e863-127">Cette valeur force l’énumération récursive dans toutes les sous-classes dérivées de la classe parente spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e863-127">This value forces recursive enumeration into all subclasses that are derived from the specified parent class.</span></span> <span data-ttu-id="1e863-128">La classe parente n’est pas retournée dans l’énumération.</span><span class="sxs-lookup"><span data-stu-id="1e863-128">The parent class is not returned in the enumeration.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="1e863-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="1e863-129"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="1e863-130">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="1e863-130">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="1e863-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="1e863-131"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="1e863-132">Provoque le blocage de cet appel jusqu’à la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="1e863-132">Causes this call to block until the call has completed.</span></span> <span data-ttu-id="1e863-133">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="1e863-133">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="1e863-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="1e863-134"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="1e863-135">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="1e863-135">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="1e863-136">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="1e863-136">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="1e863-137">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="1e863-137">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1e863-138">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="1e863-138">Typically, this is undefined.</span></span> <span data-ttu-id="1e863-139">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="1e863-139">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider servicing the request.</span></span> <span data-ttu-id="1e863-140">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="1e863-140">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e863-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1e863-141">Return value</span></span>

<span data-ttu-id="1e863-142">Si la méthode réussit, un objet [**SWbemObjectSet**](swbemobjectset.md) est retourné.</span><span class="sxs-lookup"><span data-stu-id="1e863-142">If the method is successful, an [**SWbemObjectSet**](swbemobjectset.md) object is returned.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1e863-143">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="1e863-143">Error codes</span></span>

<span data-ttu-id="1e863-144">À la fin de la méthode **SubclassesOf** , l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="1e863-144">After the completion of the **SubclassesOf** method, the **Err** object may contain one of the error codes in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="1e863-145">Une collection retournée avec zéro élément n’est pas une erreur.</span><span class="sxs-lookup"><span data-stu-id="1e863-145">A returned collection with zero elements is not an error.</span></span>

 

<dl> <dt>

<span data-ttu-id="1e863-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="1e863-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="1e863-147">L’utilisateur actuel n’a pas l’autorisation d’afficher une ou plusieurs des classes retournées par l’appel.</span><span class="sxs-lookup"><span data-stu-id="1e863-147">Current user does not have the permission to view one or more of the classes returned by the call.</span></span>

</dd> <dt>

<span data-ttu-id="1e863-148">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="1e863-148">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="1e863-149">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1e863-149">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="1e863-150">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="1e863-150">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="1e863-151">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="1e863-151">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="1e863-152">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="1e863-152">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="1e863-153">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="1e863-153">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="1e863-154">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="1e863-154">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="1e863-155">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="1e863-155">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1e863-156">Exemples</span><span class="sxs-lookup"><span data-stu-id="1e863-156">Examples</span></span>

<span data-ttu-id="1e863-157">L’exemple PowerShell suivant montre comment récupérer les sous-classes d’une classe sur un système distant.</span><span class="sxs-lookup"><span data-stu-id="1e863-157">The following PowerShell sample shows how to retrieve the subclasses of a class on a remote system.</span></span>


```PowerShell
$NameSpace = 'root\ccm'
$ComputerName = 'sccm.company.com'
$WbemLocator = New-Object -ComObject "WbemScripting.SWbemLocator"
$WbemServices = $WbemLocator.ConnectServer($ComputerName, $Namespace)
$WbemClasses = $WbemServices.SubclassesOf()
$WbemClasses
```



## <a name="requirements"></a><span data-ttu-id="1e863-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1e863-158">Requirements</span></span>



| <span data-ttu-id="1e863-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1e863-159">Requirement</span></span> | <span data-ttu-id="1e863-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="1e863-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e863-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e863-161">Minimum supported client</span></span><br/> | <span data-ttu-id="1e863-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1e863-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1e863-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1e863-163">Minimum supported server</span></span><br/> | <span data-ttu-id="1e863-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1e863-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1e863-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="1e863-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e863-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e863-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e863-167">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="1e863-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="1e863-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1e863-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1e863-169">DLL</span><span class="sxs-lookup"><span data-stu-id="1e863-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e863-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e863-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1e863-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="1e863-171">CLSID</span></span><br/>                    | <span data-ttu-id="1e863-172">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="1e863-172">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="1e863-173">IID</span><span class="sxs-lookup"><span data-stu-id="1e863-173">IID</span></span><br/>                      | <span data-ttu-id="1e863-174">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="1e863-174">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1e863-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1e863-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e863-176">**M**</span><span class="sxs-lookup"><span data-stu-id="1e863-176">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="1e863-177">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="1e863-177">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

 




