---
description: En savoir plus sur les propriétés de JET_INDEXCREATE
title: Propriétés de la JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952843"
---
# <a name="jet_indexcreate-properties"></a><span data-ttu-id="b4f15-103">Propriétés de la JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b4f15-103">JET_INDEXCREATE properties</span></span>

<span data-ttu-id="b4f15-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="b4f15-104">Include protected members</span></span>  
<span data-ttu-id="b4f15-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="b4f15-105">Include inherited members</span></span>  

<span data-ttu-id="b4f15-106">Le type de [JET_INDEXCREATE](./jet-indexcreate-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="b4f15-106">The [JET_INDEXCREATE](./jet-indexcreate-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="b4f15-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b4f15-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b4f15-108">Nom</span><span class="sxs-lookup"><span data-stu-id="b4f15-108">Name</span></span></th>
<th><span data-ttu-id="b4f15-109">Description</span><span class="sxs-lookup"><span data-stu-id="b4f15-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-111"><a href="dn335122(v=exchg.10).md">cbKey</a></span></span></td>
<td><span data-ttu-id="b4f15-112">Obtient ou définit la longueur, en caractères, de szKey, y compris les deux valeurs null de fin.</span><span class="sxs-lookup"><span data-stu-id="b4f15-112">Gets or sets the length, in characters, of szKey including the two terminating nulls.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-114"><a href="dn335156(v=exchg.10).md">cbKeyMost</a></span></span></td>
<td><span data-ttu-id="b4f15-115">Obtient ou définit la taille maximale autorisée, en octets, pour les clés dans l’index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-115">Gets or sets the maximum allowable size, in bytes, for keys in the index.</span></span> <span data-ttu-id="b4f15-116">La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255) qui est la taille de clé maximale héritée.</span><span class="sxs-lookup"><span data-stu-id="b4f15-116">The minimum supported maximum key size is JET_cbKeyMostMin (255) which is the legacy maximum key size.</span></span> <span data-ttu-id="b4f15-117">La taille de clé maximale dépend de la taille de page de la base de données <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span><span class="sxs-lookup"><span data-stu-id="b4f15-117">The maximum key size is dependent on the database page size <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>.</span></span> <span data-ttu-id="b4f15-118">La <a href="dn351156(v=exchg.10).md">taille de clé</a>maximale peut être récupérée avec.</span><span class="sxs-lookup"><span data-stu-id="b4f15-118">The maximum key size can be retrieved with <a href="dn351156(v=exchg.10).md">KeyMost</a>.</span></span> <span data-ttu-id="b4f15-119">Ce paramètre est ignoré sur Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b4f15-119">This parameter is ignored on Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b4f15-120">Contrairement à l’API non managée, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) n’est pas nécessaire, elle est ajoutée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="b4f15-120">Unlike the unmanaged API, <strong>IndexKeyMost()</strong> (JET_bitIndexKeyMost) is not needed, it will be added automatically.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-122"><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></span></span></td>
<td><span data-ttu-id="b4f15-123">Obtient ou définit la longueur maximale, en octets, de chaque colonne à stocker dans l’index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-123">Gets or sets the maximum length, in bytes, of each column to store in the index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-125"><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></span></span></td>
<td><span data-ttu-id="b4f15-126">Obtient ou définit le nombre de colonnes conditionnelles.</span><span class="sxs-lookup"><span data-stu-id="b4f15-126">Gets or sets the number of conditional columns.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-128"><a href="dn335157(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-128"><a href="dn335157(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="b4f15-129">Obtient ou définit le code d’erreur de la création de cet index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-129">Gets or sets the error code from creating this index.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-131"><a href="dn335119(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-131"><a href="dn335119(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="b4f15-132">Obtient ou définit les options de création d’index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-132">Gets or sets index creation options.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-134"><a href="dn335159(v=exchg.10).md">pidxUnicode</a></span></span></td>
<td><span data-ttu-id="b4f15-135">Obtient ou définit les options de comparaison Unicode facultatives.</span><span class="sxs-lookup"><span data-stu-id="b4f15-135">Gets or sets the optional unicode comparison options.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-137"><a href="dn335120(v=exchg.10).md">pSpaceHints</a></span></span></td>
<td><span data-ttu-id="b4f15-138">Obtient ou définit les indicateurs d’allocation, de maintenance et d’utilisation de l’espace.</span><span class="sxs-lookup"><span data-stu-id="b4f15-138">Gets or sets space allocation, maintenance, and usage hints.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-140"><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></span></span></td>
<td><span data-ttu-id="b4f15-141">Obtient ou définit les colonnes conditionnelles facultatives.</span><span class="sxs-lookup"><span data-stu-id="b4f15-141">Gets or sets the optional conditional columns.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-143"><a href="dn335121(v=exchg.10).md">szIndexName</a></span></span></td>
<td><span data-ttu-id="b4f15-144">Obtient ou définit le nom de l’index à créer.</span><span class="sxs-lookup"><span data-stu-id="b4f15-144">Gets or sets the name of the index to create.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-146"><a href="dn335161(v=exchg.10).md">szKey</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-146"><a href="dn335161(v=exchg.10).md">szKey</a></span></span></td>
<td><span data-ttu-id="b4f15-147">Obtient ou définit la description de la clé d’index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-147">Gets or sets the description of the index key.</span></span> <span data-ttu-id="b4f15-148">Il s’agit d’une chaîne double qui se termine par un caractère null des jetons délimités par des valeurs NULL.</span><span class="sxs-lookup"><span data-stu-id="b4f15-148">This is a double null-terminated string of null-delimited tokens.</span></span> <span data-ttu-id="b4f15-149">Chaque jeton se présente sous la forme [direction-specifier] [Column-Name], où direction-Specification a la valeur &quot; + &quot; ou &quot; - &quot; .</span><span class="sxs-lookup"><span data-stu-id="b4f15-149">Each token is of the form [direction-specifier][column-name], where direction-specification is either &quot;+&quot; or &quot;-&quot;.</span></span> <span data-ttu-id="b4f15-150">par exemple, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexera les trois colonnes &quot; ABC &quot; (dans l’ordre croissant), &quot; Def &quot; (dans l’ordre décroissant) et &quot; GHI &quot; (dans l’ordre croissant).</span><span class="sxs-lookup"><span data-stu-id="b4f15-150">for example, a szKey of &quot;+abc\0-def\0+ghi\0&quot; will index over the three columns &quot;abc&quot; (in ascending order), &quot;def&quot; (in descending order), and &quot;ghi&quot; (in ascending order).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="b4f15-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span><span class="sxs-lookup"><span data-stu-id="b4f15-152"><a href="dn335162(v=exchg.10).md">ulDensity</a></span></span></td>
<td><span data-ttu-id="b4f15-153">Obtient ou définit la densité de l’index.</span><span class="sxs-lookup"><span data-stu-id="b4f15-153">Gets or sets the density of the index.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b4f15-154">Haut</span><span class="sxs-lookup"><span data-stu-id="b4f15-154">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b4f15-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4f15-155">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b4f15-156">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b4f15-156">Reference</span></span>

[<span data-ttu-id="b4f15-157">Classe JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="b4f15-157">JET_INDEXCREATE class</span></span>](./jet-indexcreate-class.md)

[<span data-ttu-id="b4f15-158">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b4f15-158">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
