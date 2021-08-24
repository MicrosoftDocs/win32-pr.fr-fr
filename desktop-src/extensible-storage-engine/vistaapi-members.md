---
description: 'En savoir plus sur les éléments suivants : VistaApi'
title: Membres VistaApi (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: VistaApi members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.VistaApi
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi_members(v=EXCHG.10)
ms:contentKeyID: 55104282
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1ada48839d05f1eaeec5eae5fe541ea89c5e0b641bba35441b3f189bf2973ba0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106837"
---
# <a name="vistaapi-members"></a>Membres VistaApi

Inclure les membres protégés  
Inclure les membres hérités  

les api ESENT prises en charge pour la première fois dans Windows Vista.

Le type [VistaApi](./vistaapi-class.md) expose les membres suivants.

## <a name="methods"></a>Méthodes

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335319(v=exchg.10).md">JetGetColumnInfo</a></td>
<td>Récupère des informations sur une colonne dans une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351258(v=exchg.10).md">JetGetInstanceMiscInfo</a></td>
<td>Récupère des informations sur une instance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335320(v=exchg.10).md">JetGetRecordSize</a></td>
<td>Récupère des informations sur la taille des enregistrements à partir de l’emplacement souhaité.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351264(v=exchg.10).md">JetGetThreadStats</a></td>
<td>Récupère les informations de performance du moteur de base de données pour le thread actuel. Plusieurs appels peuvent être utilisés pour collecter des statistiques qui reflètent l’activité du moteur de base de données sur ce thread entre ces appels.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351265(v=exchg.10).md">JetInit3</a></td>
<td>Initialisez le moteur de base de données ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable</a></td>
<td>Crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle. Consultez également <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351267(v=exchg.10).md">JetOSSnapshotEnd</a></td>
<td>Notifie le moteur que la session d’instantané s’est terminée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351269(v=exchg.10).md">JetOSSnapshotGetFreezeInfo</a></td>
<td>Récupère la liste des instances et des bases de données qui font partie de la session d’instantané à un moment donné.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335341(v=exchg.10).md">JetOSSnapshotPrepareInstance</a></td>
<td>Sélectionne une instance spécifique pour faire partie de la session d’instantané.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn335343(v=exchg.10).md">JetOSSnapshotTruncateLog</a></td>
<td>Active la troncation du journal pour toutes les instances qui font partie de la session d’instantané.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn351271(v=exchg.10).md">JetOSSnapshotTruncateLogInstance</a></td>
<td>Tronque le journal pour une instance spécifiée pendant une session d’instantané.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[VistaApi, classe](./vistaapi-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
