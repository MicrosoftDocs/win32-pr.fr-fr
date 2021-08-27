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
ms.openlocfilehash: b9f8e5f278a0ef3eb44efd64314745d2fed6d89b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466616"
---
# <a name="jetterm2-function"></a>Fonction JetTerm2


_**S’applique à :** Windows | Windows Serveurs_

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

**Windows XP et versions ultérieures :**  Ce paramètre est surchargé. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur NULL** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md). Si le moteur fonctionne en mode multi-instance, ce paramètre doit être un pointeur vers une instance créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).

*grbit*

Groupe de bits qui contiennent les options à utiliser pour cet appel, qui incluent zéro, une ou plusieurs des valeurs suivantes.


| <p>Valeur</p> | <p>Signification</p> | 
|--------------|----------------|
| <p>JET_bitTermComplete</p> | <p>Demande que l’instance soit arrêtée proprement. Tout travail de nettoyage facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est immédiatement effectué.</p> | 
| <p>JET_bitTermAbrupt</p> | <p>Demande que l’instance soit arrêtée aussi rapidement que possible. Tout travail facultatif qui serait normalement effectué en arrière-plan au moment de l’exécution est abandonné.</p><p><strong>Remarque</strong>  Cette option peut entraîner une perte d’espace temporaire ou permanente dans la base de données. Cet espace perdu peut toujours être récupéré via une défragmentation hors connexion de la base de données.</p> | 
| <p>JET_bitTermStopBackup</p> | <p>Demande que l’instance soit arrêtée même si une sauvegarde est actuellement en cours. En règle générale, une sauvegarde en attente provoquerait l’échec de <a href="gg269298(v=exchg.10).md">JetTerm</a> avec JET_errBackupInProgress. Quand ce paramètre n’est pas présent, sa valeur est supposée être JET_bitTermAbrupt.</p> | 
| <p>JET_bitTermDirty</p> | <p>Demande que l’instance soit arrêtée avec toutes les bases de données attachées laissées dans un état modifié.</p><p>Windows 7 : JET_bitTermDirty est introduite dans Windows 7.</p> | 



### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Impossible de terminer l’opération, car une opération de sauvegarde est en cours sur l’instance.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu. Cette erreur est retournée par <a href="gg269298(v=exchg.10).md">JetTerm</a> lorsque le moteur est en mode multi-instance et lorsque <em>pinstance</em> fait référence à une instance non valide.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>L’opération ne peut pas se terminer car l’instance n’a pas encore été initialisée.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance est en cours d’arrêt.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>L’instance ne peut pas être arrêtée, car il existe actuellement des sessions avec des transactions actives pour l’instance spécifiée. Cette erreur se produit uniquement si le JET_bitTermComplete est utilisé.</p> | 



Si cette fonction est réussie, l’instance spécifiée est arrêtée. Le descripteur d’instance est également fermé et rendu non disponible pour toute API qui accepte un handle d’instance. Tous les autres objets associés à l’instance, tels que les sessions, sont également fermés. L’état du fichier de point de contrôle, des fichiers journaux des transactions et des fichiers de base de données attachés à l’instance sera modifié au cours du processus d’arrêt.

Si cette fonction échoue en raison d’une erreur d’utilisation, l’instance reste dans un état initialisé et rien ne change. Dans le cas contraire, l’instance est toujours arrêtée comme indiqué dans le cas de réussite. La différence est que l’instance doit passer par la récupération après incident lorsqu’elle est ensuite initialisée. Le moteur essaiera de vider le plus de données possible pour réduire la quantité de récupération requise. Conceptuellement, un tel échec de [JetTerm](./jetterm-function.md) n’est pas différent d’un blocage de processus.

#### <a name="remarks"></a>Remarques

Consultez [JetTerm](./jetterm-function.md).

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm](./jetterm-function.md)
