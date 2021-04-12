---
description: 'En savoir plus sur : membres d’API'
title: Membres d’API
TOCTitle: Api members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Api
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api_members(v=EXCHG.10)
ms:contentKeyID: 55100778
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: e1debc551dc644d71568772761cb14500d2fd546
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393323"
---
# <a name="api-members"></a>Membres d’API

Inclure les membres protégés  
Inclure les membres hérités  

Versions managées de l’API ESENT. Cette classe contient des méthodes statiques qui correspondent à l’API ESENT non managée. Ces méthodes lèvent des exceptions lorsque des erreurs sont retournées. Méthodes d’assistance pour l’API ESENT. Ces JetMakeKey de retour à la ligne. Méthodes internes uniquement de l’API. Méthodes d’assistance pour l’API ESENT. Il s’agit de la conversion de données pour JetMakeKey. Méthodes d’assistance pour l’API ESENT. Ces méthodes traitent les métadonnées de base de données. Méthodes d’assistance pour l’API ESENT. Il ne s’agit pas de versions Interop de l’API, mais qui encapsulent des utilisations très courantes des fonctions. Membres d’API marqués comme obsolètes. Méthodes d’assistance pour l’API ESENT. Il ne s’agit pas de versions Interop de l’API, mais qui encapsulent des utilisations très courantes des fonctions. Méthodes d’assistance pour l’API ESENT. Il s’agit de la conversion de données pour définir des colonnes.

Le type d' [API](./api-class.md) expose les membres suivants.

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
<td><a href="dn292138(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Désérialiser un objet à partir d’une colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292115(v=exchg.10).md">DeserializeObjectFromColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Désérialiser un objet à partir d’une colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292114(v=exchg.10).md">EscrowUpdate</a></td>
<td>Effectuer une addition atomique sur une colonne. La colonne doit être de type <a href="hh577895(v=exchg.10).md">long</a>. Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292099(v=exchg.10).md">GetBookmark</a></td>
<td>Récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de JetGotoBookmark.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292098(v=exchg.10).md">GetColumnDictionary</a></td>
<td>Crée un dictionnaire qui mappe les noms de colonnes à leurs ID de colonne.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292101(v=exchg.10).md">GetTableColumnid</a></td>
<td>Obtient le ColumnID de la colonne spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292090(v=exchg.10).md">GetTableColumns (JET_SESID, JET_TABLEID)</a></td>
<td>Itère sur toutes les colonnes de la table, en retournant des informations sur chacune d’elles.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292089(v=exchg.10).md">GetTableColumns (JET_SESID, JET_DBID, chaîne)</a></td>
<td>Itère sur toutes les colonnes de la table, en retournant des informations sur chacune d’elles.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292093(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_TABLEID)</a></td>
<td>Itère sur tous les index de la table, en retournant des informations sur chacune d’elles.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292092(v=exchg.10).md">GetTableIndexes (JET_SESID, JET_DBID, chaîne)</a></td>
<td>Itère sur tous les index de la table, en retournant des informations sur chacune d’elles.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292095(v=exchg.10).md">GetTableNames</a></td>
<td>Retourne les noms des tables dans la base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292094(v=exchg.10).md">IntersectIndexes</a></td>
<td>Croise un groupe de plages d’index et retourne les signets des enregistrements qui se trouvent dans toutes les plages d’index. Consultez également <a href="dn292212(v=exchg.10).md">JetIntersectIndexes (JET_SESID, [], Int32, JET_RECORDLIST, IntersectIndexesGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292097(v=exchg.10).md">JetAddColumn</a></td>
<td>Ajoutez une nouvelle colonne à une table existante.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292096(v=exchg.10).md">JetAttachDatabase</a></td>
<td>Joint un fichier de base de données à utiliser avec une instance de base de données. Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292100(v=exchg.10).md">JetAttachDatabase2</a></td>
<td>Joint un fichier de base de données à utiliser avec une instance de base de données. Pour pouvoir utiliser la base de données, elle doit être ouverte par la suite avec <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292102(v=exchg.10).md">JetBackupInstance</a></td>
<td>Effectue une sauvegarde en continu d’une instance de, y compris toutes les bases de données attachées, vers un répertoire. Avec plusieurs méthodes de sauvegarde prises en charge par le moteur, il s’agit de la fonction la plus simple et la plus encapsulée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance</a></td>
<td>Lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292103(v=exchg.10).md">JetBeginSession</a></td>
<td>Initialise une nouvelle session ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292105(v=exchg.10).md">JetBeginTransaction</a></td>
<td>Fait en sorte qu’une session entre dans une transaction ou crée un nouveau point d’enregistrement dans une transaction existante.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292106(v=exchg.10).md">JetBeginTransaction2</a></td>
<td>Fait en sorte qu’une session entre dans une transaction ou crée un nouveau point d’enregistrement dans une transaction existante.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292107(v=exchg.10).md">JetCloseDatabase</a></td>
<td>Ferme un fichier de base de données qui a été ouvert précédemment avec <a href="dn292219(v=exchg.10).md">JetOpenDatabase (JET_SESID, String, String, JET_DBID, OpenDatabaseGrbit)</a> ou créé avec <a href="dn292118(v=exchg.10).md">JetCreateDatabase (JET_SESID, String, String, JET_DBID, CreateDatabaseGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292108(v=exchg.10).md">JetCloseFileInstance</a></td>
<td>Ferme un fichier qui a été ouvert avec JetOpenFileInstance une fois que les données de ce fichier ont été extraites à l’aide de JetReadFileInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292109(v=exchg.10).md">JetCloseTable</a></td>
<td>Ferme une table ouverte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292110(v=exchg.10).md">JetCommitTransaction</a></td>
<td>Valide les modifications apportées à l’état de la base de données pendant le point d’enregistrement en cours et les migre vers le point d’enregistrement précédent. Si le point d’enregistrement le plus à l’extérieur est validé, les modifications apportées pendant ce point d’enregistrement sont validées à l’état de la base de données et la session quitte la transaction.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292112(v=exchg.10).md">JetCompact</a></td>
<td>Effectue une copie d’une base de données existante. La copie est compactée dans un état optimal pour l’utilisation. Les données dans les données copiées seront empaquetées en fonction des mesures choisies pour les index lors de la création de l’index. De cette façon, les données compactées peuvent être stockées aussi denses que possible. Les données compactées peuvent également réserver de l’espace pour la croissance des enregistrements ou les insertions d’index suivantes.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292113(v=exchg.10).md">JetComputeStats</a></td>
<td>Parcourt chaque index d’une table pour calculer exactement le nombre d’entrées dans un index et le nombre de clés distinctes dans un index. Ces informations, ainsi que le nombre de pages de base de données allouées pour un index et l’heure actuelle du calcul, sont stockées dans les métadonnées d’index dans la base de données. Ces données peuvent être récupérées par la suite avec les opérations d’informations.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292118(v=exchg.10).md">JetCreateDatabase</a></td>
<td>Crée et attache un fichier de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292120(v=exchg.10).md">JetCreateDatabase2</a></td>
<td>Crée et attache un fichier de base de données avec une taille de base de données maximale spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292121(v=exchg.10).md">JetCreateIndex</a></td>
<td>Crée un index sur les données d’une base de données ESE. Un index peut être utilisé pour localiser rapidement des données spécifiques.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292123(v=exchg.10).md">JetCreateIndex2</a></td>
<td>Crée des index sur des données dans une base de données ESE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292122(v=exchg.10).md">JetCreateInstance</a></td>
<td>Alloue une nouvelle instance du moteur de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292126(v=exchg.10).md">JetCreateInstance2</a></td>
<td>Allouez une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique, avec un nom d’affichage spécifié.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292127(v=exchg.10).md">JetCreateTable</a></td>
<td>Créez une table vide. La table nouvellement créée est ouverte en mode exclusif.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292129(v=exchg.10).md">JetCreateTableColumnIndex3</a></td>
<td>Crée une table, ajoute des colonnes et des index sur cette table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292130(v=exchg.10).md">JetDefragment</a></td>
<td>Démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292145(v=exchg.10).md">JetDefragment2</a></td>
<td>Démarre et arrête les tâches de défragmentation de base de données qui améliorent l’Organisation des données dans une base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292131(v=exchg.10).md">JetDelete</a></td>
<td>Supprime l’enregistrement en cours dans une table de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292133(v=exchg.10).md">JetDeleteColumn</a></td>
<td>Supprime une colonne d’une table de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292132(v=exchg.10).md">JetDeleteColumn2</a></td>
<td>Supprime une colonne d’une table de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292135(v=exchg.10).md">JetDeleteIndex</a></td>
<td>Supprime un index d’une table de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292134(v=exchg.10).md">JetDeleteTable</a></td>
<td>Supprime une table d’une base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292139(v=exchg.10).md">JetDetachDatabase</a></td>
<td>Libère un fichier de base de données qui était précédemment attaché à une session de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292136(v=exchg.10).md">JetDetachDatabase2</a></td>
<td>Libère un fichier de base de données qui était précédemment attaché à une session de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292137(v=exchg.10).md">JetDupCursor</a></td>
<td>Duplique un curseur ouvert et retourne un descripteur au curseur dupliqué. Si le curseur qui était dupliqué était un curseur en lecture seule, le curseur dupliqué est également un curseur en lecture seule. Tout État lié à la construction d’une clé de recherche ou à la mise à jour d’un enregistrement n’est pas copié dans le curseur dupliqué. En outre, l’emplacement du curseur d’origine n’est pas dupliqué dans le curseur dupliqué. Le curseur dupliqué est toujours ouvert sur l’index cluster et son emplacement est toujours sur la première ligne de la table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292140(v=exchg.10).md">JetDupSession</a></td>
<td>Initialise une nouvelle session ESE dans la même instance que le sesid donné.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292142(v=exchg.10).md">JetEndExternalBackupInstance</a></td>
<td>Met fin à une session de sauvegarde externe. Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292143(v=exchg.10).md">JetEndExternalBackupInstance2</a></td>
<td>Met fin à une session de sauvegarde externe. Cette API est la dernière API d’une série d’API qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292144(v=exchg.10).md">JetEndSession</a></td>
<td>Met fin à une session.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292148(v=exchg.10).md">JetEnumerateColumns</a></td>
<td>Récupère efficacement un ensemble de colonnes et leurs valeurs à partir de l’enregistrement actuel d’un curseur ou de la mémoire tampon de copie de ce curseur. Les colonnes et les valeurs récupérées peuvent être restreintes par une liste d’ID de colonne, de nombres itagSequence et d’autres caractéristiques. Cette API de récupération de colonne est unique dans la mesure où elle retourne des informations dans la mémoire allouée dynamiquement obtenue à l’aide d’un rappel compatible réalloué fourni par l’utilisateur. Cette nouvelle flexibilité permet une récupération efficace des données de colonne avec des caractéristiques spécifiques (telles que la taille et la multiplicité) qui sont inconnues pour l’appelant. Cela élimine le besoin d’utiliser les modes de découverte de JetRetrieveColumn pour déterminer ces caractéristiques afin de configurer un dernier appel à JetRetrieveColumn qui récupérera correctement les données souhaitées.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292150(v=exchg.10).md">JetEscrowUpdate</a></td>
<td>Effectue une opération d’addition atomique sur une colonne. Cette fonction permet à plusieurs sessions de mettre à jour le même enregistrement simultanément sans conflits. Voir aussi <a href="dn292114(v=exchg.10).md">EscrowUpdate (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292147(v=exchg.10).md">JetFreeBuffer</a></td>
<td>Libère de la mémoire qui a été allouée par un appel du moteur de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292154(v=exchg.10).md">JetGetAttachInfoInstance</a></td>
<td>Utilisé lors d’une sauvegarde initiée par <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> pour interroger une instance pour obtenir les noms des fichiers de base de données qui doivent faire partie du jeu de fichiers de sauvegarde. Seules les bases de données qui sont actuellement attachées à l’instance à l’aide de <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a> sont prises en compte. Ces fichiers peuvent ensuite être ouverts à l’aide de <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> et lus à l’aide de <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292149(v=exchg.10).md">JetGetBookmark</a></td>
<td>Récupère le signet de l’enregistrement associé à l’entrée d’index à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner ce curseur dans le même enregistrement à l’aide de <a href="dn292200(v=exchg.10).md">JetGotoBookmark (JET_SESID, JET_TABLEID, [], Int32)</a>. Le signet ne doit pas dépasser <a href="dn351215(v=exchg.10).md">BookmarkMost</a> octets. Consultez également <a href="dn292099(v=exchg.10).md">GetBookmark (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292158(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNBASE)</a></td>
<td>Récupère des informations sur une colonne dans une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292151(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNDEF)</a></td>
<td>Récupère des informations sur une colonne de table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292152(v=exchg.10).md">JetGetColumnInfo (JET_SESID, JET_DBID, String, String, JET_COLUMNLIST)</a></td>
<td>Récupère des informations sur toutes les colonnes d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292153(v=exchg.10).md">JetGetCurrentIndex</a></td>
<td>Ddetermines : nom de l’index actuel d’un curseur donné. Ce nom est également utilisé pour resélectionner ultérieurement cet index comme index actuel à l’aide de <a href="dn334011(v=exchg.10).md">JetSetCurrentIndex (JET_SESID, JET_TABLEID, String)</a>. Elle peut également être utilisée pour découvrir les propriétés de cet index à l’aide de JetGetTableIndexInfo.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292155(v=exchg.10).md">JetGetCursorInfo</a></td>
<td>Détermine si une mise à jour de l’enregistrement en cours d’un curseur entraîne un conflit d’écriture, en fonction de l’état de mise à jour actuel de l’enregistrement. Il est possible qu’un conflit d’écriture soit retourné, même si JetGetCursorInfo est retourné avec succès. parce qu’une autre session peut mettre à jour l’enregistrement avant que la session actuelle puisse mettre à jour le même enregistrement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292159(v=exchg.10).md">JetGetDatabaseFileInfo (String, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292161(v=exchg.10).md">JetGetDatabaseFileInfo (String, Int32, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292160(v=exchg.10).md">JetGetDatabaseFileInfo (String, Int64, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292162(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, JET_DBINFOMISC, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292164(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, Int32, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292167(v=exchg.10).md">JetGetDatabaseInfo (JET_SESID, JET_DBID, String, JET_DbInfo)</a></td>
<td>Récupère certaines informations sur la base de données spécifiée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292168(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST)</a></td>
<td><strong>Obsolète.</strong> Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292172(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292166(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292171(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, Int32, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292169(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, String, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292173(v=exchg.10).md">JetGetIndexInfo (JET_SESID, JET_DBID, String, String, UInt16, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292170(v=exchg.10).md">JetGetInstanceInfo</a></td>
<td>Récupère des informations sur les instances qui sont en cours d’exécution.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292175(v=exchg.10).md">JetGetLock</a></td>
<td>Réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture. Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes. Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements. Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante va être effectuée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292174(v=exchg.10).md">JetGetLogInfoInstance</a></td>
<td>Utilisé lors d’une sauvegarde initiée par <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> pour interroger une instance pour obtenir les noms des fichiers correctifs de base de données et des fichiers journaux qui doivent faire partie du jeu de fichiers de sauvegarde. Ces fichiers peuvent ensuite être ouverts à l’aide de <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a> et lus à l’aide de <a href="dn332987(v=exchg.10).md">JetReadFileInstance (JET_INSTANCE, JET_HANDLE, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292177(v=exchg.10).md">JetGetLS</a></td>
<td>Permet à l’application de récupérer le descripteur de contexte appelé stockage local qui est associé à un curseur ou la table associée à ce curseur. Ce descripteur de contexte doit avoir été défini précédemment à l’aide <a href="dn334015(v=exchg.10).md">de JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)</a>. JetGetLS peut également être utilisé pour extraire simultanément le descripteur de contexte actuel d’un curseur ou d’une table et réinitialiser ce handle de contexte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292179(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_OBJECTLIST)</a></td>
<td>Récupère des informations sur les objets de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292178(v=exchg.10).md">JetGetObjectInfo (JET_SESID, JET_DBID, JET_objtyp, String, JET_OBJECTINFO)</a></td>
<td>Récupère des informations sur les objets de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292181(v=exchg.10).md">JetGetRecordPosition</a></td>
<td>Retourne la position fractionnaire de l’enregistrement actif dans l’index actuel sous la forme d’une structure <a href="dn335256(v=exchg.10).md">JET_RECPOS</a> . Voir aussi <a href="dn292207(v=exchg.10).md">JetGotoPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292180(v=exchg.10).md">JetGetSecondaryIndexBookmark</a></td>
<td>Récupère un signet spécial pour l’entrée d’index secondaire à la position actuelle d’un curseur. Ce signet peut ensuite être utilisé pour repositionner efficacement ce curseur sur la même entrée d’index à l’aide de JetGotoSecondaryIndexBookmark. Cela est particulièrement utile lors du repositionnement sur un index secondaire qui contient des clés dupliquées ou qui contient plusieurs entrées d’index pour le même enregistrement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292182(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String, Int32)</a></td>
<td>Obtient les options de configuration de base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292185(v=exchg.10).md">JetGetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</a></td>
<td>Obtient les options de configuration de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292186(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, JET_COLUMNID, JET_COLUMNDEF)</a></td>
<td>Récupère des informations sur une colonne de table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292187(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNDEF)</a></td>
<td>Récupère des informations sur une colonne de table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292189(v=exchg.10).md">JetGetTableColumnInfo (JET_SESID, JET_TABLEID, String, JET_COLUMNLIST)</a></td>
<td>Récupère des informations sur toutes les colonnes de la table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292191(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST)</a></td>
<td><strong>Obsolète.</strong> Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292190(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXID, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292196(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, JET_INDEXLIST, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292193(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, Int32, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292192(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, String, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292195(v=exchg.10).md">JetGetTableIndexInfo (JET_SESID, JET_TABLEID, String, UInt16, JET_IdxInfo)</a></td>
<td>Récupère des informations sur les index d’une table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292197(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_DBID, JET_TblInfo)</a></td>
<td>Récupère différents éléments d’informations sur une table dans une base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292198(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, JET_OBJECTINFO, JET_TblInfo)</a></td>
<td>Récupère différents éléments d’informations sur une table dans une base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292201(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, Int32, JET_TblInfo)</a></td>
<td>Récupère différents éléments d’informations sur une table dans une base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292202(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, [], JET_TblInfo)</a></td>
<td>Récupère différents éléments d’informations sur une table dans une base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292204(v=exchg.10).md">JetGetTableInfo (JET_SESID, JET_TABLEID, String, JET_TblInfo)</a></td>
<td>Récupère différents éléments d’informations sur une table dans une base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292199(v=exchg.10).md">JetGetTruncateLogInfoInstance</a></td>
<td>Utilisé lors d’une sauvegarde initiée par <a href="dn292104(v=exchg.10).md">JetBeginExternalBackupInstance (JET_INSTANCE, BeginExternalBackupGrbit)</a> pour interroger une instance pour connaître les noms des fichiers du journal des transactions qui peuvent être supprimés en toute sécurité une fois la sauvegarde terminée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292203(v=exchg.10).md">JetGetVersion</a></td>
<td>Récupère la version du moteur de base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292200(v=exchg.10).md">JetGotoBookmark</a></td>
<td>Positionne un curseur sur une entrée d’index pour l’enregistrement associé au signet spécifié. Le signet peut être utilisé avec n’importe quel index défini sur une table. Le signet d’un enregistrement peut être récupéré à l’aide de <a href="dn292149(v=exchg.10).md">JetGetBookmark (JET_SESID, JET_TABLEID, [], Int32, Int32)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292207(v=exchg.10).md">JetGotoPosition</a></td>
<td>Déplace un curseur vers un nouvel emplacement qui est une fraction de la façon dont l’index actuel est utilisé. Voir aussi <a href="dn292181(v=exchg.10).md">JetGetRecordPosition (JET_SESID, JET_TABLEID, JET_RECPOS)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark</a></td>
<td>Positionne un curseur sur une entrée d’index associée au signet d’index secondaire spécifié. Le signet de l’index secondaire doit être utilisé avec le même index sur la même table que celle à partir de laquelle il a été récupéré à l’origine. Le signet d’index secondaire d’une entrée d’index peut être récupéré à l’aide de <a href="dn292205(v=exchg.10).md">JetGotoSecondaryIndexBookmark (JET_SESID, JET_TABLEID, [], Int32, [], Int32, GotoSecondaryIndexBookmarkGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292206(v=exchg.10).md">JetGrowDatabase</a></td>
<td>Étend la taille d’une base de données qui est actuellement ouverte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292208(v=exchg.10).md">JetIdle</a></td>
<td>Effectue des tâches de nettoyage inactives ou vérifie l’état de la Banque des versions dans ESE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292209(v=exchg.10).md">JetIndexRecordCount</a></td>
<td>Compte le nombre d’entrées dans l’index actuel à partir de la position actuelle vers l’avant. La position actuelle est incluse dans le nombre. Le nombre peut être supérieur au nombre total d’enregistrements dans la table si l’index actuel est sur une colonne à valeurs multiples et que les instances de la colonne ont des valeurs multiples. Si la table est vide, la valeur 0 est retournée pour le nombre.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292210(v=exchg.10).md">JetInit</a></td>
<td>Initialisez le moteur de base de données ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292214(v=exchg.10).md">JetInit2</a></td>
<td>Initialisez le moteur de base de données ESENT.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292212(v=exchg.10).md">JetIntersectIndexes</a></td>
<td>Calcule l’intersection entre plusieurs jeux d’entrées d’index à partir d’index secondaires différents sur la même table. Cette opération est utile pour Rechercher l’ensemble des enregistrements d’une table qui correspondent à plusieurs critères qui peuvent être exprimés à l’aide de plages d’index. Consultez également <a href="dn292094(v=exchg.10).md">IntersectIndexes (JET_SESID, [])</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292216(v=exchg.10).md">JetMakeKey</a></td>
<td>Construit des clés de recherche qui peuvent ensuite être utilisées par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292218(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, JET_Move, MoveGrbit)</a></td>
<td>Naviguer dans un index. Le curseur peut être positionné au début ou à la fin de l’index et déplacé vers l’arrière et vers l’avant par un nombre spécifié d’entrées d’index. Consultez également <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a></td>
<td>Naviguer dans un index. Le curseur peut être positionné au début ou à la fin de l’index et déplacé vers l’arrière et vers l’avant par un nombre spécifié d’entrées d’index. Consultez également <a href="dn334150(v=exchg.10).md">TryMoveFirst (JET_SESID, JET_TABLEID)</a>, <a href="dn334140(v=exchg.10).md">TryMoveLast (JET_SESID, JET_TABLEID)</a>, <a href="dn334095(v=exchg.10).md">TryMoveNext (JET_SESID, JET_TABLEID)</a>, <a href="dn334144(v=exchg.10).md">TryMovePrevious (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292219(v=exchg.10).md">JetOpenDatabase</a></td>
<td>Ouvre une base de données précédemment attachée avec <a href="dn292096(v=exchg.10).md">JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)</a>, à utiliser avec une session de base de données. Cette fonction peut être appelée plusieurs fois pour la même base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292230(v=exchg.10).md">JetOpenFileInstance</a></td>
<td>Ouvre une base de données attachée, un fichier de correctif de base de données ou un fichier journal de transactions d’une instance active pour effectuer une sauvegarde de diffusion en continu floue. Les données de ces fichiers peuvent ensuite être lues par le handle retourné à l’aide de JetReadFileInstance. Le handle retourné doit être fermé à l’aide de JetCloseFileInstance. Une sauvegarde externe de l’instance doit avoir été précédemment lancée à l’aide de JetBeginExternalBackupInstance.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292234(v=exchg.10).md">JetOpenTable</a></td>
<td>Ouvre un curseur sur une table créée précédemment.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292231(v=exchg.10).md">JetOpenTempTable</a></td>
<td>Crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle. Consultez également <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292232(v=exchg.10).md">JetOpenTempTable2</a></td>
<td>Crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle. Consultez également <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn292233(v=exchg.10).md">JetOpenTempTable3 (JET_SESID, [], Int32, JET_UNICODEINDEX, TempTableGrbit, JET_TABLEID, [])</a>. <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292233(v=exchg.10).md">JetOpenTempTable3</a></td>
<td>Crée une table temporaire avec un index unique. Une table temporaire stocke et récupère des enregistrements comme une table ordinaire créée à l’aide de JetCreateTableColumnIndex. Toutefois, les tables temporaires sont beaucoup plus rapides que les tables ordinaires en raison de leur nature volatile. Ils peuvent également être utilisés pour trier et effectuer très rapidement la suppression des doublons sur les jeux d’enregistrements lorsque vous y accédez de manière purement séquentielle. Consultez également <a href="dn292231(v=exchg.10).md">JetOpenTempTable (JET_SESID, [], Int32, TempTableGrbit, JET_TABLEID, [])</a>, <a href="dn335326(v=exchg.10).md">JetOpenTemporaryTable (JET_SESID, JET_OPENTEMPORARYTABLE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332998(v=exchg.10).md">JetOSSnapshotFreeze</a></td>
<td>Démarre un instantané. Pendant que l’instantané est en cours, aucune activité d’écriture sur le disque par le moteur ne peut avoir lieu.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn292235(v=exchg.10).md">JetOSSnapshotPrepare</a></td>
<td>Commence les préparations pour une session d’instantané. Une session d’instantané est un intervalle de temps dans lequel le moteur n’émet pas d’e/s d’écriture sur le disque, de sorte que le moteur peut participer à une session d’instantané de volume (lorsqu’il est piloté par un enregistreur d’instantané).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332986(v=exchg.10).md">JetOSSnapshotThaw</a></td>
<td>Notifie le moteur qu’il peut reprendre des opérations d’e/s normales après une période de blocage et une capture instantanée réussie.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332988(v=exchg.10).md">JetPrepareUpdate</a></td>
<td>Préparez un curseur pour la mise à jour.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332987(v=exchg.10).md">JetReadFileInstance</a></td>
<td>Récupère le contenu d’un fichier ouvert avec <a href="dn292230(v=exchg.10).md">JetOpenFileInstance (JET_INSTANCE, String, JET_HANDLE, Int64, Int64)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332989(v=exchg.10).md">JetRegisterCallback</a></td>
<td>Permet à l’application de configurer le moteur de base de données pour émettre des notifications à l’application pour des événements spécifiques. Ces notifications sont associées à une table spécifique et restent effectives uniquement jusqu’à ce que l’instance contenant la table soit arrêtée à l’aide de <a href="dn334020(v=exchg.10).md">JetTerm (JET_INSTANCE)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332990(v=exchg.10).md">JetRenameColumn</a></td>
<td>Modifie le nom d’une colonne existante.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332993(v=exchg.10).md">JetRenameTable</a></td>
<td>Modifie le nom d’une table existante.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332991(v=exchg.10).md">JetResetSessionContext</a></td>
<td>Dissocie une session du thread actuel. Elle doit être utilisée conjointement avec <a href="dn334027(v=exchg.10).md">JetSetSessionContext (JET_SESID, IntPtr)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332994(v=exchg.10).md">JetResetTableSequential</a></td>
<td>Notifie le moteur de base de données que l’application n’analyse plus la totalité de l’index sur lequel le curseur est positionné. Cet appel inverse une notification envoyée par <a href="dn334018(v=exchg.10).md">JetSetTableSequential (JET_SESID, JET_TABLEID, SetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332992(v=exchg.10).md">JetRestoreInstance</a></td>
<td>Restaure et récupère une sauvegarde en continu d’une instance, y compris toutes les bases de données attachées. Il est conçu pour fonctionner avec une sauvegarde créée avec la fonction <a href="dn292102(v=exchg.10).md">JetBackupInstance (JET_INSTANCE, String, BackupGrbit, JET_PFNSTATUS)</a> . Il s’agit de la fonction de restauration la plus simple et la plus encapsulée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332995(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn332997(v=exchg.10).md">JetRetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, Int32, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334004(v=exchg.10).md">JetRetrieveColumns</a></td>
<td>Récupère plusieurs valeurs de colonne de l’enregistrement actuel en une seule opération. Un tableau de structures de JET_RETRIEVECOLUMN est utilisé pour décrire l’ensemble des valeurs de colonne à récupérer et pour décrire les mémoires tampons de sortie pour chaque valeur de colonne à récupérer.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334002(v=exchg.10).md">JetRetrieveKey</a></td>
<td>Récupère la clé de l’entrée d’index à la position actuelle d’un curseur. Consultez également <a href="dn334085(v=exchg.10).md">RetrieveKey (JET_SESID, JET_TABLEID, RetrieveKeyGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334001(v=exchg.10).md">JetRollback</a></td>
<td>Annule les modifications apportées à l’état de la base de données et retourne au dernier point d’enregistrement. JetRollback ferme également tous les curseurs ouverts pendant le point d’enregistrement. Si le point d’enregistrement le plus à l’extérieur est annulé, la session va quitter la transaction.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334003(v=exchg.10).md">JetSeek</a></td>
<td>Positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée. Une clé de recherche doit avoir été construite précédemment à l’aide de <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Consultez également <a href="dn334145(v=exchg.10).md">TrySeek (JET_SESID, JET_TABLEID, SeekGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334009(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La fonction JetSetColumn modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours. Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue (une colonne de type <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LONGBINARY</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334008(v=exchg.10).md">JetSetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], Int32, Int32, SetColumnGrbit, JET_SETINFO)</a></td>
<td>La fonction JetSetColumn modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou à mettre à jour l’enregistrement en cours. Elle peut remplacer une valeur existante, ajouter une nouvelle valeur à une séquence de valeurs dans une colonne à valeurs multiples, supprimer une valeur d’une séquence de valeurs dans une colonne à valeurs multiples, ou mettre à jour tout ou partie d’une valeur longue (une colonne de type <a href="hh577895(v=exchg.10).md">LONGTEXT</a> ou <a href="hh577895(v=exchg.10).md">LONGBINARY</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334010(v=exchg.10).md">JetSetColumnDefaultValue</a></td>
<td>Modifie la valeur par défaut d’une colonne existante.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334006(v=exchg.10).md">JetSetColumns</a></td>
<td>Permet à une application de définir plusieurs valeurs de colonne en une seule opération. Un tableau de structures de <a href="dn335260(v=exchg.10).md">JET_SETCOLUMN</a> est utilisé pour décrire l’ensemble des valeurs de colonne à définir, et pour décrire les mémoires tampons d’entrée pour chaque valeur de colonne à définir.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334011(v=exchg.10).md">JetSetCurrentIndex</a></td>
<td>Définit l’index actuel d’un curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334005(v=exchg.10).md">JetSetCurrentIndex2</a></td>
<td>Définit l’index actuel d’un curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334012(v=exchg.10).md">JetSetCurrentIndex3</a></td>
<td>Définit l’index actuel d’un curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334013(v=exchg.10).md">JetSetCurrentIndex4</a></td>
<td>Définit l’index actuel d’un curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334014(v=exchg.10).md">JetSetDatabaseSize</a></td>
<td>Définit la taille d’un fichier de base de données non ouvert.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334024(v=exchg.10).md">JetSetIndexRange</a></td>
<td>Limite temporairement l’ensemble d’entrées d’index que le curseur peut suivre à l’aide de <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a> à ceux qui démarrent à partir de l’entrée d’index actuelle et se terminent à l’entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et les critères liés spécifiés. Une clé de recherche doit avoir été construite précédemment à l’aide de <a href="dn292216(v=exchg.10).md">JetMakeKey (JET_SESID, JET_TABLEID, [], Int32, MakeKeyGrbit)</a>. Consultez également <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334015(v=exchg.10).md">JetSetLS</a></td>
<td>Permet à l’application d’associer un handle de contexte appelé stockage local avec un curseur ou la table associée à ce curseur. Ce descripteur de contexte peut être utilisé par l’application pour stocker les données auxiliaires associées à un curseur ou une table. L’application est notifiée ultérieurement à l’aide d’un rappel d’exécution lorsque le handle de contexte doit être libéré. Cela permet d’associer l’État alloué dynamiquement à un curseur ou une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334027(v=exchg.10).md">JetSetSessionContext</a></td>
<td>Associe une session au thread actuel à l’aide du handle de contexte donné. Cette association remplace la spécification de moteur par défaut selon laquelle une transaction pour une session donnée doit se produire entièrement sur le même thread. Utilisez <a href="dn332991(v=exchg.10).md">JetResetSessionContext (JET_SESID)</a> pour supprimer l’Association.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334028(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, JET_CALLBACK, String)</a></td>
<td>Définit les options de configuration de la base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334017(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, Int32, String)</a></td>
<td>Définit les options de configuration de la base de données.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334029(v=exchg.10).md">JetSetSystemParameter (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</a></td>
<td>Définit les options de configuration de la base de données.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334018(v=exchg.10).md">JetSetTableSequential</a></td>
<td>Notifie le moteur de base de données que l’application analyse la totalité de l’index sur lequel le curseur est positionné. Par conséquent, les méthodes utilisées pour accéder aux données d’index seront paramétrées pour rendre ce scénario aussi rapide que possible. Consultez également <a href="dn332994(v=exchg.10).md">JetResetTableSequential (JET_SESID, JET_TABLEID, ResetTableSequentialGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334032(v=exchg.10).md">JetStopBackupInstance</a></td>
<td>Empêche l’activité relative à la sauvegarde en continu de se poursuivre sur une instance en cours d’exécution spécifique, ce qui met fin à la sauvegarde en continu de manière prévisible.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334035(v=exchg.10).md">JetStopServiceInstance</a></td>
<td>Prépare une instance pour l’arrêt.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334020(v=exchg.10).md">JetTerm</a></td>
<td>Termine une instance qui a été créée avec <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> ou <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334037(v=exchg.10).md">JetTerm2</a></td>
<td>Termine une instance qui a été créée avec <a href="dn292210(v=exchg.10).md">JetInit (JET_INSTANCE)</a> ou <a href="dn292122(v=exchg.10).md">JetCreateInstance (JET_INSTANCE, String)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334022(v=exchg.10).md">JetTruncateLogInstance</a></td>
<td>Utilisé lors d’une sauvegarde initiée par JetBeginExternalBackup pour supprimer tous les fichiers journaux des transactions qui ne seront plus nécessaires une fois la sauvegarde actuelle terminée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334019(v=exchg.10).md">JetUnregisterCallback</a></td>
<td>Configure le moteur de base de données pour qu’il cesse d’émettre des notifications à l’application, comme demandé précédemment via <a href="dn332989(v=exchg.10).md">JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334036(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID)</a></td>
<td>La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante. La suppression d’une ligne de table s’effectue en appelant <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334023(v=exchg.10).md">JetUpdate (JET_SESID, JET_TABLEID, [], Int32, Int32)</a></td>
<td>La fonction JetUpdate effectue une opération de mise à jour, notamment l’insertion d’une nouvelle ligne dans une table ou la mise à jour d’une ligne existante. La suppression d’une ligne de table s’effectue en appelant <a href="dn292131(v=exchg.10).md">JetDelete (JET_SESID, JET_TABLEID)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334042(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Boolean, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334026(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Byte, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334044(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, [], MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334025(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, DateTime, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334046(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, double, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334030(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Guid, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334048(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int16, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334031(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int32, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334050(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Int64, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334033(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, Single, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334052(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt16, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334054(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt32, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334034(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, UInt64, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334038(v=exchg.10).md">MakeKey (JET_SESID, JET_TABLEID, chaîne, encodage, MakeKeyGrbit)</a></td>
<td>Construit une clé de recherche qui peut ensuite être utilisée par <a href="dn334003(v=exchg.10).md">JetSeek (JET_SESID, JET_TABLEID, SeekGrbit)</a> et <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334058(v=exchg.10).md">MoveAfterLast</a></td>
<td>Positionnez le curseur après le dernier enregistrement de la table. Un déplacement suivant place le curseur sur le dernier enregistrement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334057(v=exchg.10).md">MoveBeforeFirst</a></td>
<td>Positionnez le curseur avant le premier enregistrement de la table. Un prochain déplacement suivant placera le curseur sur le premier enregistrement.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334040(v=exchg.10).md">ResetIndexRange</a></td>
<td>Supprime une plage d’index créée avec <a href="dn334024(v=exchg.10).md">JetSetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a> ou <a href="dn334099(v=exchg.10).md">TrySetIndexRange (JET_SESID, JET_TABLEID, SetIndexRangeGrbit)</a>. Si aucune plage d’index n’est présente, cette méthode n’a aucun effet.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif. En plus de récupérer la valeur réelle de la colonne, JetRetrieveColumn peut également être utilisé pour récupérer la taille d’une colonne, avant de récupérer les données de la colonne elle-même afin que les tampons d’application puissent être dimensionnés de manière appropriée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334045(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne booléenne de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334078(v=exchg.10).md">RetrieveColumnAsBoolean (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne booléenne de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334047(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne d’octets à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334074(v=exchg.10).md">RetrieveColumnAsByte (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne d’octets à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334077(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne DateTime à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334051(v=exchg.10).md">RetrieveColumnAsDateTime (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne DateTime à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334053(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne double de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334084(v=exchg.10).md">RetrieveColumnAsDouble (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne double de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334056(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne flottante à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334092(v=exchg.10).md">RetrieveColumnAsFloat (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne flottante à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334093(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne GUID à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334061(v=exchg.10).md">RetrieveColumnAsGuid (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne GUID à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334062(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334098(v=exchg.10).md">RetrieveColumnAsInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne Int16 à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334100(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334068(v=exchg.10).md">RetrieveColumnAsInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne Int32 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334066(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334091(v=exchg.10).md">RetrieveColumnAsInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334067(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. L’encodage Unicode est utilisé.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334103(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, encodage)</a></td>
<td>Récupère une valeur de colonne de type chaîne à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334070(v=exchg.10).md">RetrieveColumnAsString (JET_SESID, JET_TABLEID, JET_COLUMNID, encodage, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne de type chaîne à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334069(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne UInt16 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334106(v=exchg.10).md">RetrieveColumnAsUInt16 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne UInt16 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334108(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne UInt32 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334073(v=exchg.10).md">RetrieveColumnAsUInt32 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne UInt32 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334072(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère une valeur de colonne UInt64 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334113(v=exchg.10).md">RetrieveColumnAsUInt64 (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit)</a></td>
<td>Récupère une valeur de colonne UInt64 de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334075(v=exchg.10).md">RetrieveColumns</a></td>
<td>Récupère des colonnes dans les objets ColumnValue.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334076(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Récupère la taille d’une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334117(v=exchg.10).md">RetrieveColumnSize (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32, RetrieveColumnGrbit)</a></td>
<td>Récupère la taille d’une valeur de colonne unique à partir de l’enregistrement en cours. L’enregistrement est l’enregistrement associé à l’entrée d’index à la position actuelle du curseur. Cette fonction peut également récupérer une colonne d’un enregistrement en cours de création dans le tampon de copie de curseur. Cette fonction peut également récupérer des données de colonne à partir d’une entrée d’index qui fait référence à l’enregistrement actif.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334085(v=exchg.10).md">RetrieveKey</a></td>
<td>Récupère la clé de l’entrée d’index à la position actuelle d’un curseur.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334120(v=exchg.10).md">SerializeObjectToColumn</a></td>
<td>Écrire une forme sérialisée d’un objet dans une colonne.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334123(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Boolean)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334080(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Byte)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334121(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [])</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334082(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, DateTime)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334125(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, double)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334081(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Guid)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334127(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int16)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334083(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int32)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334130(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Int64)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334087(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, Single)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334132(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt16)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334086(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt32)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334135(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, UInt64)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334089(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, [], SetColumnGrbit)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334136(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, chaîne, encodage)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334090(v=exchg.10).md">SetColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, chaîne, encodage, SetColumnGrbit)</a></td>
<td>Modifie une valeur de colonne unique dans un enregistrement modifié à insérer ou pour mettre à jour l’enregistrement en cours.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334138(v=exchg.10).md">SetColumns</a></td>
<td>Définit des colonnes à partir d’objets ColumnValue.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334139(v=exchg.10).md">TryGetLock</a></td>
<td>Réserver explicitement la possibilité de mettre à jour une ligne, un verrou en écriture ou d’empêcher explicitement une ligne d’être mise à jour par une autre session, verrou de lecture. Normalement, les verrous d’écriture de ligne sont acquis implicitement en raison de la mise à jour des lignes. Les verrous de lecture ne sont généralement pas requis en raison du contrôle de version des enregistrements. Toutefois, dans certains cas, une transaction peut souhaiter verrouiller explicitement une ligne pour appliquer la sérialisation, ou pour s’assurer qu’une opération suivante va être effectuée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334094(v=exchg.10).md">TryMove</a></td>
<td>Essayez de naviguer dans un index. Si la navigation réussie, cette méthode retourne true. S’il n’existe aucun enregistrement pour accéder à cette méthode, retourne false. une exception est levée pour d’autres erreurs.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334150(v=exchg.10).md">TryMoveFirst</a></td>
<td>Essayez de vous déplacer vers le premier enregistrement de la table. Si la table est vide, la valeur false est retournée. Si une autre erreur se produit, une exception est levée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334140(v=exchg.10).md">TryMoveLast</a></td>
<td>Essayez de vous déplacer vers le dernier enregistrement de la table. Si la table est vide, la valeur false est retournée. Si une autre erreur se produit, une exception est levée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334095(v=exchg.10).md">TryMoveNext</a></td>
<td>Essayez de vous déplacer vers l’enregistrement suivant dans la table. Si aucun enregistrement suivant n’est présent, la valeur false est retournée, si une erreur différente est rencontrée, une exception est levée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334144(v=exchg.10).md">TryMovePrevious</a></td>
<td>Essayez de vous déplacer vers l’enregistrement précédent dans la table. S’il n’existe pas d’enregistrement précédent, la valeur false est retournée, si une erreur différente est rencontrée, une exception est levée.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334096(v=exchg.10).md">TryOpenTable</a></td>
<td>Essayez d’ouvrir une table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334145(v=exchg.10).md">TrySeek</a></td>
<td>Positionne efficacement un curseur sur une entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et l’inégalité spécifiée. Une clé de recherche doit avoir été construite précédemment à l’aide de JetMakeKey.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membre statique" alt="Static member" /></td>
<td><a href="dn334099(v=exchg.10).md">TrySetIndexRange</a></td>
<td>Limite temporairement l’ensemble d’entrées d’index que le curseur peut suivre à l’aide de JetMove pour ceux qui commencent à l’entrée d’index actuelle et se terminent à l’entrée d’index qui correspond aux critères de recherche spécifiés par la clé de recherche dans ce curseur et les critères liés spécifiés. Une clé de recherche doit avoir été construite précédemment à l’aide de JetMakeKey. Retourne la valeur true si la plage d’index n’est pas vide ; sinon, false.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
