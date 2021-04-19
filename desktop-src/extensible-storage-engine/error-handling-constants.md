---
description: En savoir plus sur les constantes de gestion des erreurs
title: Constantes de gestion des erreurs
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1ab59a8e0c721558e5c056d25798c5d1273bd86c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525717"
---
# <a name="error-handling-constants"></a>Constantes de gestion des erreurs


_**S’applique à :** Windows | Serveur Windows_

## <a name="error-handling-constants"></a>Constantes de gestion des erreurs

Les constantes suivantes sont utilisées pour définir la plage des paramètres du système de [JET_paramExceptionAction](./error-handling-parameters.md) .

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constante/valeur</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_ExceptionMsgBox<br />
0x0001</p></td>
<td><p>Affiche une boîte de message lorsqu’une exception se produit.</p></td>
</tr>
<tr class="even">
<td><p>JET_ExceptionNone<br />
0x0002</p></td>
<td><p>Ne fait rien quand une exception se produit.</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>Configuration requise

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>Client</strong></p></td>
<td><p>Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</p></td>
</tr>
<tr class="even">
<td><p><strong>Serveur</strong></p></td>
<td><p>Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</p></td>
</tr>
<tr class="odd">
<td><p><strong>En-tête</strong></p></td>
<td><p>Déclaré dans esent. h.</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[Paramètres de gestion des erreurs](./error-handling-parameters.md)
