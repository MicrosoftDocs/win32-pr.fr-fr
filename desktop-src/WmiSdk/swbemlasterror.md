---
description: Les méthodes et les propriétés de l’objet SWbemLastError contiennent et manipulent des objets Error.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objet SWbemLastError (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518394"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="24392-103">Objet SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="24392-103">SWbemLastError object</span></span>

<span data-ttu-id="24392-104">Les méthodes et les propriétés de l’objet **SWbemLastError** contiennent et manipulent des objets Error.</span><span class="sxs-lookup"><span data-stu-id="24392-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="24392-105">Les méthodes et les propriétés de cet objet sont exactement les mêmes que celles de l’objet [**SWbemObject**](swbemobject.md) , mais elles sont utilisées pour contenir les informations d’erreur au lieu des informations de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="24392-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="24392-106">Cet objet peut être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="24392-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="24392-107">Vous pouvez créer un objet d’erreur **SWbemLastError** pour inspecter les informations d’erreur étendues associées à un appel de méthode précédent.</span><span class="sxs-lookup"><span data-stu-id="24392-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="24392-108">Si les informations sur l’erreur ne sont pas disponibles, une tentative de création d’un objet d’erreur échoue.</span><span class="sxs-lookup"><span data-stu-id="24392-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="24392-109">Si l’appel a échoué et qu’un objet d’erreur retourne, l’état de l’objet est Reset.</span><span class="sxs-lookup"><span data-stu-id="24392-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="24392-110">Toute tentative supplémentaire de récupération d’un objet d’erreur échouera jusqu’à ce qu’une nouvelle erreur se produise.</span><span class="sxs-lookup"><span data-stu-id="24392-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="24392-111">Si vous effectuez un appel asynchrone qui échoue, un objet **SWbemLastError** peut être retourné par l’événement [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) dans le paramètre *objWbemErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="24392-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="24392-112">Membres</span><span class="sxs-lookup"><span data-stu-id="24392-112">Members</span></span>

<span data-ttu-id="24392-113">L’objet **SWbemLastError** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="24392-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="24392-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="24392-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="24392-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24392-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="24392-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="24392-116">Methods</span></span>

<span data-ttu-id="24392-117">L’objet **SWbemLastError** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="24392-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="24392-118">Méthode</span><span class="sxs-lookup"><span data-stu-id="24392-118">Method</span></span>                                                   | <span data-ttu-id="24392-119">Description</span><span class="sxs-lookup"><span data-stu-id="24392-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="24392-120">**Associateurs\_**</span><span class="sxs-lookup"><span data-stu-id="24392-120">**Associators\_**</span></span>                                        | <span data-ttu-id="24392-121">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-121">Not used.</span></span> <span data-ttu-id="24392-122">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-123">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="24392-124">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-124">Not used.</span></span> <span data-ttu-id="24392-125">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="24392-126">**Répliqué\_**</span><span class="sxs-lookup"><span data-stu-id="24392-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="24392-127">Effectue une copie de l’objet en cours.</span><span class="sxs-lookup"><span data-stu-id="24392-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="24392-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="24392-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="24392-129">Teste si deux objets sont égaux.</span><span class="sxs-lookup"><span data-stu-id="24392-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="24392-130">**Supprimer\_**</span><span class="sxs-lookup"><span data-stu-id="24392-130">**Delete\_**</span></span>                                             | <span data-ttu-id="24392-131">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-131">Not used.</span></span> <span data-ttu-id="24392-132">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="24392-134">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-134">Not used.</span></span> <span data-ttu-id="24392-135">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="24392-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="24392-137">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-137">Not used.</span></span> <span data-ttu-id="24392-138">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="24392-140">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-140">Not used.</span></span> <span data-ttu-id="24392-141">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="24392-142">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="24392-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="24392-143">Récupère la représentation textuelle de l’objet écrit avec la syntaxe MOF.</span><span class="sxs-lookup"><span data-stu-id="24392-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="24392-144">**Instances\_**</span><span class="sxs-lookup"><span data-stu-id="24392-144">**Instances\_**</span></span>                                          | <span data-ttu-id="24392-145">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-145">Not used.</span></span> <span data-ttu-id="24392-146">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-147">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="24392-148">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-148">Not used.</span></span> <span data-ttu-id="24392-149">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-150">**Posé\_**</span><span class="sxs-lookup"><span data-stu-id="24392-150">**Put\_**</span></span>                                                | <span data-ttu-id="24392-151">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-151">Not used.</span></span> <span data-ttu-id="24392-152">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-153">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="24392-154">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-154">Not used.</span></span> <span data-ttu-id="24392-155">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-156">**Références\_**</span><span class="sxs-lookup"><span data-stu-id="24392-156">**References\_**</span></span>                                         | <span data-ttu-id="24392-157">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-157">Not used.</span></span> <span data-ttu-id="24392-158">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-159">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="24392-160">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-160">Not used.</span></span> <span data-ttu-id="24392-161">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="24392-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="24392-163">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-163">Not used.</span></span> <span data-ttu-id="24392-164">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="24392-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="24392-166">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-166">Not used.</span></span> <span data-ttu-id="24392-167">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-168">**Sous-classes\_**</span><span class="sxs-lookup"><span data-stu-id="24392-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="24392-169">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-169">Not used.</span></span> <span data-ttu-id="24392-170">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="24392-171">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="24392-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="24392-172">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-172">Not used.</span></span> <span data-ttu-id="24392-173">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="24392-174">Propriétés</span><span class="sxs-lookup"><span data-stu-id="24392-174">Properties</span></span>

<span data-ttu-id="24392-175">L’objet **SWbemLastError** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="24392-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="24392-176">Propriété</span><span class="sxs-lookup"><span data-stu-id="24392-176">Property</span></span>                                                      | <span data-ttu-id="24392-177">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="24392-177">Access type</span></span>          | <span data-ttu-id="24392-178">Description</span><span class="sxs-lookup"><span data-stu-id="24392-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24392-179">**Dérivation\_**</span><span class="sxs-lookup"><span data-stu-id="24392-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="24392-180">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-180">Read-only</span></span><br/> | <span data-ttu-id="24392-181">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-181">Not used.</span></span> <span data-ttu-id="24392-182">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="24392-183">**Méthodes\_**</span><span class="sxs-lookup"><span data-stu-id="24392-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="24392-184">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-184">Read-only</span></span><br/> | <span data-ttu-id="24392-185">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-185">Not used.</span></span> <span data-ttu-id="24392-186">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="24392-187">**D\_**</span><span class="sxs-lookup"><span data-stu-id="24392-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="24392-188">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-188">Read-only</span></span><br/> | <span data-ttu-id="24392-189">Contient un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="24392-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="24392-190">**Propriétés\_**</span><span class="sxs-lookup"><span data-stu-id="24392-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="24392-191">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-191">Read-only</span></span><br/> | <span data-ttu-id="24392-192">Représente la collection de propriétés de l’objet **SWbemLastError** .</span><span class="sxs-lookup"><span data-stu-id="24392-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="24392-193">Cette propriété est un objet [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="24392-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="24392-194">**Qualificateurs\_**</span><span class="sxs-lookup"><span data-stu-id="24392-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="24392-195">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-195">Read-only</span></span><br/> | <span data-ttu-id="24392-196">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-196">Not used.</span></span> <span data-ttu-id="24392-197">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="24392-198">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="24392-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="24392-199">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="24392-199">Read-only</span></span><br/> | <span data-ttu-id="24392-200">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="24392-200">Not used.</span></span> <span data-ttu-id="24392-201">L’objet [**SWbemObject**](swbemobject.md) fournit la même méthode.</span><span class="sxs-lookup"><span data-stu-id="24392-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="24392-202">Exemples</span><span class="sxs-lookup"><span data-stu-id="24392-202">Examples</span></span>

<span data-ttu-id="24392-203">L’exemple VBScript suivant montre comment inspecter les informations relatives aux objets Error et Error.</span><span class="sxs-lookup"><span data-stu-id="24392-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="24392-204">L’exemple perl suivant montre comment inspecter les informations relatives aux objets Error et Error.</span><span class="sxs-lookup"><span data-stu-id="24392-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="24392-205">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="24392-205">Requirements</span></span>



| <span data-ttu-id="24392-206">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24392-206">Requirement</span></span> | <span data-ttu-id="24392-207">Valeur</span><span class="sxs-lookup"><span data-stu-id="24392-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24392-208">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24392-208">Minimum supported client</span></span><br/> | <span data-ttu-id="24392-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24392-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24392-210">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="24392-210">Minimum supported server</span></span><br/> | <span data-ttu-id="24392-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24392-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24392-212">En-tête</span><span class="sxs-lookup"><span data-stu-id="24392-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="24392-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="24392-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="24392-214">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="24392-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="24392-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="24392-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="24392-216">DLL</span><span class="sxs-lookup"><span data-stu-id="24392-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24392-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24392-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="24392-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="24392-218">CLSID</span></span><br/>                    | <span data-ttu-id="24392-219">CLSID \_ SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="24392-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="24392-220">IID</span><span class="sxs-lookup"><span data-stu-id="24392-220">IID</span></span><br/>                      | <span data-ttu-id="24392-221">IID \_ ISWbemLastError</span><span class="sxs-lookup"><span data-stu-id="24392-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="24392-222">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24392-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24392-223">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="24392-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




