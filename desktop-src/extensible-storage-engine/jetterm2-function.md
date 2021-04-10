---
description: 'En savoir plus sur : fonction JetTerm2'
title: Fonction JetTerm2
TOCTitle: JetTerm2 Function
ms:assetid: 36464e24-1cc0-4cda-9d7a-f64555c622bf
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269223(v=EXCHG.10)
ms:contentKeyID: 32765525
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm2
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dc8b0c768e981b88e8759c30d349caa8e5575a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113602"
---
# <a name="jetterm2-function"></a>Fonction JetTerm2


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetterm2-function"></a>Fonction JetTerm2

La fonction **JetTerm2** lance l’arrêt d’une instance qui a été initialisée par [JetInit](./jetinit-function.md).

**JetTerm2** peut également détruire une instance non initialisée qui a été créée par [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm2(
      __in          JET_INSTANCE instance,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

**Windows 2000 :**  Ce paramètre est ignoré et doit toujours avoir la **valeur null**.

**Windows XP et versions ultérieures :**  Ce paramètre est surchargé. Si le moteur fonctionne en mode hérité (mode de compatibilité de Windows 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur null** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md). Si le moteur fonctionne en mode multi-instance, ce paramètre doit être un pointeur vers une instance créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.

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
<td><p>JET_bitTermComplete</p></td>
<td><p>Demande que l’instance soit arrêtée proprement. Tout travail de nettoyage facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est immédiatement effectué.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermAbrupt</p></td>
<td><p>Demande que l’instance soit arrêtée aussi rapidement que possible. Tout travail facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est abandonné.</p>
<p><strong>Remarque</strong>  Cette option peut entraîner une perte d’espace temporaire ou permanente dans la base de données. Cet espace perdu peut toujours être récupéré via une défragmentation hors connexion de la base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitTermStopBackup</p></td>
<td><p>Demande que l’instance soit arrêtée même si une sauvegarde est actuellement en cours. En règle générale, une sauvegarde en attente provoquerait l’échec de <a href="gg269298(v=exchg.10).md">JetTerm</a> avec JET_errBackupInProgress. Quand ce paramètre n’est pas présent, sa valeur est supposée être JET_bitTermAbrupt.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitTermDirty</p></td>
<td><p>Demande que l’instance soit arrêtée avec toutes les bases de données attachées laissées dans un état modifié.</p>
<p>Windows 7 : JET_bitTermDirty est introduite dans Windows 7.</p></td>
</tr>
</tbody>
</table>


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
<td><p>JET_errBackupInProgress</p></td>
<td><p>Impossible de terminer l’opération, car une opération de sauvegarde est en cours sur l’instance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu. Cette erreur est retournée par <a href="gg269298(v=exchg.10).md">JetTerm</a> lorsque le moteur est en mode multi-instance et lorsque <em>pinstance</em> fait référence à une instance non valide.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="even">
<td><p>JET_errNotInitialized</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance n’a pas encore été initialisée.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>L’opération ne peut pas se terminer car l’instance est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTooManyActiveUsers</p></td>
<td><p>L’instance ne peut pas être arrêtée, car il existe actuellement des sessions avec des transactions actives pour l’instance spécifiée. Cette erreur se produit uniquement si le JET_bitTermComplete est utilisé.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est réussie, l’instance spécifiée est arrêtée. Le descripteur d’instance est également fermé et rendu non disponible pour toute API qui accepte un handle d’instance. Tous les autres objets associés à l’instance, tels que les sessions, sont également fermés. L’état du fichier de point de contrôle, des fichiers journaux des transactions et des fichiers de base de données attachés à l’instance sera modifié au cours du processus d’arrêt.

Si cette fonction échoue en raison d’une erreur d’utilisation, l’instance reste dans un état initialisé et rien ne change. Dans le cas contraire, l’instance est toujours arrêtée comme indiqué dans le cas de réussite. La différence est que l’instance doit passer par la récupération après incident lorsqu’elle est ensuite initialisée. Le moteur essaiera de vider le plus de données possible pour réduire la quantité de récupération requise. Conceptuellement, un tel échec de [JetTerm](./jetterm-function.md) n’est pas différent d’un blocage de processus.

#### <a name="remarks"></a>Notes

Consultez [JetTerm](./jetterm-function.md).

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
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
