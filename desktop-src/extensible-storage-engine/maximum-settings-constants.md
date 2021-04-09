---
description: 'En savoir plus sur : constantes de paramètres maximum'
title: Nombre maximal de constantes de paramètres
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 3754732e59c9a90c74366558d9904fc13376db7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862890"
---
# <a name="maximum-settings-constants"></a>Nombre maximal de constantes de paramètres


_**S’applique à :** Windows | Serveur Windows_

## <a name="maximum-settings-constants"></a>Nombre maximal de constantes de paramètres

Ces constantes fournissent les paramètres maximaux autorisés sur les éléments d’une base de données ESE.

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
<td><p>JET_BASE_NAME_LENGTH<br />
3</p></td>
<td><p>Définit la longueur du préfixe utilisé pour nommer les fichiers utilisés par le moteur de base de données. Cette longueur s’applique au nom défini pour le paramètre système <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_MAX_COMPUTERNAME_LENGTH<br />
15</p></td>
<td><p>Définit la longueur maximale de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbBookmarkMost<br />
256</p></td>
<td><p>Taille maximale par défaut d’un signet. Cela est valide lorsque la taille de la clé reste la valeur par défaut.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbBookmarkMostMost<br />
2000</p></td>
<td><p>Taille maximale d’un signet quand esent est configuré pour avoir les plus grandes clés possibles.</p>
<p><strong>Windows 7 :</strong> JET_cbBookmarkMostMost est introduite dans Windows 7.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbNameMost<br />
64</p></td>
<td><p>Longueur maximale d’un objet, d’une colonne, d’un index ou d’un nom de propriété.</p>
<p><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 128.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbFullNameMost<br />
255</p></td>
<td><p>Longueur maximale d’une &quot; construction Name.Name.Name... &quot; .</p>
<p><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 510.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbColumnLVPageOverhead<br />
82</p></td>
<td><p>Ce nombre peut être utilisé pour calculer la quantité maximale d’un objet BLOB qui peut être stocké par le moteur de base de données sur une page de base de données unique. La formule est Max Size = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p>
<p>Cette valeur est désormais obsolète. La taille du segment de valeur longue doit être extraite avec le paramètre JET_paramLVChunkSizeMost.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbColumnMost<br />
255</p></td>
<td><p>Taille maximale des données de colonne de valeur non longue.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbLVDefaultValueMost<br />
255</p></td>
<td><p>Taille maximale d’une colonne par défaut de valeur longue (LongBinary ou LongText).</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost<br />
255</p></td>
<td><p>Taille maximale par défaut d’une clé de tri ou d’index.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMost<br />
2000</p></td>
<td><p>Taille maximale configurable d’une clé de tri ou d’index pour toute taille de page. (Voir JET_INDEXCREATE2. cbKeyMost)</p>
<p><strong>Windows 7 :</strong> JET_cbKeyMostMost est introduite dans le système d’exploitation Windows 7.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost2KBytePage<br />
500</p></td>
<td><p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 2048 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista :</strong> JET_cbKeyMost2KBytePage est introduite dans le système d’exploitation Windows Vista.</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMost4KBytePage<br />
1 000</p></td>
<td><p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 4096 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista :</strong> JET_cbKeyMost4KBytePage est introduite dans Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbKeyMost8KBytePage<br />
2000</p></td>
<td><p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 8192 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista :  </strong> JET_cbKeyMost8KBytePage est introduit dans Windows Vista</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbKeyMostMin<br />
255</p></td>
<td><p>Taille maximale autorisée minimale pour une clé d’index. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p>
<p><strong>Windows Vista :  </strong> JET_cbKeyMostMin est introduite dans Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbLimitKeyMost<br />
256</p></td>
<td><p>Taille de clé maximale lorsque la clé est formée à l’aide d’un <em>Grbit</em>Limit, tel que JET_bitStrLimit, qui est utilisé dans la fonction <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p></td>
</tr>
<tr class="odd">
<td><p>JET_cbPrimaryKeyMost<br />
255</p></td>
<td><p>Taille maximale de l’index primaire. Cela est désormais obsolète.</p></td>
</tr>
<tr class="even">
<td><p>JET_cbSecondaryKeyMost<br />
255</p></td>
<td><p>Taille maximale de l’index secondaire. Cela est désormais obsolète.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolKeyMost<br />
12</p></td>
<td><p>Nombre maximal de composants dans une clé de tri ou d’index.</p>
<p><strong>Windows Vista :  </strong> Dans Windows Vista et les versions ultérieures de Windows, la valeur est 16.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolMost<br />
0x0000fee0</p></td>
<td><p>Nombre maximal de colonnes autorisées dans une table.</p>
<p><strong>Windows XP :  </strong> La valeur 0x0000fee0 est utilisée dans Windows XP et versions ultérieures et versions ultérieures de Windows</p>
<p><strong>Windows 2000 :  </strong> La valeur 0x00007ffe est utilisée dans Windows 2000.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolFixedMost<br />
0x0000007F</p></td>
<td><p>Nombre maximal de colonnes fixes autorisées dans une table, actuellement 127.</p></td>
</tr>
<tr class="even">
<td><p>JET_ccolVarMost<br />
0x00000080</p></td>
<td><p>Nombre maximal de colonnes de longueur variable qui peuvent être contenues dans une table, actuellement 128.</p></td>
</tr>
<tr class="odd">
<td><p>JET_ccolTaggedMost<br />
(JET_ccolMost-0x000000FF)</p></td>
<td><p>Nombre maximal de colonnes avec balises pouvant être contenues dans une table, actuellement 64993.</p></td>
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

