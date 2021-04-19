---
description: 'En savoir plus sur : fonction JetStopService'
title: Fonction JetStopService
TOCTitle: JetStopService Function
ms:assetid: 46aeb9ed-ee72-49cc-99e3-791a51a55b02
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269240(v=EXCHG.10)
ms:contentKeyID: 32765542
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetStopService
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1e66b4e5242710c89ca7e7964ecd0a72774b719d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516693"
---
# <a name="jetstopservice-function"></a>Fonction JetStopService


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetstopservice-function"></a>Fonction JetStopService

La fonction **JetStopService** prépare une instance pour l’arrêt.

**JetStopService** est l’appel hérité lorsqu’une seule instance est autorisée. Dans ce cas, la seule instance active est celle qui est préparée pour l’arrêt.

```cpp
    JET_ERR JET_API JetStopService(void);
```

### <a name="parameters"></a>Paramètres

Cette fonction n’a pas de paramètres.

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
<td><p>JET_errRunningInMultiInstanceMode</p></td>
<td><p>Il n’est pas évident de déterminer l’instance à préparer pour l’arrêt lors de l’utilisation de <strong>JetStopService</strong> avec plusieurs modes d’instance.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est réussie, elle se prépare à un arrêt ultérieur. Les étapes à suivre pour préparer un arrêt sont les suivantes :

  - Arrêtez la défragmentation en ligne si elle est en cours d’exécution.

  - Démarrez un nettoyage de la Banque des versions.

  - Réduisez la profondeur du point de contrôle en commençant à vider les pages incorrectes dans le gestionnaire de tampons.

  - Empêcher les appels ultérieurs à la plupart des fonctions pour cette instance.

Si cette fonction échoue, aucune des étapes de préparation d’un arrêt de l’instance n’est effectuée, donc aucune modification de l’état de l’instance ne se produit.

#### <a name="remarks"></a>Notes

Cette fonction réduit le travail que l’instance doit effectuer une fois qu’elle est terminée, mais ne met pas fin à l’instance. Par conséquent, cette fonction est simplement une optimisation et n’est pas obligatoire pour l’utilisation. Notez que la quantité de travail effectuée en préparation était moins importante dans Windows 2000 et Windows XP. Une fois la fonction réussie, l’appel de fonctions qui ne sont plus autorisées retourne JET_errClientRequestToStopJetService. Les fonctions qui sont toujours autorisées après cet appel sont les suivantes : [JetRollback](./jetrollback-function.md), [JetCloseTable](./jetclosetable-function.md), [JetEndSession](./jetendsession-function.md), [JetCloseDatabase](./jetclosedatabase-function.md), [JetDetachDatabase](./jetdetachdatabase-function.md) et [JetResetSessionContext](./jetresetsessioncontext-function.md).

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
[JET_INSTANCE](./jet-instance.md)  
[JetCloseDatabase](./jetclosedatabase-function.md)  
[JetCloseTable](./jetclosetable-function.md)  
[JetDetachDatabase](./jetdetachdatabase-function.md)  
[JetEndSession](./jetendsession-function.md)  
[JetResetSessionContext](./jetresetsessioncontext-function.md)  
[JetRollback](./jetrollback-function.md)  
[JetTerm](./jetterm-function.md)  
[JetTerm2](./jetterm2-function.md)
