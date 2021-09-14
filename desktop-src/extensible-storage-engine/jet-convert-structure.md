---
description: 'En savoir plus sur : structure JET_CONVERT'
title: Structure JET_CONVERT
TOCTitle: JET_CONVERT Structure
ms:assetid: 33a0ff95-e9af-44c0-bf80-03d785771d5e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269220(v=EXCHG.10)
ms:contentKeyID: 32765523
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
ms.openlocfilehash: ce3fbcc7de9c7904689de3df923a87d575b1b92b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127291655"
---
# <a name="jet_convert-structure"></a>Structure JET_CONVERT


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_convert-structure"></a>Structure JET_CONVERT

La structure **JET_CONVERT** contient le nom d’une dll de version ESE antérieure qui est utilisée pour lire les bases de données créées avec cette version antérieure. En outre, d’autres indicateurs sont fournis pour contrôler la nature de la conversion.

**Windows Server 2003 :** la fonctionnalité de [JetCompact](./jetcompact-function.md) qui a effectué une conversion a été supprimée du produit dans Windows Server 2003. il est uniquement pris en charge dans les Windows 2000 et Windows XP.

```cpp
    typedef struct tagCONVERT {
      tchar* SzOldDll;
      union {
        unsigned long fFlags;
        struct {
          unsigned long fSchemaChangesOnly  :1;
        };
      };
    } JET_CONVERT;
```

### <a name="members"></a>Membres

**SzOldDll**

Nom, y compris les informations de chemin d’accès, à la version antérieure de la DLL ESE.

**fFlags**

Réservé pour le système.

**fSchemaChangesOnly**

Réservé pour le système.

### <a name="requirements"></a>Spécifications


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 
| <p><strong>Unicode</strong></p> | <p>Implémenté comme <strong>JET_CONVERT_W</strong> (Unicode) et <strong>JET_CONVERT_A</strong> (ANSI).</p> | 



### <a name="see-also"></a>Voir aussi

[JetCompact](./jetcompact-function.md)
