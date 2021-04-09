---
description: 'En savoir plus sur : fonction JetGetInstanceInfo'
title: JetGetInstanceInfo fonction)
TOCTitle: JetGetInstanceInfo Function
ms:assetid: ffccdac0-3631-4753-876a-90ddfdd0252f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294149(v=EXCHG.10)
ms:contentKeyID: 32765763
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGetInstanceInfoW
- JetGetInstanceInfo
- JetGetInstanceInfoA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b8c8e9a279f536622cfdfccb8bc8882914aeee64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866825"
---
# <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetgetinstanceinfo-function"></a>JetGetInstanceInfo fonction)

La fonction **JetGetInstanceInfo** récupère des informations sur les instances qui sont en cours d’exécution.

**Windows XP : JetGetInstanceInfo** est introduit dans Windows XP.

```cpp
    JET_ERR JET_API JetGetInstanceInfo(
      __out         unsigned long* pcInstanceInfo,
      __out         JET_INSTANCE_INFO** paInstanceInfo
    );
```

### <a name="parameters"></a>Paramètres

*pcInstanceInfo*

Pointeur vers une mémoire tampon qui reçoit le nombre d’éléments stockés dans *paInstanceInfo*.

*paInstanceInfo*

Pointeur vers une mémoire tampon qui reçoit l’adresse du premier élément d’un tableau de structures.

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
<td><p>JET_errInvalidParameter</p></td>
<td><p>L’un des paramètres fournis contenait une valeur inattendue ou contenait une valeur qui n’a pas de sens lorsqu’elle était associée à la valeur d’un autre paramètre. Cette erreur est retournée par <strong>JetGetInstanceInfo</strong> quand :</p>
<ul>
<li><p><em>pcInstanceInfo</em> ou <em>paInstanceInfo</em> ont la valeur null.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>JET_errOutOfMemory</p></td>
<td><p>La mémoire est insuffisante pour traiter la demande.</p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a>Notes

Le moteur de base de données alloue un tableau de structures de [JET_INSTANCE_INFO](./jet-instance-info-structure.md) . L’appelant est chargé de libérer cette mémoire avec [JetFreeBuffer](./jetfreebuffer-function.md).

S’il n’y a aucune instance active, **JetGetInstanceInfo** retourne JET_errSuccess et *pcInstanceInfo* reçoit la valeur 0.

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
<td><p>Implémenté en tant que <strong>JetGetInstanceInfoW</strong> (Unicode) et <strong>JetGetInstanceInfoA</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_INSTANCE](./jet-instance.md)  
[JET_INSTANCE_INFO](./jet-instance-info-structure.md)  
[JetFreeBuffer](./jetfreebuffer-function.md)
