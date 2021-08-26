---
description: 'En savoir plus sur : fonction JetBeginExternalBackupInstance'
title: JetBeginExternalBackupInstance fonction)
TOCTitle: JetBeginExternalBackupInstance Function
ms:assetid: f1c5a73d-b1cc-4ee4-942b-b5e4ef51bc2f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294132(v=EXCHG.10)
ms:contentKeyID: 32765746
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetBeginExternalBackupInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 53583a1d51de390b0c84143dcb59f3327b7c91bb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479295"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance fonction)

La fonction **JetBeginExternalBackupInstance** lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.

**Windows xp : JetBeginExternalBackupInstance** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance de base de données à utiliser pour cet appel.

pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

pour Windows XP et versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (Windows mode de compatibilité 2000), où une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitBackupAtomic</p> | <p>Cet indicateur est déconseillé. L’utilisation de ce bit entraîne le retour de JET_errInvalidgrbit.</p> | 
| <p>JET_bitBackupIncremental</p> | <p>Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète. Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</p> | 
| <p>JET_bitBackupSnapshot</p> | <p>Réservé pour un usage futur. défini pour Windows XP.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Le système peut générer des codes de réussite ou d’échec à la suite d’un appel à cette fonction. pour obtenir la liste complète des erreurs pour cette API, consultez [Codes d’erreur du moteur d’Stockage Extensible](./extensible-storage-engine-error-codes.md).

Consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Remarques

**JetBeginExternalBackupInstance** est la première fonction d’une série de fonctions qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS). Voir aussi [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) et [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Une sauvegarde externe peut être utilisée pour implémenter des sauvegardes complètes, incrémentielles ou différentielles.

La sauvegarde sera approximative, car la sauvegarde sera cohérente à un point unique dans le temps dans l’historique des transactions, mais le contrôle du point exact dans le temps n’est pas possible pour l’instant.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetBeginExternalBackup](./jetbeginexternalbackup-function.md)  
[JetCloseFile](./jetclosefile-function.md)  
[JetEndExternalBackup](./jetendexternalbackup-function.md)  
[JetEndExternalBackupInstance2](./jetendexternalbackupinstance2-function.md)  
[JetGetAttachInfo](./jetgetattachinfo-function.md)  
[JetGetLogInfo](./jetgetloginfo-function.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetReadFile](./jetreadfile-function.md)  
[JetStopBackup](./jetstopbackup-function.md)  
[JetTruncateLog](./jettruncatelog-function.md)
