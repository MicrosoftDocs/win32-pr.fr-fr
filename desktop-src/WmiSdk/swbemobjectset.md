---
description: Un objet SWbemObjectSet est une collection d’objets SWbemObject. Pour plus d’informations, consultez accès à une collection. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 00f5317e-eb8e-42f9-bada-963e11aadda4
ms.tgt_platform: multiple
title: Objet SWbemObjectSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet
- ISWbemObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a6992658214d7ea5acbadbea396992edf0e3e9d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210542"
---
# <a name="swbemobjectset-object"></a><span data-ttu-id="8576b-105">Objet SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="8576b-105">SWbemObjectSet object</span></span>

<span data-ttu-id="8576b-106">Un objet **SWbemObjectSet** est une collection d’objets [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="8576b-106">An **SWbemObjectSet** object is a collection of [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="8576b-107">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="8576b-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="8576b-108">Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="8576b-108">This object cannot be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="8576b-109">Vous pouvez récupérer un objet **SWbemObjectSet** en appelant l’une des méthodes suivantes ou leurs équivalents asynchrones :</span><span class="sxs-lookup"><span data-stu-id="8576b-109">You can get an **SWbemObjectSet** object by calling any of the following methods or their asynchronous equivalents:</span></span>

-   [<span data-ttu-id="8576b-110">**SWbemObject. ASSOCIATORS\_**</span><span class="sxs-lookup"><span data-stu-id="8576b-110">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)
-   [<span data-ttu-id="8576b-111">**SWbemObject. instances\_**</span><span class="sxs-lookup"><span data-stu-id="8576b-111">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)
-   [<span data-ttu-id="8576b-112">**SWbemObject. References\_**</span><span class="sxs-lookup"><span data-stu-id="8576b-112">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)
-   [<span data-ttu-id="8576b-113">**SWbemObject. Subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="8576b-113">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)
-   [<span data-ttu-id="8576b-114">**SWbemServices. AssociatorsOf**</span><span class="sxs-lookup"><span data-stu-id="8576b-114">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md)
-   [<span data-ttu-id="8576b-115">**SWbemServices.ExecQuery**</span><span class="sxs-lookup"><span data-stu-id="8576b-115">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)
-   [<span data-ttu-id="8576b-116">**SWbemServices. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="8576b-116">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)
-   [<span data-ttu-id="8576b-117">**SWbemServices. ReferencesTo**</span><span class="sxs-lookup"><span data-stu-id="8576b-117">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)
-   [<span data-ttu-id="8576b-118">**SWbemServices. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="8576b-118">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)

> [!Note]  
> <span data-ttu-id="8576b-119">L’objet **SWbemObjectSet** ne prend pas en charge les méthodes facultatives **Add** et **Remove** collection.</span><span class="sxs-lookup"><span data-stu-id="8576b-119">The **SWbemObjectSet** object does not support the optional **Add** and **Remove** collection methods.</span></span>

 

> [!Note]  
> <span data-ttu-id="8576b-120">Étant donné que le rappel au récepteur peut ne pas être retourné au même niveau d’authentification que celui requis par le client, il est recommandé d’utiliser la fonction semi-synchrone au lieu de la communication asynchrone.</span><span class="sxs-lookup"><span data-stu-id="8576b-120">Because the call-back to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="8576b-121">Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8576b-121">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

## <a name="members"></a><span data-ttu-id="8576b-122">Membres</span><span class="sxs-lookup"><span data-stu-id="8576b-122">Members</span></span>

<span data-ttu-id="8576b-123">L’objet **SWbemObjectSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8576b-123">The **SWbemObjectSet** object has these types of members:</span></span>

-   [<span data-ttu-id="8576b-124">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8576b-124">Methods</span></span>](#methods)
-   [<span data-ttu-id="8576b-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8576b-125">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="8576b-126">Méthodes</span><span class="sxs-lookup"><span data-stu-id="8576b-126">Methods</span></span>

<span data-ttu-id="8576b-127">L’objet **SWbemObjectSet** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="8576b-127">The **SWbemObjectSet** object has these methods.</span></span>



| <span data-ttu-id="8576b-128">Méthode</span><span class="sxs-lookup"><span data-stu-id="8576b-128">Method</span></span>                              | <span data-ttu-id="8576b-129">Description</span><span class="sxs-lookup"><span data-stu-id="8576b-129">Description</span></span>                                                                                                                      |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8576b-130">**Élément**</span><span class="sxs-lookup"><span data-stu-id="8576b-130">**Item**</span></span>](swbemobjectset-item.md) | <span data-ttu-id="8576b-131">Récupère un objet [**SWbemObject**](swbemobject.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="8576b-131">Retrieves an [**SWbemObject**](swbemobject.md) object from the collection.</span></span> <span data-ttu-id="8576b-132">Il s’agit de la méthode par défaut de l’objet.</span><span class="sxs-lookup"><span data-stu-id="8576b-132">This is the default method of the object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="8576b-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8576b-133">Properties</span></span>

<span data-ttu-id="8576b-134">L’objet **SWbemObjectSet** possède ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="8576b-134">The **SWbemObjectSet** object has these properties.</span></span>



| <span data-ttu-id="8576b-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="8576b-135">Property</span></span>                                                  | <span data-ttu-id="8576b-136">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8576b-136">Access type</span></span>          | <span data-ttu-id="8576b-137">Description</span><span class="sxs-lookup"><span data-stu-id="8576b-137">Description</span></span>                                              |
|:----------------------------------------------------------|:---------------------|:---------------------------------------------------------|
| [<span data-ttu-id="8576b-138">**Saut**</span><span class="sxs-lookup"><span data-stu-id="8576b-138">**Count**</span></span>](swbemobjectset-count.md)<br/>          | <span data-ttu-id="8576b-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8576b-139">Read-only</span></span><br/> | <span data-ttu-id="8576b-140">Nombre d’éléments dans la collection</span><span class="sxs-lookup"><span data-stu-id="8576b-140">The number of items in the collection.</span></span><br/>        |
| [<span data-ttu-id="8576b-141">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="8576b-141">**Security\_**</span></span>](swbemobjectset-security-.md)<br/> | <span data-ttu-id="8576b-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="8576b-142">Read-only</span></span><br/> | <span data-ttu-id="8576b-143">Utilisé pour lire ou modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="8576b-143">Used to read or change the security settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8576b-144">Notes</span><span class="sxs-lookup"><span data-stu-id="8576b-144">Remarks</span></span>

<span data-ttu-id="8576b-145">Une collection **SWbemObjectSet** est une collection de zéro ou plusieurs objets [**SWbemObject**](swbemobject.md) .</span><span class="sxs-lookup"><span data-stu-id="8576b-145">An **SWbemObjectSet** is a collection of zero or more [**SWbemObject**](swbemobject.md) objects.</span></span> <span data-ttu-id="8576b-146">Chaque **SWbemObject** dans une **SWbemObjectSet** peut représenter l’un des deux éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8576b-146">Each **SWbemObject** in a **SWbemObjectSet** can represent one of two things:</span></span>

-   <span data-ttu-id="8576b-147">Instance d’une ressource managée par WMI.</span><span class="sxs-lookup"><span data-stu-id="8576b-147">An instance of a WMI-managed resource.</span></span>
-   <span data-ttu-id="8576b-148">Instance d’une définition de classe.</span><span class="sxs-lookup"><span data-stu-id="8576b-148">An instance of a class definition.</span></span>

<span data-ttu-id="8576b-149">L’utilisation la plus courante de cette classe dans WMI est la valeur de retour pour un appel [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) ou [**InstancesOf**](swbemservices-instancesof.md) , comme décrit dans l’exemple de code suivant :</span><span class="sxs-lookup"><span data-stu-id="8576b-149">The most common use of this class in WMI is as the return value for an [**ExecQuery**](/windows/desktop/api/Provider/nf-provider-provider-execquery) or [**InstancesOf**](swbemservices-instancesof.md) call, as described in the following code sample:</span></span>


```VB
strComputer = "."
Set objSWbemServices = GetObject("winmgmts:\\" & strComputer & "\root\cimv2")
Set colServices = objSWbemServices.ExecQuery("SELECT State FROM Win32_Service")
For Each objService In colServices
    Wscript.Echo objService.Name, objService.State
Next
```



<span data-ttu-id="8576b-150">Pour l’essentiel, la seule chose que vous feriez avec une **SWbemObjectSet** est d’énumérer tous les objets contenus dans la collection elle-même.</span><span class="sxs-lookup"><span data-stu-id="8576b-150">For the most part, the only thing you will ever do with an **SWbemObjectSet** is enumerate all the objects contained within the collection itself.</span></span> <span data-ttu-id="8576b-151">Toutefois, **SWbemObjectSet** inclut un nombre de propriétés qui peut être utile dans les scripts d’administration de système.</span><span class="sxs-lookup"><span data-stu-id="8576b-151">However, **SWbemObjectSet** does include a property Count that can be useful in system administration scripting.</span></span> <span data-ttu-id="8576b-152">Comme son nom l’indique, count indique le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="8576b-152">As the name implies, Count tells you the number of items in the collection.</span></span> <span data-ttu-id="8576b-153">Par exemple, ce script récupère une collection de tous les services installés sur un ordinateur, puis renvoie le nombre total de services trouvés :</span><span class="sxs-lookup"><span data-stu-id="8576b-153">For example, this script retrieves a collection of all the services installed on a computer and then echoes the total number of services found:</span></span>

<span data-ttu-id="8576b-154">Pour plus d’informations sur l’utilisation de cette classe, consultez [énumération de WMI](enumerating-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="8576b-154">For more information on how to use this class, see [Enumerating WMI](enumerating-wmi.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8576b-155">Exemples</span><span class="sxs-lookup"><span data-stu-id="8576b-155">Examples</span></span>

<span data-ttu-id="8576b-156">L’exemple de code VBScript suivant illustre la manière dont les collections **SWbemObjectSet** sont manipulées.</span><span class="sxs-lookup"><span data-stu-id="8576b-156">The following VBScript code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```VB
On Error Resume Next

Set Disks = GetObject("winmgmts:").InstancesOf ("CIM_LogicalDisk")

WScript.Echo "There are", Disks.Count, " Disks"

Set Disk = Disks("Win32_LogicalDisk.DeviceID=""C:""")
WScript.Echo Disk.Path_.Path

if Err <> 0 Then
 WScript.Echo Err.Description
 Err.Clear
End if
```



<span data-ttu-id="8576b-157">L’exemple de code perl suivant illustre la manière dont les collections **SWbemObjectSet** sont manipulées.</span><span class="sxs-lookup"><span data-stu-id="8576b-157">The following Perl code sample illustrates how **SWbemObjectSet** collections are manipulated.</span></span>


```
use strict;
use Win32::OLE;

my ($disks,$disk);

eval { $disks = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
   InstancesOf("CIM_LogicalDisk"); };
unless($@)
{
 print "\nThere are ", $disks->{Count}, " Disks \n";

 eval { $disk = $disks->Item("Win32_LogicalDisk.DeviceID=\"C:\""); };
 unless($@)
 {
  print $disk->{Path_}->{Path}, "\n";
 }
 else
 {
  print STDERR Win32::OLE->LastError, "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="8576b-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8576b-158">Requirements</span></span>



| <span data-ttu-id="8576b-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8576b-159">Requirement</span></span> | <span data-ttu-id="8576b-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="8576b-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8576b-161">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8576b-161">Minimum supported client</span></span><br/> | <span data-ttu-id="8576b-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8576b-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8576b-163">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8576b-163">Minimum supported server</span></span><br/> | <span data-ttu-id="8576b-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8576b-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8576b-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="8576b-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="8576b-166"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8576b-166"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8576b-167">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8576b-167">Type library</span></span><br/>             | <dl> <span data-ttu-id="8576b-168"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8576b-168"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8576b-169">DLL</span><span class="sxs-lookup"><span data-stu-id="8576b-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8576b-170"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8576b-170"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8576b-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="8576b-171">CLSID</span></span><br/>                    | <span data-ttu-id="8576b-172">CLSID \_ SWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="8576b-172">CLSID\_SWbemObjectSet</span></span><br/>                                                        |
| <span data-ttu-id="8576b-173">IID</span><span class="sxs-lookup"><span data-stu-id="8576b-173">IID</span></span><br/>                      | <span data-ttu-id="8576b-174">IID \_ ISWbemObjectSet</span><span class="sxs-lookup"><span data-stu-id="8576b-174">IID\_ISWbemObjectSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="8576b-175">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8576b-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8576b-176">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="8576b-176">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




