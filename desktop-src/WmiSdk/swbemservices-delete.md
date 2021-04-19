---
description: Supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet. Vous pouvez uniquement supprimer des objets dans l’espace de noms actuel.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: SWbemServices. Delete, méthode (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485441"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="0f62a-104">SWbemServices. Delete, méthode</span><span class="sxs-lookup"><span data-stu-id="0f62a-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="0f62a-105">La méthode **Delete** de l’objet [**SWbemServices**](swbemservices.md) supprime la classe ou l’instance spécifiée dans le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0f62a-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="0f62a-106">Vous pouvez uniquement supprimer des objets dans l’espace de noms actuel.</span><span class="sxs-lookup"><span data-stu-id="0f62a-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="0f62a-107">Si un fournisseur dynamique fournit la classe ou l’instance, vous ne pouvez pas supprimer cet objet, sauf si le fournisseur prend en charge la suppression de classe ou d’instance.</span><span class="sxs-lookup"><span data-stu-id="0f62a-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="0f62a-108">Cette méthode est appelée en mode synchrone.</span><span class="sxs-lookup"><span data-stu-id="0f62a-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="0f62a-109">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="0f62a-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="0f62a-110">Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="0f62a-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0f62a-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0f62a-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="0f62a-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0f62a-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f62a-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="0f62a-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="0f62a-114">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="0f62a-114">Required.</span></span> <span data-ttu-id="0f62a-115">Chaîne qui contient le chemin d’accès à l’objet que vous souhaitez supprimer.</span><span class="sxs-lookup"><span data-stu-id="0f62a-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="0f62a-116">Pour plus d’informations, consultez [Description de l’emplacement d’un objet WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="0f62a-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-117">*IFlags* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0f62a-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-118">Réservé.</span><span class="sxs-lookup"><span data-stu-id="0f62a-118">Reserved.</span></span> <span data-ttu-id="0f62a-119">Cette valeur doit être zéro.</span><span class="sxs-lookup"><span data-stu-id="0f62a-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-120">*objWbemNamedValueSet* \[ facultatif\]</span><span class="sxs-lookup"><span data-stu-id="0f62a-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-121">En général, ce n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0f62a-121">Typically, this is undefined.</span></span> <span data-ttu-id="0f62a-122">Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande.</span><span class="sxs-lookup"><span data-stu-id="0f62a-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="0f62a-123">Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.</span><span class="sxs-lookup"><span data-stu-id="0f62a-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f62a-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0f62a-124">Return value</span></span>

<span data-ttu-id="0f62a-125">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="0f62a-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0f62a-126">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="0f62a-126">Error codes</span></span>

<span data-ttu-id="0f62a-127">Une fois la méthode **Delete** terminée, l’objet **Err** peut contenir l’un des codes d’erreur répertoriés dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="0f62a-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="0f62a-128">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="0f62a-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-129">Le contexte actuel ne dispose pas des droits de sécurité adéquats pour supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="0f62a-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-130">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="0f62a-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-131">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="0f62a-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-132">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="0f62a-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-133">La classe spécifiée n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0f62a-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-134">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="0f62a-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-135">Impossible de supprimer l’objet.</span><span class="sxs-lookup"><span data-stu-id="0f62a-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-136">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="0f62a-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-137">L’objet n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="0f62a-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="0f62a-138">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="0f62a-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="0f62a-139">Mémoire insuffisante pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="0f62a-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f62a-140">Notes</span><span class="sxs-lookup"><span data-stu-id="0f62a-140">Remarks</span></span>

<span data-ttu-id="0f62a-141">La méthode **SWbemServices. Delete** peut être utilisée lorsque la propriété de clé pour l’objet n’a pas de valeur, car cette méthode requiert uniquement un chemin d’accès d’objet comme entrée.</span><span class="sxs-lookup"><span data-stu-id="0f62a-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="0f62a-142">Cette méthode peut être utilisée dans les situations où [**SWbemObject. \_ Delete**](swbemobject-delete-.md) échoue pour une valeur de clé manquante.</span><span class="sxs-lookup"><span data-stu-id="0f62a-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="0f62a-143">Si l’objet est validé dans WMI via [**SWbemObject. put \_**](swbemobject-put-.md), un objet [**SWbemObjectPath**](swbemobjectpath.md) a été obtenu par le biais de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0f62a-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="0f62a-144">Exemples</span><span class="sxs-lookup"><span data-stu-id="0f62a-144">Examples</span></span>

<span data-ttu-id="0f62a-145">L’exemple suivant crée une nouvelle classe, ajoute une propriété qui n’est pas une clé, écrit la nouvelle classe dans le référentiel et affiche le chemin d’accès du nouvel objet de classe.</span><span class="sxs-lookup"><span data-stu-id="0f62a-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="0f62a-146">Le script génère ensuite une instance de la nouvelle classe, écrit l’instance et affiche le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="0f62a-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="0f62a-147">Notez que le script supprime la classe et ses instances du référentiel en supprimant la classe.</span><span class="sxs-lookup"><span data-stu-id="0f62a-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="0f62a-148">Pour plus d’informations sur les classes et les instances WMI, consultez [manipulation d’informations sur les classes et les](manipulating-class-and-instance-information.md) instances et [Common Information Model](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="0f62a-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="0f62a-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0f62a-149">Requirements</span></span>



| <span data-ttu-id="0f62a-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0f62a-150">Requirement</span></span> | <span data-ttu-id="0f62a-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="0f62a-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f62a-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f62a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="0f62a-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0f62a-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0f62a-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0f62a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="0f62a-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0f62a-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0f62a-156">En-tête</span><span class="sxs-lookup"><span data-stu-id="0f62a-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f62a-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f62a-158">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="0f62a-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="0f62a-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="0f62a-160">DLL</span><span class="sxs-lookup"><span data-stu-id="0f62a-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f62a-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f62a-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="0f62a-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="0f62a-162">CLSID</span></span><br/>                    | <span data-ttu-id="0f62a-163">CLSID \_ SWbemServices</span><span class="sxs-lookup"><span data-stu-id="0f62a-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="0f62a-164">IID</span><span class="sxs-lookup"><span data-stu-id="0f62a-164">IID</span></span><br/>                      | <span data-ttu-id="0f62a-165">IID \_ ISWbemServices</span><span class="sxs-lookup"><span data-stu-id="0f62a-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="0f62a-166">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0f62a-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f62a-167">**M**</span><span class="sxs-lookup"><span data-stu-id="0f62a-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="0f62a-168">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="0f62a-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




