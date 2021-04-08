---
description: 'En savoir plus sur : fonction JetGetInstanceMiscInfo'
title: JetGetInstanceMiscInfo fonction)
TOCTitle: JetGetInstanceMiscInfo Function
ms:assetid: 0bfe36fe-4ddd-442b-b934-57a7bfb28e5f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269183(v=EXCHG.10)
ms:contentKeyID: 32765486
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceMiscInfo
topic_type:
- kbArticle
- apiref
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed63c6a5c6d3b2488f7226da0a1f23e1adb39e09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034904"
---
# <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetinstancemiscinfo-function"></a>JetGetInstanceMiscInfo fonction)

La fonction **JetGetInstanceMiscInfo** récupère des informations sur l’instance, tandis que l’instance est en ligne.

**Windows Vista : JetGetInstanceMiscInfo** est introduit dans Windows Vista.

```cpp
    JET_ERR JET_API JetGetInstanceMiscInfo(
      __in          JET_INSTANCE instance,
      __out         void* pvResult,
      __in          unsigned long cbMax,
      __in          unsigned long InfoLevel
    );
```

### <a name="parameters"></a>Paramètres

*instancié*

Identifie l’instance de base de données qui sera utilisée pour l’appel d’API.

*pvResult*

Pointeur vers une mémoire tampon qui recevra les informations. Le type de la mémoire tampon dépend de *InfoLevel*. L’appelant est chargé d’aligner la mémoire tampon de manière appropriée.

*cbMax*

Taille, en octets, de la mémoire tampon passée dans *pvResult*.

*InfoLevel*

Détermine le type d’informations qui sera récupéré pour l’instance spécifiée par l' *instance*. Le format des données stockées dans *pvResult* dépend de *InfoLevel*.

Les options suivantes peuvent être utilisées avec ce paramètre.

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
<td><p>JET_InstanceMiscInfoLogSignature</p></td>
<td><p><em>pvResult</em> est interprété comme une structure <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a> de la séquence du journal des transactions associée à cette instance.</p></td>
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
<td><p>JET_errBufferTooSmall</p></td>
<td><p>La mémoire tampon est insuffisante.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errInvalidParameter</p></td>
<td><p>Un <a href="gg294048(v=exchg.10).md">JET_INSTANCE</a> non valide ou un <em>InfoLevel</em> non valide a été spécifié.</p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008.</p></td>
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
[JET_SIGNATURE](./jet-signature-structure.md)
