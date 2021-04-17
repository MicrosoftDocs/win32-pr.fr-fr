---
description: En savoir plus sur les méthodes de transaction
title: Méthodes de transaction
TOCTitle: Transaction methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_methods(v=EXCHG.10)
ms:contentKeyID: 55104163
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c926d00f785aab3a63cd8ebc7eebaf74ea5f0e23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104558624"
---
# <a name="transaction-methods"></a><span data-ttu-id="67940-103">Méthodes de transaction</span><span class="sxs-lookup"><span data-stu-id="67940-103">Transaction methods</span></span>

<span data-ttu-id="67940-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="67940-104">Include protected members</span></span>  
<span data-ttu-id="67940-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="67940-105">Include inherited members</span></span>  

<span data-ttu-id="67940-106">Le type de [transaction](./transaction-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="67940-106">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="methods"></a><span data-ttu-id="67940-107">Méthodes</span><span class="sxs-lookup"><span data-stu-id="67940-107">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="67940-108">Nom</span><span class="sxs-lookup"><span data-stu-id="67940-108">Name</span></span></th>
<th><span data-ttu-id="67940-109">Description</span><span class="sxs-lookup"><span data-stu-id="67940-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-111"><a href="dn351172(v=exchg.10).md">Début</a></span><span class="sxs-lookup"><span data-stu-id="67940-111"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="67940-112">Commencer une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-112">Begin a transaction.</span></span> <span data-ttu-id="67940-113">Cet objet ne doit pas être actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-113">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="67940-115"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="67940-116">Lève une exception si cet objet a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="67940-116">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="67940-117">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-117">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-119"><a href="dn351179(v=exchg.10).md">Valider (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="67940-119"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="67940-120">Valider une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-120">Commit a transaction.</span></span> <span data-ttu-id="67940-121">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-121">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-123"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="67940-123"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="67940-124">Valider une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-124">Commit a transaction.</span></span> <span data-ttu-id="67940-125">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-125">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-127"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="67940-127"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="67940-128">Supprimez cet objet, en libérant la ressource esent sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="67940-128">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="67940-129">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-129">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-131"><a href="dn350543(v=exchg.10).md">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="67940-131"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="67940-132">Appelée par dispose et le finaliseur.</span><span class="sxs-lookup"><span data-stu-id="67940-132">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="67940-133">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-133">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="67940-135"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="67940-136">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-136">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-138"><a href="dn350552(v=exchg.10).md">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="67940-138"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="67940-139">Finalise une instance de la classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="67940-139">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="67940-140">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-140">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="67940-142"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="67940-143">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-143">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="67940-145"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="67940-146">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-146">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="67940-148"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="67940-149">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-149">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="67940-151"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="67940-152">Appelé lorsque la transaction est supprimée pendant qu’elle est active.</span><span class="sxs-lookup"><span data-stu-id="67940-152">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="67940-153">La transaction doit être restaurée.</span><span class="sxs-lookup"><span data-stu-id="67940-153">This should rollback the transaction.</span></span> <span data-ttu-id="67940-154">(Substitue <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-154">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="67940-156"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="67940-157">Appelée par une sous-classe lorsqu’une ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="67940-157">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="67940-158">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-158">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="67940-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="67940-160"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="67940-161">Appelée par une sous-classe lorsqu’une ressource est libérée.</span><span class="sxs-lookup"><span data-stu-id="67940-161">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="67940-162">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-162">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-164"><a href="dn351244(v=exchg.10).md">Restauration</a></span><span class="sxs-lookup"><span data-stu-id="67940-164"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="67940-165">Restaure une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-165">Rollback a transaction.</span></span> <span data-ttu-id="67940-166">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="67940-166">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="67940-168"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="67940-168"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="67940-169">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente la <a href="dn351174(v=exchg.10).md">transaction</a>en cours.</span><span class="sxs-lookup"><span data-stu-id="67940-169">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="67940-170">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="67940-170">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="67940-171">Haut</span><span class="sxs-lookup"><span data-stu-id="67940-171">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="67940-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67940-172">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="67940-173">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="67940-173">Reference</span></span>

[<span data-ttu-id="67940-174">classe de transaction</span><span class="sxs-lookup"><span data-stu-id="67940-174">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="67940-175">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="67940-175">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
