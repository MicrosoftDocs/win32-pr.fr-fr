---
description: 'En savoir plus sur : fonction JetOSSnapshotAbort'
title: JetOSSnapshotAbort fonction)
TOCTitle: JetOSSnapshotAbort Function
ms:assetid: 629455af-b526-4366-9b9a-112757f72c32
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269265(v=EXCHG.10)
ms:contentKeyID: 32765567
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOSSnapshotAbort
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d976f027a940bcf0199016d0e617d515273183ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521872"
---
# <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort fonction)


_**S’applique à :** Windows | Serveur Windows_

## <a name="jetossnapshotabort-function"></a>JetOSSnapshotAbort fonction)

La fonction **JetOSSnapshotAbort** avertit le moteur qu’il peut reprendre des opérations d’e/s normales après la fin d’une période de blocage avec un instantané ayant échoué.

**Windows server 2003 :**  **JetOSSnapshotAbort** est introduit dans Windows Server 2003.

```cpp
    JET_ERR JET_API JetOSSnapshotAbort(
      __in          const JET_OSSNAPID snapId,
      __in          const JET_GRBIT grbit
    );
```

### <a name="parameters"></a>Paramètres

*snapId*

Identificateur de la session d’instantané.

*grbit*

Options pour cet appel. Ce paramètre est réservé pour une utilisation ultérieure et la seule valeur valide prise en charge est 0 (zéro).

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
<td><p>La session d’instantané n’est pas valide ou le paramètre Grbit n’est pas valide.</p></td>
</tr>
<tr class="odd">
<td><p>JET_errOSSnapshotInvalidSnapId</p></td>
<td><p>L’identificateur de la session d’instantané n’est pas valide.</p></td>
</tr>
</tbody>
</table>


Si cette fonction est exécutée correctement, la session d’instantané se termine et le comportement normal du moteur reprend. Une nouvelle session d’instantané peut être démarrée ultérieurement.

Si cette fonction échoue, la session d’instantané n’est pas abandonnée.

#### <a name="remarks"></a>Notes

Cette fonction doit être appelée à la place de [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) pour informer le moteur que l’instantané a été abandonné pour des raisons qui ne sont pas liées au moteur. Ces informations peuvent être utilisées ultérieurement pour aider à émettre des messages du journal des événements concernant la session d’instantané ou pour aider à déterminer d’autres actions appropriées.

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
</tbody>
</table>


#### <a name="see-also"></a>Voir aussi

[JET_ERR](./jet-err.md)  
[JET_OSSNAPID](./jet-ossnapid.md)  
[JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md)  
[JetOSSnapshotPrepare](./jetossnapshotprepare-function.md)  
[JetOSSnapshotThaw](./jetossnapshotthaw-function.md)
