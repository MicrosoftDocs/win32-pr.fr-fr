---
description: 'En savoir plus sur : JET_COLTYP'
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04588d6a057c25c0d39e42997a67a611fdfd92d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868065"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_coltyp"></a>JET_COLTYP

Le **JET_COLTYP** groupe de constantes décrit tous les types de colonne possibles qui se trouvent dans une table.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_coltypNil<br />
0</p></td>
<td><p>Type de colonne non valide.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBit<br />
1</p></td>
<td><p>Type de colonne qui autorise trois valeurs : <strong>true</strong>, <strong>false</strong>ou <strong>null</strong>. Ce type de colonne est d’une longueur d’un octet et sa taille est fixe. <strong>False</strong> trie avant <strong>true</strong>. Notez que la taille de ce type ne correspond pas à la taille du type booléen variant.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedByte<br />
2</p></td>
<td><p>Entier non signé sur 1 octet qui peut prendre des valeurs comprises entre 0 (zéro) et 255.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypShort<br />
3</p></td>
<td><p>Entier signé sur 2 octets qui peut prendre des valeurs comprises entre-32768 et 32767. Les valeurs négatives sont triées avant les valeurs positives.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLong<br />
4</p></td>
<td><p>Entier signé sur 4 octets qui peut prendre des valeurs comprises entre-2147483648 et 2147483647. Les valeurs négatives sont triées avant les valeurs positives.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypCurrency<br />
5</p></td>
<td><p>Entier signé de 8 octets qui peut prendre des valeurs comprises entre-9223372036854775808 et 9223372036854775807. Les valeurs négatives sont triées avant les valeurs positives. Ce type de colonne est identique au type de devise variant. Ce type de colonne peut également être utilisé en tant qu’entier signé de 8 octets natif.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypIEEESingle<br />
6</p></td>
<td><p>Nombre à virgule flottante simple précision (4 octets).</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypIEEEDouble<br />
7</p></td>
<td><p>Nombre à virgule flottante double précision (8 octets).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypDateTime<br />
8</p></td>
<td><p>Nombre à virgule flottante double précision (8 octets) qui représente une date en jours fractionnaires depuis l’année 1900. Ce type de colonne est identique au type de date variant.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypBinary<br />
9</p></td>
<td><p>Colonne binaire fixe ou de longueur variable d’une longueur maximale de 255 octets.</p>
<p>Ce type de colonne peut être utilisé pour implémenter un GUID s’il est configuré en tant que colonne binaire de 16 octets de longueur fixe. Le seul inconvénient est que l’ordre relatif des valeurs dans un index sur ce type de colonne ne correspond pas à l’ordre relatif du rendu de chaîne de Registre standard d’un GUID ( &quot; {0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b} &quot; ).</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypText<br />
10</p></td>
<td><p>Colonne de texte de longueur fixe ou variable qui peut contenir jusqu’à 255 caractères ASCII ou 127 caractères Unicode.</p>
<p>Toutes les chaînes sont stockées sous la forme d’un nombre de caractères compté. Les chaînes n’ont pas besoin d’être terminées par null. En outre, il n’est pas nécessaire que le nombre inclue une marque de fin null. Enfin, les caractères null incorporés peuvent être stockés.</p>
<p>Les chaînes ASCII sont toujours traitées comme non sensibles à la casse à des fins de tri et de recherche. En outre, seuls les caractères qui précèdent le premier caractère null (le cas échéant) sont pris en compte pour le tri et la recherche.</p>
<p>Les chaînes Unicode utilisent l’API Win32 <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> pour créer des clés de tri qui sont ensuite utilisées pour le tri et la recherche de ces données. Par défaut, les chaînes Unicode sont considérées comme étant dans les paramètres régionaux anglais (États-Unis) et sont triées et recherchées à l’aide des indicateurs de normalisation suivants : NORM_IGNORECASE, NORM_IGNOREKANATYPE et NORM_IGNOREWIDTH. Dans Windows 2000, il est possible de personnaliser ces indicateurs par index pour inclure également NORM_IGNORENONSPACE. Dans Windows XP et versions ultérieures, il est possible de demander n’importe quelle combinaison des indicateurs de normalisation suivants par index : LCMAP_SORTKEY, LCMAP_BYTEREV, NORM_IGNORECASE, NORM_IGNORENONSPACE, NORM_IGNORESYMBOLS, NORM_IGNOREKANATYPE, NORM_IGNOREWIDTH et SORT_STRINGSORT.</p>
<p>Dans toutes les versions, il est possible de personnaliser les paramètres régionaux par index. Les paramètres régionaux peuvent être utilisés tant que le module linguistique approprié a été installé sur l’ordinateur. Enfin, tous les caractères null rencontrés dans une chaîne Unicode sont complètement ignorés.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongBinary<br />
11</p></td>
<td><p>Colonne binaire fixe ou de longueur variable d’une longueur maximale de 2147483647 octets. Ce type est considéré comme une valeur longue. Une valeur long est spéciale, car elle peut être volumineuse et être accessible en tant que flux. Sinon, ce type est identique à JET_coltypBinary.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypLongText<br />
12</p></td>
<td><p>Colonne de texte de longueur fixe ou variable qui peut contenir jusqu’à 2147483647 caractères ASCII ou 1073741823 caractères Unicode. Ce type est considéré comme une valeur longue. Une valeur long est spéciale, car elle peut être volumineuse et être accessible en tant que flux. Sinon, ce type est identique à JET_coltypText.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypSLV<br />
13</p></td>
<td><p>Ce type de colonne est obsolète.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypUnsignedLong<br />
14</p></td>
<td><p>Entier non signé sur 4 octets qui peut prendre des valeurs comprises entre 0 (zéro) et 4294967295.</p>
<p><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypLongLong<br />
15</p></td>
<td><p>Entier signé de 8 octets qui peut prendre des valeurs comprises entre-9223372036854775808 et 9223372036854775807. Les valeurs négatives sont triées avant les valeurs positives.</p>
<p><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypGUID<br />
16</p></td>
<td><p>Colonne binaire de 16 octets de longueur fixe qui représente en mode natif le type de données GUID. Les valeurs de colonne GUID sont triées de la même façon que les valeurs qui sont triées en tant que chaînes dans un format standard (par exemple, {4999b5c0-7657-42d9-bdc1-4b779784e013}).</p>
<p><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_coltypUnsignedShort<br />
17</p></td>
<td><p>Entier non signé sur 2 octets qui peut prendre des valeurs comprises entre 0 et 65535.</p>
<p><strong>Windows Vista et Windows Server 2008 :</strong>  Ce type de colonne est pris en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_coltypMax<br />
18</p></td>
<td><p>Constante décrivant le maximum (autrement dit, un au-delà du type de colonne valide le plus grand) pris en charge par le moteur.</p>
<p>Cette valeur doit être utilisée avec précaution, car elle changera à mesure que de nouveaux types de colonne seront pris en charge. Par exemple, il a une valeur littérale différente sur Windows 2000 que sur Windows XP et versions ultérieures.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
