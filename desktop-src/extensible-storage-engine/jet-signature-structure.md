---
description: 'En savoir plus sur : structure JET_SIGNATURE'
title: Structure JET_SIGNATURE
TOCTitle: JET_SIGNATURE Structure
ms:assetid: 90d3fd56-be65-4126-b50c-b53e3c3f38f6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269340(v=EXCHG.10)
ms:contentKeyID: 32765629
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
ms.openlocfilehash: da4684872358d9d6751812b2adb2b2bea819a2e3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476475"
---
# <a name="jet_signature-structure"></a>Structure JET_SIGNATURE


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_signature-structure"></a>Structure JET_SIGNATURE

La structure **JET_SIGNATURE** contient des informations qui identifient de façon unique une base de données.

```cpp
    typedef struct {
      unsigned long ulRandom;
      JET_LOGTIME logtimeCreate;
      char szComputerName[JET_MAX_COMPUTERNAME_LENGTH + 1];
    } JET_SIGNATURE;
```

### <a name="members"></a>Membres

**ulRandom**

Nombre assigné de manière aléatoire.

**logtimeCreate**

Le [JET_LOGTIME](./jet-logtime-structure.md) au moment de l’exécution de [JetCreateDatabase](./jetcreatedatabase-function.md) .

**szComputerName**

Valeur de chaîne facultative du nom NetBIOS de l’ordinateur. Cette valeur ne peut pas être définie.

### <a name="remarks"></a>Remarques

Il peut s’agir d’un élément de [JET_DBINFOMISC](./jet-dbinfomisc-structure.md).

### <a name="requirements"></a>Configuration requise


| | | <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | | <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | | <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)  
[JET_LOGTIME](./jet-logtime-structure.md)  
[JetCreateDatabase](./jetcreatedatabase-function.md)
