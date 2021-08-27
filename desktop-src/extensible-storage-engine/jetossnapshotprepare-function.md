---
description: 'En savoir plus sur : fonction JetOSSnapshotPrepare'
title: Fonction JetOSSnapshotPrepare
TOCTitle: JetOSSnapshotPrepare Function
ms:assetid: 364cbcba-7ddb-4748-8417-e885a5984b0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269224(v=EXCHG.10)
ms:contentKeyID: 32765526
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotPrepare
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 010cafd19ffde09b3083dd3cb6e6a69fa2268f11
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470326"
---
# <a name="jetossnapshotprepare-function"></a>Fonction JetOSSnapshotPrepare


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetossnapshotprepare-function"></a>Fonction JetOSSnapshotPrepare

La fonction **JetOSSnapshotPrepare** commence les préparations pour une session d’instantané. Une session d’instantané est un intervalle de temps dans lequel le moteur n’émet pas d’e/s d’écriture sur le disque, de sorte que le moteur peut participer à une session d’instantané de volume (lorsqu’il est piloté par un enregistreur d’instantané).

**Windows xp :****JetOSSnapshotPrepare** est introduit dans Windows xp.  

```cpp
    JET_ERR JET_API JetOSSnapshotPrepare(
      __out         JET_OSSNAPID* psnapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*psnapId*

Identificateur de la session d’instantané à démarrer.

*grbit*

Options pour cet appel. Ce paramètre peut avoir une combinaison des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>0</p> | <p>Instantané normal.</p> | 
| <p>JET_bitIncrementalSnapshot</p> | <p>Seuls les fichiers journaux seront pris.</p> | 
| <p>JET_bitCopySnapshot</p> | <p>Instantané de copie (normal ou incrémentiel) sans troncation du journal.</p> | 
| <p>JET_bitContinueAfterThaw</p> | <p>La session d’instantané se produit après <a href="gg269229(v=exchg.10).md">JetOSSnapshotThaw</a> et nécessite un appel de fonction <a href="gg294136(v=exchg.10).md">JetOSSnapshotEnd</a> .</p> | 
| <p>JET_bitExplicitPrepare</p> | <p>Aucune instance ne sera préparée par défaut.</p><p><strong>Windows 7 :</strong>  JET_bitExplicitPrepare est introduite dans Windows 7.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>Le pointeur d’ID d’instantané a la valeur NULL ou le paramètre <em>Grbit</em> n’est pas valide.</p> | 
| <p>JET_errOSSnapshotInvalidSequence</p> | <p>Une session d’instantané est déjà en cours et l’opération n’est pas autorisée à avoir plus d’une session d’instantané à un moment donné.</p> | 



Si cette fonction réussit, une session d’instantané est en mesure de démarrer à tout moment avec la phase d’interruption des e/s. L’identificateur de la session est retourné et doit être utilisé dans les appels suivants pour la session d’instantané.

Les instances en cours d’exécution du moteur seront désormais considérées comme faisant partie de la session d’instantané.

**Windows Vista :**  Pour spécifier un sous-ensemble différent d’instances, [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md) peut être appelé.

L’appel de séquence d’API normal est : **JetOSSnapshotPrepare**, éventuellement suivi d’un ou plusieurs appels à [JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md), puis de [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md). Une fois le blocage démarré, il peut être arrêté à l’aide de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md). À tout moment après la préparation, la session d’instantané peut être interrompue soudainement avec [JetOSSnapshotAbort](./jetossnapshotabort-function.md).

Si JET_bitContinueAfterThaw est spécifié après [JetOSSnapshotThaw](./jetossnapshotthaw-function.md), la session d’instantané est conservée (bien que l’e/s reprenne). Cela permet de vérifier la capture instantanée et, si nécessaire, d’activer la troncation du journal à l’aide de [JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md) et de demander un appel à [JetOSSnapshotEnd](./jetossnapshotend-function.md).

Si cette fonction échoue, aucune modification de l’état du moteur ne se produit.

#### <a name="remarks"></a>Remarques

Les entrées du journal des événements seront générées pour les différentes étapes de l’instantané.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotAbort](./jetossnapshotabort-function.md)  
[JetOSSnapshotEnd](./jetossnapshotend-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepareInstance](./jetossnapshotprepareinstance-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)  
[JetOSSnapshotTruncateLog](./jetossnapshottruncatelog-function.md)
