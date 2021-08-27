---
description: 'En savoir plus sur : fonction JetTerm'
title: Fonction JetTerm
TOCTitle: JetTerm Function
ms:assetid: 7711c960-98f4-4134-b8ae-8ddf7b26b6b0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269298(v=EXCHG.10)
ms:contentKeyID: 32765590
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetTerm
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 832f98d32f164e91cd9dfc8befac4cbd0e518632
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481155"
---
# <a name="jetterm-function"></a>Fonction JetTerm


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetterm-function"></a>Fonction JetTerm

La fonction **JetTerm** lance l’arrêt d’une instance qui a été initialisée par [JetInit](./jetinit-function.md).

**JetTerm** peut également être utilisé pour détruire une instance non initialisée qui a été créée par [JetCreateInstance](./jetcreateinstance-function.md).

```cpp
    JET_ERR JET_API JetTerm(
      __in          JET_INSTANCE instance
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Spécifie l’instance à utiliser pour cet appel.

**Windows 2000 :**  Ce paramètre est ignoré et doit toujours avoir la **valeur null**.

**Windows XP et versions ultérieures :**  Ce paramètre est surchargé. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur NULL** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md). Si le moteur fonctionne en mode multi-instance, ce paramètre doit être un pointeur vers une instance créée à l’aide de [JetCreateInstance](./jetcreateinstance-function.md).

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou la combinaison de plusieurs paramètres a généré un résultat inattendu. Cette erreur est retournée par <strong>JetTerm</strong> lorsque le moteur est en mode multi-instance et lorsque <em>pinstance</em> fait référence à une instance non valide.</p><p><strong>Windows XP :</strong>  cette valeur de retour est introduite dans Windows XP.</p> | 
| <p>JET_errNotInitialized</p> | <p>L’opération ne peut pas se terminer car l’instance n’a pas encore été initialisée.</p> | 
| <p>JET_errTermInProgress</p> | <p>L’opération ne peut pas se terminer car l’instance est en cours d’arrêt.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance.</p> | 
| <p>JET_errBackupInProgress</p> | <p>Impossible de terminer l’opération, car une opération de sauvegarde est en cours sur l’instance.</p> | 
| <p>JET_errTooManyActiveUsers</p> | <p>L’instance ne peut pas être arrêtée, car il existe actuellement des sessions avec des transactions actives pour l’instance spécifiée. Cette erreur se produit uniquement si le JET_bitTermComplete est utilisé.</p> | 



Si cette fonction est réussie, l’instance spécifiée est arrêtée. Le descripteur d’instance est également fermé et rendu non disponible pour toute API qui accepte un handle d’instance. Tous les autres objets associés à l’instance, tels que les sessions, sont également fermés. L’état du fichier de point de contrôle, des fichiers journaux des transactions et des fichiers de base de données attachés à l’instance sera modifié au cours du processus d’arrêt.

Si cette fonction échoue en raison d’une erreur d’utilisation, l’instance reste dans un état initialisé et rien ne change. Dans le cas contraire, l’instance est toujours arrêtée en fonction de la réussite de l’opération. La différence est que l’instance doit passer par la récupération après incident lorsqu’elle est ensuite initialisée. Le moteur essaiera de vider le plus de données possible pour réduire la quantité de récupération requise. Conceptuellement, un tel échec de **JetTerm** n’est pas différent d’un blocage de processus.

#### <a name="remarks"></a>Remarques

Si le processus hôte d’une instance se ferme pour une raison quelconque avant que **JetTerm** soit appelé avec succès sur cette instance, l’instance est considérée comme étant dans un état de blocage. La récupération après incident se produira lors de la prochaine tentative d’initialisation de cette instance.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | 



#### <a name="see-also"></a>Voir aussi

[fichiers de moteur d’Stockage Extensible](./extensible-storage-engine-files.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JET_ERR](./jet-err.md)  
[JET_GRBIT](./jet-grbit.md)  
[JetInit](./jetinit-function.md)  
[JET_INSTANCE](./jet-instance.md)  
[JetTerm2](./jetterm2-function.md)
