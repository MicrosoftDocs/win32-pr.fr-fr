---
description: 'En savoir plus sur : méthode API. RetrieveColumn'
title: API. RetrieveColumn, méthode
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758979"
---
# <a name="apiretrievecolumn-method"></a><span data-ttu-id="b3616-103">API. RetrieveColumn, méthode</span><span class="sxs-lookup"><span data-stu-id="b3616-103">Api.RetrieveColumn method</span></span>

<span data-ttu-id="b3616-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="b3616-104">Include protected members</span></span>  
<span data-ttu-id="b3616-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="b3616-105">Include inherited members</span></span>  

## <a name="overload-list"></a><span data-ttu-id="b3616-106">Liste de surcharge</span><span class="sxs-lookup"><span data-stu-id="b3616-106">Overload list</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="b3616-107">Nom</span><span class="sxs-lookup"><span data-stu-id="b3616-107">Name</span></span></th>
<th><span data-ttu-id="b3616-108">Description</span><span class="sxs-lookup"><span data-stu-id="b3616-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="b3616-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span><span class="sxs-lookup"><span data-stu-id="b3616-111"><a href="dn334041(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID)</a></span></span></td>
<td><span data-ttu-id="b3616-112">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="b3616-112">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b3616-113">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="b3616-113">The record is that record associated with the index entry at the current position of the cursor.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="b3616-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span><span class="sxs-lookup"><span data-stu-id="b3616-116"><a href="dn334060(v=exchg.10).md">RetrieveColumn(JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></span></span></td>
<td><span data-ttu-id="b3616-117">Récupère une valeur de colonne unique à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="b3616-117">Retrieves a single column value from the current record.</span></span> <span data-ttu-id="b3616-118">L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</span><span class="sxs-lookup"><span data-stu-id="b3616-118">The record is that record associated with the index entry at the current position of the cursor.</span></span> <span data-ttu-id="b3616-119">Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur.</span><span class="sxs-lookup"><span data-stu-id="b3616-119">Alternatively, this function can retrieve a column from a record being created in the cursor copy buffer.</span></span> <span data-ttu-id="b3616-120">Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</span><span class="sxs-lookup"><span data-stu-id="b3616-120">This function can also retrieve column data from an index entry that references the current record.</span></span> <span data-ttu-id="b3616-121">En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="b3616-121">In addition to retrieving the actual column value, JetRetrieveColumn can also be used to retrieve the size of a column, before retrieving the column data itself so that application buffers can be sized appropriately.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b3616-122">Haut</span><span class="sxs-lookup"><span data-stu-id="b3616-122">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="b3616-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b3616-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b3616-124">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="b3616-124">Reference</span></span>

[<span data-ttu-id="b3616-125">Classe d’API</span><span class="sxs-lookup"><span data-stu-id="b3616-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="b3616-126">Membres d’API</span><span class="sxs-lookup"><span data-stu-id="b3616-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="b3616-127">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="b3616-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
