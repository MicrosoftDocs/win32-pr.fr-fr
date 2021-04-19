---
description: 'En savoir plus sur : JET_LS'
title: JET_LS
TOCTitle: JET_LS
ms:assetid: 8e4e7902-84b1-404b-8654-bb430a0952aa
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269336(v=EXCHG.10)
ms:contentKeyID: 32765625
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
ms.openlocfilehash: 3300fd88c0dd1e1fca55722bf58350e28f3c3b08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522106"
---
# <a name="jet_ls"></a>JET_LS


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_ls"></a>JET_LS

Le type de données **JET_LS** contient un descripteur de contexte pour le stockage local (LS). Ce handle peut être associé à un curseur ou à une table et peut faire référence à des ressources allouées dynamiquement.

**Windows XP : JET_LS** est introduite dans Windows XP.

```cpp
    typedef JET_API_PTR JET_LS;
```

### <a name="data-types"></a>Types de données

JET_LS

La valeur JET_LSNil indique un handle de contexte non valide.

### <a name="remarks"></a>Notes

Un descripteur de contexte est initialement associé à l' **JET_LS** type de données, à l’aide de [JetSetLS](./jetsetls-function.md). Le descripteur de contexte peut être récupéré à partir du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md).

Le descripteur de contexte peut être explicitement dissocié du type de données **JET_LS** à l’aide de [JetGetLS](./jetgetls-function.md) avec JET_bitLSReset. Le handle de contexte peut également être dissocié implicitement du type de données **JET_LS** lorsque l’objet sous-jacent est libéré par le moteur de base de données à la suite d’une action directe ou indirecte de l’application. Dans le cas implicite, un rappel d’exécution est émis pour l’application afin qu’elle puisse nettoyer le handle de contexte. Pour plus d’informations sur la dissociation implicite du type de données **JET_LS** , consultez [JetSetLS](./jetsetls-function.md).

Les indicateurs suivants sont associés au type de données JET_LS.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Terme</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>JET_bitLSReset</p></td>
<td><p>Le handle de contexte est dissocié de l’objet.</p></td>
</tr>
<tr class="even">
<td><p>JET_bitLSCursor</p></td>
<td><p>Définissez ou récupérez le stockage local associé à un curseur de table.</p></td>
</tr>
<tr class="odd">
<td><p>JET_bitLSTable</p></td>
<td><p>Définissez ou récupérez le stockage local associé à une table.</p></td>
</tr>
<tr class="even">
<td><p>JET_LSNil</p></td>
<td><p>Le descripteur de contexte n’est pas valide.</p></td>
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
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[JetSetLS](./jetsetls-function.md)  
[JetGetLS](./jetgetls-function.md)
