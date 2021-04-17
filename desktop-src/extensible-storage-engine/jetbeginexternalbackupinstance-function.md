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
ms.openlocfilehash: bab2fa3d9faa7f81abea278e3d9fcf4a4022c24c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484241"
---
# <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetbeginexternalbackupinstance-function"></a>JetBeginExternalBackupInstance fonction)

La fonction **JetBeginExternalBackupInstance** lance une sauvegarde externe alors que le moteur et la base de données sont en ligne et actifs.

**Windows XP : JetBeginExternalBackupInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetBeginExternalBackupInstance(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance de base de données à utiliser pour cet appel.

Pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

Pour Windows XP et les versions ultérieures, la variante d’API qui n’accepte pas ce paramètre ne peut être appelée que lorsque le moteur est en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge. Dans le cas contraire, l’opération échouera avec JET_errRunningInMultiInstanceMode.

*grbit*

Groupe de bits spécifiant zéro ou plusieurs des options suivantes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitBackupAtomic</p></td>
<td><p>Cet indicateur est déconseillé. L’utilisation de ce bit entraîne le retour de JET_errInvalidgrbit.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitBackupIncremental</p></td>
<td><p>Crée une sauvegarde incrémentielle par opposition à une sauvegarde complète. Cela signifie que seuls les fichiers journaux depuis la dernière sauvegarde complète ou incrémentielle sont sauvegardés.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitBackupSnapshot</p></td>
<td><p>Réservé pour un usage futur. Défini pour Windows XP.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Le système peut générer des codes de réussite ou d’échec à la suite d’un appel à cette fonction. Pour obtenir la liste complète des erreurs pour cette API, consultez [codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md).

Consultez [JetBeginExternalBackup](./jetbeginexternalbackup-function.md).

#### <a name="remarks"></a>Notes

**JetBeginExternalBackupInstance** est la première fonction d’une série de fonctions qui doivent être appelées pour exécuter une sauvegarde en ligne réussie (non basée sur VSS). Voir aussi [JetBeginExternalBackup](./jetbeginexternalbackup-function.md) et [JetStopBackupInstance](./jetstopbackupinstance-function.md).

Une sauvegarde externe peut être utilisée pour implémenter des sauvegardes complètes, incrémentielles ou différentielles.

La sauvegarde sera approximative, car la sauvegarde sera cohérente à un point unique dans le temps dans l’historique des transactions, mais le contrôle du point exact dans le temps n’est pas possible pour l’instant.

#### <a name="requirements"></a>Configuration requise

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
<tr class="even">
<td><p><strong>Bibliothèque</strong></p></td>
<td><p>Utilisez ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p><strong>DLL</strong></p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


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
