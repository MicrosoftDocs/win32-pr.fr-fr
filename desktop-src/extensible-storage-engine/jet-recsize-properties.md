---
description: En savoir plus sur les propriétés de JET_RECSIZE
title: Propriétés de JET_RECSIZE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_RECSIZE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize_properties(v=EXCHG.10)
ms:contentKeyID: 39513545
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4733e1d666bdf3f938c91f437c1764811fb10f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868945"
---
# <a name="jet_recsize-properties"></a><span data-ttu-id="453fd-103">Propriétés de la JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="453fd-103">JET_RECSIZE properties</span></span>

<span data-ttu-id="453fd-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="453fd-104">Include protected members</span></span>  
<span data-ttu-id="453fd-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="453fd-105">Include inherited members</span></span>  

<span data-ttu-id="453fd-106">Le type de [JET_RECSIZE](./jet-recsize-structure2.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="453fd-106">The [JET_RECSIZE](./jet-recsize-structure2.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="453fd-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="453fd-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="453fd-108">Nom</span><span class="sxs-lookup"><span data-stu-id="453fd-108">Name</span></span></th>
<th><span data-ttu-id="453fd-109">Description</span><span class="sxs-lookup"><span data-stu-id="453fd-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-111"><a href="hh557581(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="453fd-111"><a href="hh557581(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="453fd-112">Obtient le jeu de données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-112">Gets the user data set in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="453fd-114"><a href="hh596280(v=exchg.10).md">cbDataCompressed</a></span></span></td>
<td><span data-ttu-id="453fd-115">Obtient la taille compressée des données utilisateur dans l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-115">Gets the compressed size of user data in record.</span></span> <span data-ttu-id="453fd-116">C’est le même que <a href="hh557581(v=exchg.10).md">cbData</a> si aucune valeur long intrinsèque n’est compressée).</span><span class="sxs-lookup"><span data-stu-id="453fd-116">This is the same as <a href="hh557581(v=exchg.10).md">cbData</a> if no intrinsic long-values are compressed).</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span><span class="sxs-lookup"><span data-stu-id="453fd-118"><a href="hh557913(v=exchg.10).md">cbLongValueData</a></span></span></td>
<td><span data-ttu-id="453fd-119">Obtient le jeu de données utilisateur dans l’enregistrement, mais stocké dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="453fd-119">Gets the user data set in the record, but stored in the long-value tree.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span><span class="sxs-lookup"><span data-stu-id="453fd-121"><a href="hh566144(v=exchg.10).md">cbLongValueDataCompressed</a></span></span></td>
<td><span data-ttu-id="453fd-122">Obtient la taille compressée des données utilisateur dans l’arborescence de valeurs longues.</span><span class="sxs-lookup"><span data-stu-id="453fd-122">Gets the compressed size of user data in the long-value tree.</span></span> <span data-ttu-id="453fd-123">C’est le même que <a href="hh557913(v=exchg.10).md">cbLongValueData</a> si aucune valeur long séparée n’est compressée.</span><span class="sxs-lookup"><span data-stu-id="453fd-123">This is the same as <a href="hh557913(v=exchg.10).md">cbLongValueData</a> if no separated long values are compressed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span><span class="sxs-lookup"><span data-stu-id="453fd-125"><a href="hh558003(v=exchg.10).md">cbLongValueOverhead</a></span></span></td>
<td><span data-ttu-id="453fd-126">Obtient la surcharge des données de valeur long.</span><span class="sxs-lookup"><span data-stu-id="453fd-126">Gets the overhead of the long-value data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span><span class="sxs-lookup"><span data-stu-id="453fd-128"><a href="hh565836(v=exchg.10).md">cbOverhead</a></span></span></td>
<td><span data-ttu-id="453fd-129">Obtient la surcharge de la structure d’enregistrement ESENT pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-129">Gets the overhead of the ESENT record structure for this record.</span></span> <span data-ttu-id="453fd-130">Cela comprend la taille de la clé de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-130">This includes the record's key size.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span><span class="sxs-lookup"><span data-stu-id="453fd-132"><a href="hh566154(v=exchg.10).md">cCompressedColumns</a></span></span></td>
<td><span data-ttu-id="453fd-133">Obtient le nombre total de colonnes dans l’enregistrement qui sont compressées.</span><span class="sxs-lookup"><span data-stu-id="453fd-133">Gets the total number of columns in the record which are compressed.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span><span class="sxs-lookup"><span data-stu-id="453fd-135"><a href="hh596288(v=exchg.10).md">cLongValues</a></span></span></td>
<td><span data-ttu-id="453fd-136">Obtient le nombre total de valeurs longues stockées dans l’arborescence de valeurs longues pour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-136">Gets the total number of long values stored in the long-value tree for this record.</span></span> <span data-ttu-id="453fd-137">Cela n’inclut pas les valeurs longues intrinsèques.</span><span class="sxs-lookup"><span data-stu-id="453fd-137">This does not include intrinsic long values.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span><span class="sxs-lookup"><span data-stu-id="453fd-139"><a href="hh577486(v=exchg.10).md">cMultiValues</a></span></span></td>
<td><span data-ttu-id="453fd-140">Obtient l’accumulation du nombre total de valeurs au-delà de la première pour toutes les colonnes de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-140">Gets the accumulation of the total number of values beyond the first for all columns in the record.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="453fd-142"><a href="hh578172(v=exchg.10).md">cNonTaggedColumns</a></span></span></td>
<td><span data-ttu-id="453fd-143">Obtient le nombre total de colonnes fixes et variables définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-143">Gets the total number of fixed and variable columns set in this record.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="453fd-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span><span class="sxs-lookup"><span data-stu-id="453fd-145"><a href="hh566034(v=exchg.10).md">cTaggedColumns</a></span></span></td>
<td><span data-ttu-id="453fd-146">Obtient le nombre total de colonnes avec balises définies dans cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="453fd-146">Gets the total number of tagged columns set in this record.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="453fd-147">Haut</span><span class="sxs-lookup"><span data-stu-id="453fd-147">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="453fd-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="453fd-148">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="453fd-149">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="453fd-149">Reference</span></span>

[<span data-ttu-id="453fd-150">Structure JET_RECSIZE</span><span class="sxs-lookup"><span data-stu-id="453fd-150">JET_RECSIZE structure</span></span>](./jet-recsize-structure2.md)

[<span data-ttu-id="453fd-151">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="453fd-151">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
