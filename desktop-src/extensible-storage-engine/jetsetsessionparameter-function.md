---
description: 'En savoir plus sur : fonction JetSetSessionParameter'
title: JetSetSessionParameter fonction)
TOCTitle: JetSetSessionParameter Function
ms:assetid: 11aecf42-22ef-4bea-a3d7-961a7bdc85aa
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835038(v=EXCHG.10)
ms:contentKeyID: 49894660
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetSessionParameter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 926ae0db2e47ce571f441ab5836c4ddbe6f8bcc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951041"
---
# <a name="jetsetsessionparameter-function"></a>JetSetSessionParameter fonction)


_**S’applique à :** Windows | Serveur Windows_

La fonction **JetSetSessionParameter** configure le moteur de base de données.

``` c++
JET_ERR JET_API JetSetSessionParameter (
  __in_opt      JET_SESID sesid,
  __in          unsigned long sesparamid,
  __in_read_bytes_opt_(cbParam)  void* pvParam,
  __in          unsigned long cbParam
);
```

### <a name="parameters"></a>Paramètres

*sesid*

Spécifie la session à utiliser pour cet appel.

Lorsqu’il est spécifié, l’instance spécifiée est ignorée et l’instance associée à la session est utilisée.

*sesparamid*

ID du paramètre de session à définir.

*pvParam*

Données à définir dans ce paramètre de session.

*cbParam*

Taille des données fournies.

### <a name="return-value"></a>Valeur retournée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant. Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errAlreadyInitialized</p></td>
<td><p>L’instance a été initialisée à l’aide d’un appel à la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> et cette opération ne peut pas être exécutée en conséquence. Cela peut se produire lorsqu’une tentative est effectuée pour configurer un paramètre système après qu’une modification de la valeur de paramètre ne peut plus affecter l’état du moteur de base de données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errClientRequestToStopJetService</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car toute activité sur l’instance associée à la session a cessé à la suite d’un appel à la fonction <a href="gg269240(v=exchg.10).md">JetStopService</a> .</p></td>
</tr>
<tr class="even">
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Les paramètres d’index de tuple spécifiés ne sont pas conformes. Cette erreur est retournée uniquement lorsque le paramètre <em>JET_paramIndexTuplesLengthMin</em>, <em>JET_paramIndexTuplesLengthMax</em>ou <em>JET_paramIndexTuplesToIndexMax</em> est défini sur une valeur non conforme. Pour plus d’informations sur ces paramètres, consultez <a href="gg294119(v=exchg.10).md">paramètres d’index</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInitInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’initialisation.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInstanceUnavailable</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session a rencontré une erreur irrécupérable qui requiert que l’accès à toutes les données soit révoqué pour protéger l’intégrité de ces données.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cela peut se produire dans les cas suivants :</p>
<ul>
<li><p>L’ID de paramètre système spécifié n’est pas valide ou n’est pas pris en charge.</p></li>
<li><p>Une tentative de définition d’un paramètre système à valeur de chaîne avec une chaîne dont la longueur était en dehors de la plage autorisée pour le paramètre a été effectuée.</p></li>
<li><p>Une tentative a été effectuée pour définir un paramètre système à valeur de chaîne avec un chemin d’accès de fichier où la longueur de sa représentation de chemin d’accès absolu était en dehors de la plage autorisée pour ce paramètre.</p></li>
<li><p>Une tentative a été effectuée pour définir un paramètre système de valeur entière avec un entier qui se trouvait en dehors de la plage autorisée pour le paramètre.</p></li>
<li><p>Une tentative a été effectuée pour définir JET_paramUnicodeIndexDefault avec un pointeur de <a href="gg294097(v=exchg.10).md">JET_UNICODEINDEX</a> null, un LCID non valide ou un jeu d’indicateurs <strong>LCMapString</strong> non pris en charge.</p></li>
<li><p>Impossible de définir le paramètre système spécifié, car il est en lecture seule.</p></li>
<li><p>Une tentative de définition d’un paramètre système a été effectuée après l’appel de la fonction <a href="gg294068(v=exchg.10).md">JetInit</a> , le moteur de base de données est en mode d’instance unique et aucune session n’a été spécifiée.</p></li>
<li><p>Le paramètre système spécifié est global uniquement et une tentative a été effectuée pour définir une valeur spécifique à l’instance pour ce paramètre système.</p></li>
<li><p>Le paramètre système spécifié est par instance uniquement et une tentative de définition de la valeur globale pour ce paramètre système a été effectuée.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidPath</p></td>
<td><p>Le chemin d’accès au système de fichiers spécifié n’est pas valide. Cette erreur peut être retournée par <strong>JetSetSessionParameter</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers. Par exemple, le paramètre <em>JET_paramSystemPath</em> peut retourner cette erreur. Pour plus d’informations sur ce paramètre, consultez <a href="gg269235(v=exchg.10).md">paramètres du journal des transactions</a>.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errNotInitialized</p></td>
<td><p>Impossible de terminer l’opération, car l’instance associée à la session n’a pas encore été initialisée.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRestoreInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car une opération de restauration est en cours sur l’instance associée à la session.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errTermInProgress</p></td>
<td><p>Il n’est pas possible de terminer l’opération, car l’instance associée à la session est en cours d’arrêt.</p></td>
</tr>
<tr class="even">
<td><p>JET_errInvalidSesid</p></td>
<td><p>Le descripteur de session n’est pas valide ou fait référence à une session fermée.</p>
<p>Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidInstance</p></td>
<td><p>Le descripteur d’instance n’est pas valide ou fait référence à une instance qui a été arrêtée.</p>
<p>Cette erreur n’est pas retournée dans toutes les circonstances. Les handles ne sont validés qu’à titre d’effort optimal.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, le paramètre système est défini sur la valeur fournie.

En cas d’échec, la valeur du paramètre système reste inchangée.

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

[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_SESID](./jet-sesid.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[Paramètres système](./extensible-storage-engine-system-parameters.md)
