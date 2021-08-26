---
description: 'En savoir plus sur : fonction JetFreeBuffer'
title: JetFreeBuffer fonction)
TOCTitle: JetFreeBuffer Function
ms:assetid: f37d35f6-4bea-46ba-a334-7b8ad7a1568c
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294134(v=EXCHG.10)
ms:contentKeyID: 32765748
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetFreeBuffer
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 011974154f80c2da809292530deb50657d1280172554d79629a5a4650833c347
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119944869"
---
# <a name="jetfreebuffer-function"></a>JetFreeBuffer fonction)


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jetfreebuffer-function"></a>JetFreeBuffer fonction)

La fonction **JetFreeBuffer** libère de la mémoire qui a été allouée par un appel du moteur de base de données.

**Windows xp : JetFreeBuffer** est introduit dans Windows xp.

```cpp
    JET_ERR JET_API JetFreeBuffer(
      __in          char* pbBuf
    );
```

### <a name="parameters"></a>Paramètres

*pbBuf*

Pointeur vers une zone de mémoire précédemment allouée par un appel au moteur de base de données. **Null** est acceptable et sera ignoré.

### <a name="return-value"></a>Valeur renvoyée

Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour suivants. pour plus d’informations sur les erreurs ESE possibles, consultez [erreurs du moteur de Stockage Extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).

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
</tbody>
</table>


#### <a name="remarks"></a>Remarques

Il s’agit d’un comportement indéfini pour passer de la mémoire qui n’a pas été allouée par le moteur de base de données dans à *pbBuf*.

#### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>requiert Windows Vista ou Windows XP.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>requiert Windows server 2008 ou Windows server 2003.</p></td>
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
[JetGetInstanceInfo](./jetgetinstanceinfo-function.md)
