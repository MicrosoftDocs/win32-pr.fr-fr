---
description: 'En savoir plus sur : fonction JetInit'
title: Fonction JetInit
TOCTitle: JetInit Function
ms:assetid: b7f78cca-7268-4045-bda2-20746b1d6370
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294068(v=EXCHG.10)
ms:contentKeyID: 32765683
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 308c012bc5eb144e0ac0d608c64d63ccf39aeca1
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323462"
---
# <a name="jetinit-function"></a>Fonction JetInit


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetinit-function"></a>Fonction JetInit

La fonction **JetInit** met le moteur de base de données dans un État où il peut prendre en charge l’utilisation des fichiers de base de données par l’application. Le moteur doit déjà être correctement configuré pour l’initialisation à l’aide de [JetSetSystemParameter](./jetsetsystemparameter-function.md). La récupération après incident de la base de données s’effectue automatiquement dans le cadre du processus d’initialisation.

```cpp
JET_ERR JET_API JetInit(
  __in_out_opt  JET_INSTANCE* pinstance
);
```

### <a name="parameters"></a>Paramètres

*pinstance*

Instance à utiliser pour cet appel.

Pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la valeur NULL.

Pour Windows XP et versions ultérieures, l’utilisation de ce paramètre dépend du mode de fonctionnement du moteur. Si le moteur fonctionne en mode hérité (mode de compatibilité Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la valeur NULL ou il peut avoir la valeur d’une mémoire tampon de sortie valide qui retourne le handle d’instance global créé comme effet secondaire de l’initialisation. La valeur de cette mémoire tampon de sortie doit être NULL ou JET_instanceNil. Ce handle d’instance peut ensuite être passé à toute autre fonction qui utilise une instance. Si le moteur fonctionne en mode multi-instance, ce paramètre doit être défini sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par l’instance de fonction [JetCreateInstance](./jetcreateinstance-function.md) en cours d’initialisation.


#### <a name="remarks"></a>Notes

Une instance doit être initialisée avec un appel à **JetInit** avant de pouvoir être utilisée par une autre chose que [JetSetSystemParameter](./jetsetsystemparameter-function.md).

Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de **JetInit**. Une instance est l’unité de récupérabilité pour le moteur de base de données. Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données. Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions.

Le nombre maximal d’instances qui peuvent être créées à un moment donné est contrôlé par [JET_paramMaxInstances](./resource-parameters.md), qui peut être configurée par un appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md). Lorsque le moteur de base de données est initialisé pour la première fois, **JetInit** crée un ensemble initial de fichiers pour prendre en charge cette instance. Ces fichiers incluent un fichier de point de contrôle (nommé \<[JET_paramBaseName](./transaction-log-parameters.md)\> . CHK), un ensemble de fichiers journaux de transactions réservés (nommés RES1. LOG et RES2. LOG), un fichier journal de transactions initial (nommé \<[JET_paramBaseName](./transaction-log-parameters.md)\> . LOG) et un fichier de base de données temporaire (nommé d’après [JET_paramTempPath](./temporary-database-parameters.md)). Si [JET_paramRecovery](./transaction-log-parameters.md) est défini sur « désactivé », le fichier de point de contrôle et les fichiers journaux ne seront pas créés. Si [JET_paramMaxTemporaryTables](./temporary-database-parameters.md) a la valeur zéro, le fichier de base de données temporaire ne sera pas créé. Ces fichiers représentent la quantité d’espace disque d’une instance et doivent être gérés avec précaution. Si ces fichiers sont endommagés individuellement ou par rapport à un autre, les données stockées dans les bases de données associées à l’instance peuvent être perdues.

Lorsque le moteur de base de données est initialisé avec un ensemble existant de fichiers journaux de transactions, ces fichiers sont inspectés pour voir si la première version de l’instance a subi un incident. En cas de détection d’un incident, la récupération après incident est automatiquement effectuée. Ce processus va reconstruire les bases de données attachées à l’instance au cours de la version précédente du moteur et enregistrer les modifications dans les fichiers de la base de données. Le résultat sera celui des bases de données qui sont cohérentes avec les transactions. Ce processus peut prendre un certain temps si le nombre de fichiers du journal des transactions à relire sur les bases de données est important.

En raison du fait que **JetInit** effectue la récupération après incident, presque toutes les erreurs du moteur de base de données peuvent être retournées en cas de défaillance. Dans la pratique, la plupart des erreurs rencontrées dans le déploiement se répartissent en deux catégories : la corruption des données et la gestion des fichiers. Les données endommagées se manifestent le plus souvent dans les erreurs suivantes ou similaires :

  - JET_errReadVerifyFailure

  - JET_errLogFileCorrupt

  - JET_errCheckpointCorrupt

Ces erreurs sont presque toujours dues à des problèmes matériels et ne peuvent donc pas être évitées. La gestion des erreurs de fichier se manifeste le plus souvent dans les erreurs suivantes ou similaires :

  - JET_errMissingLogFile

  - JET_errAttachedDatabaseMismatch

  - JET_errDatabaseSharingViolation

  - JET_errInvalidLogSequence

Si la récupération s’exécute sur un ensemble de journaux, pour lesquels toutes les bases de données ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales), et que le client souhaite que la récupération se poursuive malgré les bases de données manquantes, le JET_ bitReplayIgnoreMissingDB peut être utilisé pour poursuivre la récupération des bases de données disponibles. Ces erreurs sont empêchables par l’application. L’application doit veiller à protéger le référentiel de ces fichiers contre les manipulations en dehors des forces, telles que l’utilisateur ou d’autres applications. Si l’application souhaite détruire entièrement une instance, tous les fichiers associés à l’instance doivent être supprimés. Celles-ci incluent le fichier de point de contrôle, les fichiers journaux des transactions et les fichiers de base de données attachés à l’instance.

La fonction **JetInit** se comporte différemment, en ce qui concerne les fichiers de base de données attachés à l’instance, entre Windows 2000 et les versions ultérieures.

**Windows 2000 :**  Dans Windows 2000, toute base de données attachée à l’instance pendant une version précédente de cette instance reste attachée à l’instance une fois que **JetInit** s’est terminé avec succès. Il n’est pas nécessaire d’appeler [JetAttachDatabase](./jetattachdatabase-function.md) après **JetInit** pour vous assurer de l’accès ultérieur à la base de données. Si la fonction [JetAttachDatabase](./jetattachdatabase-function.md) est appelée après la fonction **JetInit** , le JET_wrnDatabaseAttached avertissement est retourné. Cet avertissement indique que la pièce jointe de la base de données a été conservée et peut être ignorée.

**Windows XP :**  Dans Windows XP et versions ultérieures, toutes les bases de données sont automatiquement détachées de l’instance par **JetInit**. Cela signifie que [JetAttachDatabase](./jetattachdatabase-function.md) doit toujours être appelé après **JetInit** dans ce cas.

Toute application écrite pour s’exécuter sur Windows 2000 et les versions ultérieures doit toujours appeler [JetAttachDatabase](./jetattachdatabase-function.md) après **JetInit**. Si l’application s’exécute sur Windows 2000, elle doit s’attendre à voir JET_wrnDatabaseAttached dans certains cas. Pour plus d’informations, consultez [JetAttachDatabase](./jetattachdatabase-function.md) .

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

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_paramMaxTemporaryTables](./temporary-database-parameters.md)  
[JET_paramRecovery](./transaction-log-parameters.md)  
[JetAttachDatabase](./jetattachdatabase-function.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit3](./jetinit3-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
