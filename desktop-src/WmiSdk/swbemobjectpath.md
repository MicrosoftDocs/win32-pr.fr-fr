---
description: Utilisez les méthodes et les propriétés de l’objet SWbemObjectPath pour construire et valider un chemin d’accès à un objet. Cet objet peut être créé par l’appel VBScript CreateObject.
ms.assetid: f2cf489d-d2a9-4926-84cf-fb33fe3d726a
ms.tgt_platform: multiple
title: Objet SWbemObjectPath (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath
- ISWbemObjectPath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1e6836cd58970f3667d8f629a678d55bec5185a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518609"
---
# <a name="swbemobjectpath-object"></a><span data-ttu-id="3aa26-104">Objet SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="3aa26-104">SWbemObjectPath object</span></span>

<span data-ttu-id="3aa26-105">Utilisez les méthodes et les propriétés de l’objet **SWbemObjectPath** pour construire et valider un chemin d’accès à un objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-105">Use the methods and properties of the **SWbemObjectPath** object to construct and validate an object path.</span></span> <span data-ttu-id="3aa26-106">Cet objet peut être créé par l’appel VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="3aa26-106">This object can be created by the VBScript **CreateObject** call.</span></span>

## <a name="members"></a><span data-ttu-id="3aa26-107">Membres</span><span class="sxs-lookup"><span data-stu-id="3aa26-107">Members</span></span>

<span data-ttu-id="3aa26-108">L’objet **SWbemObjectPath** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="3aa26-108">The **SWbemObjectPath** object has these types of members:</span></span>

-   [<span data-ttu-id="3aa26-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3aa26-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="3aa26-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3aa26-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3aa26-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="3aa26-111">Methods</span></span>

<span data-ttu-id="3aa26-112">L’objet **SWbemObjectPath** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="3aa26-112">The **SWbemObjectPath** object has these methods.</span></span>



| <span data-ttu-id="3aa26-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="3aa26-113">Method</span></span>                                                   | <span data-ttu-id="3aa26-114">Description</span><span class="sxs-lookup"><span data-stu-id="3aa26-114">Description</span></span>                                                     |
|:---------------------------------------------------------|:----------------------------------------------------------------|
| [<span data-ttu-id="3aa26-115">**SetAsClass**</span><span class="sxs-lookup"><span data-stu-id="3aa26-115">**SetAsClass**</span></span>](swbemobjectpath-setasclass.md)         | <span data-ttu-id="3aa26-116">Force le chemin d’accès à l’adresse d’une classe WMI.</span><span class="sxs-lookup"><span data-stu-id="3aa26-116">Forces the path to address a WMI class.</span></span><br/>              |
| [<span data-ttu-id="3aa26-117">**SetAsSingleton**</span><span class="sxs-lookup"><span data-stu-id="3aa26-117">**SetAsSingleton**</span></span>](swbemobjectpath-setassingleton.md) | <span data-ttu-id="3aa26-118">Force le chemin d’accès à l’adresse d’une instance WMI Singleton.</span><span class="sxs-lookup"><span data-stu-id="3aa26-118">Forces the path to address a singleton WMI instance.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3aa26-119">Propriétés</span><span class="sxs-lookup"><span data-stu-id="3aa26-119">Properties</span></span>

<span data-ttu-id="3aa26-120">L’objet **SWbemObjectPath** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="3aa26-120">The **SWbemObjectPath** object has these properties.</span></span>



| <span data-ttu-id="3aa26-121">Propriété</span><span class="sxs-lookup"><span data-stu-id="3aa26-121">Property</span></span>                                                              | <span data-ttu-id="3aa26-122">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="3aa26-122">Access type</span></span>           | <span data-ttu-id="3aa26-123">Description</span><span class="sxs-lookup"><span data-stu-id="3aa26-123">Description</span></span>                                                                                                                                                                          |
|:----------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3aa26-124">**Authority**</span><span class="sxs-lookup"><span data-stu-id="3aa26-124">**Authority**</span></span>](swbemobjectpath-authority.md)<br/>             | <span data-ttu-id="3aa26-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-125">Read/write</span></span><br/> | <span data-ttu-id="3aa26-126">Chaîne qui définit le composant d’autorité du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-126">String that defines the Authority component of the object path.</span></span><br/>                                                                                                           |
| [<span data-ttu-id="3aa26-127">**Classe**</span><span class="sxs-lookup"><span data-stu-id="3aa26-127">**Class**</span></span>](swbemobjectpath-class.md)<br/>                     | <span data-ttu-id="3aa26-128">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-128">Read/write</span></span><br/> | <span data-ttu-id="3aa26-129">Nom de la classe qui fait partie du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-129">Name of the class that is part of the object path.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="3aa26-130">**NomComplet**</span><span class="sxs-lookup"><span data-stu-id="3aa26-130">**DisplayName**</span></span>](swbemobjectpath-displayname.md)<br/>         | <span data-ttu-id="3aa26-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-131">Read/write</span></span><br/> | <span data-ttu-id="3aa26-132">Chaîne qui contient le chemin d’accès dans un formulaire qui peut être utilisé comme nom d’affichage du moniker.</span><span class="sxs-lookup"><span data-stu-id="3aa26-132">String that contains the path in a form that can be used as a moniker display name.</span></span> <span data-ttu-id="3aa26-133">Consultez [création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md).</span><span class="sxs-lookup"><span data-stu-id="3aa26-133">See [Creating a WMI Application or Script](creating-a-wmi-application-or-script.md).</span></span><br/> |
| [<span data-ttu-id="3aa26-134">**IsClass**</span><span class="sxs-lookup"><span data-stu-id="3aa26-134">**IsClass**</span></span>](swbemobjectpath-isclass.md)<br/>                 | <span data-ttu-id="3aa26-135">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa26-135">Read-only</span></span><br/>  | <span data-ttu-id="3aa26-136">Valeur booléenne qui indique si ce chemin d’accès représente une classe.</span><span class="sxs-lookup"><span data-stu-id="3aa26-136">Boolean value that indicates if this path represents a class.</span></span> <span data-ttu-id="3aa26-137">Cela est analogue à la propriété [ \_ \_ genre](wmi-system-properties.md) de l’API com.</span><span class="sxs-lookup"><span data-stu-id="3aa26-137">This is analogous to the [\_\_Genus](wmi-system-properties.md) property in the COM API.</span></span><br/>                    |
| [<span data-ttu-id="3aa26-138">**IsSingleton**</span><span class="sxs-lookup"><span data-stu-id="3aa26-138">**IsSingleton**</span></span>](swbemobjectpath-issingleton.md)<br/>         | <span data-ttu-id="3aa26-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa26-139">Read-only</span></span><br/>  | <span data-ttu-id="3aa26-140">Valeur booléenne qui indique si ce chemin d’accès représente une instance singleton.</span><span class="sxs-lookup"><span data-stu-id="3aa26-140">Boolean value that indicates if this path represents a singleton instance.</span></span><br/>                                                                                                |
| [<span data-ttu-id="3aa26-141">**Keys**</span><span class="sxs-lookup"><span data-stu-id="3aa26-141">**Keys**</span></span>](swbemobjectpath-keys.md)<br/>                       | <span data-ttu-id="3aa26-142">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa26-142">Read-only</span></span><br/>  | <span data-ttu-id="3aa26-143">Objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) qui contient les liaisons de valeur de clé.</span><span class="sxs-lookup"><span data-stu-id="3aa26-143">An [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that contains the key value bindings.</span></span><br/>                                                                          |
| [<span data-ttu-id="3aa26-144">**Paramètres régionaux**</span><span class="sxs-lookup"><span data-stu-id="3aa26-144">**Locale**</span></span>](swbemobjectpath-locale.md)<br/>                   | <span data-ttu-id="3aa26-145">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-145">Read/write</span></span><br/> | <span data-ttu-id="3aa26-146">Chaîne qui contient les paramètres régionaux pour le chemin d’accès de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-146">String that contains the locale for this object path.</span></span><br/>                                                                                                                     |
| [<span data-ttu-id="3aa26-147">**Espace de noms**</span><span class="sxs-lookup"><span data-stu-id="3aa26-147">**Namespace**</span></span>](swbemobjectpath-namespace.md)<br/>             | <span data-ttu-id="3aa26-148">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-148">Read/write</span></span><br/> | <span data-ttu-id="3aa26-149">Nom de l’espace de noms qui fait partie du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-149">Name of the namespace that is part of the object path.</span></span> <span data-ttu-id="3aa26-150">Il s’agit de la même propriété d' [ \_ \_ espace de noms](wmi-system-properties.md) dans l’API com.</span><span class="sxs-lookup"><span data-stu-id="3aa26-150">This is the same as the [\_\_Namespace](wmi-system-properties.md) property in the COM API.</span></span><br/>                        |
| [<span data-ttu-id="3aa26-151">**ParentNamespace**</span><span class="sxs-lookup"><span data-stu-id="3aa26-151">**ParentNamespace**</span></span>](swbemobjectpath-parentnamespace.md)<br/> | <span data-ttu-id="3aa26-152">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa26-152">Read-only</span></span><br/>  | <span data-ttu-id="3aa26-153">Nom du parent de l’espace de noms qui fait partie du chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-153">Name of the parent of the namespace that is part of the object path.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="3aa26-154">**D**</span><span class="sxs-lookup"><span data-stu-id="3aa26-154">**Path**</span></span>](swbemobjectpath-path.md)<br/>                       | <span data-ttu-id="3aa26-155">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-155">Read/write</span></span><br/> | <span data-ttu-id="3aa26-156">Contient le chemin d’accès absolu.</span><span class="sxs-lookup"><span data-stu-id="3aa26-156">Contains the absolute path.</span></span> <span data-ttu-id="3aa26-157">Il est identique à la propriété système [ \_ \_ path](wmi-system-properties.md) dans l’API com.</span><span class="sxs-lookup"><span data-stu-id="3aa26-157">This is the same as the [\_\_Path](wmi-system-properties.md) system property in the COM API.</span></span> <span data-ttu-id="3aa26-158">Il s’agit de la propriété par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="3aa26-158">This is the default property of this object.</span></span><br/>    |
| [<span data-ttu-id="3aa26-159">**Constitue**</span><span class="sxs-lookup"><span data-stu-id="3aa26-159">**Relpath**</span></span>](swbemobjectpath-relpath.md)<br/>                 | <span data-ttu-id="3aa26-160">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-160">Read/write</span></span><br/> | <span data-ttu-id="3aa26-161">Contient le chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="3aa26-161">Contains the relative path.</span></span> <span data-ttu-id="3aa26-162">Il est identique à la propriété système [ \_ \_ RelPath](wmi-system-properties.md) dans l’API com.</span><span class="sxs-lookup"><span data-stu-id="3aa26-162">This is the same as the [\_\_Relpath](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                              |
| [<span data-ttu-id="3aa26-163">**Sécurité\_**</span><span class="sxs-lookup"><span data-stu-id="3aa26-163">**Security\_**</span></span>](swbemobjectpath-security-.md)<br/>            | <span data-ttu-id="3aa26-164">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="3aa26-164">Read-only</span></span><br/>  | <span data-ttu-id="3aa26-165">Utilisé pour lire ou modifier les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="3aa26-165">Used to read or change the security settings.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="3aa26-166">**Serveur**</span><span class="sxs-lookup"><span data-stu-id="3aa26-166">**Server**</span></span>](swbemobjectpath-server.md)<br/>                   | <span data-ttu-id="3aa26-167">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="3aa26-167">Read/write</span></span><br/> | <span data-ttu-id="3aa26-168">Nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="3aa26-168">Name of the server.</span></span> <span data-ttu-id="3aa26-169">C’est la même chose que la propriété système du [ \_ \_ serveur](wmi-system-properties.md) dans l’API com.</span><span class="sxs-lookup"><span data-stu-id="3aa26-169">This is the same as the [\_\_Server](wmi-system-properties.md) system property in the COM API.</span></span><br/>                                                       |



 

## <a name="examples"></a><span data-ttu-id="3aa26-170">Exemples</span><span class="sxs-lookup"><span data-stu-id="3aa26-170">Examples</span></span>

<span data-ttu-id="3aa26-171">L’exemple de code VBScript suivant montre comment générer des chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="3aa26-171">The following VBScript code sample demonstrates how to build object paths.</span></span>


```VB
on error resume next 
Set ObjectPath = CreateObject("WbemScripting.SWbemObjectPath")
ObjectPath.Server = "dingle"
ObjectPath.Namespace = "root/default/something"
ObjectPath.Class = "ho"
ObjectPath.Keys.Add "fred1", 10
ObjectPath.Keys.Add "fred2", -34
ObjectPath.Keys.Add "fred3", 65234654
ObjectPath.Keys.Add "fred4", "Wahaay"
ObjectPath.Keys.Add "fred5", -786186777

if err <> 0 then 
 WScript.Echo err.number
end if 

WScript.Echo "Pass 1:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.ImpersonationLevel = 3

WScript.Echo "Pass 2:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.Security_.AuthenticationLevel = 5

WScript.Echo "Pass 3:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

Set Privileges = ObjectPath.Security_.Privileges
if err <> 0 then
 WScript.Echo Hex(Err.Number), Err.Description
end if
Privileges.Add 8
Privileges.Add 20, false

WScript.Echo "Pass 4:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""

ObjectPath.DisplayName = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah"

WScript.Echo "Pass 5:"
WScript.Echo ObjectPath.Path
WScript.Echo ObjectPath.DisplayName
WScript.Echo ""
```



<span data-ttu-id="3aa26-172">L’exemple de code perl suivant montre comment générer des chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="3aa26-172">The following Perl code sample demonstrates how to build object paths.</span></span>


```
use strict;
use Win32::OLE;
use constant FALSE=>"false";

my ( $ObjectPath, $Privileges );

eval { $ObjectPath = new Win32::OLE 'WbemScripting.SWbemObjectPath'; };
unless($@)
{
 eval
 {
  $ObjectPath->{Server} = "dingle";
  $ObjectPath->{Namespace} = "root/default/something";
  $ObjectPath->{Class} = "ho";
  $ObjectPath->{Keys}->Add("fred1", 10);
  $ObjectPath->{Keys}->Add("fred2", -34);
  $ObjectPath->{Keys}->Add("fred3", 65234654);
  $ObjectPath->{Keys}->Add("fred4", "Wahaay");
  $ObjectPath->{Keys}->Add("fred5", -786186777);
 };
 unless($@)
 {
  print "\n";
  print "Pass 1:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{ImpersonationLevel} = 3 ;

  print "Pass 2:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  $ObjectPath->{Security_}->{AuthenticationLevel} = 5 ;

  print "Pass 3:\n";
  print $ObjectPath->{Path}, "\n";
  print $ObjectPath->{DisplayName} , "\n\n";

  eval { $Privileges = $ObjectPath->{Security_}->{Privileges}; };
  unless($@)
  {
   $Privileges->Add(8);
   $Privileges->Add(20,FALSE);

   print "Pass 4:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n\n";

   $ObjectPath->{DisplayName} = "winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktprivacy,(Debug,!IncreaseQuota, CreatePagefile ) }!//fred/root/blah";

   print "Pass 5:\n";
   print $ObjectPath->{Path}, "\n";
   print $ObjectPath->{DisplayName} , "\n";
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
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="3aa26-173">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3aa26-173">Requirements</span></span>



| <span data-ttu-id="3aa26-174">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3aa26-174">Requirement</span></span> | <span data-ttu-id="3aa26-175">Valeur</span><span class="sxs-lookup"><span data-stu-id="3aa26-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa26-176">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa26-176">Minimum supported client</span></span><br/> | <span data-ttu-id="3aa26-177">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3aa26-177">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3aa26-178">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3aa26-178">Minimum supported server</span></span><br/> | <span data-ttu-id="3aa26-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3aa26-179">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3aa26-180">En-tête</span><span class="sxs-lookup"><span data-stu-id="3aa26-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="3aa26-181"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3aa26-181"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3aa26-182">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3aa26-182">Type library</span></span><br/>             | <dl> <span data-ttu-id="3aa26-183"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3aa26-183"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3aa26-184">DLL</span><span class="sxs-lookup"><span data-stu-id="3aa26-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3aa26-185"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3aa26-185"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3aa26-186">CLSID</span><span class="sxs-lookup"><span data-stu-id="3aa26-186">CLSID</span></span><br/>                    | <span data-ttu-id="3aa26-187">CLSID \_ SWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="3aa26-187">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="3aa26-188">IID</span><span class="sxs-lookup"><span data-stu-id="3aa26-188">IID</span></span><br/>                      | <span data-ttu-id="3aa26-189">IID \_ ISWbemObjectPath</span><span class="sxs-lookup"><span data-stu-id="3aa26-189">IID\_ISWbemObjectPath</span></span><br/>                                                        |



## <a name="see-also"></a><span data-ttu-id="3aa26-190">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3aa26-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa26-191">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="3aa26-191">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




