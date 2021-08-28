---
description: 'En savoir plus sur : fonction JetInit2'
title: Fonction JetInit2
TOCTitle: JetInit2 Function
ms:assetid: b5541429-6ce6-457b-88cf-673d267f6209
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294065(v=EXCHG.10)
ms:contentKeyID: 32765680
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit2
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7874c475dc18beb5d7f6849b9f628ea06cbc32a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470454"
---
# <a name="jetinit2-function"></a>Fonction JetInit2


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetinit2-function"></a>Fonction JetInit2

La fonction **JetInit2** met le moteur de base de données dans un État où il peut prendre en charge l’utilisation des fichiers de base de données par l’application. Le moteur doit déjà être correctement configuré pour l’initialisation à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md). La récupération après incident de la base de données s’effectue automatiquement dans le cadre du processus d’initialisation.

**Windows xp :****JetInit2** est introduit dans Windows xp.  

Cette fonction est obsolète. Utilisez [JetInit3](./jetinit3-function.md) à la place.

```cpp
JET_ERR JET_API JetInit2(
  __in_out_opt  JET_INSTANCE* pinstance,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a>Paramètres

*pinstance*

Instance à utiliser pour cet appel.

pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la valeur NULL.

pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur null ou il peut être défini sur une mémoire tampon de sortie valide contenant la valeur null ou JET_instanceNil qui retourne le handle d’instance global créé comme effet secondaire de l’initialisation. Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance. Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par le [JetCreateInstance](./jetcreateinstance-function.md) en cours d’initialisation.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitReplayReplicatedLogFiles</p> | <p>Réservé pour un usage futur.</p> | 
| <p>JET_bitCreateSFSVolumeIfNotExist</p> | <p>Réservé pour un usage futur.</p> | 
| <p>JET_bitReplayIgnoreMissingDB</p> | <p>Cette option permet à l’utilisateur d’exécuter la récupération sur un ensemble de fichiers journaux, sans que toutes les bases de données présentes, soient attachées à un point du jeu de journaux.</p> | 
| <p>JET_bitRecoveryWithoutUndo</p> | <p>Effectuer la récupération, mais s’arrêter à la phase de restauration. Cela permet la copie et l’application des journaux de transactions supplémentaires.</p> | 
| <p>JET_bitTruncateLogsAfterRecovery</p> | <p>En cas de récupération logicielle réussie, tronquez les fichiers journaux.</p> | 
| <p>JET_bitReplayMissingMapEntryDB</p> | <p>L’entrée de mappage de base de données est manquante par défaut au même emplacement.</p> | 
| <p>JET_bitReplayIgnoreLostLogs</p> | <p>Ignorer les journaux perdus à la fin du flux de journal.</p><p><strong>Windows 7 : JET_bitReplayIgnoreLostLogs</strong> est introduite dans Windows 7.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


#### <a name="remarks"></a>Remarques

Une instance doit être initialisée avec un appel à **JetInit2** avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md). Une instance est l’unité de récupérabilité pour le moteur de base de données. Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données. Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.

Si la récupération s’exécute sur un ensemble de journaux, pour lesquels toutes les bases de données ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales), et que le client souhaite que la récupération se poursuive malgré les bases de données manquantes, le JET_ bitReplayIgnoreMissingDB est utilisé pour poursuivre la récupération des bases de données disponibles.

Pour plus d’informations, consultez la section Notes dans [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista ou Windows XP.</p> | | <p><strong>Serveur</strong></p> | <p>requiert Windows server 2008 ou Windows server 2003.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres de ressource](./resource-parameters.md)
