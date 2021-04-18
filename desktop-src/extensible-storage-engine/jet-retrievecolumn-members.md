---
description: 'En savoir plus sur les membres suivants : JET_RETRIEVECOLUMN'
title: Membres JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_members(v=EXCHG.10)
ms:contentKeyID: 55103877
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9a5eda1d671cfe6225a8419314b2f53558294754
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104562792"
---
# <a name="jet_retrievecolumn-members"></a><span data-ttu-id="be6d8-103">Membres JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="be6d8-103">JET_RETRIEVECOLUMN members</span></span>

<span data-ttu-id="be6d8-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="be6d8-104">Include protected members</span></span>  
<span data-ttu-id="be6d8-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="be6d8-105">Include inherited members</span></span>  

<span data-ttu-id="be6d8-106">Contient les paramètres d’entrée et de sortie pour [JetRetrieveColumns (JET_SESID, JET_TABLEID, \[ \] , Int32)](./api.jetretrievecolumns-method.md).</span><span class="sxs-lookup"><span data-stu-id="be6d8-106">Contains input and output parameters for [JetRetrieveColumns(JET_SESID, JET_TABLEID, \[\], Int32)](./api.jetretrievecolumns-method.md).</span></span> <span data-ttu-id="be6d8-107">Les champs de la structure décrivent la valeur de colonne à récupérer, la méthode de récupération et l’emplacement d’enregistrement des résultats.</span><span class="sxs-lookup"><span data-stu-id="be6d8-107">Fields in the structure describe what column value to retrieve, how to retrieve it, and where to save results.</span></span>

<span data-ttu-id="be6d8-108">Le type de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="be6d8-108">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="constructors"></a><span data-ttu-id="be6d8-109">Constructeurs</span><span class="sxs-lookup"><span data-stu-id="be6d8-109">Constructors</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="be6d8-110">Nom</span><span class="sxs-lookup"><span data-stu-id="be6d8-110">Name</span></span></th>
<th><span data-ttu-id="be6d8-111">Description</span><span class="sxs-lookup"><span data-stu-id="be6d8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="be6d8-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-113"><a href="dn351036(v=exchg.10).md">JET_RETRIEVECOLUMN</a></span></span></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be6d8-114">Haut</span><span class="sxs-lookup"><span data-stu-id="be6d8-114">Top</span></span>

## <a name="properties"></a><span data-ttu-id="be6d8-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="be6d8-115">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="be6d8-116">Nom</span><span class="sxs-lookup"><span data-stu-id="be6d8-116">Name</span></span></th>
<th><span data-ttu-id="be6d8-117">Description</span><span class="sxs-lookup"><span data-stu-id="be6d8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-119"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="be6d8-120">Obtient la taille, en octets, des données récupérées par une opération de récupération de colonne.</span><span class="sxs-lookup"><span data-stu-id="be6d8-120">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-122"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-122"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="be6d8-123">Obtient ou définit la taille de la mémoire tampon <a href="dn351040(v=exchg.10).md">pvData</a> , en octets.</span><span class="sxs-lookup"><span data-stu-id="be6d8-123">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="be6d8-124">L’opération de récupération de colonne ne stocke pas plus de données dans pvData que cbData.</span><span class="sxs-lookup"><span data-stu-id="be6d8-124">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-126"><a href="dn335230(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-126"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="be6d8-127">Obtient ou définit l’identificateur de colonne pour la colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="be6d8-127">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-129"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="be6d8-130">Obtient le ColumnID de la colonne balisée, à valeurs multiples ou fragmentées lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID.</span><span class="sxs-lookup"><span data-stu-id="be6d8-130">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-132"><a href="dn335231(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-132"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="be6d8-133">Obtient l’avertissement retourné par la récupération de la colonne.</span><span class="sxs-lookup"><span data-stu-id="be6d8-133">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-135"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-135"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="be6d8-136">Obtient ou définit les options pour la récupération de colonne.</span><span class="sxs-lookup"><span data-stu-id="be6d8-136">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-138"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-138"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="be6d8-139">Obtient ou définit le décalage dans la mémoire tampon dans lequel les données seront stockées.</span><span class="sxs-lookup"><span data-stu-id="be6d8-139">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-141"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="be6d8-142">Obtient ou définit le décalage vers le premier octet à récupérer à partir d’une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="be6d8-142">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-144"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="be6d8-145">Obtient ou définit le numéro de séquence des valeurs contenues dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="be6d8-145">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="be6d8-146">Si itagSequence est égal à 0, le nombre d’instances d’une colonne à valeurs multiples est retourné à la place des données de colonne.</span><span class="sxs-lookup"><span data-stu-id="be6d8-146">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="be6d8-148"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-148"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="be6d8-149">Obtient ou définit la mémoire tampon qui stocke les données extraites de la colonne.</span><span class="sxs-lookup"><span data-stu-id="be6d8-149">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be6d8-150">Haut</span><span class="sxs-lookup"><span data-stu-id="be6d8-150">Top</span></span>

## <a name="methods"></a><span data-ttu-id="be6d8-151">Méthodes</span><span class="sxs-lookup"><span data-stu-id="be6d8-151">Methods</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="be6d8-152">Nom</span><span class="sxs-lookup"><span data-stu-id="be6d8-152">Name</span></span></th>
<th><span data-ttu-id="be6d8-153">Description</span><span class="sxs-lookup"><span data-stu-id="be6d8-153">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="be6d8-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-155"><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Equals</a></span></span></td>
<td><span data-ttu-id="be6d8-156">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-156">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="be6d8-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-158"><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></span></span></td>
<td><span data-ttu-id="be6d8-159">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-159">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="be6d8-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-161"><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></span></span></td>
<td><span data-ttu-id="be6d8-162">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-162">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="be6d8-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-164"><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></span></span></td>
<td><span data-ttu-id="be6d8-165">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-165">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><span data-ttu-id="be6d8-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-167"><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></span></span></td>
<td><span data-ttu-id="be6d8-168">(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-168">(Inherited from <a href="/dotnet/api/system.object">Object</a>.)</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><span data-ttu-id="be6d8-170"><a href="dn335224(v=exchg.10).md">ToString</a></span><span class="sxs-lookup"><span data-stu-id="be6d8-170"><a href="dn335224(v=exchg.10).md">ToString</a></span></span></td>
<td><span data-ttu-id="be6d8-171">Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>actuel.</span><span class="sxs-lookup"><span data-stu-id="be6d8-171">Returns a <a href="/dotnet/api/system.string">String</a> that represents the current <a href="dn351033(v=exchg.10).md">JET_RETRIEVECOLUMN</a>.</span></span> <span data-ttu-id="be6d8-172">(Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</span><span class="sxs-lookup"><span data-stu-id="be6d8-172">(Overrides <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>.)</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="be6d8-173">Haut</span><span class="sxs-lookup"><span data-stu-id="be6d8-173">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="be6d8-174">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="be6d8-174">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="be6d8-175">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="be6d8-175">Reference</span></span>

[<span data-ttu-id="be6d8-176">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="be6d8-176">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="be6d8-177">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="be6d8-177">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
