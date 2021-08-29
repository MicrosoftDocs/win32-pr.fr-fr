---
description: 'En savoir plus sur les éléments suivants : Server2003Grbits'
title: Membres Server2003Grbits (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: Server2003Grbits members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_members(v=EXCHG.10)
ms:contentKeyID: 55107767
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 57e1dffd37dc54955ca2cb0ed28bc8aca37a35cb7ddc6792f497e7b8ca11513a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093199"
---
# <a name="server2003grbits-members"></a>Membres Server2003Grbits

Inclure les membres protégés  
Inclure les membres hérités  

Grbits qui ont été ajoutés à la version 2003 du serveur Windows d’ESENT.

Le type [Server2003Grbits](./server2003grbits-class.md) expose les membres suivants.

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
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>Si une colonne donnée n’est pas présente dans l’enregistrement et qu’elle a une valeur par défaut définie par l’utilisateur, aucune valeur de colonne n’est retournée. Cette option empêchera le rappel qui calcule la valeur par défaut définie par l’utilisateur pour la colonne à être appelée lors de l’énumération des valeurs de cette colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Cette option demande que la table temporaire soit créée uniquement si le gestionnaire de tables temporaire peut utiliser l’implémentation optimisée pour les résultats de requête intermédiaires. Si une caractéristique de la table temporaire empêche l’utilisation de cette optimisation, l’opération échoue avec JET_errCannotMaterializeForwardOnlySort. L’un des effets secondaires de cette option est de permettre à la table temporaire de contenir des enregistrements avec des clés d’index dupliquées. Pour plus d’informations, consultez <a href="hh558517(v=exchg.10).md">unique</a> .</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Champ public" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Toutes les transactions précédemment validées par une session qui n’ont pas encore été vidées dans le fichier journal des transactions seront vidées immédiatement. Cette API attend que les transactions aient été vidées avant de retourner à l’appelant. Cette option peut être utilisée même si la session n’est pas actuellement dans une transaction. Cette option ne peut pas être utilisée conjointement avec une autre option.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Server2003Grbits, classe](./server2003grbits-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
