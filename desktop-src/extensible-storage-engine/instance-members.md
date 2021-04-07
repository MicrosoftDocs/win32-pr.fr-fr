---
description: 'En savoir plus sur : membres d’instance'
title: Membres d’instance
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 8ba8dad079feba566dbb8fca873fcea19af778ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863201"
---
# <a name="instance-members"></a><span data-ttu-id="d45ad-103">Membres d’instance</span><span class="sxs-lookup"><span data-stu-id="d45ad-103">Instance members</span></span>

<span data-ttu-id="d45ad-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="d45ad-104">Include protected members</span></span>  
<span data-ttu-id="d45ad-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="d45ad-105">Include inherited members</span></span>  

<span data-ttu-id="d45ad-106">Classe qui encapsule un [JET_INSTANCE](./jet-instance-structure.md) dans un objet jetable.</span><span class="sxs-lookup"><span data-stu-id="d45ad-106">A class that encapsulates a [JET_INSTANCE](./jet-instance-structure.md) in a disposable object.</span></span> <span data-ttu-id="d45ad-107">L’instance doit être fermée en dernier et la fermeture de l’instance libère toutes les autres ressources pour l’instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-107">The instance must be closed last and closing the instance releases all other resources for the instance.</span></span>

<span data-ttu-id="d45ad-108">Le type d' [instance](./instance-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="d45ad-108">The [Instance](./instance-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="d45ad-109">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="d45ad-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d45ad-110">Nom</span><span class="sxs-lookup"><span data-stu-id="d45ad-110">Name</span></span></th>
<th><span data-ttu-id="d45ad-111">Description</span><span class="sxs-lookup"><span data-stu-id="d45ad-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-113"><a href="dn350924(v=exchg.10).md">Instance (String)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-113"><a href="dn350924(v=exchg.10).md">Instance(String)</a></span></span></td>
<td><span data-ttu-id="d45ad-114">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-114">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="d45ad-115">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="d45ad-115">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-117"><a href="dn350927(v=exchg.10).md">Instance (String, String)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-117"><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></span></span></td>
<td><span data-ttu-id="d45ad-118">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-118">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="d45ad-119">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="d45ad-119">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-121"><a href="dn350948(v=exchg.10).md">Instance (String, String, TermGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-121"><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></span></span></td>
<td><span data-ttu-id="d45ad-122">Initialise une nouvelle instance de la classe d’instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-122">Initializes a new instance of the Instance class.</span></span> <span data-ttu-id="d45ad-123">Le JET_INSTANCE sous-jacent est alloué, mais pas initialisé.</span><span class="sxs-lookup"><span data-stu-id="d45ad-123">The underlying JET_INSTANCE is allocated, but not initialized.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45ad-124">Haut</span><span class="sxs-lookup"><span data-stu-id="d45ad-124">Top</span></span>

## <a name="properties"></a><span data-ttu-id="d45ad-125">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d45ad-125">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d45ad-126">Nom</span><span class="sxs-lookup"><span data-stu-id="d45ad-126">Name</span></span></th>
<th><span data-ttu-id="d45ad-127">Description</span><span class="sxs-lookup"><span data-stu-id="d45ad-127">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="d45ad-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-129"><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></span></span></td>
<td><span data-ttu-id="d45ad-130">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-130">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="d45ad-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-132"><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></span></span></td>
<td><span data-ttu-id="d45ad-133">(Héritée de <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-133">(Inherited from <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="d45ad-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-135"><a href="dn350941(v=exchg.10).md">JetInstance</a></span></span></td>
<td><span data-ttu-id="d45ad-136">Obtient le JET_INSTANCE contenu dans cette instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-136">Gets the JET_INSTANCE that this instance contains.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="d45ad-138"><a href="dn350962(v=exchg.10).md">Paramètres</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-138"><a href="dn350962(v=exchg.10).md">Parameters</a></span></span></td>
<td><span data-ttu-id="d45ad-139">Obtient le InstanceParameters pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-139">Gets the InstanceParameters for this instance.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="d45ad-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-141"><a href="dn350964(v=exchg.10).md">TermGrbit</a></span></span></td>
<td><span data-ttu-id="d45ad-142">Obtient ou définit le TermGrbit pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-142">Gets or sets the TermGrbit for this instance.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45ad-143">Haut</span><span class="sxs-lookup"><span data-stu-id="d45ad-143">Top</span></span>

## <a name="methods"></a><span data-ttu-id="d45ad-144">Méthodes</span><span class="sxs-lookup"><span data-stu-id="d45ad-144">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d45ad-145">Nom</span><span class="sxs-lookup"><span data-stu-id="d45ad-145">Name</span></span></th>
<th><span data-ttu-id="d45ad-146">Description</span><span class="sxs-lookup"><span data-stu-id="d45ad-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Fermer</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-148"><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Close</a></span></span></td>
<td><span data-ttu-id="d45ad-149">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-149">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-151"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></span></span></td>
<td><span data-ttu-id="d45ad-152">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-152">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-154"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></span></span></td>
<td><span data-ttu-id="d45ad-155">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-155">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-157"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></span></span></td>
<td><span data-ttu-id="d45ad-158">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-158">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-160"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></span></span></td>
<td><span data-ttu-id="d45ad-161">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-161">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="d45ad-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-163"><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="d45ad-164">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-164">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-166"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="d45ad-167">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="d45ad-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-169"><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="d45ad-170">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-170">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-172"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="d45ad-173">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-175"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="d45ad-176">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-176">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-178"><a href="dn350932(v=exchg.10).md">Init ()</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-178"><a href="dn350932(v=exchg.10).md">Init()</a></span></span></td>
<td><span data-ttu-id="d45ad-179">Initialisez le JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="d45ad-179">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-181"><a href="dn350954(v=exchg.10).md">Init (InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-181"><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></span></span></td>
<td><span data-ttu-id="d45ad-182">Initialisez le JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="d45ad-182">Initialize the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-184"><a href="dn350934(v=exchg.10).md">Init (JET_RSTINFO, InitGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-184"><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></span></span></td>
<td><span data-ttu-id="d45ad-185">Initialisez le JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="d45ad-185">Initialize the JET_INSTANCE.</span></span> <span data-ttu-id="d45ad-186">Cette API nécessite au moins la version Vista d’ESENT.</span><span class="sxs-lookup"><span data-stu-id="d45ad-186">This API requires at least the Vista version of ESENT.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="d45ad-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-188"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="d45ad-189">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-189">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="d45ad-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-191"><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></span></span></td>
<td><span data-ttu-id="d45ad-192">Libère le handle pour cette instance.</span><span class="sxs-lookup"><span data-stu-id="d45ad-192">Release the handle for this instance.</span></span> <span data-ttu-id="d45ad-193">(Substitue <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle. ReleaseHandle ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-193">(Overrides <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="d45ad-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-195"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></span></span></td>
<td><span data-ttu-id="d45ad-196">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-196">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-198"><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></span></span></td>
<td><span data-ttu-id="d45ad-199">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-199">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-201"><a href="dn350935(v=exchg.10).md">Terme</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-201"><a href="dn350935(v=exchg.10).md">Term</a></span></span></td>
<td><span data-ttu-id="d45ad-202">Terminez le JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="d45ad-202">Terminate the JET_INSTANCE.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="d45ad-204"><a href="dn350960(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-204"><a href="dn350960(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="d45ad-205">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente l' <a href="dn350923(v=exchg.10).md">instance</a>actuelle.</span><span class="sxs-lookup"><span data-stu-id="d45ad-205">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn350923(v=exchg.10).md">Instance</a>.</span></span> <span data-ttu-id="d45ad-206">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-206">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45ad-207">Haut</span><span class="sxs-lookup"><span data-stu-id="d45ad-207">Top</span></span>

## <a name="operators"></a><span data-ttu-id="d45ad-208">Opérateurs</span><span class="sxs-lookup"><span data-stu-id="d45ad-208">Operators</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d45ad-209">Nom</span><span class="sxs-lookup"><span data-stu-id="d45ad-209">Name</span></span></th>
<th><span data-ttu-id="d45ad-210">Description</span><span class="sxs-lookup"><span data-stu-id="d45ad-210">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Opérateur public" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="d45ad-213"><a href="dn350950(v=exchg.10).md">Implicite (instance to JET_INSTANCE)</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-213"><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></span></span></td>
<td><span data-ttu-id="d45ad-214">Fournir la conversion implicite d’un objet d’instance en une structure JET_INSTANCE.</span><span class="sxs-lookup"><span data-stu-id="d45ad-214">Provide implicit conversion of an Instance object to a JET_INSTANCE structure.</span></span> <span data-ttu-id="d45ad-215">Cette opération est effectuée afin qu’une instance puisse être utilisée partout où une JET_INSTANCE est requise.</span><span class="sxs-lookup"><span data-stu-id="d45ad-215">This is done so that an Instance can be used anywhere a JET_INSTANCE is required.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45ad-216">Haut</span><span class="sxs-lookup"><span data-stu-id="d45ad-216">Top</span></span>

## <a name="fields"></a><span data-ttu-id="d45ad-217">Champs</span><span class="sxs-lookup"><span data-stu-id="d45ad-217">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="d45ad-218">Nom</span><span class="sxs-lookup"><span data-stu-id="d45ad-218">Name</span></span></th>
<th><span data-ttu-id="d45ad-219">Description</span><span class="sxs-lookup"><span data-stu-id="d45ad-219">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Champ protégé" alt="Protected field" /></td>
<td><span data-ttu-id="d45ad-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">traitée</a></span><span class="sxs-lookup"><span data-stu-id="d45ad-221"><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></span></span></td>
<td><span data-ttu-id="d45ad-222">(Hérité de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span><span class="sxs-lookup"><span data-stu-id="d45ad-222">(Inherited from <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="d45ad-223">Haut</span><span class="sxs-lookup"><span data-stu-id="d45ad-223">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="d45ad-224">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d45ad-224">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d45ad-225">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="d45ad-225">Reference</span></span>

[<span data-ttu-id="d45ad-226">Classe d’instance</span><span class="sxs-lookup"><span data-stu-id="d45ad-226">Instance class</span></span>](./instance-class.md)

[<span data-ttu-id="d45ad-227">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="d45ad-227">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
