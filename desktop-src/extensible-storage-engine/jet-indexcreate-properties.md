---
description: En savoir plus sur les propriétés de JET_INDEXCREATE
title: Propriétés de la JET_INDEXCREATE
TOCTitle: JET_INDEXCREATE properties
ms:assetid: Properties.T:Microsoft.Isam.Esent.Interop.JET_INDEXCREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_indexcreate_properties(v=EXCHG.10)
ms:contentKeyID: 55103645
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 66b6ada105e6f6d12cb754f288478e85d75a07e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127236652"
---
# <a name="jet_indexcreate-properties"></a>Propriétés de la JET_INDEXCREATE

Inclure les membres protégés  
Inclure les membres hérités  

Le type de [JET_INDEXCREATE](./jet-indexcreate-class.md) expose les membres suivants.

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
<td><a href="dn335122(v=exchg.10).md">cbKey</a></td>
<td>Obtient ou définit la longueur, en caractères, de szKey, y compris les deux valeurs null de fin.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335156(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtient ou définit la taille maximale autorisée, en octets, pour les clés dans l’index. La taille de clé maximale prise en charge minimale est JET_cbKeyMostMin (255) qui est la taille de clé maximale héritée. La taille de clé maximale dépend de la taille de page de la base de données <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. La <a href="dn351156(v=exchg.10).md">taille de clé</a>maximale peut être récupérée avec. ce paramètre est ignoré sur Windows XP et Windows Server 2003. Contrairement à l’API non managée, <strong>IndexKeyMost ()</strong> (JET_bitIndexKeyMost) n’est pas nécessaire, elle est ajoutée automatiquement.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335158(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtient ou définit la longueur maximale, en octets, de chaque colonne à stocker dans l’index.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335118(v=exchg.10).md">cConditionalColumn</a></td>
<td>Obtient ou définit le nombre de colonnes conditionnelles.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335157(v=exchg.10).md">Raise</a></td>
<td>Obtient ou définit le code d’erreur de la création de cet index.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335119(v=exchg.10).md">grbit</a></td>
<td>Obtient ou définit les options de création d’index.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335159(v=exchg.10).md">pidxUnicode</a></td>
<td>Obtient ou définit les options de comparaison Unicode facultatives.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335120(v=exchg.10).md">pSpaceHints</a></td>
<td>Obtient ou définit les indicateurs d’allocation, de maintenance et d’utilisation de l’espace.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335160(v=exchg.10).md">rgconditionalcolumn</a></td>
<td>Obtient ou définit les colonnes conditionnelles facultatives.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335121(v=exchg.10).md">szIndexName</a></td>
<td>Obtient ou définit le nom de l’index à créer.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335161(v=exchg.10).md">szKey</a></td>
<td>Obtient ou définit la description de la clé d’index. Il s’agit d’une chaîne double qui se termine par un caractère null des jetons délimités par des valeurs NULL. Chaque jeton se présente sous la forme [direction-specifier] [Column-Name], où direction-Specification a la valeur &quot; + &quot; ou &quot; - &quot; . par exemple, un szKey de &quot; + abc\0-def\0 + ghi\0 &quot; indexera les trois colonnes &quot; ABC &quot; (dans l’ordre croissant), &quot; Def &quot; (dans l’ordre décroissant) et &quot; GHI &quot; (dans l’ordre croissant).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335162(v=exchg.10).md">ulDensity</a></td>
<td>Obtient ou définit la densité de l’index.</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Référence

[Classe JET_INDEXCREATE](./jet-indexcreate-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
