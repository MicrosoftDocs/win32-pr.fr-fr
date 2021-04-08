---
description: 'En savoir plus sur : fonction JetStopServiceInstance2'
title: JetStopServiceInstance2 fonction)
TOCTitle: JetStopServiceInstance2 Function
ms:assetid: ac021e13-ec83-42eb-9aef-a906d7a7ed39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835046(v=EXCHG.10)
ms:contentKeyID: 49894668
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetStopServiceInstance2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5029e2cf45ec91d0282f32491895a24b32e6259e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752277"
---
# <a name="jetstopserviceinstance2-function"></a>JetStopServiceInstance2 fonction)


_**S’applique à :** Windows | Serveur Windows_

La fonction **JetStopServiceInstance2** prépare une instance avant de suspendre et prépare une instance après la reprise. Les États d’interruption et de reprise sont les États d’exécution du modèle de cycle de vie des applications du Windows Store.

La fonction **JetStopServiceInstance2** a été introduite dans Windows 8.

``` c++
JET_ERR JET_API JetStopServiceInstance2(
  _In_          JET_INSTANCE       instance
  _In_          const JET_GRBIT    grbit
);
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance cible. Le type de données **JET_INSTANCE** est un descripteur de l’instance de la base de données à utiliser pour un appel à l’API jet. Ce descripteur est obtenu lorsque vous créez une instance de la base de données en appelant les fonctions [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .

*grbit*

Groupe de bits qui spécifie une ou plusieurs des valeurs énumérées et définies dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitStopServiceAll</p></td>
<td><p>Arrête tous les services ESE (Extensible Storage Engine) pour l’instance spécifiée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceBackgroundUserTasks</p></td>
<td><p>Arrête les tâches de maintenance en arrière-plan du client redémarrables (par exemple, la défragmentation B + Tree).</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitStopServiceQuiesceCaches</p></td>
<td><p>Quiesces tous les caches modifiés sur le disque. Cette valeur est asynchrone et peut être annulée.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitStopServiceResume</p></td>
<td><p>Reprend les opérations StopService précédemment émises ; autrement dit, il redémarre le service. Cette valeur peut être combinée avec le paramètre <em>grbits</em> pour reprendre des services spécifiques, ou avec JET_bitStopServiceAll pour reprendre tous les services précédemment arrêtés. Ce bit ne peut être utilisé que pour reprendre StopServiceBackgroundUserTasks et JET_bitStopServiceQuiesceCaches. Si vous avez précédemment appelé avec JET_bitStopServiceAll, une tentative d’utilisation de JET_bitStopServiceResume échouera. Si la deuxième étape de reprise n’est pas appelée, l’application aura une dégradation des performances. Dans ce cas, le point de contrôle est conservé à zéro.</p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a>Valeur retournée

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
</tbody>
</table>


#### <a name="remarks"></a>Notes

Cette fonction permet à une application JET de déplacer le cache de base de données à un état propre ou presque propre (avec les e/s du système d’exploitation inactives), de sorte que si l’application doit être arrêtée, la récupération est rapide. Cette approche est préférable à l’arrêt de JET en appelant les fonctions [JetTerm](./jetterm-function.md) ou [JetDetachDatabase](./jetdetachdatabase-function.md) , de sorte que dans le scénario le plus courant, l’application n’est pas suspendue, et par la suite, l’application dispose de l’ensemble du cache et est prête à être utilisée dès que possible.

Si cette fonction est réussie, elle prépare le cache de base de données pour une suspension imminente. Cette fonction met en file d’attente le travail sur un thread de travail en arrière-plan et retourne immédiatement à l’appelant. La fonction doit être appelée en fonction de l’VisibilityNotice de PLM, plutôt que d’appeler à partir du gestionnaire d’événements de suspension de l’application pour s’assurer que JET a le temps de vider les tampons modifiés avant que la gestion PLM interrompe/arrête le processus. En interne, JET déclenche une distribution immédiate de la maintenance des points de contrôle lors de la modification de la configuration (soit la mise à jour des points de contrôle, soit le nouveau bit de suspension des caches). Pour plus d’informations sur les événements VisibilityNotice, consultez [classe VisibilityChangedEventArgs](/uwp/api/windows.ui.core.visibilitychangedeventargs).

Cette fonction doit être appelée deux fois. Elle est appelée une fois que l’application a reçu l’avis de suspension du système d’exploitation, mais avant que l’application ne soit interrompue. Ensuite, il est à nouveau appelé après que le système d’exploitation a repris l’application. Par exemple :

En cas d’appel pour suspendre : JET_ERR JET_API JetStopServiceInstance2 (instance, JET_bitStopServiceQuiesceCaches);

En cas de reprise : JET_ERR JET_API JetStopServiceInstance2 (instance, JET_bitStopServiceQuiesceCaches | JET_bitStopServiceResume);

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Requiert Windows 8.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2012.</p></td>
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
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
