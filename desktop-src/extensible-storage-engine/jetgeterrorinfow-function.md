---
description: 'En savoir plus sur : fonction JetGetErrorInfoW'
title: JetGetErrorInfoW fonction)
TOCTitle: JetGetErrorInfoW Function
ms:assetid: 7a84f937-7a16-434e-896d-789f316ee833
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475859(v=EXCHG.10)
ms:contentKeyID: 37033565
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetErrorInfoW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1bf4db5d8d34a741e57f72e8f237f1497de0bacf
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "104116319"
---
# <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgeterrorinfow-function"></a>JetGetErrorInfoW fonction)

BAS_ fonction **JetGetErrorInfoW** du moteur de base de données.

Remarque : cette documentation est basée sur une version préliminaire du moteur de stockage extensible. Ces informations sont susceptibles d’être modifiées.

```cpp
JET_ERR JET_API JetGetErrorInfoW( 
    _In_opt_ void *                      pvContext, 
    _Out_writes_bytes_( cbMax ) void *   pvResult, 
    _In_ unsigned long                   cbMax, 
    _In_ unsigned long                   InfoLevel, 
    _In_ JET_GRBIT                       grbit );
```

### <a name="parameters"></a>Paramètres

*pvContext*

Contexte ou valeur d’erreur pour lequel les informations d’erreur étendues sont nécessaires. La valeur passée dépend de la valeur du paramètre *InfoLevel* .

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de la valeur du paramètre *InfoLevel* . L’appelant doit être configuré pour aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille maximale de la structure *pvResult* qui est passée.

*InfoLevel*

Le type d’informations qui sera récupéré pour les informations d’erreur/contexte est spécifié par le paramètre *pvContext* . Le format des données stockées dans *pvResult* dépend de *InfoLevel*.

Le tableau suivant répertorie les valeurs possibles pour ce paramètre.

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
<td><p>JET_ErrorInfoSpecificErr</p></td>
<td><p><em>pvContext</em> est interprété comme un <a href="gg269297(v=exchg.10).md">JET_ERR</a>code/Error, <em>pvResult</em> est interprété comme un <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a>et les champs de la structure <a href="hh475861(v=exchg.10).md">JET_ERRINFOBASIC_W</a> sont remplis de manière appropriée.</p></td>
</tr>
</tbody>
</table>


*grbit*

Réservé.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./extensible-storage-engine-error-codes.md) avec l’un des codes de retour énumérés dans le tableau suivant. Pour plus d’informations sur les erreurs ESE possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contient une valeur inattendue ou contient une valeur qui n’a pas de sens lorsqu’elle est associée à la valeur d’un autre paramètre. Cela peut se produire pour <strong>JetGetErrorInfo</strong> dans les cas suivants :</p>
<ul>
<li><p>La valeur du paramètre <em>InfoLevel</em> spécifiée n’est pas valide.</p></li>
<li><p>La valeur <em>Grbit</em> spécifiée n’est pas valide.</p></li>
<li><p>La valeur <em>cbMax</em> de la mémoire tampon du paramètre <em>pvResult</em> spécifiée est inférieure à la taille requise pour la sortie de ce paramètre <em>InfoLevel</em> .</p></li>
<li><p>Pour <em>InfoLevel</em> = JET_ErrorInfoSpecificErr, la valeur <a href="gg294092(v=exchg.10).md">JET_ERR</a> passée est inconnue pour le moteur.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errDisabledFunctionality</p></td>
<td><p>Si cette référence de Windows ne prend pas en charge cette fonction, cette erreur est retournée.</p></td>
</tr>
</tbody>
</table>


En cas de réussite, la mémoire tampon de sortie qui est appropriée pour le contexte/la valeur de l’erreur demandée sera définie sur les informations d’erreur étendues demandées.

En cas d’échec, l’état des mémoires tampons de sortie n’est pas défini.

### <a name="remarks"></a>Notes

La fonction [JET_ERRINFOBASIC_W](./jet-errinfobasic-w-structure.md) et [JET_ERRCAT](./jet-errcat.md) groupe de constantes contiennent la documentation sur les informations d’erreur étendues retournées pour *InfoLevel* = JET_ErrorInfoSpecificErr.

### <a name="requirements"></a>Configuration requise

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
<td><p>Nécessite Windows 8 Server.</p></td>
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
<td><p>Remarque : seul le <strong>JetGetErrorInfoW</strong> (Unicode) est implémenté. Cette API n’a pas de version (ANSI).</p></td>
</tr>
</tbody>
</table>
