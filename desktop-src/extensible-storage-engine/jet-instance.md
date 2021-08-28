---
description: 'En savoir plus sur : JET_INSTANCE'
title: JET_INSTANCE
TOCTitle: JET_INSTANCE
ms:assetid: a4136bec-95b3-42d7-b21b-1df09197bb11
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294048(v=EXCHG.10)
ms:contentKeyID: 32765647
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
ms.openlocfilehash: 1fc288c17c90070d48669c7ad6f1554d52c83278
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481765"
---
# <a name="jet_instance"></a>JET_INSTANCE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_instance"></a>JET_INSTANCE

Le type de données **JET_INSTANCE** contient un descripteur de l’instance de la base de données à utiliser pour un appel à l’API jet.

```cpp
    typedef JET_API_PTR JET_INSTANCE;
```

### <a name="data-types"></a>Types de données

JET_INSTANCE

La **valeur null** ou [JET_instanceNil](./invalid-handle-constants.md) peut être utilisée pour indiquer un handle d’instance non valide.

### <a name="remarks"></a>Remarques

Ce descripteur est obtenu lorsque vous créez une instance de la base de données en appelant les fonctions [JetCreateInstance](./jetcreateinstance-function.md), [JetCreateInstance2](./jetcreateinstance2-function.md), [JetInit](./jetinit-function.md)ou [JetInit2](./jetinit2-function.md) .

**Windows XP :**  l’utilisation explicite des instances est uniquement prise en charge sur Windows XP et les versions ultérieures.

**Windows 2000 :**  Une seule instance globale est prise en charge par processus.

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetCreateInstance2](./jetcreateinstance2-function.md)  
[JetInit](./jetinit-function.md)  
[JetInit2](./jetinit2-function.md)
