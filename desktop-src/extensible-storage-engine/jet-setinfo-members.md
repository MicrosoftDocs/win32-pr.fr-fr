---
description: 'En savoir plus sur les membres suivants : JET_SETINFO'
title: Membres JET_SETINFO
TOCTitle: JET_SETINFO members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_members(v=EXCHG.10)
ms:contentKeyID: 55103871
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: c782eace916b3871ade67870b08e1766faeafd28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750492"
---
# <a name="jet_setinfo-members"></a><span data-ttu-id="6e4bf-103">Membres JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6e4bf-103">JET_SETINFO members</span></span>

<span data-ttu-id="6e4bf-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="6e4bf-104">Include protected members</span></span>  
<span data-ttu-id="6e4bf-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="6e4bf-105">Include inherited members</span></span>  

<span data-ttu-id="6e4bf-106">Paramètres pour JetSetColumn.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-106">Settings for JetSetColumn.</span></span>

<span data-ttu-id="6e4bf-107">Le type de [JET_SETINFO](./jet-setinfo-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-107">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="6e4bf-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="6e4bf-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6e4bf-109">Nom</span><span class="sxs-lookup"><span data-stu-id="6e4bf-109">Name</span></span></th>
<th><span data-ttu-id="6e4bf-110">Description</span><span class="sxs-lookup"><span data-stu-id="6e4bf-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-112"><a href="dn351031(v=exchg.10).md">JET_SETINFO</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e4bf-113">Haut</span><span class="sxs-lookup"><span data-stu-id="6e4bf-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="6e4bf-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e4bf-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6e4bf-115">Nom</span><span class="sxs-lookup"><span data-stu-id="6e4bf-115">Name</span></span></th>
<th><span data-ttu-id="6e4bf-116">Description</span><span class="sxs-lookup"><span data-stu-id="6e4bf-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="6e4bf-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-118"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="6e4bf-119">Obtient ou définit offset pour le premier octet à définir dans une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-119">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="6e4bf-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-121"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="6e4bf-122">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-122">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="6e4bf-123">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-123">The array of values is one-based.</span></span> <span data-ttu-id="6e4bf-124">La première valeur est Sequence 1, et non 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="6e4bf-124">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="6e4bf-125">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme itagSequence si cette valeur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-125">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="6e4bf-126">La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-126">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e4bf-127">Haut</span><span class="sxs-lookup"><span data-stu-id="6e4bf-127">Top</span></span>

## <a name="methods"></a><span data-ttu-id="6e4bf-128">Méthodes</span><span class="sxs-lookup"><span data-stu-id="6e4bf-128">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="6e4bf-129">Nom</span><span class="sxs-lookup"><span data-stu-id="6e4bf-129">Name</span></span></th>
<th><span data-ttu-id="6e4bf-130">Description</span><span class="sxs-lookup"><span data-stu-id="6e4bf-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-132"><a href="dn351060(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="6e4bf-133">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-133">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-135"><a href="dn351032(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="6e4bf-136">Retourne une copie complète de l’objet.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-136">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-138"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="6e4bf-139">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-139">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="6e4bf-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-141"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="6e4bf-142">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-142">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-144"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="6e4bf-145">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-145">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-147"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="6e4bf-148">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-148">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="6e4bf-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-150"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="6e4bf-151">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-151">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="6e4bf-153"><a href="dn351062(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="6e4bf-153"><a href="dn351062(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="6e4bf-154">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="6e4bf-154">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351059(v=exchg.10).md">JET_SETINFO</a>.</span></span> <span data-ttu-id="6e4bf-155">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="6e4bf-155">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e4bf-156">Haut</span><span class="sxs-lookup"><span data-stu-id="6e4bf-156">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="6e4bf-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6e4bf-157">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6e4bf-158">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="6e4bf-158">Reference</span></span>

[<span data-ttu-id="6e4bf-159">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="6e4bf-159">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="6e4bf-160">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="6e4bf-160">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
