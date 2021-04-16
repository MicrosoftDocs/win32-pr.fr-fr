---
description: 'En savoir plus sur : fonction JetReadFileInstance'
title: Fonction JetReadFileInstance
TOCTitle: JetReadFileInstance Function
ms:assetid: b17b4b43-86e5-4507-8a85-bbd5eac0aa3c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294060(v=EXCHG.10)
ms:contentKeyID: 32765675
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetReadFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e9aad9828a92d67f2e7411aa534103696d913934
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524958"
---
# <a name="jetreadfileinstance-function"></a>Fonction JetReadFileInstance


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetreadfileinstance-function"></a>Fonction JetReadFileInstance

La fonction **JetReadFileInstance** récupère le contenu d’un fichier ouvert avec la fonction [JetOpenFileInstance](./jetopenfileinstance-function.md) .

**Windows XP**:   **JetReadFileInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetReadFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile,
      __out         void* pv,
      __in          unsigned long cb,
      __out_opt     unsigned long* pcb
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour un appel d’API particulier.

Notez que pour Windows 2000, la variante d’API qui accepte ce paramètre n’est pas disponible, car une seule instance est prise en charge. L’utilisation de cette instance globale est implicitement dans ce cas.

Pour Windows XP et les versions ultérieures, vous pouvez appeler la variante API qui n’accepte pas ce paramètre uniquement quand le moteur est en mode hérité (mode de compatibilité Windows 2000) dans les cas où une seule instance est prise en charge. Dans le cas contraire, l’opération échoue et retourne l’erreur JET_errRunningInMultiInstanceMode.

*hfFile*

Handle du fichier à lire.

*va*

Mémoire tampon de sortie qui recevra les données du fichier.

*libéré*

Taille maximale, en octets, de la mémoire tampon de sortie.

*PCB*

Quantité réelle de données de fichier récupérées.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction facilite le retour de tout [JET_ERR](./jet-err.md) types de données définis dans l’API ESE (Extensible Storage Engine). Pour plus d’informations sur les erreurs JET, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Code de retour</p></th>
<th><p>Signification</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_errSuccess</p></td>
<td><p>L’opération s’est terminée avec succès.</p></td>
</tr>
<tr class="even">
<td><p>JET_errBackupAbortByServer</p></td>
<td><p>L’opération a échoué, car la sauvegarde externe actuelle a été abandonnée par un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> . Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable nécessitant que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres spécifiés contient une valeur inattendue ou une valeur qui n’a pas de sens lorsqu’elle est associée à la valeur d’un autre paramètre. Cela peut se produire pour la fonction <strong>JetReadFileInstance</strong> lorsque l’un des éléments suivants se produit :</p>
<ul>
<li><p>Le handle d’instance spécifié n’est pas valide. Windows XP et versions ultérieures de Windows.</p></li>
<li><p>La taille de la mémoire tampon de sortie n’est pas un multiple de la taille de page de la base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>). Windows XP et versions ultérieures de Windows.</p></li>
<li><p>La taille de la mémoire tampon de sortie est inférieure à trois pages de base de données (<a href="gg269337(v=exchg.10).md">JET_paramDatabasePageSize</a>), et il s’agit du premier appel à la fonction <strong>JetReadFileInstance</strong> pour le handle spécifié. Windows XP et versions ultérieures de Windows.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errLogReadVerifyFailure</p></td>
<td><p>L’opération a échoué car une altération des données irrécupérable a été détectée lors de la lecture d’un fichier journal de transactions. Cette erreur est retournée uniquement par Windows XP et les versions ultérieures de Windows.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNoBackup</p></td>
<td><p>L’opération a échoué, car aucune sauvegarde externe n’est en cours.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à cette session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errReadVerifyFailure</p></td>
<td><p>L’opération a échoué car une altération des données irrécupérable a été détectée lors de la lecture d’une page de base de données à partir d’un fichier de base de données ou d’un fichier correctif</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à cette session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>L’opération a échoué en raison d’une tentative d’utilisation du moteur en mode hérité (mode de compatibilité de Windows 2000) dans le cas où une seule instance est prise en charge, alors que plusieurs instances existent déjà.</p></td>
</tr>
<tr class="even">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à cette session est en cours d’arrêt.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le segment de données suivant du fichier est lu dans la mémoire tampon de sortie. Le nombre réel d’octets récupérés est également retourné. Le décalage de fichier à partir duquel la lecture suivante aura lieu sera avancé par ce montant.

En cas d’échec, l’état de la mémoire tampon de sortie n’est pas défini. L’échec entraîne l’annulation de l’ensemble du processus de sauvegarde pour l’instance actuelle. Dans Windows XP et les versions ultérieures de Windows, la sauvegarde n’est pas annulée si une erreur s’est produite lors de la lecture d’un fichier de base de données. Toutefois, la sauvegarde de ce fichier de base de données restera annulée et le descripteur correspondant sera automatiquement fermé.

#### <a name="remarks"></a>Notes

Tout appel à la fonction **JetReadFileInstance** effectué à l’aide d’un handle qui a déjà retourné toutes les données du fichier sous-jacent (par exemple, si un appel précédent a retourné moins d’octets que la taille de la mémoire tampon de sortie) est toujours concluant, mais retourne zéro octet de données.

Vous devez utiliser une mémoire tampon de sortie importante pour optimiser les performances de sauvegarde. Vous devrez peut-être faire des essais pour trouver le compromis optimal entre la consommation des ressources et le débit pour une situation particulière. Dans tous les cas, la mémoire tampon de sortie ne doit pas être inférieure à 64 Ko. Le pointeur que vous transmettez à **JetReadFileInstance** doit être aligné sur une limite de page mémoire (soit 4 Ko soit 8 Ko). Pour ce faire, vous pouvez appeler la fonction **VirtualAlloc** .

Plusieurs appels simultanés à **JetReadFileInstance** effectués à l’aide du même descripteur de fichier ne sont pas pris en charge. Cela signifie qu’il n’est pas possible de mettre en file d’attente plusieurs mémoires tampons pour la lecture simultanée dans le même fichier afin d’obtenir un débit séquentiel élevé. Vous devez utiliser un seul tampon de grande taille à la place.

Si vous avez configuré une instance particulière de telle sorte que la modification de pages de base de données soit activée (voir le paramètre [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)), les données supprimées sont supprimées de la base de données en tant qu’effet secondaire d’un appel à **JetReadFileInstance** sur le fichier de base de données.

Il est très important de comprendre comment la sauvegarde et l’altération des données interagissent. Si le moteur de base de données détecte une altération des données au cours d’une sauvegarde, il échouera à la sauvegarde de la base de données concernée ou de la totalité de l’instance. Il s’agit d’une décision de conception consciente destinée à vous protéger contre la perte de données. Si le moteur de base de données a permis à une sauvegarde de se dérouler alors que des données sont endommagées, il est possible qu’une sauvegarde plus ancienne et non endommagée soit ignorée. Cela serait désastreux, car il serait possible de corriger les données endommagées sur l’instance en direct en restaurant cette sauvegarde et en relisant tous les fichiers du journal des transactions sur cette base de données. Ce scénario de perte de données nulle suppose que l’enregistrement circulaire n’est pas activé (voir [JET_paramCircularLog](./transaction-log-parameters.md) dans les [paramètres système](./extensible-storage-engine-system-parameters.md)).

Il est également important de comprendre que les cas d’endommagement des données sont généralement détectés pour la première fois lors de la sauvegarde en continu. Cela est dû au fait que la sauvegarde en continu est le seul processus qui analyse régulièrement chaque page d’un fichier de base de données. Il est également probable que la sauvegarde en continu sera le premier processus de détection des signes précoces de défaillance matérielle comme indiqué par des erreurs de corruption de données intermittentes, en raison de la quantité de données récupérées par la sauvegarde et de la vitesse à laquelle ces données sont récupérées.

La corruption des données est détectée par le moteur de base de données via l’utilisation de sommes de contrôle de bloc. Ces sommes de contrôle sont définies juste avant l’écriture d’une page de base de données et sont vérifiées lors de la lecture d’une page de base de données. Ce schéma permet au moteur de base de données de déterminer que les données ont été endommagées à un moment donné, mais ne permet pas au moteur de base de données de déterminer la source de l’altération. Historiquement, les instances de ces données endommagées proviennent de sources autres que le moteur de base de données lui-même.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>Serveur</p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
</tr>
<tr class="odd">
<td><p>En-tête</p></td>
<td><p>Est déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothèque</p></td>
<td><p>Utilise ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_HANDLE](./jet-handle.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetOpenFileInstance](./jetopenfileinstance-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
