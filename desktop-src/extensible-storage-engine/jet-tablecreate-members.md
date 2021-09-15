---
description: 'En savoir plus sur les membres suivants : JET_TABLECREATE'
title: Membres JET_TABLECREATE
TOCTitle: JET_TABLECREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_members(v=EXCHG.10)
ms:contentKeyID: 55103926
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7f08d8fe464aec1ccf1eff51598ff8ef506d8707
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127521577"
---
# <a name="jet_tablecreate-members"></a>Membres JET_TABLECREATE

Inclure les membres protégés  
Inclure les membres hérités  

Contient les informations nécessaires à la création d’une table dans une base de données ESE. Contient les informations nécessaires à la création d’une table dans une base de données ESE.

Le type de [JET_TABLECREATE](./jet-tablecreate-class.md) expose les membres suivants.

## <a name="constructors"></a>Constructeurs

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351074(v=exchg.10).md">JET_TABLECREATE</a></td>
<td></td>
</tr>
</tbody>
</table>


Haut

## <a name="properties"></a>Propriétés

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351077(v=exchg.10).md">cbSeparateLV</a></td>
<td>Obtient ou définit la taille heuristique pour séparer un VL intrinsèque de l’enregistrement principal.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">cbtyp</a></td>
<td>Obtient ou définit un type de la fonction de rappel.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">cColumns</a></td>
<td>Obtient ou définit le nombre de colonnes à créer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">Encore</a></td>
<td>Obtient ou définit le nombre d’objets créés (colonnes + table + index + rappels).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">cIndexes</a></td>
<td>Obtient ou définit le nombre d’index à créer.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">grbit</a></td>
<td>Obtient ou définit les options de la table.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">pLVSpacehints</a></td>
<td>Obtient ou définit les indicateurs d’allocation, de maintenance et d’utilisation de l’espace pour l’arborescence LV séparée, de type <a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">pSeqSpacehints</a></td>
<td>Obtient ou définit les indicateurs d’allocation, de maintenance et d’utilisation de l’espace pour l’index séquentiel par défaut.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">rgcolumncreate</a></td>
<td>Obtient ou définit un tableau d’informations de création de colonne, de type <a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">rgindexcreate</a></td>
<td>Obtient ou définit un tableau d’index à créer, de type <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">szCallback</a></td>
<td>Obtient ou définit une fonction de rappel à utiliser pour la table. Il se présente sous la forme &quot; module ! nomfonction &quot; et suppose un code non managé. Pour une alternative, consultez <strong>JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</strong> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">szTableName</a></td>
<td>Obtient ou définit le nom de la table à créer.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">szTemplateTableName</a></td>
<td>Obtient ou définit le nom de la table à partir de laquelle hériter le DDL de base.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">TableID</a></td>
<td>Obtient ou définit le tabledid retourné.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">ulDensity</a></td>
<td>Obtient ou définit la densité de la table.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">ulPages</a></td>
<td>Obtient ou définit les pages initiales à allouer pour la table.</td>
</tr>
</tbody>
</table>


Haut

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351122(v=exchg.10).md">ContentEquals</a></td>
<td>Retourne une valeur indiquant si cette instance est égale à une autre instance.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351123(v=exchg.10).md">DeepClone</a></td>
<td>Retourne une copie complète de l’objet.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Égal à</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finaliser</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Méthode protégée" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Héritée de <a href="/dotnet/api/system.object">Object</a>.)</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Méthode publique" alt="Public method" /></td>
<td><a href="dn351076(v=exchg.10).md">ToString</a></td>
<td>Génère une représentation sous forme de chaîne de l’instance. (Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe JET_TABLECREATE](./jet-tablecreate-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
