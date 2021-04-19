---
description: D’un point de vue conceptuel similaire à un Uniform Resource Locator (URL), un chemin d’accès d’objet WMI est une chaîne qui identifie de façon unique l’espace de noms sur un serveur, une classe dans un espace de noms ou des instances d’une classe.
ms.assetid: 7a390541-609d-4b97-b91c-1a41d21ec17d
ms.tgt_platform: multiple
title: Description de l’emplacement d’un objet WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b58b58a6b668955d6eba1e4c51f6f8dccdac890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521507"
---
# <a name="describing-the-location-of-a-wmi-object"></a><span data-ttu-id="0d9de-103">Description de l’emplacement d’un objet WMI</span><span class="sxs-lookup"><span data-stu-id="0d9de-103">Describing the Location of a WMI Object</span></span>

<span data-ttu-id="0d9de-104">D’un point de vue conceptuel similaire à un Uniform Resource Locator (URL), un chemin d’accès d’objet WMI est une chaîne qui identifie de façon unique l’espace de noms sur un serveur, une classe dans un espace de noms ou des instances d’une classe.</span><span class="sxs-lookup"><span data-stu-id="0d9de-104">Conceptually similar to a Uniform Resource Locator (URL), a WMI object path is a string that uniquely identifies the namespace on a server, a class within a namespace, or instances of a class.</span></span> <span data-ttu-id="0d9de-105">Un chemin d’accès d’objet est hiérarchique et contient plusieurs éléments qui décrivent l’emplacement de l’objet en question.</span><span class="sxs-lookup"><span data-stu-id="0d9de-105">An object path is hierarchical, and contains several elements that describe the location of the object in question.</span></span> <span data-ttu-id="0d9de-106">Comme les chemins d’accès aux fichiers, les chemins d’accès d’objet WMI peuvent être décrits dans l’intégralité ou spécifiés en tant que chemin d’accès relatif.</span><span class="sxs-lookup"><span data-stu-id="0d9de-106">Like file paths, WMI object paths can be described in full or specified as a relative path.</span></span>

<span data-ttu-id="0d9de-107">L’espace de noms d’un objet WMI est indiqué sur la page de référence WMI.</span><span class="sxs-lookup"><span data-stu-id="0d9de-107">The namespace of a WMI object is listed on the WMI reference page.</span></span> <span data-ttu-id="0d9de-108">Par exemple, l’emplacement de la plupart des classes prises en charge par les [fournisseurs WMI cimwin32](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) se trouvent dans l' \\ espace de \\ noms CIMV2 racine.</span><span class="sxs-lookup"><span data-stu-id="0d9de-108">For example, the location of most of the classes supported by the [CIMWin32 WMI Providers](/windows/desktop/CIMWin32Prov/cimwin32-wmi-providers) are located in the \\root\\cimv2 namespace.</span></span> <span data-ttu-id="0d9de-109">Le code PowerShell suivant décrit un appel pour récupérer l' [**objet \_ ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem) sur votre ordinateur local :</span><span class="sxs-lookup"><span data-stu-id="0d9de-109">The following PowerShell code describes a call to retrieve the [**Win32\_ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem) object on your local machine:</span></span>

`Get-WmiObject -Class Win32_ComputerSystem -Namespace "root\cimv2" -ComputerName "."`

<span data-ttu-id="0d9de-110">Une instance spécifique du [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) peut également avoir le chemin d’accès suivant à partir de la propriété [**SWbemObject. Path \_**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9de-110">Alternately, a specific instance of [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) may have the following path from the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>

`\\Machine1\root\cimv2:Win32_LogicalDisk.DeviceID="C:"`

<span data-ttu-id="0d9de-111">L’exemple suivant montre le chemin d’accès relatif à cette instance, comme indiqué par l’affichage de la propriété [**RelPath**](swbemobjectpath-relpath.md) de l’objet [**SWbemObjectPath**](swbemobjectpath.md) retourné par l’appel à [**SWbemObject. \_ path**](swbemobject-path-.md).</span><span class="sxs-lookup"><span data-stu-id="0d9de-111">The following example shows the relative path to this instance, as seen by displaying the [**Relpath**](swbemobjectpath-relpath.md) property of the [**SWbemObjectPath**](swbemobjectpath.md) object returned by the call to [**SWbemObject.Path\_**](swbemobject-path-.md).</span></span>

`Win32_LogicalDisk.DeviceID="A:"`

<span data-ttu-id="0d9de-112">Notez que **DeviceID** est la propriété de clé de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="0d9de-112">Note that **DeviceID** is the key property of the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>

## <a name="c"></a><span data-ttu-id="0d9de-113">C++</span><span class="sxs-lookup"><span data-stu-id="0d9de-113">C++</span></span>

<span data-ttu-id="0d9de-114">Le tableau suivant répertorie les types de chemin d’accès d’objet et les méthodes associées qui requièrent des chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="0d9de-114">The following table lists object path types and the associated methods that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d9de-115">Type de chemin d’accès de l’objet</span><span class="sxs-lookup"><span data-stu-id="0d9de-115">Object path type</span></span></th>
<th><span data-ttu-id="0d9de-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="0d9de-116">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d9de-117"><a href="describing-a-wmi-namespace-object-path.md">Espace de noms</a></span><span class="sxs-lookup"><span data-stu-id="0d9de-117"><a href="describing-a-wmi-namespace-object-path.md">Namespace</a></span></span></td>
<td><dl><span data-ttu-id="0d9de-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices :: OpenNamespace,</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-118"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-opennamespace"><strong>IWbemServices::OpenNamespace</strong></a></span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d9de-119"><a href="describing-a-class-object-path.md">Classe</a></span><span class="sxs-lookup"><span data-stu-id="0d9de-119"><a href="describing-a-class-object-path.md">Class</a></span></span></td>
<td><dl><span data-ttu-id="0d9de-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices :: ExecMethod</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-120"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod"><strong>IWbemServices::ExecMethod</strong></a></span></span><br />
<span data-ttu-id="0d9de-121">[<strong>IWbemServices :: ExecMethodAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span><span class="sxs-lookup"><span data-stu-id="0d9de-121">[<strong>IWbemServices::ExecMethodAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0d9de-122"><a href="describing-a-class-object-path.md">Classe</a> ou <a href="describing-an-instance-object-path.md">instance</a></span><span class="sxs-lookup"><span data-stu-id="0d9de-122"><a href="describing-a-class-object-path.md">Class</a> or <a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="0d9de-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices :: GetObject</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-123"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobject"><strong>IWbemServices::GetObject</strong></a></span></span><br />
<span data-ttu-id="0d9de-124">[<strong>IWbemServices :: GetObjectAsync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span><span class="sxs-lookup"><span data-stu-id="0d9de-124">[<strong>IWbemServices::GetObjectAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d9de-125"><a href="describing-an-instance-object-path.md">Instance</a></span><span class="sxs-lookup"><span data-stu-id="0d9de-125"><a href="describing-an-instance-object-path.md">Instance</a></span></span></td>
<td><dl><span data-ttu-id="0d9de-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices ::D eleteInstance</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-126"><a href="/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance"><strong>IWbemServices::DeleteInstance</strong></a></span></span><br />
<span data-ttu-id="0d9de-127">[<strong>IWbemServices ::D eleteinstanceasync</strong>] (/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span><span class="sxs-lookup"><span data-stu-id="0d9de-127">[<strong>IWbemServices::DeleteInstanceAsync</strong>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

## <a name="script"></a><span data-ttu-id="0d9de-128">Script</span><span class="sxs-lookup"><span data-stu-id="0d9de-128">Script</span></span>

<span data-ttu-id="0d9de-129">Les chemins d’accès aux objets peuvent être créés de plusieurs façons :</span><span class="sxs-lookup"><span data-stu-id="0d9de-129">Object paths can be constructed in several ways:</span></span>

-   <span data-ttu-id="0d9de-130">Récupérez la propriété d’une méthode qui retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9de-130">Retrieve the property of a method that returns an [**SWbemObjectPath**](swbemobjectpath.md) object.</span></span>
-   <span data-ttu-id="0d9de-131">Récupérez la propriété [**SWbemObject \_ . Path**](swbemobject-path-.md) .</span><span class="sxs-lookup"><span data-stu-id="0d9de-131">Retrieve the [**SWbemObject.Path\_**](swbemobject-path-.md) property.</span></span>
-   <span data-ttu-id="0d9de-132">Créez une variable de chaîne qui contient le chemin d’accès de l’objet.</span><span class="sxs-lookup"><span data-stu-id="0d9de-132">Create a string variable that contains the object path.</span></span>

<span data-ttu-id="0d9de-133">Le tableau suivant répertorie les objets de script qui requièrent des chemins d’accès aux objets.</span><span class="sxs-lookup"><span data-stu-id="0d9de-133">The following table lists the scripting objects that require object paths.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d9de-134">Objet de script</span><span class="sxs-lookup"><span data-stu-id="0d9de-134">Scripting object</span></span></th>
<th><span data-ttu-id="0d9de-135">Méthode</span><span class="sxs-lookup"><span data-stu-id="0d9de-135">Method</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d9de-136"><a href="swbemservices.md"><strong>M</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-136"><a href="swbemservices.md"><strong>SWbemServices</strong></a></span></span></td>
<td><dl><span data-ttu-id="0d9de-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-137"><a href="swbemservices-associatorsof.md"><strong>AssociatorsOf</strong></a></span></span><br />
<span data-ttu-id="0d9de-138">[<strong>AssociatorsOfAsync</strong>] (swbemservices-associatorsofasync.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-138">[<strong>AssociatorsOfAsync</strong>](swbemservices-associatorsofasync.md)</span></span><br />
<span data-ttu-id="0d9de-139">[<strong>Supprimer</strong>] (swbemservices-delete.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-139">[<strong>Delete</strong>](swbemservices-delete.md)</span></span><br />
<span data-ttu-id="0d9de-140">[<strong>DeleteAsync</strong>] (swbemservices-deleteasync.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-140">[<strong>DeleteAsync</strong>](swbemservices-deleteasync.md)</span></span><br />
<span data-ttu-id="0d9de-141">[<strong>ExecMethod</strong>] (swbemservices-execmethod.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-141">[<strong>ExecMethod</strong>](swbemservices-execmethod.md)</span></span><br />
<span data-ttu-id="0d9de-142">[<strong>ExecMethodAsync</strong>] (swbemservices-execmethodasync.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-142">[<strong>ExecMethodAsync</strong>](swbemservices-execmethodasync.md)</span></span><br />
<span data-ttu-id="0d9de-143">[<strong>Obtient</strong>] (swbemservices-get.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-143">[<strong>Get</strong>](swbemservices-get.md)</span></span><br />
<span data-ttu-id="0d9de-144">[<strong>GetAsync</strong>] (swbemservices-getasync.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-144">[<strong>GetAsync</strong>](swbemservices-getasync.md)</span></span><br />
<span data-ttu-id="0d9de-145">[<strong>ReferencesTo</strong>] (swbemservices-referencesto.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-145">[<strong>ReferencesTo</strong>](swbemservices-referencesto.md)</span></span><br />
<span data-ttu-id="0d9de-146">[<strong>ReferencesToAsync</strong>] (swbemservices-referencestoasync.md)</span><span class="sxs-lookup"><span data-stu-id="0d9de-146">[<strong>ReferencesToAsync</strong>](swbemservices-referencestoasync.md)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d9de-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-147"><a href="swbemobjectset.md"><strong>SWbemObjectSet</strong></a></span></span></td>
<td><dl><span data-ttu-id="0d9de-148"><a href="swbemobjectset-item.md"><strong>Élément</strong></a></span><span class="sxs-lookup"><span data-stu-id="0d9de-148"><a href="swbemobjectset-item.md"><strong>Item</strong></a></span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

 

 
