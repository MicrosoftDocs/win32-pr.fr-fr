---
description: 'En savoir plus sur les éléments suivants : Server2003Grbits'
title: Membres Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 21008153606a6c35c76daf3c2758211f3fcdd42e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865613"
---
# <a name="server2003grbits-members"></a><span data-ttu-id="0e927-103">Membres Server2003Grbits</span><span class="sxs-lookup"><span data-stu-id="0e927-103">Server2003Grbits members</span></span>

<span data-ttu-id="0e927-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="0e927-104">Include protected members</span></span>  
<span data-ttu-id="0e927-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="0e927-105">Include inherited members</span></span>  

<span data-ttu-id="0e927-106">Grbits qui ont été ajoutés à la version Windows Server 2003 d’ESENT.</span><span class="sxs-lookup"><span data-stu-id="0e927-106">Grbits that have been added to the Windows Server 2003 version of ESENT.</span></span>

<span data-ttu-id="0e927-107">Le type [Server2003Grbits](./server2003grbits-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="0e927-107">The [Server2003Grbits](./server2003grbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="0e927-108">Champs</span><span class="sxs-lookup"><span data-stu-id="0e927-108">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0e927-109">Nom</span><span class="sxs-lookup"><span data-stu-id="0e927-109">Name</span></span></th>
<th><span data-ttu-id="0e927-110">Description</span><span class="sxs-lookup"><span data-stu-id="0e927-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0e927-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span><span class="sxs-lookup"><span data-stu-id="0e927-113"><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></span></span></td>
<td><span data-ttu-id="0e927-114">Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée.</span><span class="sxs-lookup"><span data-stu-id="0e927-114">If a given column is not present in the record and it has a user defined default value then no column value will be returned.</span></span> <span data-ttu-id="0e927-115">Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</span><span class="sxs-lookup"><span data-stu-id="0e927-115">This option will prevent the callback that computes the user defined default value for the column from being called when enumerating the values for that column.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0e927-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span><span class="sxs-lookup"><span data-stu-id="0e927-118"><a href="dn351284(v=exchg.10).md">ForwardOnly</a></span></span></td>
<td><span data-ttu-id="0e927-119">Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="0e927-119">This option requests that the temporary table only be created if the temporary table manager can use the implementation optimized for intermediate query results.</span></span> <span data-ttu-id="0e927-120">Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort.</span><span class="sxs-lookup"><span data-stu-id="0e927-120">If any characteristic of the temporary table would prevent the use of this optimization then the operation will fail with JET_errCannotMaterializeForwardOnlySort.</span></span> <span data-ttu-id="0e927-121">L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées.</span><span class="sxs-lookup"><span data-stu-id="0e927-121">A side effect of this option is to allow the temporary table to contain records with duplicate index keys.</span></span> <span data-ttu-id="0e927-122">Pour plus d’informations, consultez <a href="hh558517(v=exchg.10).md">unique</a> .</span><span class="sxs-lookup"><span data-stu-id="0e927-122">See <a href="hh558517(v=exchg.10).md">Unique</a> for more information.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0e927-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span><span class="sxs-lookup"><span data-stu-id="0e927-125"><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></span></span></td>
<td><span data-ttu-id="0e927-126">Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement.</span><span class="sxs-lookup"><span data-stu-id="0e927-126">All transactions previously committed by any session that have not yet been flushed to the transaction log file will be flushed immediately.</span></span> <span data-ttu-id="0e927-127">Cette API attend que les transactions aient été vidées avant de retourner à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="0e927-127">This API will wait until the transactions have been flushed before returning to the caller.</span></span> <span data-ttu-id="0e927-128">Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction.</span><span class="sxs-lookup"><span data-stu-id="0e927-128">This option may be used even if the session is not currently in a transaction.</span></span> <span data-ttu-id="0e927-129">Cette option ne peut pas être utilisée conjointement avec une autre option.</span><span class="sxs-lookup"><span data-stu-id="0e927-129">This option cannot be used in combination with any other option.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0e927-130">Haut</span><span class="sxs-lookup"><span data-stu-id="0e927-130">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0e927-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e927-131">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0e927-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0e927-132">Reference</span></span>

[<span data-ttu-id="0e927-133">Server2003Grbits, classe</span><span class="sxs-lookup"><span data-stu-id="0e927-133">Server2003Grbits class</span></span>](./server2003grbits-class.md)

[<span data-ttu-id="0e927-134">Espace de noms Microsoft. ISAM. esent. Interop. Server2003</span><span class="sxs-lookup"><span data-stu-id="0e927-134">Microsoft.Isam.Esent.Interop.Server2003 namespace</span></span>](./microsoft.isam.esent.interop.server2003-namespace.md)
