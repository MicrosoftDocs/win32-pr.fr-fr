---
description: En savoir plus sur les propriétés de JET_ENUMCOLUMNID
title: Propriétés de la JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_ENUMCOLUMNID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_enumcolumnid_properties(v=EXCHG.10)
ms:contentKeyID: 55103627
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1e45574d7cabd937d6b2d7351a917ac62340f355
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525029"
---
# <a name="jet_enumcolumnid-properties"></a><span data-ttu-id="c109c-103">Propriétés de la JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="c109c-103">JET_ENUMCOLUMNID properties</span></span>

<span data-ttu-id="c109c-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="c109c-104">Include protected members</span></span>  
<span data-ttu-id="c109c-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="c109c-105">Include inherited members</span></span>  

<span data-ttu-id="c109c-106">Le type de [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="c109c-106">The [JET_ENUMCOLUMNID](./jet-enumcolumnid-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="c109c-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c109c-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="c109c-108">Nom</span><span class="sxs-lookup"><span data-stu-id="c109c-108">Name</span></span></th>
<th><span data-ttu-id="c109c-109">Description</span><span class="sxs-lookup"><span data-stu-id="c109c-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="c109c-111"><a href="dn335141(v=exchg.10).md">ColumnID</a></span><span class="sxs-lookup"><span data-stu-id="c109c-111"><a href="dn335141(v=exchg.10).md">columnid</a></span></span></td>
<td><span data-ttu-id="c109c-112">Obtient ou définit l’ID ColumnID à énumérer.</span><span class="sxs-lookup"><span data-stu-id="c109c-112">Gets or sets the columnid ID to enumerate.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="c109c-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span><span class="sxs-lookup"><span data-stu-id="c109c-114"><a href="dn335092(v=exchg.10).md">ctagSequence</a></span></span></td>
<td><span data-ttu-id="c109c-115">Obtient ou définit le nombre de valeurs de colonne (par index de base un) à énumérer pour l’ID de colonne spécifié.</span><span class="sxs-lookup"><span data-stu-id="c109c-115">Gets or sets the count of column values (by one-based index) to enumerate for the specified column ID.</span></span> <span data-ttu-id="c109c-116">Si ctagSequence a la valeur 0 (zéro), rgtagSequence est ignoré et toutes les valeurs de colonne pour l’ID de colonne spécifié seront énumérées.</span><span class="sxs-lookup"><span data-stu-id="c109c-116">If ctagSequence is 0 (zero) then rgtagSequence is ignored and all column values for the specified column ID will be enumerated.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="c109c-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span><span class="sxs-lookup"><span data-stu-id="c109c-118"><a href="dn335093(v=exchg.10).md">rgtagSequence</a></span></span></td>
<td><span data-ttu-id="c109c-119">Obtient ou définit le tableau d’index de base un dans le tableau de valeurs de colonne pour une colonne donnée.</span><span class="sxs-lookup"><span data-stu-id="c109c-119">Gets or sets the array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="c109c-120">Un élément unique est un itagSequence qui est défini dans JET_RETRIEVECOLUMN.</span><span class="sxs-lookup"><span data-stu-id="c109c-120">A single element is an itagSequence which is defined in JET_RETRIEVECOLUMN.</span></span> <span data-ttu-id="c109c-121">Un itagSequence de 0 (zéro) signifie &quot; Skip &quot; .</span><span class="sxs-lookup"><span data-stu-id="c109c-121">An itagSequence of 0 (zero) means &quot;skip&quot;.</span></span> <span data-ttu-id="c109c-122">Un itagSequence de 1 signifie que retourne la première valeur de colonne de la colonne, 2 le second, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c109c-122">An itagSequence of 1 means return the first column value of the column, 2 means the second, and so on.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c109c-123">Haut</span><span class="sxs-lookup"><span data-stu-id="c109c-123">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="c109c-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c109c-124">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c109c-125">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c109c-125">Reference</span></span>

[<span data-ttu-id="c109c-126">Classe JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="c109c-126">JET_ENUMCOLUMNID class</span></span>](./jet-enumcolumnid-class.md)

[<span data-ttu-id="c109c-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="c109c-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
