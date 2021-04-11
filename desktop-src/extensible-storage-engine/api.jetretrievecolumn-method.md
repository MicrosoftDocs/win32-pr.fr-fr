---
description: 'En savoir plus sur : méthode API. JetRetrieveColumn'
title: API. JetRetrieveColumn, méthode
TOCTitle: 'JetRetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetretrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100791
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: e4e43d57f4393d6b0d4ce2f1cdbe4ecd8338ec54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210717"
---
# <a name="apijetretrievecolumn-method"></a><span data-ttu-id="b1cf9-103">API. JetRetrieveColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="b1cf9-103">Api.JetRetrieveColumn method</span></span>

<span data-ttu-id="b1cf9-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="b1cf9-104">Include protected members</span></span>  
<span data-ttu-id="b1cf9-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="b1cf9-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="b1cf9-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="b1cf9-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b1cf9-107">Nom</span><span class="sxs-lookup"><span data-stu-id="b1cf9-107">Name</span></span></th>
<th><span data-ttu-id="b1cf9-108">Description</span><span class="sxs-lookup"><span data-stu-id="b1cf9-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="b1cf9-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="b1cf9-111"><a href="dn332995(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="b1cf9-112">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b1cf9-113">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-113">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="b1cf9-114">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-114">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="b1cf9-115">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-115">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="b1cf9-116">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-116">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="b1cf9-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="b1cf9-119"><a href="dn332997(v=exchg.10).md">JetRetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="b1cf9-120">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-120">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b1cf9-121">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-121">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="b1cf9-122">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-122">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="b1cf9-123">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-123">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="b1cf9-124">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b1cf9-124">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1cf9-125">Haut</span><span class="sxs-lookup"><span data-stu-id="b1cf9-125">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b1cf9-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b1cf9-126">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b1cf9-127">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b1cf9-127">Reference</span></span>

[<span data-ttu-id="b1cf9-128">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b1cf9-128">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b1cf9-129">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b1cf9-129">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b1cf9-130">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b1cf9-130">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
