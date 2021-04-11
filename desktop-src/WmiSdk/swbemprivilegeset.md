---
description: Un objet SWbemPrivilegeSet est une collection d’objets SWbemPrivilege dans un objet SWbemSecurity qui demande des privilèges spécifiques pour un objet Windows Management Instrumentation (WMI).
ms.assetid: 073cf2d4-f7ee-45a6-8fa6-ca77a4870346
ms.tgt_platform: multiple
title: Objet SWbemPrivilegeSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPrivilegeSet
- ISWbemPrivilegeSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b2946f8b1f745c0db123ed33dab312cbbe9d16c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318865"
---
# <a name="swbemprivilegeset-object"></a><span data-ttu-id="7e470-103">Objet SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="7e470-103">SWbemPrivilegeSet object</span></span>

<span data-ttu-id="7e470-104">Un objet **SWbemPrivilegeSet** est une collection d’objets [**SWbemPrivilege**](swbemprivilege.md) dans un objet [**SWbemSecurity**](swbemsecurity.md) qui demande des privilèges spécifiques pour un objet Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="7e470-104">An **SWbemPrivilegeSet** object is a collection of [**SWbemPrivilege**](swbemprivilege.md) objects in an [**SWbemSecurity**](swbemsecurity.md) object that requests specific privileges for a Windows Management Instrumentation (WMI) object.</span></span> <span data-ttu-id="7e470-105">Consultez la liste des privilèges dans [**constantes de privilège**](privilege-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7e470-105">See the list of privileges in [**Privilege Constants**](privilege-constants.md).</span></span> <span data-ttu-id="7e470-106">Les éléments sont ajoutés à la collection à l’aide des méthodes [**Add**](swbemprivilegeset-add.md) et [**AddAsString**](swbemprivilegeset-addasstring.md) .</span><span class="sxs-lookup"><span data-stu-id="7e470-106">Items are added to the collection using the [**Add**](swbemprivilegeset-add.md) and [**AddAsString**](swbemprivilegeset-addasstring.md) methods.</span></span> <span data-ttu-id="7e470-107">Les éléments sont récupérés à partir de la collection à l’aide de la méthode [**Item**](swbemprivilegeset-item.md) et supprimés à l’aide de la méthode [**Remove**](swbemprivilegeset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="7e470-107">Items are retrieved from the collection using the [**Item**](swbemprivilegeset-item.md) method, and removed using the [**Remove**](swbemprivilegeset-remove.md) method.</span></span> <span data-ttu-id="7e470-108">Cet objet ne peut pas être créé par l’appel de méthode VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="7e470-108">This object cannot be created by the VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) method call.</span></span> <span data-ttu-id="7e470-109">Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="7e470-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="7e470-110">Un objet **SWbemPrivilegeSet** est un ensemble de demandes de remplacement de privilège pour un objet spécifique.</span><span class="sxs-lookup"><span data-stu-id="7e470-110">An **SWbemPrivilegeSet** object is a set of privilege override requests for a specific object.</span></span> <span data-ttu-id="7e470-111">Lorsqu’un appel d’API est effectué à l’aide de cet objet, les demandes de remplacement de privilège sont tentées.</span><span class="sxs-lookup"><span data-stu-id="7e470-111">When an API call is made using this object, the privilege override requests are attempted.</span></span> <span data-ttu-id="7e470-112">L’objet **SWbemPrivilegeSet** ne définit pas les privilèges disponibles pour l’utilisateur ou le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="7e470-112">The **SWbemPrivilegeSet** object does not define the privileges available to the current user or process.</span></span> <span data-ttu-id="7e470-113">En d’autres termes, l’obtention des privilèges pour n’importe quel objet WMI n’identifie pas les paramètres de privilège établis sur la connexion à WMI, ou les privilèges en vigueur lorsqu’un objet est remis à un récepteur.</span><span class="sxs-lookup"><span data-stu-id="7e470-113">In other words, obtaining the privileges for any WMI object does not identify the privilege settings that are made on the connection to WMI, or the privileges in effect when an object is delivered to a sink.</span></span>

## <a name="members"></a><span data-ttu-id="7e470-114">Membres</span><span class="sxs-lookup"><span data-stu-id="7e470-114">Members</span></span>

<span data-ttu-id="7e470-115">L’objet **SWbemPrivilegeSet** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7e470-115">The **SWbemPrivilegeSet** object has these types of members:</span></span>

-   [<span data-ttu-id="7e470-116">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e470-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="7e470-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e470-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="7e470-118">Méthodes</span><span class="sxs-lookup"><span data-stu-id="7e470-118">Methods</span></span>

<span data-ttu-id="7e470-119">L’objet **SWbemPrivilegeSet** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="7e470-119">The **SWbemPrivilegeSet** object has these methods.</span></span>



| <span data-ttu-id="7e470-120">Méthode</span><span class="sxs-lookup"><span data-stu-id="7e470-120">Method</span></span>                                               | <span data-ttu-id="7e470-121">Description</span><span class="sxs-lookup"><span data-stu-id="7e470-121">Description</span></span>                                                                                                                                                             |
|:-----------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e470-122">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="7e470-122">**Add**</span></span>](swbemprivilegeset-add.md)                 | <span data-ttu-id="7e470-123">Ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** à l’aide d’une constante [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) .</span><span class="sxs-lookup"><span data-stu-id="7e470-123">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a [WbemPrivilegeEnum](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum) constant.</span></span><br/> |
| [<span data-ttu-id="7e470-124">**AddAsString**</span><span class="sxs-lookup"><span data-stu-id="7e470-124">**AddAsString**</span></span>](swbemprivilegeset-addasstring.md) | <span data-ttu-id="7e470-125">Ajoute un objet [**SWbemPrivilege**](swbemprivilege.md) à la collection **SWbemPrivilegeSet** à l’aide d’une chaîne de privilèges.</span><span class="sxs-lookup"><span data-stu-id="7e470-125">Adds an [**SWbemPrivilege**](swbemprivilege.md) object to the **SWbemPrivilegeSet** collection using a privilege string.</span></span><br/>                                    |
| [<span data-ttu-id="7e470-126">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="7e470-126">**DeleteAll**</span></span>](swbemprivilegeset-deleteall.md)     | <span data-ttu-id="7e470-127">Supprime tous les privilèges de la collection.</span><span class="sxs-lookup"><span data-stu-id="7e470-127">Deletes all the privileges from the collection.</span></span><br/>                                                                                                              |
| [<span data-ttu-id="7e470-128">**Élément**</span><span class="sxs-lookup"><span data-stu-id="7e470-128">**Item**</span></span>](swbemprivilegeset-item.md)               | <span data-ttu-id="7e470-129">Récupère un objet [**SWbemPrivilege**](swbemprivilege.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="7e470-129">Retrieves an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span> <span data-ttu-id="7e470-130">Il s’agit de la méthode par défaut de cet objet.</span><span class="sxs-lookup"><span data-stu-id="7e470-130">This is the default method of this object.</span></span><br/>                                 |
| [<span data-ttu-id="7e470-131">**Installez**</span><span class="sxs-lookup"><span data-stu-id="7e470-131">**Remove**</span></span>](swbemprivilegeset-remove.md)           | <span data-ttu-id="7e470-132">Supprime un objet [**SWbemPrivilege**](swbemprivilege.md) de la collection.</span><span class="sxs-lookup"><span data-stu-id="7e470-132">Removes an [**SWbemPrivilege**](swbemprivilege.md) object from the collection.</span></span><br/>                                                                              |



 

### <a name="properties"></a><span data-ttu-id="7e470-133">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7e470-133">Properties</span></span>

<span data-ttu-id="7e470-134">L’objet **SWbemPrivilegeSet** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7e470-134">The **SWbemPrivilegeSet** object has these properties.</span></span>



| <span data-ttu-id="7e470-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="7e470-135">Property</span></span>                                            | <span data-ttu-id="7e470-136">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7e470-136">Access type</span></span>          | <span data-ttu-id="7e470-137">Description</span><span class="sxs-lookup"><span data-stu-id="7e470-137">Description</span></span>                                       |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="7e470-138">**Saut**</span><span class="sxs-lookup"><span data-stu-id="7e470-138">**Count**</span></span>](swbemprivilegeset-count.md)<br/> | <span data-ttu-id="7e470-139">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7e470-139">Read-only</span></span><br/> | <span data-ttu-id="7e470-140">Nombre d’éléments dans la collection</span><span class="sxs-lookup"><span data-stu-id="7e470-140">The number of items in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="7e470-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="7e470-141">Examples</span></span>

<span data-ttu-id="7e470-142">L’exemple de code VBScript suivant obtient un objet SWbemPrivileges et ajoute tous les privilèges disponibles à la collection par valeur de privilège, comme défini dans [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span><span class="sxs-lookup"><span data-stu-id="7e470-142">The following VBScript code example obtains an SWbemPrivileges object and adds all the available privileges to the collection by privilege value, as defined in [**WbemPrivilegeEnum**](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum).</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:\\" _
    & strComputer & "\root\cimv2")
set colPrivileges = objWMIService.Security_.Privileges
For I = 1 To 27
colPrivileges.Add(I)
Next
' Display information about each privilege 
For Each objItem In colPrivileges
wscript.echo objItem.Identifier & vbtab & objItem.Name _
    & vbtab & objItem.Displayname _
    & vbtab & "Enabled = " & objItem.IsEnabled
Next
```



<span data-ttu-id="7e470-143">L’exemple de code VBScript suivant montre comment ajouter des privilèges à l’aide de l’objet **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="7e470-143">The following VBScript code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```VB
on error resume next

const wbemPrivilegeSecurity = 8
const wbemPrivilegeDebug = 20

set locator = CreateObject("WbemScripting.SWbemLocator")

' Add a single privilege using SWbemPrivilegeSet.Add

locator.Security_.Privileges.Add wbemPrivilegeSecurity 
Set Privilege = locator.Security_.Privileges(wbemPrivilegeSecurity)
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
locator.Security_.Privileges.Add 6535
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

locator.Security_.Privileges.Add wbemPrivilegeDebug 

locator.Security_.Privileges(wbemPrivilegeDebug).IsEnabled = false

' Add a single privilege using SWbemPrivilegeSet.AddAsString

Set Privilege = locator.Security_.Privileges.AddAsString ("SeChangeNotifyPrivilege")
WScript.Echo Privilege.Name

' Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
locator.Security_.Privileges.AddAsString "SeChungeNotifyPrivilege"
if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
 err.clear
end if 

WScript.Echo ""
for each Privilege in locator.Security_.Privileges
 WScript.Echo "[" & Privilege.DisplayName & "]", Privilege.Identifier, Privilege.Name, Privilege.IsEnabled
next

if err <> 0 then
 WScript.Echo Err.Number, Err.Description, Err.Source
end if 
```



<span data-ttu-id="7e470-144">L’exemple de code perl suivant montre comment ajouter des privilèges à l’aide de l’objet **SWbemPrivilegeSet** .</span><span class="sxs-lookup"><span data-stu-id="7e470-144">The following Perl code example demonstrates how to add privileges using the **SWbemPrivilegeSet** object.</span></span>


```
use strict;
use Win32::OLE;

close(STDERR);

my ($locator, $Privilege);
my $wbemPrivilegeSecurity = 8;
my $wbemPrivilegeDebug = 20;

eval { $locator = new Win32::OLE 'WbemScripting.SWbemLocator';};

if (!$@ && defined $locator)
{
 # Add a single privilege using SWbemPrivilegeSet.Add
 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeSecurity);
 $Privilege = $locator->{Security_}->Privileges($wbemPrivilegeSecurity);
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.Add
 eval { $locator->{Security_}->{Privileges}->Add(6535); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);

 $locator->{Security_}->{Privileges}->Add($wbemPrivilegeDebug); 
 $locator->{Security_}->Privileges($wbemPrivilegeDebug)->{IsEnabled} = 0;

 # Add a single privilege using SWbemPrivilegeSet.AddAsString
 $Privilege = $locator->{Security_}->{Privileges}->AddAsString ("SeChangeNotifyPrivilege");
 print "\n", $Privilege->{Name}, "\n\n";

 # Attempt to add an illegal privilege using SWbemPrivilegeSet.AddAsString
 eval {$locator->{Security_}->{Privileges}->AddAsString ("SeChungeNotifyPrivilege"); };
 print Win32::OLE->LastError, "\n" if ($@ || Win32::OLE->LastError);
 print "\n";

 foreach $Privilege (in {$locator->{Security_}->{Privileges}})
 {
  printf "[%s] %d %s %d \n" , $Privilege->{DisplayName}, $Privilege->{Identifier}, $Privilege->{Name}, $Privilege->{IsEnabled};
 }
}
else
{
 print Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="7e470-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e470-145">Requirements</span></span>



| <span data-ttu-id="7e470-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e470-146">Requirement</span></span> | <span data-ttu-id="7e470-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e470-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e470-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e470-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7e470-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7e470-149">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7e470-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e470-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7e470-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7e470-151">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7e470-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="7e470-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e470-153"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e470-153"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7e470-154">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7e470-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="7e470-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7e470-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7e470-156">DLL</span><span class="sxs-lookup"><span data-stu-id="7e470-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e470-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e470-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7e470-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="7e470-158">CLSID</span></span><br/>                    | <span data-ttu-id="7e470-159">CLSID \_ SWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="7e470-159">CLSID\_SWbemPrivilegeSet</span></span><br/>                                                     |
| <span data-ttu-id="7e470-160">IID</span><span class="sxs-lookup"><span data-stu-id="7e470-160">IID</span></span><br/>                      | <span data-ttu-id="7e470-161">IID \_ ISWbemPrivilegeSet</span><span class="sxs-lookup"><span data-stu-id="7e470-161">IID\_ISWbemPrivilegeSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="7e470-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e470-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e470-163">Exécution des opérations privilégiées</span><span class="sxs-lookup"><span data-stu-id="7e470-163">Executing Privileged Operations</span></span>](executing-privileged-operations.md)
</dt> <dt>

[<span data-ttu-id="7e470-164">Exécution d’opérations privilégiées à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="7e470-164">Executing Privileged Operations Using VBScript</span></span>](executing-privileged-operations-using-vbscript.md)
</dt> <dt>

[<span data-ttu-id="7e470-165">WbemPrivilegeEnum</span><span class="sxs-lookup"><span data-stu-id="7e470-165">WbemPrivilegeEnum</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> <dt>

[<span data-ttu-id="7e470-166">Scripts d’objets d’API</span><span class="sxs-lookup"><span data-stu-id="7e470-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="7e470-167">**Constantes de privilège**</span><span class="sxs-lookup"><span data-stu-id="7e470-167">**Privilege Constants**</span></span>](privilege-constants.md)
</dt> </dl>

 

