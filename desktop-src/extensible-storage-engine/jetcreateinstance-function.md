---
description: 'En savoir plus sur : fonction JetCreateInstance'
title: Fonction JetCreateInstance
TOCTitle: JetCreateInstance Function
ms:assetid: 9d6c8c9f-3d3b-4308-87d3-84b1ef270262
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269354(v=EXCHG.10)
ms:contentKeyID: 32765641
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCreateInstanceW
- JetCreateInstance
- JetCreateInstanceA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: aa64c9aadd9402ee8356a8f4db81f878022b838b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529472"
---
# <a name="jetcreateinstance-function"></a>Fonction JetCreateInstance


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetcreateinstance-function"></a>Fonction JetCreateInstance

La fonction **JetCreateInstance** alloue une nouvelle instance du moteur de base de données pour une utilisation dans un processus unique.

**Windows XP : JetCreateInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetCreateInstance(
      __out         JET_INSTANCE* pinstance,
      __in_opt      const tchar* szInstanceName
    );
```

### <a name="parameters"></a>Paramètres

*pinstance*

Mémoire tampon de sortie qui reçoit l’instance nouvellement créée.

*szInstanceName*

Identificateur de chaîne unique pour l’instance à créer. Cette chaîne doit être unique au sein d’un processus donné hébergeant le moteur de base de données.

**Remarque** Une valeur NULL est traitée comme un identificateur de chaîne valide pour une instance. Une seule instance peut avoir un identificateur de chaîne NULL.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceNameInUse</p></td>
<td><p>Le nom d’instance spécifié est déjà utilisé pour ce processus.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetCreateInstance</strong> lorsque <em>Pinstance</em> a la <strong>valeur null</strong>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>L’opération a échoué, car elle ne peut pas être utilisée lorsque le moteur de base de données fonctionne en mode d’instance unique (mode de compatibilité Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyInstances</p></td>
<td><p>Impossible de créer une nouvelle instance, car le nombre maximal d’instances a été atteint. Le nombre maximal d’instances prises en charge est configuré à l’aide de <a href="gg294044(v=exchg.10).md">JetSetSystemParameter</a> à l’aide de <em>JET_paramMaxInstances</em>.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, une nouvelle instance sera allouée et l’identificateur correspondant sera retourné. À ce stade, tous les paramètres système de l’instance auront les valeurs des paramètres système par défaut globaux. Une fois qu’une instance sera allouée, elle doit être arrêtée et/ou libérée ultérieurement.

En cas d’échec, une erreur qui représente la cause de l’échec est retournée et aucune instance n’est allouée.

#### <a name="remarks"></a>Notes

Une instance doit être initialisée avec un appel à [JetInit](./jetinit-function.md) avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de [JetInit](./jetinit-function.md). Le nombre maximal d’instances pouvant être créées à un moment donné est contrôlé par [JET_paramMaxInstances](./resource-parameters.md), qui peut être configurée par un appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md). Une instance est l’unité de récupérabilité pour le moteur de base de données. Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données. Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.

Si la fonction s’exécute correctement, le moteur de base de données est automatiquement remplacé par le mode multi-instance comme un effet secondaire de cet appel. Si l’application souhaite autoriser une seule instance du processus, [JetInit](./jetinit-function.md) doit être utilisé pour démarrer le moteur de base de données en mode de compatibilité Windows 2000.

S’il est présent, le *szDisplayName* sera utilisé pour identifier l’instance dans des emplacements tels que le journal des événements ou vers d’autres appelants comme des applications de sauvegarde (via des fonctions telles que [JetGetInstanceInfo](./jetgetinstanceinfo-function.md) ou [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)). Si le nom complet n’est pas fourni, le *szInstanceName* unique est utilisé à la place, s’il est présent ; sinon, une chaîne vide est retournée. Si le mode d’exécution n’a pas été défini pour le moteur, après cet appel, il sera défini en mode multi-instance.

La séquence de démarrage classique d’un processus potentiellement exécutant plusieurs instances de jet serait la suivante :

  - Un appel à [JetCreateInstance2](./jetcreateinstance2-function.md) , qui allouera et nommera l’instance.

  - Plusieurs appels à [JetSetSystemParameter](./jetsetsystemparameter-function.md) pour cette instance afin de définir différents paramètres système. Notez que certains paramètres système doivent être uniques par instance (comme [JET_paramSystemPath](./transaction-log-parameters.md) ou [JET_paramLogFilePath](./transaction-log-parameters.md)). il est donc très probable que vous deviez définir chacun d’eux.

  - Démarrez l’instance à l’aide de [JetInit](./jetinit-function.md) ou [JetInit2](./jetinit2-function.md). Pour arrêter et/ou libérer une instance, [JetTerm](./jetterm-function.md), [JetTerm2](./jetterm2-function.md) doit être utilisé.

S’il s’agit de la première instance à démarrer, il existe un certain nombre d’étapes supplémentaires qui seront exécutées au cours de cet appel afin d’effectuer une initialisation et une configuration de base du système. Un certain nombre de ces étapes peuvent entraîner des erreurs spécifiques à partir de JET_errOutOfMemory mais d’autres également (voir les erreurs ci-dessus).

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetCreateInstanceW</strong> (Unicode) et <strong>JetCreateInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
