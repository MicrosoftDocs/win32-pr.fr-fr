---
description: 'En savoir plus sur : fonction JetSetSystemParameter'
title: JetSetSystemParameter fonction)
TOCTitle: JetSetSystemParameter Function
ms:assetid: a244b5c9-6f6e-49d1-a6f7-9248feb9b92d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294044(v=EXCHG.10)
ms:contentKeyID: 32765643
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetSystemParameterA
- JetSetSystemParameterW
- JetSetSystemParameter
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4da3dc4c0d211039378b5cc1301a84e35f67ab24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475795"
---
# <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetsetsystemparameter-function"></a>JetSetSystemParameter fonction)

La fonction **JetSetSystemParameter** est utilisée pour définir les nombreux paramètres de configuration du moteur de base de données.

```cpp
    JET_ERR JET_API JetSetSystemParameter(
      __in_out_opt  JET_INSTANCE* pinstance,
      __in          JET_SESID sesid,
      __in          unsigned long paramid,
      __in          JET_API_PTR lParam,
      __in_opt      JET_PCSTR szParam
    );
```

### <a name="parameters"></a>Paramètres

*pinstance*

Spécifie l’instance à utiliser pour cet appel.

**Windows 2000 :**  pour Windows 2000, ce paramètre est ignoré et doit toujours avoir la **valeur NULL**.

**Windows XP :**  pour Windows XP et versions ultérieures, ce paramètre est quelque peu surchargé. si le moteur fonctionne en mode hérité (Windows mode de compatibilité 2000) alors qu’une seule instance est prise en charge, ce paramètre peut avoir la **valeur NULL** ou peut contenir l’instance réelle retournée par [JetInit](./jetinit-function.md). Dans les deux cas, tous les paramètres système sont lus à partir de cette instance. Si le moteur fonctionne en mode multi-instance, ce paramètre peut avoir la **valeur null** ou être un pointeur vers une instance créée à l’aide de [JetInit](./jetinit-function.md) ou [JetCreateIndex](./jetcreateindex-function.md). Lorsque ce paramètre a la **valeur null** , le paramètre global du système (ou par défaut) est lu. Lorsque ce paramètre est une instance, le paramètre système défini pour cette instance est Read.

Même s’il s’agit d’un paramètre de sortie techniquement, cette API ne modifie jamais le contenu de la mémoire tampon fournie.

*sesid*

Spécifie la session à utiliser pour cet appel.

Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.

*paramid*

ID du paramètre système qui sera défini. Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système](./extensible-storage-engine-system-parameters.md) .

*lParam*

Fournit la valeur à définir pour le paramètre système sélectionné si ce paramètre système est d’un type entier.

*szParam*

Fournit la valeur du paramètre système sélectionné si ce paramètre système est de type chaîne.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).


| <p>Code de retour</p> | <p>Description</p> | 
|--------------------|--------------------|
| <p>JET_errSuccess</p> | <p>L’opération s’est terminée avec succès.</p><p><strong>Windows Vista :</strong>  sur Windows Vista et les versions ultérieures, la réussite peut être retournée sans modification de la valeur du paramètre du système. Pour plus d’informations, consultez le paramètre système JET_paramEnableAdvanced dans la rubrique <a href="gg269346(v=exchg.10).md">méta-paramètres</a> .</p> | 
| <p>JET_errAlreadyInitialized</p> | <p>L’instance a été initialisée à l’aide d’un appel à <a href="gg294068(v=exchg.10).md">JetInit</a> et cette opération ne peut pas être exécutée en conséquence. Cela peut se produire pour <strong>JetSetSystemParameter</strong> quand une tentative est faite pour configurer un paramètre système après qu’une modification de sa valeur ne peut pas affecter l’état du moteur de base de données.</p> | 
| <p>JET_errClientRequestToStopJetService</p> | <p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a été interrompue suite à un appel à <a href="gg269240(v=exchg.10).md">JetStopService</a>.</p> | 
| <p>JET_errIndexTuplesInvalidLimits</p> | <p>Les paramètres d’index de tuple spécifiés ne sont pas conformes. Cette erreur peut être retournée par <strong>JetSetSystemParameter</strong> uniquement lorsque vous définissez <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> sur une valeur non conforme.</p><p><strong>Windows XP et Windows Server 2003 :</strong>  cela peut se produire uniquement sur Windows XP et Windows Server 2003.</p> | 
| <p>JET_errInitInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</p> | 
| <p>JET_errInstanceUnavailable</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p><p><strong>Windows XP :</strong>  cette erreur est renvoyée uniquement par Windows XP et les versions ultérieures.</p> | 
| <p>JET_errInvalidParameter</p> | <p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetSetSystemParameter</strong> dans les cas suivants :</p><ul><li><p>L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</p></li><li><p>Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec une chaîne dont la longueur était en dehors de la plage autorisée pour le paramètre.</p></li><li><p>Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec un chemin d’accès de fichier où la longueur de sa représentation de chemin d’accès absolu était en dehors de la plage autorisée pour ce paramètre.</p><p><strong>Windows Vista :</strong>  cela peut se produire uniquement sur Windows Vista et versions ultérieures.</p></li><li><p>Une tentative a été effectuée pour définir un paramètre système de valeur entière avec un entier qui se trouvait en dehors de la plage autorisée pour le paramètre.</p></li><li><p>Une tentative a été effectuée pour définir JET_paramUnicodeIndexDefault avec un pointeur de<a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> <strong>null</strong>, un LCID non valide ou un jeu d’indicateurs LCMapString non pris en charge.</p><p><strong>Windows Vista :</strong>  cela peut se produire uniquement sur Windows Vista et versions ultérieures.</p></li><li><p>Impossible de définir le paramètre système spécifié, car il est en lecture seule.</p></li><li><p>Une tentative de définition d’un paramètre système a été effectuée après l’appel de <a href="gg294068(v=exchg.10).md">JetInit</a> , le moteur de base de données est en mode d’instance unique et aucune session n’a été spécifiée.</p><p><strong>Windows XP et Windows Server 2003 :</strong>  cela peut se produire uniquement sur Windows XP et Windows Server 2003.</p></li><li><p>Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour définir une valeur spécifique à une instance pour ce paramètre système.</p><p><strong>Windows XP et Windows Server 2003 :</strong>  cela peut se produire uniquement sur Windows XP et Windows Server 2003.</p></li><li><p>Le paramètre système spécifié est par instance uniquement et une tentative de définition de la valeur globale pour ce paramètre système a été effectuée.</p><p><strong>Windows XP et Windows Server 2003 :</strong>  cela peut se produire uniquement sur Windows XP et Windows Server 2003.</p></li></ul> | 
| <p>JET_errInvalidPath</p> | <p>Le chemin d’accès au système de fichiers spécifié n’est pas valide. Cette erreur peut être retournée par <strong>JetSetSystemParameter</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers. Par exemple, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> peut retourner cette erreur.</p> | 
| <p>JET_errNotInitialized</p> | <p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p> | 
| <p>JET_errRestoreInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p> | 
| <p>JET_errTermInProgress</p> | <p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p> | 
| <p>JET_errInvalidSesid</p> | <p>Le descripteur de session n’est pas valide ou fait référence à une session fermée.</p><p>Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p> | 
| <p>JET_errInvalidInstance</p> | <p>Le handle d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</p><p>Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p><p><strong>Windows Vista :</strong>  cette erreur est renvoyée uniquement par Windows Vista et les versions ultérieures.</p> | 



En cas de réussite, le paramètre du paramètre système est défini sur la valeur fournie.

En cas d’échec, le paramètre du paramètre système reste inchangé.

#### <a name="remarks"></a>Remarques

**JetSetSystemParameter** effectue une tâche médiocre de validation du paramètre choisi pour chaque paramètre système. Vous devez veiller à ne pas compter sur cette validation pour appliquer les bons paramètres. Veuillez prêter une attention particulière à la description de chaque paramètre système et suivez ces instructions pour un paramètre système correct.

Il existe un ensemble de paramètres système qui doivent toujours être définis pour garantir que le moteur de base de données fonctionne comme prévu. Plus précisément, tous les paramètres système qui affectent la disposition physique des fichiers utilisés par le moteur de base de données doivent toujours être définis. Pour plus d’informations, consultez [paramètres système](./extensible-storage-engine-system-parameters.md).

Chaque paramètre système a une valeur par défaut. Ces valeurs par défaut ont évolué au fil du temps et sont relativement arbitraires. Il est fortement recommandé qu’une application évalue toutes les valeurs par défaut pour s’assurer qu’elles sont appropriées. S’ils ne sont pas appropriés, ils doivent être configurés par l’application. Cela est important, car un grand nombre de ces paramètres peuvent avoir un impact considérable sur la fiabilité, les performances et l’utilisation des ressources du moteur de base de données.

#### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | | <p><strong>Bibliothèque</strong></p> | <p>Utilisez ESENT. lib.</p> | | <p><strong>DLL</strong></p> | <p>Requiert ESENT.dll.</p> | | <p><strong>Unicode</strong></p> | <p>Implémenté en tant que <strong>JetSetSystemParameterW</strong> (Unicode) et <strong>JetSetSystemParameterA</strong> (ANSI).</p> | 



#### <a name="see-also"></a>Voir aussi

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
