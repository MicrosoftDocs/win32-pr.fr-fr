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
# <a name="vistagrbits-fields"></a>Champs VistaGrbits

Inclure les membres protégés  
Inclure les membres hérités  

Le type [VistaGrbits](./vistagrbits-class.md) expose les membres suivants.

## <a name="fields"></a>Champs

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nom</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351283(v=exchg.10).md">ContinueAfterThaw</a></td>
<td>La session d’instantané se poursuit après JetOSSnapshotThaw et nécessitera un appel de fonction JetOSSnapshotEnd.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335364(v=exchg.10).md">IndexCrossProduct</a></td>
<td>La spécification de cet indicateur pour un index qui a plusieurs colonnes clés qui est une colonne à plusieurs valeurs entraîne la création d’une entrée d’index pour chaque résultat d’un produit croisé de toutes les valeurs dans ces colonnes clés. Dans le cas contraire, l’index comporte une seule entrée pour chaque valeur multiple dans la colonne clé la plus significative qui est une colonne à valeurs multiples et chacune de ces entrées d’index utilise la première valeur multiple de toutes les autres colonnes clés qui sont des colonnes à valeurs multiples. Par exemple, si vous avez spécifié cet indicateur pour un index sur la colonne a qui a les valeurs &quot; rouge &quot; et &quot; bleu &quot; et sur la colonne B qui a les valeurs &quot; 1 &quot; et &quot; 2, &quot; les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; rouge &quot; , &quot; 2 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 2 &quot; . Dans le cas contraire, les entrées d’index suivantes sont créées : &quot; rouge &quot; , &quot; 1 &quot; ; &quot; bleu &quot; , &quot; 1 &quot; .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335368(v=exchg.10).md">IndexDisallowTruncation</a></td>
<td>Si vous spécifiez cet indicateur, toute mise à jour de l’index entraînant l’échec d’une clé tronquée avec <a href="hh564840(v=exchg.10).md">keytruncate</a>. Dans le cas contraire, les clés sont tronquées en mode silencieux.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351285(v=exchg.10).md">IndexNestedTable</a></td>
<td>Index sur plusieurs colonnes à valeurs multiples, mais uniquement avec des valeurs de même itagSequence.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335282(v=exchg.10).md">LogStreamMustExist</a></td>
<td>Les journaux des transactions doivent exister dans le répertoire du fichier journal (autrement dit, impossible de démarrer automatiquement un nouveau flux).</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335367(v=exchg.10).md">RecoveryWithoutUndo</a></td>
<td>Effectuer la récupération, mais s’arrêter à la phase de restauration. Autorise la relecture des journaux présents, puis les journaux supplémentaires peuvent être copiés et relus ultérieurement.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335375(v=exchg.10).md">ReplayMissingMapEntryDB</a></td>
<td>L’entrée de mappage de base de données est manquante par défaut au même emplacement.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335283(v=exchg.10).md">TruncateDone</a></td>
<td>Le moteur peut marquer les en-têtes de base de données comme il convient (par exemple, une sauvegarde complète est terminée), même si l’appel à TRUNCATE n’a pas été effectué.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335371(v=exchg.10).md">TruncateLogsAfterRecovery</a></td>
<td>En cas de récupération logicielle réussie, tronquez les fichiers journaux.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[VistaGrbits, classe](./vistagrbits-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
