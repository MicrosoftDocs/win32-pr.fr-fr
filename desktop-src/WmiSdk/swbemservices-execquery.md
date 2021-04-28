---
description: SWbemServices.Exeméthode cQuery-exécute une requête pour récupérer des objets.
ms.assetid: 06b9d4c9-cd72-49b2-92b0-d18d94dfbd9f
ms.tgt_platform: multiple
title: SWbemServices.Exeméthode cQuery (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecQuery
- ISWbemServices.ExecQuery
- ISWbemServices.ExecQuery
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3009d2dc88e9987a3559da91eed1aa5aa1b248f9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098331"
---
# <a name="swbemservicesexecquery-method"></a><span data-ttu-id="401c1-103">SWbemServices.Exeméthode cQuery</span><span class="sxs-lookup"><span data-stu-id="401c1-103">SWbemServices.ExecQuery method</span></span>

<span data-ttu-id="401c1-104">La méthode **ExecQuery** de l’objet [**SWbemServices**](swbemservices.md) exécute une requête pour récupérer des objets.</span><span class="sxs-lookup"><span data-stu-id="401c1-104">The **ExecQuery** method of the [**SWbemServices**](swbemservices.md) object executes a query to retrieve objects.</span></span> <span data-ttu-id="401c1-105">Ces objets sont disponibles par le biais de la collection [**SWbemObjectSet**](swbemobjectset.md) retournée.</span><span class="sxs-lookup"><span data-stu-id="401c1-105">These objects are available through the returned [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span>

<span data-ttu-id="401c1-106">Cette méthode est appelée en mode semi-synchrone.</span><span class="sxs-lookup"><span data-stu-id="401c1-106">This method is called in the semisynchronous mode.</span></span> <span data-ttu-id="401c1-107">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-107">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="401c1-108">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="401c1-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="401c1-109">Syntax</span></span>


```VB
objWbemObjectSet = .ExecQuery( _
  ByVal strQuery, _
  [ ByVal strQueryLanguage ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="401c1-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="401c1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="401c1-111">*strQuery*</span><span class="sxs-lookup"><span data-stu-id="401c1-111">*strQuery*</span></span> 
</dt> <dd>

<span data-ttu-id="401c1-112">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="401c1-112">Required.</span></span> <span data-ttu-id="401c1-113">Chaîne qui contient le texte de la requête.</span><span class="sxs-lookup"><span data-stu-id="401c1-113">String that contains the text of the query.</span></span> <span data-ttu-id="401c1-114">Ce paramètre ne peut pas être vide.</span><span class="sxs-lookup"><span data-stu-id="401c1-114">This parameter cannot be blank.</span></span> <span data-ttu-id="401c1-115">Pour plus d’informations sur la création de chaînes de requête WMI, consultez [interrogation avec WQL](querying-with-wql.md) et la référence [WQL](wql-sql-for-wmi.md) .</span><span class="sxs-lookup"><span data-stu-id="401c1-115">For more information on building WMI query strings, see [Querying with WQL](querying-with-wql.md) and the [WQL](wql-sql-for-wmi.md) reference.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-116">*strQueryLanguage* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="401c1-116">*strQueryLanguage* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="401c1-117">Chaîne qui contient le langage de requête à utiliser.</span><span class="sxs-lookup"><span data-stu-id="401c1-117">String that contains the query language to be used.</span></span> <span data-ttu-id="401c1-118">S’il est spécifié, cette valeur doit être « WQL ».</span><span class="sxs-lookup"><span data-stu-id="401c1-118">If specified, this value must be "WQL".</span></span>

</dd> <dt>

<span data-ttu-id="401c1-119">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="401c1-119">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="401c1-120">Entier qui détermine le comportement de la requête et détermine si cet appel est retourné immédiatement.</span><span class="sxs-lookup"><span data-stu-id="401c1-120">Integer that determines the behavior of the query and determines whether this call returns immediately.</span></span> <span data-ttu-id="401c1-121">La valeur par défaut de ce paramètre est **wbemFlagReturnImmediately**.</span><span class="sxs-lookup"><span data-stu-id="401c1-121">The default value for this parameter is **wbemFlagReturnImmediately**.</span></span> <span data-ttu-id="401c1-122">Ce paramètre peut accepter les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="401c1-122">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>

<span data-ttu-id="401c1-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>wbemFlagForwardOnly \* \* \* \* (32 (0x20))</span><span class="sxs-lookup"><span data-stu-id="401c1-123"><span id="wbemFlagForwardOnly"></span><span id="wbemflagforwardonly"></span><span id="WBEMFLAGFORWARDONLY"></span>\*\*\*\*wbemFlagForwardOnly\*\*\*\* (32 (0x20))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-124">Entraîne le retour d’un énumérateur avant uniquement.</span><span class="sxs-lookup"><span data-stu-id="401c1-124">Causes a forward-only enumerator to be returned.</span></span> <span data-ttu-id="401c1-125">Les énumérateurs avant uniquement sont généralement beaucoup plus rapides et utilisent moins de mémoire que les énumérateurs conventionnels, mais ils n’autorisent pas les appels à [**SWbemObject. Clone \_**](swbemobject-clone-.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-125">Forward-only enumerators are generally much faster and use less memory than conventional enumerators, but they do not allow calls to [**SWbemObject.Clone\_**](swbemobject-clone-.md).</span></span>

</dd> <dt>

<span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>

<span data-ttu-id="401c1-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>wbemFlagBidirectional \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="401c1-126"><span id="wbemFlagBidirectional"></span><span id="wbemflagbidirectional"></span><span id="WBEMFLAGBIDIRECTIONAL"></span>\*\*\*\*wbemFlagBidirectional\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-127">Fait en sorte que WMI conserve les pointeurs vers les objets de l’énumération jusqu’à ce que le client libère l’énumérateur.</span><span class="sxs-lookup"><span data-stu-id="401c1-127">Causes WMI to retain pointers to objects of the enumeration until the client releases the enumerator.</span></span>

</dd> <dt>

<span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>

<span data-ttu-id="401c1-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>wbemFlagReturnImmediately \* \* \* \* (16 (0x10))</span><span class="sxs-lookup"><span data-stu-id="401c1-128"><span id="wbemFlagReturnImmediately"></span><span id="wbemflagreturnimmediately"></span><span id="WBEMFLAGRETURNIMMEDIATELY"></span>\*\*\*\*wbemFlagReturnImmediately\*\*\*\* (16 (0x10))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-129">Provoque le retour immédiat de l’appel.</span><span class="sxs-lookup"><span data-stu-id="401c1-129">Causes the call to return immediately.</span></span>

</dd> <dt>

<span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>

<span data-ttu-id="401c1-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>wbemFlagReturnWhenComplete \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="401c1-130"><span id="wbemFlagReturnWhenComplete"></span><span id="wbemflagreturnwhencomplete"></span><span id="WBEMFLAGRETURNWHENCOMPLETE"></span>\*\*\*\*wbemFlagReturnWhenComplete\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-131">Entraîne le blocage de cet appel jusqu’à ce que la requête soit terminée.</span><span class="sxs-lookup"><span data-stu-id="401c1-131">Causes this call to block until the query is complete.</span></span> <span data-ttu-id="401c1-132">Cet indicateur appelle la méthode en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="401c1-132">This flag calls the method in the synchronous mode.</span></span>

</dd> <dt>

<span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>

<span data-ttu-id="401c1-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>wbemQueryFlagPrototype \* \* \* \* (2 (0X2))</span><span class="sxs-lookup"><span data-stu-id="401c1-133"><span id="wbemQueryFlagPrototype"></span><span id="wbemqueryflagprototype"></span><span id="WBEMQUERYFLAGPROTOTYPE"></span>\*\*\*\*wbemQueryFlagPrototype\*\*\*\* (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-134">Utilisé pour le prototypage.</span><span class="sxs-lookup"><span data-stu-id="401c1-134">Used for prototyping.</span></span> <span data-ttu-id="401c1-135">Cet indicateur empêche la requête de se produire et retourne un objet qui ressemble à un objet de résultat standard.</span><span class="sxs-lookup"><span data-stu-id="401c1-135">This flag stops the query from happening and returns an object that looks like a typical result object.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="401c1-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="401c1-136"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="401c1-137">Fait en sorte que WMI retourne des données de modification de classe avec la définition de classe de base.</span><span class="sxs-lookup"><span data-stu-id="401c1-137">Causes WMI to return class amendment data with the base class definition.</span></span> <span data-ttu-id="401c1-138">Pour plus d’informations, consultez [localisation des informations de classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-138">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="401c1-139">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="401c1-139">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="401c1-140">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="401c1-140">Typically, this is undefined.</span></span> <span data-ttu-id="401c1-141">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="401c1-141">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="401c1-142">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="401c1-142">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="401c1-143">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="401c1-143">Return value</span></span>

<span data-ttu-id="401c1-144">Si aucune erreur ne se produit, cette méthode retourne un objet [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="401c1-144">If no error occurs, this method returns an [**SWbemObjectSet**](swbemobjectset.md) object.</span></span> <span data-ttu-id="401c1-145">Il s’agit d’une collection d’objets qui contient le jeu de résultats de la requête.</span><span class="sxs-lookup"><span data-stu-id="401c1-145">This is an object collection that contains the result set of the query.</span></span> <span data-ttu-id="401c1-146">L’appelant peut examiner la collection à l’aide de l’implémentation des collections pour le langage de programmation que vous utilisez.</span><span class="sxs-lookup"><span data-stu-id="401c1-146">The caller can examine the collection using the implementation of collections for the programming language you are using.</span></span> <span data-ttu-id="401c1-147">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-147">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="401c1-148">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="401c1-148">Error codes</span></span>

<span data-ttu-id="401c1-149">À la fin de la méthode **ExecQuery** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="401c1-149">After the completion of the **ExecQuery** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object can contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="401c1-150">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="401c1-150">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-151">L’utilisateur actuel n’a pas l’autorisation d’afficher le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="401c1-151">Current user does not have the permission to view the result set.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-152">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="401c1-152">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-153">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="401c1-153">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-154">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="401c1-154">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-155">Un paramètre non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="401c1-155">Invalid parameter was specified.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-156">**wbemErrInvalidQuery** -2147749911 (0x80041017)</span><span class="sxs-lookup"><span data-stu-id="401c1-156">**wbemErrInvalidQuery** - 2147749911 (0x80041017)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-157">La syntaxe de la requête n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="401c1-157">Query syntax is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-158">**wbemErrInvalidQueryType** -2147749912 (0x80041018)</span><span class="sxs-lookup"><span data-stu-id="401c1-158">**wbemErrInvalidQueryType** - 2147749912 (0x80041018)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-159">Le langage de requête demandé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="401c1-159">Requested query language is not supported.</span></span>

</dd> <dt>

<span data-ttu-id="401c1-160">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="401c1-160">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="401c1-161">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="401c1-161">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="401c1-162">Notes </span><span class="sxs-lookup"><span data-stu-id="401c1-162">Remarks</span></span>

<span data-ttu-id="401c1-163">**ExecQuery** est l’un des appels les plus couramment utilisés pour récupérer des informations WMI.</span><span class="sxs-lookup"><span data-stu-id="401c1-163">**ExecQuery** is one of the most commonly-used calls to retrieve WMI information.</span></span> <span data-ttu-id="401c1-164">Un appel standard à **ExecQuery** ressemble à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="401c1-164">A standard call to **ExecQuery** looks like the following:</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colServices = objWMIService.ExecQuery ("Select * from Win32_Service where Name='Alerter'")
For Each objService in colServices
    Return = objService.StopService()
    If Return <> 0 Then
        Wscript.Echo "Failed " &VBNewLine & "Error code = " & Return 
    Else
       WScript.Echo "Succeeded"
    End If
Next
```



<span data-ttu-id="401c1-165">Notez que vous créez l’objet [**SWbemServices**](swbemservices.md) avec un moniker qui représente l’espace de noms et la sécurité appropriés, puis effectuez l’appel **ExecQuery** par le biais du service.</span><span class="sxs-lookup"><span data-stu-id="401c1-165">Note that you create the [**SWbemServices**](swbemservices.md) object with a moniker that represents the appropriate namespace and security, then make the **ExecQuery** call through the service.</span></span> <span data-ttu-id="401c1-166">Pour une description plus complète, consultez [création d’un script WMI](creating-a-wmi-script.md) et [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-166">For a more complete discussion, see [Creating a WMI Script](creating-a-wmi-script.md) and [Enumerating WMI](enumerating-wmi.md).</span></span>

<span data-ttu-id="401c1-167">À l’instar de la méthode [**InstancesOf**](swbemservices-instancesof.md) , la méthode **ExecQuery** retourne toujours une collection [**SWbemObjectSet**](swbemobjectset.md) .</span><span class="sxs-lookup"><span data-stu-id="401c1-167">Like the [**InstancesOf**](swbemservices-instancesof.md) method, the **ExecQuery** method always returns an [**SWbemObjectSet**](swbemobjectset.md) collection.</span></span> <span data-ttu-id="401c1-168">Par conséquent, votre script WMI doit énumérer la collection ExecQuery retourne afin d’accéder à chaque instance de ressource gérée dans la collection, comme illustré ici :</span><span class="sxs-lookup"><span data-stu-id="401c1-168">Thus your WMI script must enumerate the collection ExecQuery returns in order to access each managed resource instance in the collection, as shown here:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colSWbemObjectSet = objSWbemServices.ExecQuery _
   ("SELECT * FROM Win32_Service")
For Each objSWbemObject In colSWbemObjectSet
    Wscript.Echo "Name: " & objSWbemObject.Name
Next
```



<span data-ttu-id="401c1-169">Les autres méthodes [**SWbemServices**](swbemservices.md) qui retournent une [**SWbemObjectSet**](swbemobjectset.md) incluent [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md)et [**SubclassesOf**](swbemservices-subclassesof.md).</span><span class="sxs-lookup"><span data-stu-id="401c1-169">Other [**SWbemServices**](swbemservices.md) methods that return an [**SWbemObjectSet**](swbemobjectset.md) include [**AssociatorsOf**](swbemservices-associatorsof.md), [**ReferencesTo**](swbemservices-referencesto.md), and [**SubclassesOf**](swbemservices-subclassesof.md).</span></span>

<span data-ttu-id="401c1-170">La requête ne peut pas retourner un jeu de résultats vide.</span><span class="sxs-lookup"><span data-stu-id="401c1-170">It is not an error for the query to return an empty result set.</span></span> <span data-ttu-id="401c1-171">La méthode **ExecQuery** retourne des propriétés de clé, que la propriété de clé soit demandée ou non dans l’argument *strQuery* .</span><span class="sxs-lookup"><span data-stu-id="401c1-171">The **ExecQuery** method returns key properties whether or not the key property is requested in the *strQuery* argument.</span></span> <span data-ttu-id="401c1-172">Si une erreur se produit lors de l’exécution de cette méthode et que vous n’utilisez pas l’indicateur **wbemFlagReturnImmediately** , l’objet [Err](/previous-versions//sbf5ze0e(v=vs.85)) n’est pas défini tant que vous n’avez pas essayé d’accéder au jeu d’objets retourné.</span><span class="sxs-lookup"><span data-stu-id="401c1-172">If an error occurs when executing this method and you do not use the **wbemFlagReturnImmediately** flag, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object is not set until you attempt to access the returned object set.</span></span> <span data-ttu-id="401c1-173">Toutefois, si vous utilisez l’indicateur **wbemFlagReturnWhenComplete** , l’objet Err est défini lorsque la méthode **ExecQuery** est appelée.</span><span class="sxs-lookup"><span data-stu-id="401c1-173">However, if you use the **wbemFlagReturnWhenComplete** flag, the Err object is set when the **ExecQuery** method is called.</span></span>

<span data-ttu-id="401c1-174">Il existe des limites concernant le nombre de mots clés **and** et **or** qui peuvent être utilisés dans les requêtes WQL.</span><span class="sxs-lookup"><span data-stu-id="401c1-174">There are limits to the number of **AND** and **OR** keywords that can be used in WQL queries.</span></span> <span data-ttu-id="401c1-175">Un grand nombre de mots clés WQL utilisés dans une requête complexe peut faire en sorte que WMI retourne le code d’erreur de **\_ \_ \_ violation de quota E WBEM** en tant que valeur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="401c1-175">Large numbers of WQL keywords that are used in a complex query can cause WMI to return the **WBEM\_E\_QUOTA\_VIOLATION** error code as an **HRESULT** value.</span></span> <span data-ttu-id="401c1-176">La limite des mots clés WQL dépend de la complexité de la requête.</span><span class="sxs-lookup"><span data-stu-id="401c1-176">The limit of WQL keywords depends on how complex the query is.</span></span>

## <a name="examples"></a><span data-ttu-id="401c1-177">Exemples</span><span class="sxs-lookup"><span data-stu-id="401c1-177">Examples</span></span>

<span data-ttu-id="401c1-178">L’exemple de code VBScript suivant localise tous les lecteurs de disque sur l’ordinateur local et affiche l’ID de l’appareil et le type du lecteur de disque.</span><span class="sxs-lookup"><span data-stu-id="401c1-178">The following VBScript code example locates all the disk drives on the local computer and displays the device ID and the type of the disk drive.</span></span>


```VB
Set colDisks = GetObject( _
    "Winmgmts:").ExecQuery("Select * from Win32_LogicalDisk")
For Each objDisk in colDisks
 
    Select Case objDisk.DriveType
        Case 1
            Wscript.Echo "No root directory. Drive type could not be determined."
        Case 2
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Removable drive" 
        Case 3
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Local hard disk" 
        Case 4
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Network disk" 
        Case 5
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = Compact disk" 
        Case 6
            Wscript.Echo "DeviceID= "& objDisk.DeviceID & "  DriveType = RAM disk" 
        Case Else
            Wscript.Echo "Drive type could not be determined."
    End Select
Next
```



## <a name="requirements"></a><span data-ttu-id="401c1-179">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="401c1-179">Requirements</span></span>



| <span data-ttu-id="401c1-180">Condition requise</span><span class="sxs-lookup"><span data-stu-id="401c1-180">Requirement</span></span> | <span data-ttu-id="401c1-181">Valeur</span><span class="sxs-lookup"><span data-stu-id="401c1-181">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="401c1-182">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="401c1-182">Minimum supported client</span></span><br/> | <span data-ttu-id="401c1-183">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="401c1-183">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="401c1-184">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="401c1-184">Minimum supported server</span></span><br/> | <span data-ttu-id="401c1-185">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="401c1-185">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="401c1-186">En-tête</span><span class="sxs-lookup"><span data-stu-id="401c1-186">Header</span></span><br/>                   | <dl> <span data-ttu-id="401c1-187"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="401c1-187"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="401c1-188">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="401c1-188">Type library</span></span><br/>             | <dl> <span data-ttu-id="401c1-189"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="401c1-189"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="401c1-190">DLL</span><span class="sxs-lookup"><span data-stu-id="401c1-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="401c1-191"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="401c1-191"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="401c1-192">CLSID</span><span class="sxs-lookup"><span data-stu-id="401c1-192">CLSID</span></span><br/>                    | <span data-ttu-id="401c1-193">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="401c1-193">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="401c1-194">IID</span><span class="sxs-lookup"><span data-stu-id="401c1-194">IID</span></span><br/>                      | <span data-ttu-id="401c1-195">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="401c1-195">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="401c1-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="401c1-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="401c1-197">**M**</span><span class="sxs-lookup"><span data-stu-id="401c1-197">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="401c1-198">**SWbemServices.**</span><span class="sxs-lookup"><span data-stu-id="401c1-198">**SWbemServices.Get**</span></span>](swbemservices-get.md)
</dt> <dt>

[<span data-ttu-id="401c1-199">Interrogation avec WQL</span><span class="sxs-lookup"><span data-stu-id="401c1-199">Querying with WQL</span></span>](querying-with-wql.md)
</dt> <dt>

[<span data-ttu-id="401c1-200">Création d’un script WMI</span><span class="sxs-lookup"><span data-stu-id="401c1-200">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
</dt> <dt>

[<span data-ttu-id="401c1-201">Énumération de WMI</span><span class="sxs-lookup"><span data-stu-id="401c1-201">Enumerating WMI</span></span>](enumerating-wmi.md)
</dt> </dl>

 

