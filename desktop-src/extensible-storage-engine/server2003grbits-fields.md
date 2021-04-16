---
description: 'En savoir plus sur les champs suivants : Server2003Grbits'
title: Champs Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: ed7a99118674d955fc6a882ac08407e45837af77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104560167"
---
# <a name="server2003grbits-fields"></a><span data-ttu-id="c5b9e-103">Champs Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="c5b9e-103">Server2003Grbits fields</span></span>

<span data-ttu-id="c5b9e-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="c5b9e-104">Include protected members</span></span>  
<span data-ttu-id="c5b9e-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="c5b9e-105">Include inherited members</span></span>  

<span data-ttu-id="c5b9e-106">Le type [Server2003Grbits](./server2003grbits-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-106">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="c5b9e-107">Champs</span><span class="sxs-lookup"><span data-stu-id="c5b9e-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="c5b9e-108">Nom</span><span class="sxs-lookup"><span data-stu-id="c5b9e-108">Name</span></span></th>
<th><span data-ttu-id="c5b9e-109">Description</span><span class="sxs-lookup"><span data-stu-id="c5b9e-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="c5b9e-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="c5b9e-112"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="c5b9e-113">Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-113">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="c5b9e-114">Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-114">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="c5b9e-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="c5b9e-117"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="c5b9e-118">Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-118">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="c5b9e-119">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-119">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="c5b9e-120">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-120">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="c5b9e-121">Pour plus d’informations, consultez <a href="hh558517(v=exchg.10).md">unique</a> .</span><span class="sxs-lookup"><span data-stu-id="c5b9e-121">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="c5b9e-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="c5b9e-124"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="c5b9e-125">Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-125">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="c5b9e-126">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-126">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="c5b9e-127">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-127">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="c5b9e-128">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="c5b9e-128">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c5b9e-129">Haut</span><span class="sxs-lookup"><span data-stu-id="c5b9e-129">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="c5b9e-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c5b9e-130">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="c5b9e-131">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="c5b9e-131">Reference</span></span>

[<span data-ttu-id="c5b9e-132">Server2003Grbits, classe</span><span class="sxs-lookup"><span data-stu-id="c5b9e-132">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="c5b9e-133">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="c5b9e-133">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
