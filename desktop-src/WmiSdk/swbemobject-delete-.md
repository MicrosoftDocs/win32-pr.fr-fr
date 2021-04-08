---
description: La \_ méthode Delete de l’objet SWbemObject supprime la classe en cours ou l’instance actuelle.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Méthode SWbemObject.Delete_ (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034837"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="004d3-103">SWbemObject. Delete, \_ méthode</span><span class="sxs-lookup"><span data-stu-id="004d3-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="004d3-104">La **méthode \_ Delete** de l’objet [**SWbemObject**](swbemobject.md) supprime la classe en cours ou l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="004d3-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="004d3-105">Si un fournisseur dynamique fournit la classe ou l’instance, il est parfois impossible de supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance.</span><span class="sxs-lookup"><span data-stu-id="004d3-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="004d3-106">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="004d3-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="004d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="004d3-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="004d3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="004d3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="004d3-109">*IFlags* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="004d3-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="004d3-110">Réservé et doit avoir la valeur 0 (zéro) si elle est spécifiée.</span><span class="sxs-lookup"><span data-stu-id="004d3-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-111">*objwbemNamedValueSet* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="004d3-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="004d3-112">Ce paramètre n’est généralement pas défini.</span><span class="sxs-lookup"><span data-stu-id="004d3-112">This parameter is typically undefined.</span></span> <span data-ttu-id="004d3-113">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui traite la requête.</span><span class="sxs-lookup"><span data-stu-id="004d3-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="004d3-114">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="004d3-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="004d3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="004d3-115">Return value</span></span>

<span data-ttu-id="004d3-116">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="004d3-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="004d3-117">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="004d3-117">Error codes</span></span>

<span data-ttu-id="004d3-118">Une fois la méthode **Delete \_** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="004d3-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="004d3-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="004d3-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-120">Le contexte actuel ne dispose pas des droits de sécurité adéquats pour supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="004d3-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-121">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="004d3-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-122">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="004d3-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-123">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="004d3-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-124">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="004d3-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-125">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="004d3-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-126">Impossible de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="004d3-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-127">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="004d3-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-128">L’objet n’existait pas.</span><span class="sxs-lookup"><span data-stu-id="004d3-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="004d3-129">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="004d3-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="004d3-130">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="004d3-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="004d3-131">Notes</span><span class="sxs-lookup"><span data-stu-id="004d3-131">Remarks</span></span>

<span data-ttu-id="004d3-132">La **méthode \_ Delete** échoue si une nouvelle instance de [**SWbemObject**](swbemobject.md) est créée, mais aucune valeur n’est fournie pour la propriété Key.</span><span class="sxs-lookup"><span data-stu-id="004d3-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="004d3-133">Windows Management Instrumentation (WMI) génère automatiquement une valeur d’identificateur global unique (GUID), mais une valeur GUID n’est pas acceptée par **SWbemObject. Delete \_**.</span><span class="sxs-lookup"><span data-stu-id="004d3-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="004d3-134">Dans ce cas, [**SWbemServices. Delete**](swbemservices-delete.md), qui utilise le chemin d’accès de l’objet, fonctionne.</span><span class="sxs-lookup"><span data-stu-id="004d3-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="004d3-135">Notez qu’un objet [**SWbemObjectPath**](swbemobjectpath.md) est retourné par la méthode [**SWbemObject. \_ put**](swbemobject-put-.md) après qu’un objet a été validé dans WMI.</span><span class="sxs-lookup"><span data-stu-id="004d3-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="004d3-136">Exemples</span><span class="sxs-lookup"><span data-stu-id="004d3-136">Examples</span></span>

<span data-ttu-id="004d3-137">L’exemple suivant crée une nouvelle classe. Ajoute une propriété de clé ; écrit la nouvelle classe dans le référentiel ; et affiche le chemin d’accès du nouvel objet de classe.</span><span class="sxs-lookup"><span data-stu-id="004d3-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="004d3-138">Le script génère ensuite une instance de la nouvelle classe ; l’écrit ; et affiche le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="004d3-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="004d3-139">Notez que le script supprime la classe et ses instances du référentiel en supprimant simplement la classe.</span><span class="sxs-lookup"><span data-stu-id="004d3-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="004d3-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="004d3-140">Requirements</span></span>



| <span data-ttu-id="004d3-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="004d3-141">Requirement</span></span> | <span data-ttu-id="004d3-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="004d3-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="004d3-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004d3-143">Minimum supported client</span></span><br/> | <span data-ttu-id="004d3-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="004d3-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="004d3-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="004d3-145">Minimum supported server</span></span><br/> | <span data-ttu-id="004d3-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="004d3-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="004d3-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="004d3-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="004d3-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="004d3-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="004d3-149">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="004d3-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="004d3-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="004d3-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="004d3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="004d3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="004d3-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="004d3-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="004d3-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="004d3-153">CLSID</span></span><br/>                    | <span data-ttu-id="004d3-154">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="004d3-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="004d3-155">IID</span><span class="sxs-lookup"><span data-stu-id="004d3-155">IID</span></span><br/>                      | <span data-ttu-id="004d3-156">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="004d3-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




