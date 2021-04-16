---
description: En savoir plus sur les propriétés de JET_RETINFO
title: Propriétés de la JET_RETINFO
TOCTitle: JET_RETINFO properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_RETINFO
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_retinfo_properties(v=EXCHG.10)
ms:contentKeyID: 55103867
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 4724651b0184bae0b4acca049a8a16653282ce85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104554125"
---
# <a name="jet_retinfo-properties"></a><span data-ttu-id="91db4-103">Propriétés de la JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="91db4-103">JET_RETINFO properties</span></span>

<span data-ttu-id="91db4-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="91db4-104">Include protected members</span></span>  
<span data-ttu-id="91db4-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="91db4-105">Include inherited members</span></span>  

<span data-ttu-id="91db4-106">Le type de [JET_RETINFO](./jet-retinfo-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="91db4-106">The [JET_RETINFO](./jet-retinfo-class.md) type exposes the following members.</span></span>

## <a name="properties"></a><span data-ttu-id="91db4-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="91db4-107">Properties</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="91db4-108">Nom</span><span class="sxs-lookup"><span data-stu-id="91db4-108">Name</span></span></th>
<th><span data-ttu-id="91db4-109">Description</span><span class="sxs-lookup"><span data-stu-id="91db4-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="91db4-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span><span class="sxs-lookup"><span data-stu-id="91db4-111"><a href="dn335221(v=exchg.10).md">columnidNextTagged</a></span></span></td>
<td><span data-ttu-id="91db4-112">Obtient le ColumnID de la colonne balisée, à valeurs multiples ou partiellement allouées Récupérée lorsque toutes les colonnes avec balises sont récupérées en passant 0 comme ColumnID à JetRetrieveColumn.</span><span class="sxs-lookup"><span data-stu-id="91db4-112">Gets the columnid of the retrieved tagged, multi-valued or sparse, column when all tagged columns are retrieved by passing 0 as the columnid to JetRetrieveColumn.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="91db4-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span><span class="sxs-lookup"><span data-stu-id="91db4-114"><a href="dn335220(v=exchg.10).md">ibLongValue</a></span></span></td>
<td><span data-ttu-id="91db4-115">Obtient ou définit le décalage vers le premier octet à récupérer à partir d’une colonne de type <a href="hh577895(v=exchg.10).md">LONGBINARY</a>, ou <a href="hh577895(v=exchg.10).md">LONGTEXT</a>.</span><span class="sxs-lookup"><span data-stu-id="91db4-115">Gets or sets the offset to the first byte to be retrieved from a column of type <a href="hh577895(v=exchg.10).md">LongBinary</a>, or <a href="hh577895(v=exchg.10).md">LongText</a>.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><span data-ttu-id="91db4-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span><span class="sxs-lookup"><span data-stu-id="91db4-117"><a href="dn351035(v=exchg.10).md">itagSequence</a></span></span></td>
<td><span data-ttu-id="91db4-118">Obtient ou définit le numéro de séquence de la valeur dans une colonne à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="91db4-118">Gets or sets the sequence number of value in a multi-valued column.</span></span> <span data-ttu-id="91db4-119">Le tableau de valeurs est de base un.</span><span class="sxs-lookup"><span data-stu-id="91db4-119">The array of values is one-based.</span></span> <span data-ttu-id="91db4-120">La première valeur est séquence 1, et non 0.</span><span class="sxs-lookup"><span data-stu-id="91db4-120">The first value is sequence 1, not 0.</span></span> <span data-ttu-id="91db4-121">Si la colonne d’enregistrement n’a qu’une seule valeur, 1 doit être passé en tant que itagSequence.</span><span class="sxs-lookup"><span data-stu-id="91db4-121">If the record column has only one value then 1 should be passed as the itagSequence.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91db4-122">Haut</span><span class="sxs-lookup"><span data-stu-id="91db4-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="91db4-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91db4-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="91db4-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="91db4-124">Reference</span></span>

[<span data-ttu-id="91db4-125">Classe JET_RETINFO</span><span class="sxs-lookup"><span data-stu-id="91db4-125">JET_RETINFO class</span></span>](./jet-retinfo-class.md)

[<span data-ttu-id="91db4-126">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="91db4-126">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
