---
description: 'En savoir plus sur les champs suivants : VistaGrbits'
title: Champs VistaGrbits (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: VistaGrbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Vista.VistaGrbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistagrbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104318
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 3694dae8c55a5da838b8fcc058b369d7f0a59ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869130"
---
# <a name="vistagrbits-fields"></a><span data-ttu-id="0cdab-103">Champs VistaGrbits</span><span class="sxs-lookup"><span data-stu-id="0cdab-103">VistaGrbits fields</span></span>

<span data-ttu-id="0cdab-104">Inclure les membres protégés</span><span class="sxs-lookup"><span data-stu-id="0cdab-104">Include protected members</span></span>  
<span data-ttu-id="0cdab-105">Inclure les membres hérités</span><span class="sxs-lookup"><span data-stu-id="0cdab-105">Include inherited members</span></span>  

<span data-ttu-id="0cdab-106">Le type [VistaGrbits](./vistagrbits-class.md) expose les membres suivants.</span><span class="sxs-lookup"><span data-stu-id="0cdab-106">The [VistaGrbits](./vistagrbits-class.md) type exposes the following members.</span></span>

## <a name="fields"></a><span data-ttu-id="0cdab-107">Champs</span><span class="sxs-lookup"><span data-stu-id="0cdab-107">Fields</span></span>

<table>
<thead>
<tr class="header">
<th> </th>
<th><span data-ttu-id="0cdab-108">Nom</span><span class="sxs-lookup"><span data-stu-id="0cdab-108">Name</span></span></th>
<th><span data-ttu-id="0cdab-109">Description</span><span class="sxs-lookup"><span data-stu-id="0cdab-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-112"><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></span></span></td>
<td><span data-ttu-id="0cdab-113">La session d’instantané se poursuit après JetOSSnapshotThaw et nécessitera un appel de fonction JetOSSnapshotEnd.</span><span class="sxs-lookup"><span data-stu-id="0cdab-113">The snapshot session continues after JetOSSnapshotThaw and will require a JetOSSnapshotEnd function call.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-116"><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></span></span></td>
<td><span data-ttu-id="0cdab-117">La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à plusieurs valeurs entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés.</span><span class="sxs-lookup"><span data-stu-id="0cdab-117">Specifying this flag for an index that has more than one key column that is a multi-valued column will result in an index entry being created for each result of a cross product of all the values in those key columns.</span></span> <span data-ttu-id="0cdab-118">Dans le cas contraire, l’index comporte une seule entrée pour chaque valeur multiple dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utilise la première valeur multiple de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="0cdab-118">Otherwise, the index would only have one entry for each multi-value in the most significant key column that is a multi-valued column and each of those index entries would use the first multi-value from any other key columns that are multi-valued columns.</span></span> <span data-ttu-id="0cdab-119">Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs &quot; rouge &quot; et &quot; bleu &quot; et sur la colonne B qui a les valeurs &quot; 1 &quot; et &quot; 2, &quot; les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; rouge &quot; , &quot; 2 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 2 &quot; .</span><span class="sxs-lookup"><span data-stu-id="0cdab-119">For example, if you specified this flag for an index over column A that has the values &quot;red&quot; and &quot;blue&quot; and over column B that has the values &quot;1&quot; and &quot;2&quot; then the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;red&quot;, &quot;2&quot;; &quot;blue&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;2&quot;.</span></span> <span data-ttu-id="0cdab-120">Dans le cas contraire, les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; .</span><span class="sxs-lookup"><span data-stu-id="0cdab-120">Otherwise, the following index entries would be created: &quot;red&quot;, &quot;1&quot;; &quot;blue&quot;, &quot;1&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-123"><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></span></span></td>
<td><span data-ttu-id="0cdab-124">Si vous spécifiez cet indicateur, toute mise à jour de l’index entraînant l’échec d’une clé tronquée avec <a href="hh564840(v=exchg.10).md">keytruncate</a>.</span><span class="sxs-lookup"><span data-stu-id="0cdab-124">Specifying this flag will cause any update to the index that would result in a truncated key to fail with <a href="hh564840(v=exchg.10).md">KeyTruncated</a>.</span></span> <span data-ttu-id="0cdab-125">Dans le cas contraire, les clés sont tronquées en mode silencieux.</span><span class="sxs-lookup"><span data-stu-id="0cdab-125">Otherwise, keys will be silently truncated.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-128"><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></span></span></td>
<td><span data-ttu-id="0cdab-129">Index sur plusieurs colonnes à valeurs multiples, mais uniquement avec des valeurs de même itagSequence.</span><span class="sxs-lookup"><span data-stu-id="0cdab-129">Index over multiple multi-valued columns but only with values of same itagSequence.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-132"><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></span></span></td>
<td><span data-ttu-id="0cdab-133">Les journaux des transactions doivent exister dans le répertoire du fichier journal (autrement dit, impossible de démarrer automatiquement un nouveau flux).</span><span class="sxs-lookup"><span data-stu-id="0cdab-133">Transaction logs must exist in the log file directory (i.e. can't auto-start a new stream).</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-136"><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></span></span></td>
<td><span data-ttu-id="0cdab-137">Effectuer la récupération, mais s’arrêter à la phase de restauration.</span><span class="sxs-lookup"><span data-stu-id="0cdab-137">Perform recovery, but halt at the Undo phase.</span></span> <span data-ttu-id="0cdab-138">Autorise la relecture des journaux présents, puis les journaux supplémentaires peuvent être copiés et relus ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="0cdab-138">Allows whatever logs are present to be replayed, then later additional logs can be copied and replayed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-141"><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></span></span></td>
<td><span data-ttu-id="0cdab-142">L’entrée de mappage de base de données est manquante par défaut au même emplacement.</span><span class="sxs-lookup"><span data-stu-id="0cdab-142">Missing database map entry default to same location.</span></span></td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-145"><a href="dn335283(v=exchg.10).md">TruncateDone</a></span></span></td>
<td><span data-ttu-id="0cdab-146">Le moteur peut marquer les en-têtes de base de données comme il convient (par exemple, une sauvegarde complète est terminée), même si l’appel à TRUNCATE n’a pas été effectué.</span><span class="sxs-lookup"><span data-stu-id="0cdab-146">The engine can mark the database headers as appropriate (for example, a full backup completed), even though the call to truncate was not completed.</span></span></td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><span data-ttu-id="0cdab-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span><span class="sxs-lookup"><span data-stu-id="0cdab-149"><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></span></span></td>
<td><span data-ttu-id="0cdab-150">En cas de récupération logicielle réussie, tronquez les fichiers journaux.</span><span class="sxs-lookup"><span data-stu-id="0cdab-150">On successful soft recovery, truncate log files.</span></span></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0cdab-151">Haut</span><span class="sxs-lookup"><span data-stu-id="0cdab-151">Top</span></span>

## <a name="see-also"></a><span data-ttu-id="0cdab-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0cdab-152">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="0cdab-153">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="0cdab-153">Reference</span></span>

[<span data-ttu-id="0cdab-154">VistaGrbits, classe</span><span class="sxs-lookup"><span data-stu-id="0cdab-154">VistaGrbits class</span></span>](./vistagrbits-class.md)

[<span data-ttu-id="0cdab-155">Espace de noms Microsoft. ISAM. esent. Interop. Vista</span><span class="sxs-lookup"><span data-stu-id="0cdab-155">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
