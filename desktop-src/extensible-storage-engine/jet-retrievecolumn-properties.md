---
description: En savoir plus sur les propriétés de JET_RETRIEVECOLUMN
title: Propriétés de la JET_RETRIEVECOLUMN
TOCTitle: JET_RETRIEVECOLUMN properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETRIEVECOLUMN
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retrievecolumn_properties(v=EXCHG.10)
ms:contentKeyID: 55103808
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2a42337e361fc7cbef60db70662ab7388c678903
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758506"
---
# <a name="jet_retrievecolumn-properties"></a><span data-ttu-id="343c1-103">Propriétés de la JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="343c1-103">JET_RETRIEVECOLUMN properties</span></span>

<span data-ttu-id="343c1-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="343c1-104">Include protected members</span></span>  
<span data-ttu-id="343c1-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="343c1-105">Include inherited members</span></span>  

<span data-ttu-id="343c1-106">Le type de [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="343c1-106">The [JET_RETRIEVECOLUMN](./jet-retrievecolumn-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="343c1-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="343c1-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="343c1-108">Nom</span><span class="sxs-lookup"><span data-stu-id="343c1-108">Name</span></span></th>
<th><span data-ttu-id="343c1-109">Description</span><span class="sxs-lookup"><span data-stu-id="343c1-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span><span class="sxs-lookup"><span data-stu-id="343c1-111"><a href="dn335226(v=exchg.10).md">cbActual</a></span></span></td>
<td><span data-ttu-id="343c1-112">Obtient la taille, en octets, des données récupérées par une opération de récupération de colonne.</span><span class="sxs-lookup"><span data-stu-id="343c1-112">Gets the size, in bytes, of data that is retrieved by a retrieve column operation.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-114"><a href="dn335228(v=exchg.10).md">cbData</a></span><span class="sxs-lookup"><span data-stu-id="343c1-114"><a href="dn335228(v=exchg.10).md">cbData</a></span></span></td>
<td><span data-ttu-id="343c1-115">Obtient ou définit la taille de la mémoire tampon <a href="dn351040(v=exchg.10).md">pvData</a> , en octets.</span><span class="sxs-lookup"><span data-stu-id="343c1-115">Gets or sets the size of the <a href="dn351040(v=exchg.10).md">pvData</a> buffer, in bytes.</span></span> <span data-ttu-id="343c1-116">L’opération de récupération de colonne ne stocke pas plus de données dans pvData que cbData.</span><span class="sxs-lookup"><span data-stu-id="343c1-116">The retrieve column operation will not store more data in pvData than cbData.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-118"><a href="dn335230(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="343c1-118"><a href="dn335230(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="343c1-119">Obtient ou définit l’identificateur de colonne pour la colonne à récupérer.</span><span class="sxs-lookup"><span data-stu-id="343c1-119">Gets or sets the column identifier for the column to retrieve.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="343c1-121"><a href="dn335229(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="343c1-122">Obtient le ColumnID de la colonne balisée, à valeurs multiples ou fragmentées lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID.</span><span class="sxs-lookup"><span data-stu-id="343c1-122">Gets the columnid of the tagged, multi-valued, or sparse column when all tagged columns are retrieved by passing 0 as the columnid.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-124"><a href="dn335231(v=exchg.10).md">Raise</a></span><span class="sxs-lookup"><span data-stu-id="343c1-124"><a href="dn335231(v=exchg.10).md">err</a></span></span></td>
<td><span data-ttu-id="343c1-125">Obtient l’avertissement retourné par la récupération de la colonne.</span><span class="sxs-lookup"><span data-stu-id="343c1-125">Gets the warning returned from the retrieval of the column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-127"><a href="dn335232(v=exchg.10).md">grbit</a></span><span class="sxs-lookup"><span data-stu-id="343c1-127"><a href="dn335232(v=exchg.10).md">grbit</a></span></span></td>
<td><span data-ttu-id="343c1-128">Obtient ou définit les options pour la récupération de colonne.</span><span class="sxs-lookup"><span data-stu-id="343c1-128">Gets or sets the options for column retrieval.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-130"><a href="dn335233(v=exchg.10).md">ibData</a></span><span class="sxs-lookup"><span data-stu-id="343c1-130"><a href="dn335233(v=exchg.10).md">ibData</a></span></span></td>
<td><span data-ttu-id="343c1-131">Obtient ou définit le décalage dans la mémoire tampon dans lequel les données seront stockées.</span><span class="sxs-lookup"><span data-stu-id="343c1-131">Gets or sets the offset in the buffer that data will be stored in.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="343c1-133"><a href="dn335234(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="343c1-134">Obtient ou définit le décalage vers le premier octet à récupérer à partir d’une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="343c1-134">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="343c1-136"><a href="dn351039(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="343c1-137">Obtient ou définit le numéro de séquence des valeurs contenues dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="343c1-137">Gets or sets the sequence number of the values that are contained in a multi-valued column.</span></span> <span data-ttu-id="343c1-138">Si itagSequence est égal à 0, le nombre d’instances d’une colonne à valeurs multiples est retourné à la place des données de colonne.</span><span class="sxs-lookup"><span data-stu-id="343c1-138">If the itagSequence is 0 then the number of instances of a multi-valued column are returned instead of any column data.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="343c1-140"><a href="dn351040(v=exchg.10).md">pvData</a></span><span class="sxs-lookup"><span data-stu-id="343c1-140"><a href="dn351040(v=exchg.10).md">pvData</a></span></span></td>
<td><span data-ttu-id="343c1-141">Obtient ou définit la mémoire tampon qui stocke les données extraites de la colonne.</span><span class="sxs-lookup"><span data-stu-id="343c1-141">Gets or sets the buffer that will store data that is retrieved from the column.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="343c1-142">Haut</span><span class="sxs-lookup"><span data-stu-id="343c1-142">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="343c1-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="343c1-143">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="343c1-144">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="343c1-144">Reference</span></span>

[<span data-ttu-id="343c1-145">Classe JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="343c1-145">JET_RETRIEVECOLUMN class</span></span>](./jet-retrievecolumn-class.md)

[<span data-ttu-id="343c1-146">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="343c1-146">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
