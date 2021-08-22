---
description: 'En savoir plus sur les membres suivants : JET_OPENTEMPORARYTABLE'
title: Membres JET_OPENTEMPORARYTABLE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_OPENTEMPORARYTABLE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Vista.JET_OPENTEMPORARYTABLE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_opentemporarytable_members(v=EXCHG.10)
ms:contentKeyID: 55104223
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 934ea18663e2fd2de786bb44d32482f42fd45d38b9e6ec23e73caf815560b264
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119560039"
---
# <a name="jet_opentemporarytable-members"></a>Membres JET_OPENTEMPORARYTABLE

Inclure les membres protégés  
Inclure les membres hérités  

Collection de paramètres pour la méthode JetOpenTemporaryTable.

Le type de [JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md) expose les membres suivants.

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
<td><a href="dn351224(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a></td>
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
<td><a href="dn335290(v=exchg.10).md">cbKeyMost</a></td>
<td>Obtient ou définit la taille maximale d’une clé représentant une ligne donnée. La taille de clé maximale peut être définie pour contrôler la façon dont les clés sont tronquées. La troncation de clé est importante, car elle peut affecter le moment où les lignes sont considérées comme distinctes. si ce paramètre a la valeur 0 ou 255, la taille maximale de la clé et sa sémantique restent identiques à la taille de clé maximale prise en charge par Windows Server 2003. Ce paramètre peut également être défini sur une valeur supérieure en fonction de la taille de page de la base de données pour l’instance <a href="hh596135(v=exchg.10).md">DatabasePageSize</a>. Pour <a href="dn335292(v=exchg.10).md">plus</a> d’informations, consultez.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351219(v=exchg.10).md">cbVarSegMac</a></td>
<td>Obtient ou définit la quantité maximale de données qui seront utilisées à partir de n’importe quelle variable lengthcolumn pour construire une clé pour une ligne donnée. Ce paramètre peut être utilisé pour contrôler la quantité d’espace clé consommée par une colonne clé donnée. Cette limite est en octets. Si ce paramètre est égal à zéro ou est identique à la propriété <a href="dn335290(v=exchg.10).md">cbKeyMost</a> , aucune limite n’est appliquée.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335287(v=exchg.10).md">ccolumn</a></td>
<td>Obtient ou définit le nombre de colonnes dans <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351232(v=exchg.10).md">grbit</a></td>
<td>Obtient ou définit les options de la table Temp.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335288(v=exchg.10).md">pidxunicode</a></td>
<td>Obtient ou définit les indicateurs de normalisation et l’ID de paramètres régionaux à utiliser pour comparer les données de colonne de clé Unicode dans la table temporaire. Lorsque ce paramètre a la valeur null, le LCID par défaut est utilisé pour comparer les colonnes clés Unicode de la table temporaire. Le LCID par défaut est le paramètre régional anglais (États-Unis). Lorsque ce paramètre a la valeur null, les indicateurs de normalisation par défaut sont utilisés pour comparer les données de colonne de clé Unicode dans la table temporaire. Les indicateurs de normalisation par défaut sont les suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351228(v=exchg.10).md">prgcolumndef</a></td>
<td>Obtient ou définit les définitions de colonne pour les colonnes créées dans la table temporaire.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn351233(v=exchg.10).md">prgcolumnid</a></td>
<td>Obtient ou définit la mémoire tampon de sortie qui reçoit le tableau d’ID de colonne générés pendant la création de la table temporaire. Les ID de colonne dans ce tableau correspondent exactement au tableau d’entrée des définitions de colonne. Par conséquent, la taille de cette mémoire tampon doit correspondre à la taille de <a href="dn351228(v=exchg.10).md">prgcolumndef</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propriété publique" alt="Public property" /></td>
<td><a href="dn335293(v=exchg.10).md">TableID</a></td>
<td>Obtient le descripteur de table pour la table temporaire créée à la suite d’un appel réussi à JetOpenTemporaryTable.</td>
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
<td><a href="dn335286(v=exchg.10).md">ToString</a></td>
<td>Retourne une <a href="/dotnet/api/system.string">chaîne</a> qui représente le <a href="dn351217(v=exchg.10).md">JET_OPENTEMPORARYTABLE</a>actuel. (Substitue <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.)</td>
</tr>
</tbody>
</table>


Haut

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_OPENTEMPORARYTABLE](./jet-opentemporarytable-class.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
