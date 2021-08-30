---
description: 'En savoir plus sur : fonction JetGetSystemParameter'
title: JetGetSystemParameter fonction)
TOCTitle: JetGetSystemParameter Function
ms:assetid: 6e6ddb49-702c-4c45-ac9f-35ae817696dd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269291(v=EXCHG.10)
ms:contentKeyID: 32765583
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetSystemParameter
- JetGetSystemParameterA
- JetGetSystemParameterW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4cdb8769ff05dde61df13d07564a1e0467fa8897
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474075"
---
# <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetgetsystemparameter-function"></a>JetGetSystemParameter fonction)

La fonction **JetGetSystemParameter** lit les nombreux paramètres de configuration du moteur de base de données.

```cpp
    JET_ERR JET_API JetGetSystemParameter(
      __in          JET_INSTANCE instance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in_out_opt  JET_API_PTR* plParam,
      __out_opt     JET_PSTR szParam,
      __in          unsigned long cbMax
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Instance à utiliser pour cet appel.

pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la **valeur NULL**.

pour Windows XP et versions ultérieures, ce paramètre est quelque peu surchargé. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur NULL** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md). Dans les deux cas, tous les paramètres système sont lus à partir de cette instance. Si le moteur fonctionne en mode multi-instance, ce paramètre peut avoir la **valeur null** ou être un pointeur vers une instance créée à l’aide de [JetInit](./jetinit-function.md) ou [JetCreateInstance](./jetcreateinstance-function.md). Lorsque ce paramètre a la **valeur null** , le paramètre global du système (ou par défaut) est lu. Lorsque ce paramètre est une instance, le paramètre système défini pour cette instance est Read.

*sesid*

Session à utiliser pour cet appel.

Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.

*paramid*

ID du paramètre système qui sera lu.

Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .

*plParam*

Mémoire tampon de sortie qui reçoit la valeur du paramètre système sélectionné si ce paramètre système est d’un type entier.

*szParam*

Mémoire tampon de sortie qui reçoit la valeur du paramètre système sélectionné si ce paramètre système est un type chaîne.

*cbMax*

Taille maximale, en octets, de la mémoire tampon de sortie de chaîne.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errInitInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données. cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre.</p><p>Cela peut se produire pour <strong>JetGetSystemParameter</strong> dans les cas suivants :</p><ul><li><p>L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</p></li><li><p>Le paramètre système spécifié requiert que la mémoire tampon de sortie entier soit fournie et que le pointeur de la mémoire tampon de sortie ait la <strong>valeur null</strong>.</p></li><li><p>Le paramètre système spécifié requiert la spécification d’une mémoire tampon de sortie de chaîne et le pointeur de la mémoire tampon de sortie a la <strong>valeur null</strong>.</p><p><strong>Windows Vista :</strong> cela peut se produire uniquement sur Windows Vista et versions ultérieures.</p></li><li><p>Le paramètre système spécifié requiert la spécification d’une mémoire tampon de sortie de chaîne et la taille de cette mémoire tampon de sortie est trop petite pour accepter une chaîne terminée par le caractère null.</p><p><strong>Windows Vista :</strong> cela peut se produire uniquement sur Windows Vista et versions ultérieures.</p></li><li><p>Le paramètre système spécifié ne peut pas être lu, car il est en écriture seule.</p></li><li><p>Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour lire une valeur spécifique à l’instance pour ce paramètre système. cela peut se produire uniquement dans Windows XP et versions ultérieures.</p></li><li><p>Le paramètre système spécifié est par instance uniquement et une tentative a été effectuée pour lire la valeur globale de ce paramètre système. cela peut se produire uniquement dans Windows XP et versions ultérieures.</p></li></ul> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Le descripteur de session n’est pas valide ou fait référence à une session fermée. Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p> | 
| <p>JET_errInvalidInstance</p> | <p>Le handle d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée. Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p><p><strong>Windows Vista :</strong> cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</p> | 
| <p>JET_wrnBufferTruncated</p> | <p>L’opération s’est terminée correctement, mais la mémoire tampon de sortie était trop petite pour recevoir l’ensemble du paramètre système.</p><p>La mémoire tampon de sortie a été remplie avec la plus grande partie du paramètre système. Si la mémoire tampon de sortie a au moins un caractère de longueur, la chaîne de cette mémoire tampon de sortie se termine par une valeur null.</p><p><strong>Remarque  </strong> Cette erreur n’est pas renvoyée par toutes les mises en production. Pour plus d’informations, consultez la section Notes.</p> | 
| <p>JET_errBufferTooSmall</p> | <p>L’opération a échoué, car la mémoire tampon de sortie était trop petite pour recevoir l’ensemble du paramètre système.</p><p><strong>Remarque  </strong> Cette erreur n’est pas retournée dans certains cas pour préserver la compatibilité des applications. Pour plus d’informations, consultez la section Notes.</p><p><strong>Windows Vista :</strong> cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</p> | 



En cas de réussite, la mémoire tampon de sortie appropriée pour le paramètre système demandé sera définie sur la valeur de ce paramètre système.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.

#### <a name="remarks"></a>Remarques

Il existe un problème important dans cette API qui est présent dans toutes les versions. Si un paramètre système avec une valeur de chaîne est demandé et que la mémoire tampon de sortie est trop petite pour recevoir la totalité du paramètre système, JET_wrnBufferTruncated n’est pas retourné. JET_errSuccess est retourné à la place. Si la longueur de la chaîne retournée est égale à la taille de la mémoire tampon de sortie inférieure au terminateur **null** , l’appelant doit réagir comme si JET_wrnBufferTruncated étaient retournés. Si une mémoire tampon de sortie de chaîne de taille zéro est spécifiée, l’appelant doit réagir comme si JET_errInvalidParameter étaient retournés.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetGetSystemParameterW</strong> (Unicode) et <strong>JetGetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)  
[JetStopService](./jetstopservice-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
