---
description: 'En savoir plus sur : méta-paramètres'
title: Paramètres méta
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542892"
---
# <a name="meta-parameters"></a>Paramètres méta


_**S’applique à :** Windows | Serveur Windows_

## <a name="meta-parameters"></a>Paramètres méta

Cette rubrique contient des paramètres qui permettent de contrôler d’autres paramètres.

JET_paramConfiguration  
129  
Ce paramètre expose plusieurs jeux de valeurs par défaut pour l’ensemble des paramètres système. Quand ce paramètre est défini sur une configuration spécifique, toutes les valeurs des paramètres système sont réinitialisées à leurs valeurs par défaut pour cette configuration. Si la configuration est définie pour une instance spécifique, les valeurs par défaut des paramètres système globaux ne sont pas réinitialisées.

En outre, le paramètre lui-même peut avoir d’autres effets sur le comportement du moteur de base de données.

À ce stade, il existe deux configurations prises en charge :

  - Petite configuration (0) : le moteur de base de données est optimisé pour l’utilisation de la mémoire.

  - Configuration héritée (1) : le moteur de base de données a ses valeurs par défaut traditionnelles.

Une petite configuration modifie les valeurs par défaut des paramètres système suivants pour les valeurs spécifiées :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Paramètre système</p></th>
<th><p>Nouvelle valeur par défaut</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_paramMaxSessions</p></td>
<td><p>30000</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxOpenTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxCursors</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramMaxVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramMaxTemporaryTables</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLogFileSize</p></td>
<td><p>64</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogBuffers</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDbExtensionSize</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageTempDBMin</p></td>
<td><p>14</p></td>
</tr>
<tr class="even">
<td><p>JET_paramCacheSizeMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointDepthMax</p></td>
<td><p>65536</p></td>
</tr>
<tr class="even">
<td><p>JET_paramLRUKHistoryMax</p></td>
<td><p>10</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramOutstandingIOMax</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramStartFlushThreshold</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramStopFlushThreshold</p></td>
<td><p>2</p></td>
</tr>
<tr class="even">
<td><p>JET_paramNoInformationEvent</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCacheSizeMin</p></td>
<td><p>16</p></td>
</tr>
<tr class="even">
<td><p>JET_paramPreferredVerPages</p></td>
<td><p>2147483647</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramLogFileCreateAsynch</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>JET_paramGlobalMinVerPages</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramPageHintCacheSize</p></td>
<td><p>32</p></td>
</tr>
<tr class="even">
<td><p>JET_paramDisablePerfmon</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramEnableFileCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableViewCache</p></td>
<td><p>1</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramVerPageSize</p></td>
<td><p>1 024</p></td>
</tr>
<tr class="even">
<td><p>JET_paramEnableAdvanced</p></td>
<td><p>0</p></td>
</tr>
<tr class="odd">
<td><p>JET_paramCheckpointIOMax</p></td>
<td><p>8</p></td>
</tr>
</tbody>
</table>


Une petite configuration a également plusieurs autres effets sur le moteur de base de données, notamment :

  - Toutes les ressources gérées par les paramètres système sont allouées à partir du segment de mémoire en fonction des besoins

  - Les autres ressources internes utilisées par le moteur de base de données sont réduites en taille

  - Diverses activités de maintenance sont mises à l’échelle pour éviter l’activité des threads en arrière-plan

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>1 (hérité)</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Integer</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>0 – 1</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>À compter de Windows Server 2008 et Windows Vista</p></td>
</tr>
</tbody>
</table>


JET_paramEnableAdvanced  
130  
Ce paramètre est utilisé pour contrôler le moment où le moteur de base de données accepte ou rejette les modifications apportées à un sous-ensemble des paramètres système. Ce paramètre est utilisé conjointement avec JET_paramConfiguration pour empêcher la définition de certains paramètres système à partir des valeurs par défaut de la configuration sélectionnée.

Les paramètres système suivants seront protégés de la définition lorsque ce paramètre est défini sur false :

  - JET_paramMaxSessionsfon

  - JET_paramMaxOpenTables

  - JET_paramPreferredMaxOpenTables

  - JET_paramMaxCursors

  - JET_paramMaxVerPages

  - JET_paramMaxTemporaryTables

  - JET_paramLogBuffers

  - JET_paramWaitLogFlush

  - JET_paramLogCheckpointPeriod

  - JET_paramLogWaitingUserMax

  - JET_paramDbExtensionSize

  - JET_paramPageTempDBMin

  - JET_paramPageFragment

  - JET_paramBatchIOBufferMax

  - JET_paramCacheSizeMax

  - JET_paramLRUKCorrInterval

  - JET_paramLRUKHistoryMax

  - JET_paramLRUKPolicy

  - JET_paramLRUKTimeout

  - JET_paramLRUKTrxCorrInterval

  - JET_paramOutstandingIOMax

  - JET_paramStartFlushThreshold

  - JET_paramStopFlushThreshold

  - JET_paramCacheSize

  - JET_paramCacheSizeMin

  - JET_paramPreferredVerPages

  - JET_paramBackupChunkSize

  - JET_paramBackupOutstandingReads

  - JET_paramLogFileCreateAsynch

  - JET_paramRecordUpgradeDirtyLevel

  - JET_paramGlobalMinVerPages

  - JET_paramPageHintCacheSize

  - JET_paramVersionStoreTaskQueueMax

  - JET_paramDBAPageAvailMin

  - JET_paramMaxRandomIOSize

  - JET_paramCachedClosedTables

  - JET_paramEnableFileCache

  - JET_paramEnableViewCache

  - JET_paramVerPageSize

  - JET_paramCheckpointIOMax

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Valeur par défaut :</p></td>
<td><p>Vrai</p></td>
</tr>
<tr class="even">
<td><p>Tapez :</p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="odd">
<td><p>Plage valide :</p></td>
<td><p>False, True</p></td>
</tr>
<tr class="even">
<td><p>Étendue :</p></td>
<td><p>Instance</p></td>
</tr>
<tr class="odd">
<td><p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="even">
<td><p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p></td>
<td><p>Oui</p></td>
</tr>
<tr class="odd">
<td><p>Affecte la disposition physique :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte la fiabilité :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Affecte les performances :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="even">
<td><p>Affecte les ressources :</p></td>
<td><p>Non</p></td>
</tr>
<tr class="odd">
<td><p>Disponibilité :</p></td>
<td><p>À compter de Windows Server 2008 et Windows Vista</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
