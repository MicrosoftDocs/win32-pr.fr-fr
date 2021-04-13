---
description: 'En savoir plus sur : fonction JetInit3'
title: Fonction JetInit3
TOCTitle: JetInit3 Function
ms:assetid: 752589b6-1b8f-4b6f-a14a-00f4b1405db5
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269296(v=EXCHG.10)
ms:contentKeyID: 32765588
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetInit3
- JetInit3A
- JetInit3W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c96171920b7538e71e822eaf0879e476fb2fd31e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321145"
---
# <a name="jetinit3-function"></a>Fonction JetInit3


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetinit3-function"></a>Fonction JetInit3

La fonction **JetInit3** place le moteur de base de données dans un État dans lequel il peut prendre en charge l’utilisation des fichiers de base de données par l’application. Le moteur doit déjà être correctement configuré pour l’initialisation, ce que vous effectuez à l’aide de la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) . Notez que la récupération après incident de la base de données se produit automatiquement dans le cadre du processus d’initialisation.

**Windows Vista :**  **JetInit3** est introduit dans Windows Vista.

```cpp
    JET_ERR JET_API JetInit3(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in_opt      JET_RSTINFO* prstInfo,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*pinstance*

Instance que vous utilisez pour un appel particulier. L’utilisation de ce paramètre dépend du mode de fonctionnement du moteur. Si le moteur fonctionne en mode hérité (mode de compatibilité Windows 2000), dans lequel une seule instance est prise en charge, vous pouvez définir ce paramètre sur **null** ou sur une mémoire tampon de sortie valide contenant **null** ou JET_instanceNil, qui retourne le handle d’instance global créé comme un effet secondaire de l’initialisation. Ce descripteur d’instance peut ensuite être passé à toute autre API qui prend une instance. Si le moteur fonctionne en mode multi-instance, vous devez définir ce paramètre sur une mémoire tampon d’entrée valide qui contient le handle d’instance retourné par la fonction [JetCreateInstance](./jetcreateinstance-function.md) qui est en cours d’initialisation.

*prstInfo*

Paramètres de récupération supplémentaires utilisés pour le remappage des bases de données lors de la récupération, pour définir la position d’arrêt de la récupération ou pour déterminer l’état actuel de la récupération.

*grbit*

Groupe de bits qui spécifie zéro, une ou plusieurs des options énumérées et définies dans le tableau suivant.

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
<td><p>JET_bitReplayReplicatedLogFiles</p></td>
<td><p>Cette valeur est réservée à une utilisation ultérieure.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitCreateSFSVolumeIfNotExist</p></td>
<td><p>Cette valeur est réservée à une utilisation ultérieure.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreMissingDB</p></td>
<td><p>Cette valeur permet à l’utilisateur d’exécuter la récupération sur un ensemble de fichiers journaux, même en l’absence de bases de données attachées au fichier journal défini à un moment donné.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitRecoveryWithoutUndo</p></td>
<td><p>Cette valeur permet à l’utilisateur d’effectuer la récupération, mais uniquement jusqu’à la phase d’annulation (sans inclure). À l’aide de cette valeur, les journaux de transactions supplémentaires peuvent être copiés et appliqués.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTruncateLogsAfterRecovery</p></td>
<td><p>Cette valeur entraîne la troncation des fichiers journaux au cours d’une récupération logicielle réussie.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitReplayMissingMapEntryDB</p></td>
<td><p>Cette valeur entraîne l’absence d’une entrée de mappage de base de données par défaut au même emplacement.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitReplayIgnoreLostLogs</p></td>
<td><p>Cette valeur entraîne l’ignorance des journaux perdus à partir de la fin du flux de journal au cours d’une récupération.</p>
<p><strong>Windows 7 : JET_bitReplayIgnoreLostLogs</strong> est introduite dans Windows 7.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


#### <a name="remarks"></a>Notes

Une instance doit être initialisée avec un appel à la fonction **JetInit3** avant de pouvoir être utilisée par autre chose que la fonction [JetSetSystemParameter](./jetsetsystemparameter-function.md) .

Une instance est détruite par un appel à la fonction [JetTerm](./jetterm-function.md) , même si cette instance n’a jamais été initialisée à l’aide de la fonction [JetInit](./jetinit-function.md) . Une instance est l’unité de récupérabilité pour le moteur de base de données. Il contrôle le cycle de vie de tous les fichiers utilisés pour protéger l’intégrité des données dans un ensemble de fichiers de base de données. Ces fichiers incluent le fichier de point de contrôle et les fichiers journaux des transactions. Notez que [JetTerm](./jetterm-function.md) ne doit pas être appelé si la fonction **JetInit3** échoue. Toutefois, [JetTerm](./jetterm-function.md) doit toujours être appelé pour toutes les instances créées par **JetCreateInstance2** si **JetInit3** n’a jamais été appelé ou si **JetInit3** s’exécute correctement.

Si la récupération s’exécute sur un ensemble de journaux pour lesquels toutes les bases de données associées ne sont pas présentes (ce qui renvoie l’erreur JET_errAttachedDatabaseMismatch dans des conditions normales) et que le client souhaite que la récupération continue malgré les bases de données manquantes, l’erreur JET_bitReplayIgnoreMissingDB est utilisée pour poursuivre la récupération des bases de données disponibles.

Comme la récupération après incident ne se produit généralement pas sur le même ordinateur (et avec la même configuration) qu’au moment de l’incident, une base de données ne change pas d’emplacement en général. Dans certains scénarios, tels que le déplacement de fichiers vers un autre ordinateur ou la restauration d’une sauvegarde d’instantané vers différents emplacements, ce n’est plus le cas. La fonction **JetInit3** vous permet de spécifier un mappage (à l’aide des structures [JET_RSTINFO](./jet-rstinfo-structure.md) et [JET_RSTMAP](./jet-rstmap-structure.md) ) entre l’ancien emplacement de base de données et son nouvel emplacement. En fait, vous n’avez besoin que du nouvel emplacement tant que les fichiers de base de données sont présents à cet emplacement. Dès que vous connaissez l’emplacement des bases de données restaurées, la signature de base de données est utilisée pour identifier la base de données par le biais du processus de restauration. Vous aurez besoin de l’emplacement de la base de données d’origine uniquement si vous devez recréer une base de données, auquel cas la signature est connue.

En outre, si vous devez arrêter une récupération après une opération d’annulation, vous pouvez spécifier une position de journal particulière à laquelle la récupération s’arrêtera. Notez que cela comprend la possibilité de s’arrêter à la fin d’une génération de journal particulière si la position spécifiée fait partie de la génération, mais au-delà de la fin du journal réel.

Pour plus d’informations, consultez la section « Notes » de la rubrique [JetInit](./jetinit-function.md) .

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Client</p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p>Serveur</p></td>
<td><p>Requiert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p>En-tête</p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
<tr class="even">
<td><p>Bibliothèque</p></td>
<td><p>Utilise ESENT. lib.</p></td>
</tr>
<tr class="odd">
<td><p>DLL</p></td>
<td><p>Requiert ESENT.dll.</p></td>
</tr>
<tr class="even">
<td><p>Unicode</p></td>
<td><p>Implémenté en tant que <strong>JetInit3W</strong> (Unicode) et <strong>JetInit3A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[Fichiers ESE (Extensible Storage Engine)](./extensible-storage-engine-files.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_RSTINFO](./jet-rstinfo-structure.md)  
[JET_RSTMAP](./jet-rstmap-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[Paramètres de ressource](./resource-parameters.md)
