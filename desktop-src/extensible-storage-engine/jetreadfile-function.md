---
description: 'En savoir plus sur : fonction JetReadFile'
title: JetReadFile fonction)
TOCTitle: JetReadFile Function
ms:assetid: 59dc9e04-7e02-4835-9aed-95cfcf74d780
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269257(v=EXCHG.10)
ms:contentKeyID: 32765559
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFile
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 57e11f3b5478f18bc7883974c2f598bf24dcb8fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203889"
---
# <a name="jetreadfile-function"></a>JetReadFile fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetreadfile-function"></a>JetReadFile fonction)

La fonction **JetReadFile** récupère le contenu d’un fichier ouvert avec [JetOpenFile](./jetopenfile-function.md).

```cpp
    JET_ERR JET_API JetReadFile(
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcbActual
    );
```

### <a name="parameters"></a>Paramètres

*hfFile*

Handle du fichier à lire.

*va*

Mémoire tampon de sortie qui recevra les données du fichier.

*libéré*

Taille maximale, en octets, de la mémoire tampon de sortie.

*pcbActual*

Reçoit la quantité réelle de données de fichier récupérées.

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
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetReadFile</strong> dans les cas suivants :</p>
<ul>
<li><p>Le handle d’instance spécifié n’est pas valide. Windows XP et versions ultérieures.</p></li>
<li><p>La taille de la mémoire tampon de sortie n’est pas un multiple de la taille de page de la base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP et versions ultérieures.</p></li>
<li><p>La taille de la mémoire tampon de sortie est inférieure à trois pages de base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>) et il s’agit du premier appel à <strong>JetReadFile</strong> pour le handle spécifié. Windows XP et versions ultérieures.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>L’opération a échoué car des données non récupérables ont été détectées lors de la lecture d’une page de base de données dans un fichier de base de données ou un fichier correctif de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>L’opération a échoué car des données non récupérables ont été détectées lors de la lecture d’un fichier journal de transactions. Cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000), où une seule instance est prise en charge lorsque plusieurs instances existent déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le segment de données suivant du fichier est lu dans la mémoire tampon de sortie. Le nombre réel d’octets récupérés est également retourné. Le décalage de fichier à partir duquel la lecture suivante aura lieu sera avancé par ce montant.

En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde de l’instance. Sur Windows XP et versions ultérieures, la sauvegarde n’est pas annulée si une erreur s’est produite lors de la lecture d’un fichier de base de données. Toutefois, la sauvegarde de ce fichier de base de données restera annulée et le descripteur correspondant sera automatiquement fermé.

#### <a name="remarks"></a>Notes

Tout appel à **JetReadFile** à l’aide d’un handle qui a déjà retourné toutes les données du fichier sous-jacent (par exemple, un appel précédent ayant retourné moins d’octets que la taille de la mémoire tampon de sortie) fonctionne toujours, mais retourne zéro octet de données.

Un grand tampon de sortie doit être utilisé pour optimiser les performances de sauvegarde. Certaines expérimentations peuvent être nécessaires pour trouver le bon compromis entre la consommation des ressources et le débit pour une situation donnée. Dans tous les cas, la mémoire tampon de sortie ne doit pas être inférieure à 64 Ko.

Plusieurs appels simultanés à **JetReadFile** à l’aide du même descripteur de fichier ne sont pas pris en charge. Cela signifie qu’il n’est pas possible de mettre en file d’attente plusieurs mémoires tampons en lecture simultanée sur le même fichier pour obtenir un débit séquentiel élevé. Une seule mémoire tampon de grande taille doit être utilisée à la place.

Si l’instance est configurée de telle sorte que le nettoyage des pages de base de données est activé (voir JET_paramZeroDatabaseDuringBackup dans les paramètres système), les données supprimées seront supprimées de la base de données en tant qu’effet secondaire d’un appel à **JetReadFile** dans le fichier de base de données.

Il est très important de comprendre comment la sauvegarde et l’altération des données interagissent. Si le moteur de base de données détecte une altération des données au cours d’une sauvegarde, il échouera à la sauvegarde de la base de données affectée ou de la totalité de l’instance. Il s’agit d’une décision de conception consciente destinée à vous protéger contre la perte de données. Si le moteur de base de données a permis une sauvegarde réussie là où la corruption des données était présente, il est possible qu’une sauvegarde plus ancienne et non endommagée soit ignorée. Cela peut être un problème, car il serait possible de corriger l’altération des données sur l’instance en direct en restaurant cette sauvegarde et en relisant tous les fichiers du journal des transactions sur cette base de données. Ce scénario de perte de données nulle suppose que l’enregistrement circulaire n’est pas activé (voir [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)).

Il est également important de comprendre que lorsque la corruption des données est présente, la sauvegarde en continu est la plus probable où elle sera détectée en premier. C’est le cas parce que la sauvegarde en continu est le seul processus qui analyse régulièrement chaque page d’un fichier de base de données. Il est également probable que la sauvegarde en continu sera le premier processus de détection des signes précoces de défaillance matérielle, comme le manifestent les erreurs de corruption de données intermittentes. Cela est dû à la quantité de données récupérées par la sauvegarde et à la vitesse à laquelle elles sont récupérées.

La corruption des données est détectée par le moteur de base de données via l’utilisation de sommes de contrôle de bloc. Ces sommes de contrôle sont définies juste avant l’écriture d’une page de base de données et sont vérifiées lors de la lecture d’une page de base de données. Ce schéma permet au moteur de base de données de déterminer si les données ont été endommagées à un moment donné, mais elles ne permettent pas au moteur de base de données de déterminer la source de cette altération. Historiquement, la cause dominante de cette altération a été constatée comme provenant de sources autres que le moteur de base de données lui-même.

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
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFile](./jetopenfile-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
