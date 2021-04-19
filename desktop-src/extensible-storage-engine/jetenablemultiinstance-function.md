---
description: 'En savoir plus sur : fonction JetEnableMultiInstance'
title: JetEnableMultiInstance fonction)
TOCTitle: JetEnableMultiInstance Function
ms:assetid: d88a7b2a-c0d1-47de-9239-3631150d92da
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294107(v=EXCHG.10)
ms:contentKeyID: 32765722
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetEnableMultiInstanceW
- JetEnableMultiInstanceA
- JetEnableMultiInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 61fb058b14d9a8abeb282d4227b110ba50304a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535704"
---
# <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetenablemultiinstance-function"></a>JetEnableMultiInstance fonction)

La fonction **JetEnableMultiInstance** configure le moteur de base de données pour une utilisation avec plusieurs instances dans le même processus. Un tableau facultatif de paramètres système globaux est disponible pour le premier appelant, ce qui permet la modification du mode multi-instance.

**Windows XP : JetEnableMultiInstance** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetEnableMultiInstance(
      __in_opt      JET_SETSYSPARAM* psetsysparam,
      __in_opt      unsigned long csetsysparam,
      __out_opt     unsigned long* pcsetsucceed
    );
```

### <a name="parameters"></a>Paramètres

*psetsysparam*

Tableau de paramètres système globaux à définir si et seulement si le moteur passe en mode multi-instance à la suite de cet appel. Si *csetsysparam* est égal à zéro, *psetsysparam* est ignoré.

*csetsysparam*

Nombre d’éléments pour le tableau de paramètres globaux à définir si et seulement si le moteur passe en mode multi-instance à la suite de cet appel. Si *csetsysparam* est égal à zéro, *psetsysparam* est ignoré.

*pcsetsucceed*

Pointeur vers le nombre de paramètres système globaux qui ont été correctement configurés à la suite de cet appel.

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
<td><p>JET_errIndexTuplesInvalidLimits</p></td>
<td><p>Les paramètres d’index de tuple spécifiés ne sont pas autorisés. Cette erreur peut être retournée par <strong>JetEnableMultiInstance</strong> uniquement lorsque vous définissez <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMin</a>, <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesLengthMax</a>ou <a href="gg294119(v=exchg.10).md">JET_paramIndexTuplesToIndexMax</a> sur une valeur non conforme.</p>
<p><strong>Windows XP :</strong>  Cette valeur de retour est introduite dans Windows XP.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidPath</p></td>
<td><p>Le chemin d’accès au système de fichiers spécifié n’est pas valide. Cette erreur peut être retournée par <strong>JetEnableMultiInstance</strong> uniquement lors de la définition des paramètres système qui représentent les chemins d’accès du système de fichiers. Par exemple, <a href="gg269235(v=exchg.10).md">JET_paramSystemPath</a> pouvez retourner cette erreur.</p></td>
</tr>
<tr class="even">
<td><p>JET_errRunningInOneInstanceMode</p></td>
<td><p>L’opération a échoué, car elle n’est pas conforme lorsque le moteur de base de données fonctionne en mode d’instance unique (mode de compatibilité Windows 2000).</p></td>
</tr>
<tr class="odd">
<td><p>JET_errSystemParamsAlreadySet</p></td>
<td><p><strong>JetEnableMultiInstance</strong> a échoué, car le moteur est déjà en mode multi-instance.</p>
<p><strong>Remarque  </strong> Cela se produit même si aucun paramètre système n’est spécifié.</p></td>
</tr>
</tbody>
</table>


Si cette fonction fonctionne, le moteur de base de données sera configuré pour s’exécuter en mode multi-instance. Le moteur a été configuré avec succès avec la liste facultative de paramètres système globaux.

Si cette fonction échoue, le moteur de base de données reste dans le mode actuel. Si *pcsetsucceed* est différent de zéro, ce nombre de paramètres système restera défini.

#### <a name="remarks"></a>Notes

Cette fonction doit être utilisée uniquement si l’application doit configurer de manière atomique un ensemble donné de paramètres système lors de la configuration du moteur de base de données pour une utilisation dans un scénario multi-utilisateur dans le même processus. Si une autre méthode de synchronisation est disponible, il est préférable d’appeler [JetCreateInstance](./jetcreateinstance-function.md) et [JetSetSystemParameter](./jetsetsystemparameter-function.md) séparément.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008 ou Windows Server 2003.</p></td>
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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté en tant que <strong>JetEnableMultiInstanceW</strong> (Unicode) et <strong>JetEnableMultiInstanceA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_SETSYSPARAM](./jet-setsysparam-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
