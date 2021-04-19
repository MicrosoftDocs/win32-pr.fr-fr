---
description: En savoir plus sur les constantes de journalisation des événements
title: Constantes de journalisation des événements
TOCTitle: Event Logging Constants
ms:assetid: d24603a9-a9be-4700-bc20-4e3f0661e741
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294101(v=EXCHG.10)
ms:contentKeyID: 32765716
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
ms.openlocfilehash: e7ada5c71b603bf530c62d9f3af238131e305e42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106540869"
---
# <a name="event-logging-constants"></a>Constantes de journalisation des événements


_**S’applique à :** Windows | Serveur Windows_

## <a name="event-logging-constants"></a>Constantes de journalisation des événements

Les constantes suivantes indiquent le niveau de détail des messages du journal des événements pour le paramètre système [JET_ParamEventLoggingLevel](./event-log-parameters.md) .

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
<td><p>JET_EventLoggingDisable<br />
0</p></td>
<td><p>Désactive la journalisation des événements.</p></td>
</tr>
<tr class="even">
<td><p>JET_EventLoggingLevelMax<br />
100</p></td>
<td><p>Définit le niveau maximal à utiliser pour les journaux des événements, qui est actuellement de 100 caractères.</p></td>
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

[Paramètres du journal des événements](./event-log-parameters.md)
