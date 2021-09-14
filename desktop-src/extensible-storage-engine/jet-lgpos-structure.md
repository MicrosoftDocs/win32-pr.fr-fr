---
description: 'En savoir plus sur : structure JET_LGPOS'
title: Structure JET_LGPOS
TOCTitle: JET_LGPOS Structure
ms:assetid: dbce1a60-b32b-40c1-a215-e93bb77cd8c1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294113(v=EXCHG.10)
ms:contentKeyID: 32765727
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
ms.openlocfilehash: e3e83786236a95cf2b0c4d77e26e6987334a5b00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915952"
---
# <a name="jet_lgpos-structure"></a>Structure JET_LGPOS


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_lgpos-structure"></a>Structure JET_LGPOS

La structure **JET_LGPOS** contient des données qui sont internes au mécanisme de journalisation du moteur de base de données. Cette structure est considérée comme interne.

```cpp
    typedef struct {
      unsigned short ib;
      unsigned short isec;
      long lGeneration;
    } JET_LGPOS;
```

### <a name="members"></a>Membres

**IB**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

**ISEC**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

**lGeneration**

Prend en charge l’infrastructure ESE et ne peut pas être utilisé à partir de votre code.

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JET_BKINFO](./jet-bkinfo-structure.md)  
[JET_DBINFOMISC](./jet-dbinfomisc-structure.md)
