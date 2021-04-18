---
description: 'En savoir plus sur : les membres de transaction'
title: Membres de transaction
TOCTitle: Transaction members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Transaction
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.transaction_members(v=EXCHG.10)
ms:contentKeyID: 55104159
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4a11aba5d3ffdc8a0e02bd166aa0a433d4860af5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563442"
---
# <a name="transaction-members"></a><span data-ttu-id="273f0-103">Membres de transaction</span><span class="sxs-lookup"><span data-stu-id="273f0-103">Transaction members</span></span>

<span data-ttu-id="273f0-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="273f0-104">Include protected members</span></span>  
<span data-ttu-id="273f0-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="273f0-105">Include inherited members</span></span>  

<span data-ttu-id="273f0-106">Classe qui encapsule une transaction sur un JET_SESID.</span><span class="sxs-lookup"><span data-stu-id="273f0-106">A class that encapsulates a transaction on a JET_SESID.</span></span>

<span data-ttu-id="273f0-107">Le type de [transaction](./transaction-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="273f0-107">The [Transaction](./transaction-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="273f0-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="273f0-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="273f0-109">Nom</span><span class="sxs-lookup"><span data-stu-id="273f0-109">Name</span></span></th>
<th><span data-ttu-id="273f0-110">Description</span><span class="sxs-lookup"><span data-stu-id="273f0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span><span class="sxs-lookup"><span data-stu-id="273f0-112"><a href="dn351177(v=exchg.10).md">Transaction</a></span></span></td>
<td><span data-ttu-id="273f0-113">Initialise une nouvelle instance de la classe transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-113">Initializes a new instance of the Transaction class.</span></span> <span data-ttu-id="273f0-114">Une transaction est alors automatiquement lancée.</span><span class="sxs-lookup"><span data-stu-id="273f0-114">This automatically begins a transaction.</span></span> <span data-ttu-id="273f0-115">La transaction sera restaurée si elle n’est pas explicitement validée.</span><span class="sxs-lookup"><span data-stu-id="273f0-115">The transaction will be rolled back if not explicitly committed.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="273f0-116">Haut</span><span class="sxs-lookup"><span data-stu-id="273f0-116">Top</span></span>

## <a name="properties"></a><span data-ttu-id="273f0-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="273f0-117">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="273f0-118">Nom</span><span class="sxs-lookup"><span data-stu-id="273f0-118">Name</span></span></th>
<th><span data-ttu-id="273f0-119">Description</span><span class="sxs-lookup"><span data-stu-id="273f0-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Propriété protégée" alt="Protected property" /></td>
<td><span data-ttu-id="273f0-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span><span class="sxs-lookup"><span data-stu-id="273f0-121"><a href="dn350578(v=exchg.10).md">HasResource</a></span></span></td>
<td><span data-ttu-id="273f0-122">Obtient une valeur indiquant si la ressource sous-jacente est actuellement allouée.</span><span class="sxs-lookup"><span data-stu-id="273f0-122">Gets a value indicating whether the underlying resource is currently allocated.</span></span> <span data-ttu-id="273f0-123">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-123">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="273f0-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span><span class="sxs-lookup"><span data-stu-id="273f0-125"><a href="dn351180(v=exchg.10).md">IsInTransaction</a></span></span></td>
<td><span data-ttu-id="273f0-126">Obtient une valeur indiquant si cet objet est actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-126">Gets a value indicating whether this object is currently in a transaction.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="273f0-127">Haut</span><span class="sxs-lookup"><span data-stu-id="273f0-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="273f0-128">Méthodes</span><span class="sxs-lookup"><span data-stu-id="273f0-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="273f0-129">Nom</span><span class="sxs-lookup"><span data-stu-id="273f0-129">Name</span></span></th>
<th><span data-ttu-id="273f0-130">Description</span><span class="sxs-lookup"><span data-stu-id="273f0-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-132"><a href="dn351172(v=exchg.10).md">Début</a></span><span class="sxs-lookup"><span data-stu-id="273f0-132"><a href="dn351172(v=exchg.10).md">Begin</a></span></span></td>
<td><span data-ttu-id="273f0-133">Commencer une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-133">Begin a transaction.</span></span> <span data-ttu-id="273f0-134">Cet objet ne doit pas être actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-134">This object should not currently be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span><span class="sxs-lookup"><span data-stu-id="273f0-136"><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></span></span></td>
<td><span data-ttu-id="273f0-137">Lève une exception si cet objet a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="273f0-137">Throw an exception if this object has been disposed.</span></span> <span data-ttu-id="273f0-138">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-138">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-140"><a href="dn351179(v=exchg.10).md">Valider (CommitTransactionGrbit)</a></span><span class="sxs-lookup"><span data-stu-id="273f0-140"><a href="dn351179(v=exchg.10).md">Commit(CommitTransactionGrbit)</a></span></span></td>
<td><span data-ttu-id="273f0-141">Valider une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-141">Commit a transaction.</span></span> <span data-ttu-id="273f0-142">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-142">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-144"><a href="dn351243(v=exchg.10).md">Commit (CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span><span class="sxs-lookup"><span data-stu-id="273f0-144"><a href="dn351243(v=exchg.10).md">Commit(CommitTransactionGrbit, TimeSpan, JET_COMMIT_ID)</a></span></span></td>
<td><span data-ttu-id="273f0-145">Valider une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-145">Commit a transaction.</span></span> <span data-ttu-id="273f0-146">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-146">This object should be in a transaction.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-148"><a href="dn350553(v=exchg.10).md">Dispose ()</a></span><span class="sxs-lookup"><span data-stu-id="273f0-148"><a href="dn350553(v=exchg.10).md">Dispose()</a></span></span></td>
<td><span data-ttu-id="273f0-149">Supprimez cet objet, en libérant la ressource esent sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="273f0-149">Dispose of this object, releasing the underlying Esent resource.</span></span> <span data-ttu-id="273f0-150">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-150">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-152"><a href="dn350543(v=exchg.10).md">Dispose (booléen)</a></span><span class="sxs-lookup"><span data-stu-id="273f0-152"><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></span></span></td>
<td><span data-ttu-id="273f0-153">Appelée par dispose et le finaliseur.</span><span class="sxs-lookup"><span data-stu-id="273f0-153">Called by Dispose and the finalizer.</span></span> <span data-ttu-id="273f0-154">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-154">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="273f0-156"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="273f0-157">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-157">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-159"><a href="dn350552(v=exchg.10).md">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="273f0-159"><a href="dn350552(v=exchg.10).md">Finalize</a></span></span></td>
<td><span data-ttu-id="273f0-160">Finalise une instance de la classe EsentResource.</span><span class="sxs-lookup"><span data-stu-id="273f0-160">Finalizes an instance of the EsentResource class.</span></span> <span data-ttu-id="273f0-161">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-161">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="273f0-163"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="273f0-164">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="273f0-166"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="273f0-167">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="273f0-169"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="273f0-170">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span><span class="sxs-lookup"><span data-stu-id="273f0-172"><a href="dn351176(v=exchg.10).md">ReleaseResource</a></span></span></td>
<td><span data-ttu-id="273f0-173">Appelé lorsque la transaction est supprimée pendant qu’elle est active.</span><span class="sxs-lookup"><span data-stu-id="273f0-173">Called when the transaction is being disposed while active.</span></span> <span data-ttu-id="273f0-174">La transaction doit être restaurée.</span><span class="sxs-lookup"><span data-stu-id="273f0-174">This should rollback the transaction.</span></span> <span data-ttu-id="273f0-175">(Substitue <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-175">(Overrides <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span><span class="sxs-lookup"><span data-stu-id="273f0-177"><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></span></span></td>
<td><span data-ttu-id="273f0-178">Appelée par une sous-classe lorsqu’une ressource est allouée.</span><span class="sxs-lookup"><span data-stu-id="273f0-178">Called by a subclass when a resource is allocated.</span></span> <span data-ttu-id="273f0-179">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-179">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="273f0-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span><span class="sxs-lookup"><span data-stu-id="273f0-181"><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></span></span></td>
<td><span data-ttu-id="273f0-182">Appelée par une sous-classe lorsqu’une ressource est libérée.</span><span class="sxs-lookup"><span data-stu-id="273f0-182">Called by a subclass when a resource is freed.</span></span> <span data-ttu-id="273f0-183">(Héritée de <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-183">(Inherited from <a href="dn319890(v=exchg.10).md">EsentResource</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-185"><a href="dn351244(v=exchg.10).md">Restauration</a></span><span class="sxs-lookup"><span data-stu-id="273f0-185"><a href="dn351244(v=exchg.10).md">Rollback</a></span></span></td>
<td><span data-ttu-id="273f0-186">Restaure une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-186">Rollback a transaction.</span></span> <span data-ttu-id="273f0-187">Cet objet doit être dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="273f0-187">This object should be in a transaction.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="273f0-189"><a href="dn351181(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="273f0-189"><a href="dn351181(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="273f0-190">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente la <a href="dn351174(v=exchg.10).md">transaction</a>en cours.</span><span class="sxs-lookup"><span data-stu-id="273f0-190">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351174(v=exchg.10).md">Transaction</a>.</span></span> <span data-ttu-id="273f0-191">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="273f0-191">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="273f0-192">Haut</span><span class="sxs-lookup"><span data-stu-id="273f0-192">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="273f0-193">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="273f0-193">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="273f0-194">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="273f0-194">Reference</span></span>

[<span data-ttu-id="273f0-195">classe de transaction</span><span class="sxs-lookup"><span data-stu-id="273f0-195">Transaction class</span></span>](./transaction-class.md)

[<span data-ttu-id="273f0-196">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="273f0-196">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
