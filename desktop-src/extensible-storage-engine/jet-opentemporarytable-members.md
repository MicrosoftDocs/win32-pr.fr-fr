---
description: 'En savoir plus sur les membres suivants : JET_OPENTEMPORARYTABLE'
title: Membres JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af149ecba6858aca4b4877fc9446872386406838
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563376"
---
# <a name="jet_opentemporarytable-members"></a><span data-ttu-id="a0717-103">Membres JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="a0717-103">JET_OPENTEMPORARYTABLE members</span></span>

<span data-ttu-id="a0717-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="a0717-104">Include protected members</span></span>  
<span data-ttu-id="a0717-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="a0717-105">Include inherited members</span></span>  

<span data-ttu-id="a0717-106">Collection de paramètres pour la méthode JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="a0717-106">A collection of parameters for the JetOpenTemporaryTable method.</span></span>

<span data-ttu-id="a0717-107">Le type de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="a0717-107">The [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="a0717-108">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="a0717-108">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a0717-109">Nom</span><span class="sxs-lookup"><span data-stu-id="a0717-109">Name</span></span></th>
<th><span data-ttu-id="a0717-110">Description</span><span class="sxs-lookup"><span data-stu-id="a0717-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="a0717-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span><span class="sxs-lookup"><span data-stu-id="a0717-112"><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0717-113">Haut</span><span class="sxs-lookup"><span data-stu-id="a0717-113">Top</span></span>

## <a name="properties"></a><span data-ttu-id="a0717-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="a0717-114">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a0717-115">Nom</span><span class="sxs-lookup"><span data-stu-id="a0717-115">Name</span></span></th>
<th><span data-ttu-id="a0717-116">Description</span><span class="sxs-lookup"><span data-stu-id="a0717-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="a0717-118"><a href="dn335290(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="a0717-119">Obtient ou définit la taille maximale d’une clé représentant une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="a0717-119">Gets or sets the maximum size for a key representing a given row.</span></span> <span data-ttu-id="a0717-120">La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées.</span><span class="sxs-lookup"><span data-stu-id="a0717-120">The maximum key size may be set to control how keys are truncated.</span></span> <span data-ttu-id="a0717-121">La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes.</span><span class="sxs-lookup"><span data-stu-id="a0717-121">Key truncation is important because it can affect when rows are considered to be distinct.</span></span> <span data-ttu-id="a0717-122">Si ce paramètre a la valeur 0 ou 255, la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="a0717-122">If this parameter is set to 0 or 255 then the maximum key size and its semantics will remain identical to the maximum key size supported by Windows Server 2003.</span></span> <span data-ttu-id="a0717-123">Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données pour l’instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="a0717-123">This parameter may also be set to a larger value as a function of the database page size for the instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="a0717-124">Pour <a href="dn335292(v=exchg.10).md">plus</a> d’informations, consultez.</span><span class="sxs-lookup"><span data-stu-id="a0717-124">See <a href="dn335292(v=exchg.10).md">KeyMost</a> for more information.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="a0717-126"><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="a0717-127">Obtient ou définit la quantité maximale de données qui seront utilisées à partir de n’importe quelle variable lengthcolumn pour construire une clé pour une ligne donnée.</span><span class="sxs-lookup"><span data-stu-id="a0717-127">Gets or sets maximum amount of data that will be used from any variable lengthcolumn to construct a key for a given row.</span></span> <span data-ttu-id="a0717-128">Ce paramètre peut être utilisé pour contrôler la quantité d’espace clé consommée par une colonne clé donnée.</span><span class="sxs-lookup"><span data-stu-id="a0717-128">This parameter may be used to control the amount of key space consumed by any given key column.</span></span> <span data-ttu-id="a0717-129">Cette limite est en octets.</span><span class="sxs-lookup"><span data-stu-id="a0717-129">This limit is in bytes.</span></span> <span data-ttu-id="a0717-130">Si ce paramètre est égal à zéro ou est identique à la propriété <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , aucune limite n’est appliquée.</span><span class="sxs-lookup"><span data-stu-id="a0717-130">If this parameter is zero or is the same as the <a href="dn335290(v=exchg.10).md">cbKeyMost</a> property then no limit is in effect.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span><span class="sxs-lookup"><span data-stu-id="a0717-132"><a href="dn335287(v=exchg.10).md">ccolumn</a></span></span></td>
<td><span data-ttu-id="a0717-133">Obtient ou définit le nombre de colonnes dans <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="a0717-133">Gets or sets the number of columns in <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-135"><a href="dn351232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="a0717-135"><a href="dn351232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="a0717-136">Obtient ou définit les options de la table Temp.</span><span class="sxs-lookup"><span data-stu-id="a0717-136">Gets or sets options for the temp table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span><span class="sxs-lookup"><span data-stu-id="a0717-138"><a href="dn335288(v=exchg.10).md">pidxunicode</a></span></span></td>
<td><span data-ttu-id="a0717-139">Obtient ou définit les indicateurs de normalisation et l’ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0717-139">Gets or sets the locale ID and normalization flags to use to compare any Unicode key column data in the temporary table.</span></span> <span data-ttu-id="a0717-140">Lorsque ce paramètre a la valeur null, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0717-140">When this parameter is null, then the default LCID will be used to compare any Unicode key columns in the temporary table.</span></span> <span data-ttu-id="a0717-141">Le LCID par défaut est le paramètre régional anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="a0717-141">The default LCID is the U.S. English locale.</span></span> <span data-ttu-id="a0717-142">Lorsque ce paramètre a la valeur null, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0717-142">When this parameter is null, then the default normalization flags will be used to compare any Unicode key column data in the temp table.</span></span> <span data-ttu-id="a0717-143">Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="a0717-143">The default normalization flags are: NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span><span class="sxs-lookup"><span data-stu-id="a0717-145"><a href="dn351228(v=exchg.10).md">prgcolumndef</a></span></span></td>
<td><span data-ttu-id="a0717-146">Obtient ou définit les définitions de colonne pour les colonnes créées dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0717-146">Gets or sets the column definitions for the columns created in the temporary table.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span><span class="sxs-lookup"><span data-stu-id="a0717-148"><a href="dn351233(v=exchg.10).md">prgcolumnid</a></span></span></td>
<td><span data-ttu-id="a0717-149">Obtient ou définit la mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés pendant la création de la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="a0717-149">Gets or sets the output buffer that receives the array of column IDs generated during the creation of the temporary table.</span></span> <span data-ttu-id="a0717-150">Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne.</span><span class="sxs-lookup"><span data-stu-id="a0717-150">The column IDs in this array will exactly correspond to the input array of column definitions.</span></span> <span data-ttu-id="a0717-151">Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span><span class="sxs-lookup"><span data-stu-id="a0717-151">As a result, the size of this buffer must correspond to the size of <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="a0717-153"><a href="dn335293(v=exchg.10).md">TableID</a></span><span class="sxs-lookup"><span data-stu-id="a0717-153"><a href="dn335293(v=exchg.10).md">tableid</a></span></span></td>
<td><span data-ttu-id="a0717-154">Obtient le descripteur de table pour la table temporaire créée à la suite d’un appel réussi à JetOpenTemporaryTable.</span><span class="sxs-lookup"><span data-stu-id="a0717-154">Gets the table handle for the temporary table created as a result of a successful call to JetOpenTemporaryTable.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0717-155">Haut</span><span class="sxs-lookup"><span data-stu-id="a0717-155">Top</span></span>

## <a name="methods"></a><span data-ttu-id="a0717-156">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a0717-156">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="a0717-157">Nom</span><span class="sxs-lookup"><span data-stu-id="a0717-157">Name</span></span></th>
<th><span data-ttu-id="a0717-158">Description</span><span class="sxs-lookup"><span data-stu-id="a0717-158">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="a0717-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="a0717-160"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="a0717-161">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-161">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="a0717-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="a0717-163"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="a0717-164">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-164">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="a0717-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="a0717-166"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="a0717-167">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-167">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="a0717-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="a0717-169"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="a0717-170">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-170">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="a0717-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="a0717-172"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="a0717-173">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-173">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="a0717-175"><a href="dn335286(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="a0717-175"><a href="dn335286(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="a0717-176">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="a0717-176">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>.</span></span> <span data-ttu-id="a0717-177">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="a0717-177">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0717-178">Haut</span><span class="sxs-lookup"><span data-stu-id="a0717-178">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="a0717-179">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a0717-179">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a0717-180">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="a0717-180">Reference</span></span>

[<span data-ttu-id="a0717-181">Classe JET_OPENTEMPORARYTABLE</span><span class="sxs-lookup"><span data-stu-id="a0717-181">JET_OPENTEMPORARYTABLE class</span></span>](./jet-opentemporarytable-class.md)

[<span data-ttu-id="a0717-182">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="a0717-182">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
