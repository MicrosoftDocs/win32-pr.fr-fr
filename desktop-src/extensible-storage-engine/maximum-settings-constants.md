---
description: 'en savoir plus sur : nombre maximal de constantes de Paramètres'
title: nombre maximal de constantes de Paramètres
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
ms.openlocfilehash: 38184176e5803cfd22d7b63f9d85e5b62f7ecff1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478965"
---
# <a name="maximum-settings-constants"></a>nombre maximal de constantes de Paramètres


_**S’applique à :** Windows | Windows Serveurs_

## <a name="maximum-settings-constants"></a>nombre maximal de constantes de Paramètres

Ces constantes fournissent les paramètres maximaux autorisés sur les éléments d’une base de données ESE.


| <p>Constante/valeur</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>Définit la longueur du préfixe utilisé pour nommer les fichiers utilisés par le moteur de base de données. Cette longueur s’applique au nom défini pour le paramètre système <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> .</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>Définit la longueur maximale de <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>.</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>Taille maximale par défaut d’un signet. Cela est valide lorsque la taille de la clé reste la valeur par défaut.</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>Taille maximale d’un signet quand esent est configuré pour avoir les plus grandes clés possibles.</p><p><strong>Windows 7 :</strong> JET_cbBookmarkMostMost est introduite dans Windows 7.</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>Longueur maximale d’un objet, d’une colonne, d’un index ou d’un nom de propriété.</p><p><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 128.</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>La longueur maximale d’un « name.name.name... » composer.</p><p><strong>Remarque</strong>  Si la valeur est Unicode, la valeur est 510.</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>Ce nombre peut être utilisé pour calculer la quantité maximale d’un objet BLOB qui peut être stocké par le moteur de base de données sur une page de base de données unique. La formule est Max Size = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead.</p><p>Cette valeur est désormais obsolète. La taille du segment de valeur longue doit être extraite avec le paramètre JET_paramLVChunkSizeMost.</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>Taille maximale des données de colonne de valeur non longue.</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>Taille maximale d’une colonne par défaut de valeur longue (LongBinary ou LongText).</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>Taille maximale par défaut d’une clé de tri ou d’index.</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>Taille maximale configurable d’une clé de tri ou d’index pour toute taille de page. (Voir JET_INDEXCREATE2. cbKeyMost)</p><p><strong>Windows 7 :</strong> JET_cbKeyMostMost est introduite dans le système d’exploitation Windows 7.</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 2048 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista :</strong> JET_cbKeyMost2KBytePage est introduite dans le système d’exploitation Windows Vista.</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1 000</p> | <p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 4096 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista :</strong> JET_cbKeyMost4KBytePage est introduite dans Windows Vista.</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>Taille maximale configurable maximale autorisée pour une clé d’index dans une base de données utilisant des pages de 8192 octets. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista :</strong> JET_cbKeyMost8KBytePage est introduite dans Windows Vista</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>Taille maximale autorisée minimale pour une clé d’index. Pour plus d’informations, consultez <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> .</p><p><strong>Windows Vista :</strong> JET_cbKeyMostMin est introduite dans Windows Vista.</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>Taille de clé maximale lorsque la clé est formée à l’aide d’un <em>Grbit</em>Limit, tel que JET_bitStrLimit, qui est utilisé dans la fonction <a href="gg269329(v=exchg.10).md">JetMakeKey</a> .</p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>Taille maximale de l’index primaire. Cela est désormais obsolète.</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>Taille maximale de l’index secondaire. Cela est désormais obsolète.</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>Nombre maximal de composants dans une clé de tri ou d’index.</p><p><strong>Windows Vista :</strong> dans Windows Vista et les versions ultérieures de Windows la valeur est 16.</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>Nombre maximal de colonnes autorisées dans une table.</p><p><strong>Windows XP :</strong> la valeur 0x0000fee0 est utilisée dans Windows XP et versions ultérieures et versions ultérieures de Windows</p><p><strong>Windows 2000 :</strong> la valeur 0x00007ffe est utilisée dans Windows 2000.</p> | 
| <p>JET_ccolFixedMost<br />0x0000007F</p> | <p>Nombre maximal de colonnes fixes autorisées dans une table, actuellement 127.</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>Nombre maximal de colonnes de longueur variable qui peuvent être contenues dans une table, actuellement 128.</p> | 
| <p>JET_ccolTaggedMost<br />(JET_ccolMost-0x000000FF)</p> | <p>Nombre maximal de colonnes avec balises pouvant être contenues dans une table, actuellement 64993.</p> | 



### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


