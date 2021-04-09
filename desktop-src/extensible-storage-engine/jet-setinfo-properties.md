---
description: En savoir plus sur les propriétés de JET_SETINFO
title: Propriétés de la JET_SETINFO
TOCTitle: JET_SETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_SETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_setinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103917
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: af54ddfc09cce0a9c9498dea2060fb83baa0d6f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112531"
---
# <a name="jet_setinfo-properties"></a><span data-ttu-id="2ea13-103">Propriétés de la JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="2ea13-103">JET_SETINFO properties</span></span>

<span data-ttu-id="2ea13-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="2ea13-104">Include protected members</span></span>  
<span data-ttu-id="2ea13-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="2ea13-105">Include inherited members</span></span>  

<span data-ttu-id="2ea13-106">Le type de [JET_SETINFO](./jet-setinfo-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="2ea13-106">The [JET_SETINFO](./jet-setinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="2ea13-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2ea13-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="2ea13-108">Nom</span><span class="sxs-lookup"><span data-stu-id="2ea13-108">Name</span></span></th>
<th><span data-ttu-id="2ea13-109">Description</span><span class="sxs-lookup"><span data-stu-id="2ea13-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="2ea13-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="2ea13-111"><a href="dn351064(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="2ea13-112">Obtient ou définit offset pour le premier octet à définir dans une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a> ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="2ea13-112">Gets or sets offset to the first byte to be set in a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a> or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="2ea13-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="2ea13-114"><a href="dn351037(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="2ea13-115">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples à définir.</span><span class="sxs-lookup"><span data-stu-id="2ea13-115">Gets or sets the sequence number of value in a multi-valued column to be set.</span></span> <span data-ttu-id="2ea13-116">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="2ea13-116">The array of values is one-based.</span></span> <span data-ttu-id="2ea13-117">La première valeur est Sequence 1, et non 0 (zéro).</span><span class="sxs-lookup"><span data-stu-id="2ea13-117">The first value is sequence 1, not 0 (zero).</span></span> <span data-ttu-id="2ea13-118">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé comme itagSequence si cette valeur est remplacée.</span><span class="sxs-lookup"><span data-stu-id="2ea13-118">If the record column has only one value then 1 should be passed as the itagSequence if that value is being replaced.</span></span> <span data-ttu-id="2ea13-119">La valeur 0 (zéro) signifie que vous pouvez ajouter une nouvelle instance de valeur de colonne à la fin de la séquence de valeurs de colonne.</span><span class="sxs-lookup"><span data-stu-id="2ea13-119">A value of 0 (zero) means to add a new column value instance to the end of the sequence of column values.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2ea13-120">Haut</span><span class="sxs-lookup"><span data-stu-id="2ea13-120">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="2ea13-121">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ea13-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2ea13-122">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="2ea13-122">Reference</span></span>

[<span data-ttu-id="2ea13-123">Classe JET_SETINFO</span><span class="sxs-lookup"><span data-stu-id="2ea13-123">JET_SETINFO class</span></span>](./jet-setinfo-class.md)

[<span data-ttu-id="2ea13-124">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="2ea13-124">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
