---
description: 'En savoir plus sur : fonction JetGetRecordPosition'
title: Fonction JetGetRecordPosition
TOCTitle: JetGetRecordPosition Function
ms:assetid: 811d9e68-0594-4f70-b854-c3ec966b2705
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269316(v=EXCHG.10)
ms:contentKeyID: 32765606
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetRecordPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 570b3b94859db939c6f8a6944673f88dc47be9e6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481335"
---
# <a name="jetgetrecordposition-function"></a>Fonction JetGetRecordPosition


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetrecordposition-function"></a>Fonction JetGetRecordPosition

La fonction **JetGetRecordPosition** retourne la position fractionnaire de l’enregistrement actif dans l’index actuel sous la forme d’une structure [JET_RECPOS](./jet-recpos-structure.md) . Cette structure décrit les positions fractionnaires en termes de nombre approximatif d’entrées d’index avant l’enregistrement actif et un nombre total approximatif d’entrées dans l’index.

```cpp
    JET_ERR JET_API JetGetRecordPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __out         JET_RECPOS* precpos,
      __in          unsigned long cbRecpos
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*precpos*

Description de la fraction à utiliser pour obtenir la position de l’enregistrement actif dans l’index actuel.

*cbRecpos*

Taille de la mémoire allouée à *precpos*.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Impossible d’effectuer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Impossible d’effectuer cette opération, car l’instance, associée à la session, a rencontré une erreur irrécupérable. Il est nécessaire que l’accès à toutes les données soit révoqué afin de protéger l’intégrité de ces données.</p><p><strong>Windows 2000 :</strong>  cette erreur ne sera pas retournée par le système d’exploitation Windows 2000.</p> | 
| <p>JET_errInvalidParameter</p> | <p>La taille de la mémoire allouée sur <em>precpos</em> n’est pas suffisante.</p> | 
| <p>JET_errNoCurrentRecord</p> | <p>Le curseur ne se trouve pas actuellement sur un enregistrement et ne peut pas retourner de position.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows 2000 :</strong>  cette erreur ne sera pas retournée par le système d’exploitation Windows 2000.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance associée à la session est en cours d’arrêt.</p> | 



En cas de réussite, le nombre approximatif d’entrées d’index précédant l’enregistrement en cours dans l’index est retourné dans precpos- \> centriesLT. 1 est retourné dans precpos- \> centriesInRange. Le nombre approximatif d’entrées dans l’index est retourné dans precpos- \> centriesTotal.

En cas d’échec, aucune modification n’est apportée à la mémoire allouée sur *precpos*.

#### <a name="remarks"></a>Remarques

Cette opération renvoie des données variables lorsque les mises à jour se produisent en continu sur la table. Les modifications apportées aux valeurs ne correspondent pas toujours aux attentes en fonction de la connaissance des mises à jour, car les valeurs sont des approximations basées sur les propriétés physiques de l’index. L’isolation transactionnelle ne s’applique pas aux positions de **JetGetRecordPosition** , car les valeurs dépendent des propriétés physiques de l’index qui ne sont pas des transactions isolées.

[JET_RECPOS](./jet-recpos-structure.md) ne doit pas être utilisé pour décrire un enregistrement dans une table ou pour repositionner un enregistrement à proximité d’un enregistrement existant. Au lieu de cela, les signets d’un enregistrement existant doivent être récupérés, puis utilisés pour repositionner le même enregistrement.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)  
[JetGotoPosition](./jetgotoposition-function.md)  
[JetStopService](./jetstopservice-function.md)
