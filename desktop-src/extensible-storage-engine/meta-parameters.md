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
ms.openlocfilehash: 2f821d3aea8055f6c1344ed9d5107417adbaf604
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985512"
---
# <a name="meta-parameters"></a>Paramètres méta


_**S’applique à :** Windows | Windows Serveurs_

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


| <p>Paramètre système</p> | <p>Nouvelle valeur par défaut</p> | 
|-------------------------|--------------------------|
| <p>JET_paramMaxSessions</p> | <p>30000</p> | 
| <p>JET_paramMaxOpenTables</p> | <p>2147483647</p> | 
| <p>JET_paramMaxCursors</p> | <p>2147483647</p> | 
| <p>JET_paramMaxVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramMaxTemporaryTables</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileSize</p> | <p>64</p> | 
| <p>JET_paramLogBuffers</p> | <p>1</p> | 
| <p>JET_paramDbExtensionSize</p> | <p>16</p> | 
| <p>JET_paramPageTempDBMin</p> | <p>14</p> | 
| <p>JET_paramCacheSizeMax</p> | <p>16</p> | 
| <p>JET_paramCheckpointDepthMax</p> | <p>65536</p> | 
| <p>JET_paramLRUKHistoryMax</p> | <p>10</p> | 
| <p>JET_paramOutstandingIOMax</p> | <p>16</p> | 
| <p>JET_paramStartFlushThreshold</p> | <p>1</p> | 
| <p>JET_paramStopFlushThreshold</p> | <p>2</p> | 
| <p>JET_paramNoInformationEvent</p> | <p>1</p> | 
| <p>JET_paramCacheSizeMin</p> | <p>16</p> | 
| <p>JET_paramPreferredVerPages</p> | <p>2147483647</p> | 
| <p>JET_paramLogFileCreateAsynch</p> | <p>0</p> | 
| <p>JET_paramGlobalMinVerPages</p> | <p>1</p> | 
| <p>JET_paramPageHintCacheSize</p> | <p>32</p> | 
| <p>JET_paramDisablePerfmon</p> | <p>1</p> | 
| <p>JET_paramEnableFileCache</p> | <p>1</p> | 
| <p>JET_paramEnableViewCache</p> | <p>1</p> | 
| <p>JET_paramVerPageSize</p> | <p>1 024</p> | 
| <p>JET_paramEnableAdvanced</p> | <p>0</p> | 
| <p>JET_paramCheckpointIOMax</p> | <p>8</p> | 



Une petite configuration a également plusieurs autres effets sur le moteur de base de données, notamment :

  - Toutes les ressources gérées par les paramètres système sont allouées à partir du segment de mémoire en fonction des besoins

  - Les autres ressources internes utilisées par le moteur de base de données sont réduites en taille

  - Diverses activités de maintenance sont mises à l’échelle pour éviter l’activité des threads en arrière-plan


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>1 (hérité)</p> | 
| <p>Tapez :</p> | <p>Entier</p> | 
| <p>Plage valide :</p> | <p>0 – 1</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>No</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>Yes</p> | 
| <p>Affecte les ressources :</p> | <p>Yes</p> | 
| <p>Disponibilité :</p> | <p>à compter de Windows Server 2008 et Windows Vista</p> | 



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


| Étiquette | Valeur |
|--------|-------|
| <p>Valeur par défaut :</p> | <p>Vrai</p> | 
| <p>Tapez :</p> | <p>Booléen</p> | 
| <p>Plage valide :</p> | <p>False, True</p> | 
| <p>Étendue :</p> | <p>Instance</p> | 
| <p>Définir après <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</p> | <p>Yes</p> | 
| <p>Définir après <a href="gg294068(v=exchg.10).md">JetInit</a>:</p> | <p>Yes</p> | 
| <p>Affecte la disposition physique :</p> | <p>No</p> | 
| <p>Affecte la fiabilité :</p> | <p>No</p> | 
| <p>Affecte les performances :</p> | <p>No</p> | 
| <p>Affecte les ressources :</p> | <p>No</p> | 
| <p>Disponibilité :</p> | <p>à compter de Windows Server 2008 et Windows Vista</p> | 



### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)
