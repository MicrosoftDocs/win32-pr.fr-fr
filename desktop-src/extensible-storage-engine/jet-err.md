---
description: 'En savoir plus sur : JET_ERR'
title: JET_ERR
TOCTitle: JET_ERR
ms:assetid: cd9cb876-251c-458d-a015-8e9045e77fc9
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294092(v=EXCHG.10)
ms:contentKeyID: 32765707
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- kbArticle
- apiref
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 35120be9a26dcbdc8d012cd12c871ddcf8f71555
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2021
ms.locfileid: "106522400"
---
# <a name="jet_err"></a>JET_ERR


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_err"></a>JET_ERR

Le type de données **JET_ERR** contient un [code d’erreur ESE (Extensible Storage Engine](./extensible-storage-engine-error-codes.md)).

```cpp
typedef long JET_ERR;
```

### <a name="data-types"></a>Types de données

JET_ERR

Une valeur zéro (correspondant à JET_errSuccess) indique que l’appel a réussi. Une valeur positive indique qu’une condition non irrécupérable s’est produite lors d’un appel de réussite. Une valeur négative indique que l’appel a échoué.

### <a name="remarks"></a>Notes

Pour plus d’informations sur le renvoi d’erreurs en tant que HRESULT, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md). Pour plus d’informations sur les indicateurs permettant de configurer la base de données afin de gérer les erreurs, consultez [paramètres de gestion des erreurs](./error-handling-parameters.md).

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

[Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md)  
[Codes d’erreur du moteur de stockage extensible](./extensible-storage-engine-error-codes.md)  
[Paramètres de gestion des erreurs](./error-handling-parameters.md)
