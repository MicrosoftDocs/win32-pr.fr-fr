---
description: 'En savoir plus sur les membres suivants : JET_INDEXCREATE'
title: Membres JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_members(v=EXCHG.10)
ms:contentKeyID: 55103641
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: cbe9ce962221db30c8cdae90461fa55fc0baea19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210109"
---
# <a name="jet_indexcreate-members"></a><span data-ttu-id="ab5e3-103">Membres JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="ab5e3-103">JET_INDEXCREATE members</span></span>

<span data-ttu-id="ab5e3-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="ab5e3-104">Include protected members</span></span>  
<span data-ttu-id="ab5e3-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="ab5e3-105">Include inherited members</span></span>  

<span data-ttu-id="ab5e3-106">Contient les informations nécessaires à la création d’un index sur des données dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-106">Contains the information needed to create an index over data in an ESE database.</span></span> <span data-ttu-id="ab5e3-107">Contient les informations nécessaires à la création d’un index sur des données dans une base de données ESE.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-107">Contains the information needed to create an index over data in an ESE database.</span></span>

<span data-ttu-id="ab5e3-108">Le type de [JET_INDEXCREATE](./jet-indexcreate-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-108">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="ab5e3-109">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="ab5e3-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ab5e3-110">Nom</span><span class="sxs-lookup"><span data-stu-id="ab5e3-110">Name</span></span></th>
<th><span data-ttu-id="ab5e3-111">Description</span><span class="sxs-lookup"><span data-stu-id="ab5e3-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-113"><a href="dn335115(v=exchg.10).md">JET_INDEXCREATE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab5e3-114">Haut</span><span class="sxs-lookup"><span data-stu-id="ab5e3-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="ab5e3-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ab5e3-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ab5e3-116">Nom</span><span class="sxs-lookup"><span data-stu-id="ab5e3-116">Name</span></span></th>
<th><span data-ttu-id="ab5e3-117">Description</span><span class="sxs-lookup"><span data-stu-id="ab5e3-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-119"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="ab5e3-120">Obtient ou définit la longueur, en caractères, de szKey, y compris les deux valeurs null de fin.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-120">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-122"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="ab5e3-123">Obtient ou définit la taille maximale autorisée, en octets, pour les clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-123">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="ab5e3-124">La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255) qui est la taille de clé maximale héritée.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-124">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="ab5e3-125">La taille de clé maximale dépend de la taille de page de la base de données <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-125">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="ab5e3-126">La <a href="dn351156(v=exchg.10).md">taille de clé</a>maximale peut être récupérée avec.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-126">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="ab5e3-127">Ce paramètre est ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-127">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="ab5e3-128">Contrairement à l’API non managée, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) n’est pas nécessaire, elle est ajoutée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-128">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-130"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="ab5e3-131">Obtient ou définit la longueur maximale, en octets, de chaque colonne à stocker dans l’index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-131">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-133"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="ab5e3-134">Obtient ou définit le nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-134">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-136"><a href="dn335157(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-136"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="ab5e3-137">Obtient ou définit le code d’erreur de la création de cet index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-137">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-139"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-139"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="ab5e3-140">Obtient ou définit les options de création d’index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-140">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-142"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="ab5e3-143">Obtient ou définit les options de comparaison Unicode facultatives.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-143">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-145"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="ab5e3-146">Obtient ou définit les indicateurs d’allocation, de maintenance et d’utilisation de l’espace.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-146">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-148"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="ab5e3-149">Obtient ou définit les colonnes conditionnelles facultatives.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-149">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-151"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="ab5e3-152">Obtient ou définit le nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-152">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-154"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-154"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="ab5e3-155">Obtient ou définit la description de la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-155">Gets or sets the description of the index key.</span></span> <span data-ttu-id="ab5e3-156">Il s’agit d’une chaîne double qui se termine par un caractère null des jetons délimités par des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-156">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="ab5e3-157">Chaque jeton se présente sous la forme [direction-specifier] [Column-Name], où direction-Specification a la valeur &quot; + &quot; ou &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="ab5e3-157">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="ab5e3-158">par exemple, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexera les trois colonnes &quot; ABC &quot; (dans l’ordre croissant), &quot; Def &quot; (dans l’ordre décroissant) et &quot; GHI &quot; (dans l’ordre croissant).</span><span class="sxs-lookup"><span data-stu-id="ab5e3-158">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="ab5e3-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-160"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="ab5e3-161">Obtient ou définit la densité de l’index.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-161">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab5e3-162">Haut</span><span class="sxs-lookup"><span data-stu-id="ab5e3-162">Top</span></span>

## <a name="methods"></a><span data-ttu-id="ab5e3-163">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ab5e3-163">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="ab5e3-164">Nom</span><span class="sxs-lookup"><span data-stu-id="ab5e3-164">Name</span></span></th>
<th><span data-ttu-id="ab5e3-165">Description</span><span class="sxs-lookup"><span data-stu-id="ab5e3-165">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-167"><a href="dn335116(v=exchg.10).md">ContentEquals</a></span></span></td>
<td><span data-ttu-id="ab5e3-168">Retourne une valeur indiquant si cette instance est égale à une autre instance.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-168">Returns a value indicating whether this instance is equal to another instance.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-170"><a href="dn335153(v=exchg.10).md">DeepClone</a></span></span></td>
<td><span data-ttu-id="ab5e3-171">Retourne une copie complète de l’objet.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-171">Returns a deep copy of the object.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-173"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="ab5e3-174">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-174">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="ab5e3-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-176"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="ab5e3-177">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-177">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-179"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="ab5e3-180">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-180">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-182"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="ab5e3-183">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-183">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="ab5e3-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-185"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="ab5e3-186">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-186">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="ab5e3-188"><a href="dn335154(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="ab5e3-188"><a href="dn335154(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="ab5e3-189">Génère une représentation sous forme de chaîne de l’instance.</span><span class="sxs-lookup"><span data-stu-id="ab5e3-189">Generate a string representation of the instance.</span></span> <span data-ttu-id="ab5e3-190">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="ab5e3-190">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ab5e3-191">Haut</span><span class="sxs-lookup"><span data-stu-id="ab5e3-191">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="ab5e3-192">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab5e3-192">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="ab5e3-193">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="ab5e3-193">Reference</span></span>

[<span data-ttu-id="ab5e3-194">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="ab5e3-194">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="ab5e3-195">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="ab5e3-195">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
