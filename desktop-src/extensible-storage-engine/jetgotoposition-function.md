---
description: 'En savoir plus sur : fonction JetGotoPosition'
title: JetGotoPosition fonction)
TOCTitle: JetGotoPosition Function
ms:assetid: 77b099f1-4a21-4ddb-b269-83ca74219b4d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269300(v=EXCHG.10)
ms:contentKeyID: 32765592
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGotoPosition
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3b8f18af3efcf35170f02b42a8f4b9da43f93824
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465425"
---
# <a name="jetgotoposition-function"></a>JetGotoPosition fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgotoposition-function"></a>JetGotoPosition fonction)

La fonction **JetGotoPosition** déplace un curseur vers un nouvel emplacement qui est une fraction de la façon dont l’index actuel est utilisé. La fraction est approximativement égale à ce qui suit :

precpos- \> centriesLT/precpos- \> centriesTotal

Cette opération est exécutée en réponse à l’entrée de la boîte de défilement utilisateur qui est reçue quand l’utilisateur tente d’afficher des données qui démarrent de façon partielle via un jeu de données.

```cpp
    JET_ERR JET_API JetGotoPosition(
      __in          JET_SESID sesid,
      __in          JET_TABLEID tableid,
      __in          JET_RECPOS* precpos
    );
```

### <a name="parameters"></a>Paramètres

*sesid*

Session à utiliser pour cet appel.

*TableID*

Curseur à utiliser pour cet appel.

*precpos*

Description de la fraction à utiliser pour positionner le curseur dans l’index actuel.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>L’opération n’a pas pu se terminer, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>L’opération n’a pas pu se terminer car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le precpos- &gt; cbStruct donné n’est pas une taille valide pour la structure <a href="gg269308(v=exchg.10).md">JET_RECPOS</a> , ou precpos- &gt; centriesLT est supérieur à precpos- &gt; centriesTotal.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible d’effectuer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRecordNotFound</p> | <p>Cette erreur est retournée si l’index est vide.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Impossible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errSessionSharingViolation</p> | <p>La même session ne peut pas être utilisée simultanément pour plusieurs threads.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance qui est associée à la session est en cours d’arrêt.</p> | 



Si cette fonction est réussie, le curseur est déplacé vers un enregistrement actif qui est une fraction de la façon dont la fraction est precpos- \> centriesLT divisée par precpos- \> centriesTotal.

Si cette fonction échoue, l’emplacement du curseur reste inchangé.

#### <a name="remarks"></a>Remarques

Cette opération déplace le curseur de la table vers une position au point approximatif suivant : precpos- \> centriesLT divisé par precpos- \> centriesTotal.

Lorsque des mises à jour se produisent en continu sur la table, les appels suivants avec le même [JET_RECPOS](./jet-recpos-structure.md) peuvent déplacer le curseur vers des positions différentes dans l’index, avant et après la position précédente. L’isolation transactionnelle ne s’applique pas au positionnement dans [JET_RECPOS](./jet-recpos-structure.md) , car elle dépend des propriétés physiques de l’index qui ne sont pas des transactions isolées.

[JET_RECPOS](./jet-recpos-structure.md) ne doit pas être utilisé pour décrire un enregistrement dans une table ou pour repositionner un enregistrement à proximité d’un enregistrement existant. Au lieu de cela, les signets d’un enregistrement existant doivent être récupérés après un **JetGotoPosition** initial, puis utilisés pour repositionner le même enregistrement.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_COLUMNID](./jet-columnid.md)  
[JET_ERR](./jet-err.md)  
[JET_SESID](./jet-sesid.md)  
[JET_TABLEID](./jet-tableid.md)  
[JET_RECPOS](./jet-recpos-structure.md)  
[JET_SETINFO](./jet-setinfo-structure.md)
