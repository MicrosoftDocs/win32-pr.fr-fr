---
description: En savoir plus sur les méthodes de session
title: Méthodes de session
TOCTitle: Session methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Session
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.session_methods(v=EXCHG.10)
ms:contentKeyID: 55104007
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 11f8b31d8c74e3074788b60f62677e9e81135ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753204"
---
# <a name="session-methods"></a><span data-ttu-id="31f5f-103">Méthodes de session</span><span class="sxs-lookup"><span data-stu-id="31f5f-103">Session methods</span></span>

<span data-ttu-id="31f5f-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="31f5f-104">Include protected members</span></span>  
<span data-ttu-id="31f5f-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="31f5f-105">Include inherited members</span></span>  

<span data-ttu-id="31f5f-106">Le type de [session](./session-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="31f5f-106">The [Session](./session-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="31f5f-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="31f5f-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="31f5f-108">Nom</span><span class="sxs-lookup"><span data-stu-id="31f5f-108">Name</span></span></th>
<th><span data-ttu-id="31f5f-109">Description</span><span class="sxs-lookup"><span data-stu-id="31f5f-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-111"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="31f5f-112">Lève une exception si cet objet a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="31f5f-112">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="31f5f-113">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-113">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-115"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-115"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="31f5f-116">Supprimez cet objet, en libérant la ressource esent sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="31f5f-116">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="31f5f-117">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-119"><a href="dn350543(v=exchg.10).md">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-119"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="31f5f-120">Appelée par dispose et le finaliseur.</span><span class="sxs-lookup"><span data-stu-id="31f5f-120">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="31f5f-121">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-121">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-123"><a href="dn351128(v=exchg.10).md">Effet</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-123"><a href="dn351128(v=exchg.10).md">End</a></span></span></td>
<td><span data-ttu-id="31f5f-124">Mettez fin à la session.</span><span class="sxs-lookup"><span data-stu-id="31f5f-124">Terminate the session.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-126"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="31f5f-127">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-127">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-129"><a href="dn350552(v=exchg.10).md">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-129"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="31f5f-130">Finalise une instance de la classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="31f5f-130">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="31f5f-131">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-131">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-133"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="31f5f-134">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-134">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-136"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="31f5f-137">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-137">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-139"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="31f5f-140">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-140">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-142"><a href="dn351165(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-142"><a href="dn351165(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="31f5f-143">Libérez le JET_SESID sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="31f5f-143">Free the underlying JET_SESID.</span></span> <span data-ttu-id="31f5f-144">(Substitue <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-144">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-146"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="31f5f-147">Appelée par une sous-classe lorsqu’une ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="31f5f-147">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="31f5f-148">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-148">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="31f5f-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-150"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="31f5f-151">Appelée par une sous-classe lorsqu’une ressource est libérée.</span><span class="sxs-lookup"><span data-stu-id="31f5f-151">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="31f5f-152">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-152">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="31f5f-154"><a href="dn351129(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="31f5f-154"><a href="dn351129(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="31f5f-155">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente la <a href="dn351164(v=exchg.10).md">session</a>active.</span><span class="sxs-lookup"><span data-stu-id="31f5f-155">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351164(v=exchg.10).md">Session</a>.</span></span> <span data-ttu-id="31f5f-156">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="31f5f-156">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="31f5f-157">Haut</span><span class="sxs-lookup"><span data-stu-id="31f5f-157">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="31f5f-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31f5f-158">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31f5f-159">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="31f5f-159">Reference</span></span>

<span data-ttu-id="31f5f-160">[Session class](./session-class.md) (Classe Session)</span><span class="sxs-lookup"><span data-stu-id="31f5f-160">[Session class](./session-class.md)</span></span>

[<span data-ttu-id="31f5f-161">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="31f5f-161">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
