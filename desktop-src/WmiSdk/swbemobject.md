---
description: Vous pouvez utiliser les méthodes et propriétés de l’objet SWbemObject pour représenter une définition de classe ou une instance d’objet Windows Management Instrumentation (WMI).
ms.assetid: d303ec1a-5e0c-4a5e-8ed3-ed353a138755
ms.tgt_platform: multiple
title: SWbemObject, objet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject
- ISWbemObject
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 287395b976177170c8bdffa0e1817a8755a4d397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518393"
---
# <a name="swbemobject-object"></a><span data-ttu-id="4135a-103">SWbemObject, objet</span><span class="sxs-lookup"><span data-stu-id="4135a-103">SWbemObject object</span></span>

<span data-ttu-id="4135a-104">Vous pouvez utiliser les méthodes et propriétés de l’objet **SWbemObject** pour représenter une définition de classe ou une instance d’objet Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-104">You can use the methods and properties of the **SWbemObject** object to represent one Windows Management Instrumentation (WMI) class definition or object instance.</span></span> <span data-ttu-id="4135a-105">Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="4135a-105">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call.</span></span>

<span data-ttu-id="4135a-106">Cet objet prend en charge deux types de propriétés et de méthodes.</span><span class="sxs-lookup"><span data-stu-id="4135a-106">This object supports two types of properties and methods.</span></span> <span data-ttu-id="4135a-107">Ceux qui sont définis dans cette section sont des propriétés et des méthodes génériques qui s’appliquent à tous les objets WMI.</span><span class="sxs-lookup"><span data-stu-id="4135a-107">Those defined in this section are generic properties and methods that apply to all WMI objects.</span></span> <span data-ttu-id="4135a-108">En outre, cet objet expose les propriétés et les méthodes de l’objet sous-jacent sous forme de propriétés Automation dynamiques et de méthodes de **SWbemObject**.</span><span class="sxs-lookup"><span data-stu-id="4135a-108">In addition, this object exposes the properties and methods of the underlying object as dynamic automation properties and methods of **SWbemObject**.</span></span> <span data-ttu-id="4135a-109">Les noms et les types de ces propriétés et méthodes dépendent de l’objet WMI sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4135a-109">The names and types of these properties and methods depend on the underlying WMI object.</span></span> <span data-ttu-id="4135a-110">Pour plus d’informations sur la façon dont ces propriétés et méthodes dynamiques sont exposées, consultez [manipulation des informations relatives aux classes et aux instances](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="4135a-110">For more information about how these dynamic properties and methods are exposed, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="4135a-111">Du point de vue du client WMI, cet objet est toujours in-process.</span><span class="sxs-lookup"><span data-stu-id="4135a-111">From the WMI client perspective, this object is always in-process.</span></span> <span data-ttu-id="4135a-112">Les opérations d’écriture affectent uniquement la copie locale de l’objet, et les opérations de lecture récupèrent toujours les valeurs à partir de la copie locale.</span><span class="sxs-lookup"><span data-stu-id="4135a-112">Write operations only affect the local copy of the object, and read operations always retrieve values from the local copy.</span></span> <span data-ttu-id="4135a-113">Les mises à jour de WMI sont effectuées uniquement lorsque des objets entiers sont écrits à l’aide d’un appel à la méthode [**SWbemObject. put \_**](swbemobject-put-.md) .</span><span class="sxs-lookup"><span data-stu-id="4135a-113">Updates to WMI are performed only when entire objects are written using a call to the [**SWbemObject.Put\_**](swbemobject-put-.md) method.</span></span> <span data-ttu-id="4135a-114">Si vous modifiez les propriétés ou les méthodes dans un objet **SWbemObject** , vos modifications ne sont pas écrites dans WMI tant que vous n’avez pas appelé **SWbemObject. put \_**.</span><span class="sxs-lookup"><span data-stu-id="4135a-114">If you modify the properties or methods in an **SWbemObject** object, your changes are not written to WMI until you call **SWbemObject.Put\_**.</span></span>

<span data-ttu-id="4135a-115">La méthode générique et les noms de propriété définis dans cette section se terminent toujours par un trait de soulignement (« \_ ») de fin pour les différencier des méthodes et des propriétés WMI dynamiques de l’objet sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="4135a-115">The generic method and property names defined in this section always end with a trailing underscore ("\_") to differentiate them from the dynamic WMI methods and properties of the underlying object.</span></span>

<span data-ttu-id="4135a-116">Notez que **SWbemObject** ne peut pas être créé à l’aide de la méthode VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).</span><span class="sxs-lookup"><span data-stu-id="4135a-116">Note that **SWbemObject** cannot be created using the VBScript [**GetObject**](https://msdn.microsoft.com/library/e9waz863(v=VS.71).aspx).method.</span></span> <span data-ttu-id="4135a-117">Si vous souhaitez créer une nouvelle classe vide, utilisez [**SWbemServices. obtenir**](swbemservices-get.md) avec un paramètre de chemin d’accès vide.</span><span class="sxs-lookup"><span data-stu-id="4135a-117">If you want to create a new, empty class use [**SWbemServices.Get**](swbemservices-get.md) with an empty path parameter.</span></span> <span data-ttu-id="4135a-118">Cet appel retourne un objet **SWbemObject** vide qui peut devenir une classe.</span><span class="sxs-lookup"><span data-stu-id="4135a-118">This call returns an empty **SWbemObject** object that can become a class.</span></span> <span data-ttu-id="4135a-119">Vous pouvez ensuite fournir un nom de classe pour la propriété de [**classe**](swbemobjectpath-class.md) de l’objet [**SWbemObjectPath**](swbemobjectpath.md) retourné par l’appel de [**chemin \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="4135a-119">You can then supply a class name for the [**Class**](swbemobjectpath-class.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the [**Path\_**](swbemobject-path-.md) call.</span></span> <span data-ttu-id="4135a-120">Ajoutez des propriétés à la nouvelle classe par la méthode [**Properties \_**](swbemobject-properties-.md) .</span><span class="sxs-lookup"><span data-stu-id="4135a-120">Add properties to the new class by the [**Properties\_**](swbemobject-properties-.md) method.</span></span> <span data-ttu-id="4135a-121">Pour créer une instance, appelez **GetObject** sur la nouvelle classe.</span><span class="sxs-lookup"><span data-stu-id="4135a-121">To create an instance, call **GetObject** on the new class.</span></span>

<span data-ttu-id="4135a-122">L’exemple de code suivant montre comment obtenir une nouvelle classe et lui ajouter une propriété.</span><span class="sxs-lookup"><span data-stu-id="4135a-122">The following code example shows how to obtain a new class and add a property to it.</span></span> <span data-ttu-id="4135a-123">L’objet **SWbemObject** qui représente la classe doit être réécrit dans le référentiel WMI par un appel à [**put \_**](swbemobject-put-.md).</span><span class="sxs-lookup"><span data-stu-id="4135a-123">The **SWbemObject** object that represents the class must be written back to the WMI repository by a call to [**Put\_**](swbemobject-put-.md).</span></span>


```VB
wbemCimtypeString = 8
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString  
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.add "key", true

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
WScript.Echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").Spawninstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
WScript.Echo objInstancePath.Path

```



<span data-ttu-id="4135a-124">Vous pouvez examiner le référentiel à l’aide d’un outil d’affichage tel que [CIM Studio](further-information.md) pour vérifier que la nouvelle classe et l’instance s’affichent.</span><span class="sxs-lookup"><span data-stu-id="4135a-124">You can examine the repository with a viewing tool such as [CIM Studio](further-information.md) to verify that the new class and instance appear.</span></span> <span data-ttu-id="4135a-125">Pour obtenir un exemple de suppression d’une classe et d’une instance du référentiel, consultez [**SWbemServices. Delete**](swbemservices-delete.md) ou [**SWbemObject. \_ Delete**](swbemobject-delete-.md).</span><span class="sxs-lookup"><span data-stu-id="4135a-125">For an example of removing a class and instance from the repository, see [**SWbemServices.Delete**](swbemservices-delete.md) or [**SWbemObject.Delete\_**](swbemobject-delete-.md).</span></span>

## <a name="members"></a><span data-ttu-id="4135a-126">Membres</span><span class="sxs-lookup"><span data-stu-id="4135a-126">Members</span></span>

<span data-ttu-id="4135a-127">L’objet **SWbemObject** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4135a-127">The **SWbemObject** object has these types of members:</span></span>

-   [<span data-ttu-id="4135a-128">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4135a-128">Methods</span></span>](#methods)
-   [<span data-ttu-id="4135a-129">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4135a-129">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4135a-130">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4135a-130">Methods</span></span>

<span data-ttu-id="4135a-131">L’objet **SWbemObject** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4135a-131">The **SWbemObject** object has these methods.</span></span>



| <span data-ttu-id="4135a-132">Méthode</span><span class="sxs-lookup"><span data-stu-id="4135a-132">Method</span></span>                                                        | <span data-ttu-id="4135a-133">Description</span><span class="sxs-lookup"><span data-stu-id="4135a-133">Description</span></span>                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4135a-134">**Associateurs\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-134">**Associators\_**</span></span>](swbemobject-associators-.md)             | <span data-ttu-id="4135a-135">Récupère les associateurs de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-135">Retrieves the associators of the object.</span></span><br/>                                                     |
| [<span data-ttu-id="4135a-136">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-136">**AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)   | <span data-ttu-id="4135a-137">Récupère de manière asynchrone les associateurs de l’objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-137">Asynchronously retrieves the associators of the object.</span></span><br/>                                      |
| [<span data-ttu-id="4135a-138">**Répliqué\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-138">**Clone\_**</span></span>](swbemobject-clone-.md)                         | <span data-ttu-id="4135a-139">Effectue une copie de l’objet en cours.</span><span class="sxs-lookup"><span data-stu-id="4135a-139">Makes a copy of the current object.</span></span><br/>                                                          |
| [<span data-ttu-id="4135a-140">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-140">**CompareTo\_**</span></span>](swbemobject-compareto-.md)                 | <span data-ttu-id="4135a-141">Teste si deux objets sont égaux.</span><span class="sxs-lookup"><span data-stu-id="4135a-141">Tests two objects for equality.</span></span><br/>                                                              |
| [<span data-ttu-id="4135a-142">**Supprimer\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-142">**Delete\_**</span></span>](swbemobject-delete-.md)                       | <span data-ttu-id="4135a-143">Supprime l’objet de WMI.</span><span class="sxs-lookup"><span data-stu-id="4135a-143">Deletes the object from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="4135a-144">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-144">**DeleteAsync\_**</span></span>](swbemobject-deleteasync-.md)             | <span data-ttu-id="4135a-145">Supprime de façon asynchrone l’objet de WMI.</span><span class="sxs-lookup"><span data-stu-id="4135a-145">Asynchronously deletes the object from WMI.</span></span><br/>                                                  |
| [<span data-ttu-id="4135a-146">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-146">**ExecMethod\_**</span></span>](swbemobject-execmethod-.md)               | <span data-ttu-id="4135a-147">Exécute une méthode exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="4135a-147">Executes a method exported by a method provider.</span></span><br/>                                             |
| [<span data-ttu-id="4135a-148">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-148">**ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)     | <span data-ttu-id="4135a-149">Exécute de façon asynchrone une méthode exportée par un fournisseur de méthode.</span><span class="sxs-lookup"><span data-stu-id="4135a-149">Asynchronously executes a method exported by a method provider.</span></span><br/>                              |
| [<span data-ttu-id="4135a-150">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-150">**GetObjectText\_**</span></span>](swbemobject-getobjecttext-.md)         | <span data-ttu-id="4135a-151">Récupère la représentation textuelle de l’objet (syntaxe MOF).</span><span class="sxs-lookup"><span data-stu-id="4135a-151">Retrieves the textual representation of the object (MOF syntax).</span></span><br/>                             |
| [<span data-ttu-id="4135a-152">**Fois\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-152">**Instances\_**</span></span>](swbemobject-instances-.md)                 | <span data-ttu-id="4135a-153">Retourne une collection d’instances de l’objet (qui doit être une classe WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-153">Returns a collection of instances of the object (which must be a WMI class).</span></span><br/>                 |
| [<span data-ttu-id="4135a-154">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-154">**InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)       | <span data-ttu-id="4135a-155">Retourne de façon asynchrone une collection d’instances de l’objet (qui doit être une classe WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-155">Asynchronously returns a collection of instances of the object (which must be a WMI class).</span></span><br/>  |
| [<span data-ttu-id="4135a-156">**Posé\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-156">**Put\_**</span></span>](swbemobject-put-.md)                             | <span data-ttu-id="4135a-157">Crée ou met à jour l’objet dans WMI.</span><span class="sxs-lookup"><span data-stu-id="4135a-157">Creates or updates the object in WMI.</span></span><br/>                                                        |
| [<span data-ttu-id="4135a-158">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-158">**PutAsync\_**</span></span>](swbemobject-putasync-.md)                   | <span data-ttu-id="4135a-159">Crée ou met à jour de façon asynchrone l’objet dans WMI.</span><span class="sxs-lookup"><span data-stu-id="4135a-159">Asynchronously creates or updates the object in WMI.</span></span><br/>                                         |
| [<span data-ttu-id="4135a-160">**Références\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-160">**References\_**</span></span>](swbemobject-references-.md)               | <span data-ttu-id="4135a-161">Retourne des références à l’objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-161">Returns references to the object.</span></span><br/>                                                            |
| [<span data-ttu-id="4135a-162">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-162">**ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)     | <span data-ttu-id="4135a-163">Retourne de façon asynchrone des références à l’objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-163">Asynchronously returns references to the object.</span></span><br/>                                             |
| [<span data-ttu-id="4135a-164">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-164">**SpawnDerivedClass\_**</span></span>](swbemobject-spawnderivedclass-.md) | <span data-ttu-id="4135a-165">Crée une classe dérivée à partir de l’objet actuel (qui doit être une classe WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-165">Creates a new derived class from the current object (which must be a WMI class).</span></span><br/>             |
| [<span data-ttu-id="4135a-166">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-166">**SpawnInstance\_**</span></span>](swbemobject-spawninstance-.md)         | <span data-ttu-id="4135a-167">Crée une nouvelle instance de à partir de l’objet en cours.</span><span class="sxs-lookup"><span data-stu-id="4135a-167">Creates a new instance from the current object.</span></span><br/>                                              |
| [<span data-ttu-id="4135a-168">**Sous-classes\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-168">**Subclasses\_**</span></span>](swbemobject-subclasses-.md)               | <span data-ttu-id="4135a-169">Retourne une collection de sous-classes de l’objet (qui doit être une classe WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-169">Returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/>                |
| [<span data-ttu-id="4135a-170">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-170">**SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)     | <span data-ttu-id="4135a-171">Retourne de façon asynchrone une collection de sous-classes de l’objet (qui doit être une classe WMI).</span><span class="sxs-lookup"><span data-stu-id="4135a-171">Asynchronously returns a collection of subclasses of the object (which must be a WMI class).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="4135a-172">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4135a-172">Properties</span></span>

<span data-ttu-id="4135a-173">L’objet **SWbemObject** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="4135a-173">The **SWbemObject** object has these properties.</span></span>



| <span data-ttu-id="4135a-174">Propriété</span><span class="sxs-lookup"><span data-stu-id="4135a-174">Property</span></span>                                                   | <span data-ttu-id="4135a-175">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="4135a-175">Access type</span></span>          | <span data-ttu-id="4135a-176">Description</span><span class="sxs-lookup"><span data-stu-id="4135a-176">Description</span></span>                                                                                                                                |
|:-----------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4135a-177">**Dérivation\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-177">**Derivation\_**</span></span>](swbemobject-derivation-.md)<br/> | <span data-ttu-id="4135a-178">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-178">Read-only</span></span><br/> | <span data-ttu-id="4135a-179">Contient un tableau de chaînes qui décrit la hiérarchie de dérivation pour la classe.</span><span class="sxs-lookup"><span data-stu-id="4135a-179">Contains an array of strings that describes the derivation hierarchy for the class.</span></span><br/>                                             |
| [<span data-ttu-id="4135a-180">**Méthodes\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-180">**Methods\_**</span></span>](swbemobject-methods-.md)<br/>       | <span data-ttu-id="4135a-181">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-181">Read-only</span></span><br/> | <span data-ttu-id="4135a-182">Objet [**SWbemMethodSet**](swbemmethodset.md) qui est la collection de méthodes pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-182">An [**SWbemMethodSet**](swbemmethodset.md) object that is the collection of methods for this object.</span></span><br/>                           |
| [<span data-ttu-id="4135a-183">**D\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-183">**Path\_**</span></span>](swbemobject-path-.md)<br/>             | <span data-ttu-id="4135a-184">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-184">Read-only</span></span><br/> | <span data-ttu-id="4135a-185">Contient un objet [**SWbemObjectPath**](swbemobjectpath.md) qui représente le chemin d’accès de l’objet de la classe ou de l’instance actuelle.</span><span class="sxs-lookup"><span data-stu-id="4135a-185">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/> |
| [<span data-ttu-id="4135a-186">**Propriétés\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-186">**Properties\_**</span></span>](swbemobject-properties-.md)<br/> | <span data-ttu-id="4135a-187">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-187">Read-only</span></span><br/> | <span data-ttu-id="4135a-188">Objet [**SWbemPropertySet**](swbempropertyset.md) qui est la collection de propriétés pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-188">An [**SWbemPropertySet**](swbempropertyset.md) object that is the collection of properties for this object.</span></span><br/>                    |
| [<span data-ttu-id="4135a-189">**Qualificateurs\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-189">**Qualifiers\_**</span></span>](swbemobject-qualifiers-.md)<br/> | <span data-ttu-id="4135a-190">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-190">Read-only</span></span><br/> | <span data-ttu-id="4135a-191">Objet [**SWbemQualifierSet**](swbemqualifierset.md) qui est la collection de qualificateurs pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="4135a-191">An [**SWbemQualifierSet**](swbemqualifierset.md) object that is the collection of qualifiers for this object.</span></span><br/>                  |
| [<span data-ttu-id="4135a-192">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="4135a-192">**Security\_**</span></span>](swbemobject-security-.md)<br/>     | <span data-ttu-id="4135a-193">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4135a-193">Read-only</span></span><br/> | <span data-ttu-id="4135a-194">Contient un objet [**SWbemSecurity**](swbemsecurity.md) utilisé pour lire ou modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="4135a-194">Contains an [**SWbemSecurity**](swbemsecurity.md) object used to read or change the security settings.</span></span><br/>                         |



 

## <a name="examples"></a><span data-ttu-id="4135a-195">Exemples</span><span class="sxs-lookup"><span data-stu-id="4135a-195">Examples</span></span>

<span data-ttu-id="4135a-196">La [liste de toutes les propriétés et méthodes pour un](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) exemple de code VBScript de classe WMI dans la Galerie TechNet utilise SWbemObject pour répertorier toutes les méthodes et propriétés d’une classe WMI spécifiée.</span><span class="sxs-lookup"><span data-stu-id="4135a-196">The [List All the Properties and Methods for a WMI Class](https://Gallery.TechNet.Microsoft.Com/f0666124-3b67-4254-8ff1-3b75ae15776d) VBScript code sample on TechNet Gallery uses the SWbemObject to list all of the methods and properties for a specified WMI class.</span></span>

## <a name="requirements"></a><span data-ttu-id="4135a-197">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4135a-197">Requirements</span></span>



| <span data-ttu-id="4135a-198">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4135a-198">Requirement</span></span> | <span data-ttu-id="4135a-199">Valeur</span><span class="sxs-lookup"><span data-stu-id="4135a-199">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4135a-200">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4135a-200">Minimum supported client</span></span><br/> | <span data-ttu-id="4135a-201">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4135a-201">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4135a-202">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4135a-202">Minimum supported server</span></span><br/> | <span data-ttu-id="4135a-203">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4135a-203">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4135a-204">En-tête</span><span class="sxs-lookup"><span data-stu-id="4135a-204">Header</span></span><br/>                   | <dl> <span data-ttu-id="4135a-205"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="4135a-205"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="4135a-206">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4135a-206">Type library</span></span><br/>             | <dl> <span data-ttu-id="4135a-207"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="4135a-207"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="4135a-208">DLL</span><span class="sxs-lookup"><span data-stu-id="4135a-208">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4135a-209"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4135a-209"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="4135a-210">CLSID</span><span class="sxs-lookup"><span data-stu-id="4135a-210">CLSID</span></span><br/>                    | <span data-ttu-id="4135a-211">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="4135a-211">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="4135a-212">IID</span><span class="sxs-lookup"><span data-stu-id="4135a-212">IID</span></span><br/>                      | <span data-ttu-id="4135a-213">IID \_ ISWbemObject</span><span class="sxs-lookup"><span data-stu-id="4135a-213">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="4135a-214">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4135a-214">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4135a-215">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="4135a-215">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="4135a-216">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="4135a-216">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

