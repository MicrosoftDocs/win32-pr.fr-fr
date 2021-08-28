---
description: 'En savoir plus sur : fonction JetCreateIndex'
title: Fonction JetCreateIndex
TOCTitle: JetCreateIndex Function
ms:assetid: d164e74a-7719-4587-9059-8fb18b365133
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294099(v=EXCHG.10)
ms:contentKeyID: 32765714
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateIndexA
- JetCreateIndex
- JetCreateIndexW
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 698f9a050415568c06c8e10819cfed12a4a17181
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478395"
---
# <a name="jetcreateindex-function"></a>Fonction JetCreateIndex


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetcreateindex-function"></a>Fonction JetCreateIndex

la fonction **JetCreateIndex** vous permet de créer un index de données dans une base de données ESE (Extensible Stockage Engine), que vous pouvez utiliser pour rechercher rapidement des données spécifiques.

```cpp
    JET_ERR JET_API JetCreateIndex(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_PCSTR szIndexName,
      __in          JET_GRBIT grbit,
      __in          const tchar* szKey,
      __in          unsigned long cbKey,
      __in          unsigned long lDensity
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Contexte de la session de base de données à utiliser pour un appel d’API particulier.

*TableID*

Table pour laquelle un index sera créé.

*szIndexName*

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de l’index à créer.

Le nom de l’index doit être conforme aux indications suivantes :

  - Il doit contenir moins de caractères que JET_cbNameMost, à l’exclusion du caractère null de fin.

  - Il doit contenir uniquement des caractères des catégories suivantes : 0 à 9, A à Z, a à z et tous les caractères de ponctuation, à l’exception de « \! » (point d’exclamation), « , » (virgule), « \[ » (crochet ouvrant) et « \] » (crochet fermant), c’est-à-dire les caractères ASCII 0x20, 0X22 à 0x2D, 0x2F à 0x5A, 0x5c et 0x5d à 0x7F.

  - Il ne doit pas commencer par un espace.

  - Il doit contenir au moins un caractère autre qu’un espace.

*grbit*

Groupe de bits qui contient les options à utiliser pour un appel particulier. Ce paramètre peut inclure zéro, une ou plusieurs des options figurant dans la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*szKey*

Pointeur vers une chaîne double se terminant par un caractère null des jetons délimités par des valeurs NULL.

Pour plus d’informations sur ce paramètre, consultez la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

*cbKey*

Longueur, en octets, du paramètre *szKey* , y compris les deux caractères null de fin.

*lDensity*

Densité de pourcentage de l’index initial B +.

Pour plus d’informations sur ce paramètre, consultez la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) .

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Signification</p> | 
|--------------------|----------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 



Pour obtenir la liste des erreurs supplémentaires qui peuvent être retournées par la fonction **JetCreateIndex** , consultez [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="remarks"></a>Remarques

L’appel de la fonction **JetCreateIndex** est identique à l’appel de la fonction [JetCreateIndex2](./jetcreateindex2-function.md) avec une structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) contenant les mêmes paramètres que les paramètres de **JetCreateIndex** et un paramètre *cIndexCreate* égal à 1. Pour les champs de la structure [JET_INDEXCREATE](./jet-indexcreate-structure.md) qui n’ont pas de paramètres correspondants dans **JetCreateIndex**, la valeur 0 est utilisée par défaut.

Notez que **JetCreateIndex** a été remplacé par [JetCreateIndex2](./jetcreateindex2-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p>Client</p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p>Serveur</p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p>En-tête</p> | <p>Est déclaré dans esent. h.</p> | | <p>Bibliothèque</p> | <p>Utilise ESENT. lib.</p> | | <p>DLL</p> | <p>Requiert ESENT.dll.</p> | | <p>Unicode</p> | <p>Est implémenté en tant que <strong>JetCreateIndexW</strong> (Unicode) et <strong>JetCreateIndexA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JetCreateIndex2](./jetcreateindex2-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)  
[JetCreateTableColumnIndex2](./jetcreatetablecolumnindex2-function.md)
