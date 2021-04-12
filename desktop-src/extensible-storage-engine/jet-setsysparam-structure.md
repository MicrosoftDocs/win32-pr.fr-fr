---
description: 'En savoir plus sur : structure JET_SETSYSPARAM'
title: Structure JET_SETSYSPARAM
TOCTitle: JET_SETSYSPARAM Structure
ms:assetid: 3c0fdd28-99bd-4026-b64b-6859ef9dc91b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269230(v=EXCHG.10)
ms:contentKeyID: 32765532
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
ms.openlocfilehash: 0e88795bb3ee966bf2ad7fa50cc7d2180d7264bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318173"
---
# <a name="jet_setsysparam-structure"></a>Structure JET_SETSYSPARAM


_**S’applique à :** Windows | Serveur Windows_

## <a name="jet_setsysparam-structure"></a>Structure JET_SETSYSPARAM

Un tableau de structures de **JET_SETSYSPARAM** indique un ensemble spécifique de paramètres système globaux définis comme argument lors de l’utilisation de la fonction [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .

**Windows XP :** Cette structure est introduite dans Windows XP.

```cpp
    typedef struct {
      unsigned long paramid;
      JET_API_PTR lParam;
      const tchar* sz;
      JET_ERR err;
    } JET_SETSYSPARAM;
```

### <a name="members"></a>Membres

**paramid**

ID du paramètre système qui sera défini.

Pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système du moteur de stockage extensible](./extensible-storage-engine-system-parameters.md) .

**lParam**

Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est d’un type entier.

**SZ**

Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est un type chaîne.

**Raise**

Erreur résultant de l’appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec les paramètres spécifiés précédemment.

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
<tr class="even">
<td><p><strong>Unicode</strong></p></td>
<td><p>Implémenté comme <strong>JET_ SETSYSPARAM_W</strong> (Unicode) et <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>Voir aussi

[Paramètres système du moteur de stockage extensible](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
