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
ms.openlocfilehash: 7309d803421d4bf9221ba1d968d5034f940b016f
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983772"
---
# <a name="jet_setsysparam-structure"></a>Structure JET_SETSYSPARAM


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_setsysparam-structure"></a>Structure JET_SETSYSPARAM

Un tableau de structures de **JET_SETSYSPARAM** indique un ensemble spécifique de paramètres système globaux définis comme argument lors de l’utilisation de la fonction [JetEnableMultiInstance](./jetenablemultiinstance-function.md) .

**Windows XP :** cette structure est introduite dans Windows XP.

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

pour obtenir la liste complète des paramètres système et leurs propriétés, consultez [paramètres système du moteur de Stockage Extensible](./extensible-storage-engine-system-parameters.md) .

**lParam**

Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est d’un type entier.

**SZ**

Valeur facultative à définir pour le paramètre système sélectionné si ce paramètre système est un type chaîne.

**Raise**

Erreur résultant de l’appel à [JetSetSystemParameter](./jetsetsystemparameter-function.md) avec les paramètres spécifiés précédemment.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_ SETSYSPARAM_W</strong> (Unicode) et <strong>JET_ SETSYSPARAM_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[paramètres système du moteur de Stockage Extensible](./extensible-storage-engine-system-parameters.md)  
[JET_API_PTR](./jet-api-ptr.md)  
[JET_ERR](./jet-err.md)  
[JetEnableMultiInstance](./jetenablemultiinstance-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
