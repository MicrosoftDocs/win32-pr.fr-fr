---
description: 'En savoir plus sur : structure JET_THREADSTATS'
title: Structure JET_THREADSTATS
TOCTitle: JET_THREADSTATS Structure
ms:assetid: 37e86e14-7719-4991-aae8-bcff1baa80df
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269227(v=EXCHG.10)
ms:contentKeyID: 32765529
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
ms.openlocfilehash: 7f94c9911fb7ab974f87cfed41e92b53ac0a66cb
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122983562"
---
# <a name="jet_threadstats-structure"></a>Structure JET_THREADSTATS


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_threadstats-structure"></a>Structure JET_THREADSTATS

La structure **JET_THREADSTATS** contient des statistiques cumulatives sur le travail effectué par le moteur de base de données sur le thread actuel. Ces informations sont retournées via [JetGetThreadStats](./jetgetthreadstats-function.md).

**Windows Vista :**  la structure **JET_THREADSTATS** est introduite dans Windows Vista.

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cPageReferenced;
      unsigned long cPageRead;
      unsigned long cPagePreread;
      unsigned long cPageDirtied;
      unsigned long cPageRedirtied;
      unsigned long cLogRecord;
      unsigned long cbLogRecord;
    } JET_THREADSTATS;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure **JET_THREADSTATS** retournée, en octets.

**Remarque**  La structure **JET_THREADSTATS** sera développée à l’avenir pour contenir plus de statistiques. De nouvelles statistiques seront ajoutées à la fin de la structure et peuvent être récupérées avec une taille de mémoire tampon de sortie accrue. La présence de statistiques supplémentaires peut être déduite par une valeur **cbStruct** plus grande.

**cPageReferenced**

Nombre total de pages de base de données visitées par le moteur de base de données sur le thread actuel.

**cPageRead**

Nombre total de pages de base de données extraites du disque par le moteur de base de données sur le thread actuel.

**cPagePreread**

Nombre total de pages de base de données prérécupérées à partir du disque par le moteur de base de données sur le thread actuel.

**cPageDirtied**

Nombre total de pages de base de données, sans modification non écrite, qui ont été modifiées par le moteur de base de données sur le thread actuel.

**cPageRedirtied**

Nombre total de pages de base de données, avec des modifications non écrites, qui ont été modifiées par le moteur de base de données sur le thread actuel.

**cLogRecord**

Nombre total d’enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.

**cbLogRecord**

Taille totale, en octets, des enregistrements du journal des transactions qui ont été générés par le moteur de base de données sur le thread actuel.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista.</p> | 
| <p><strong>Serveur</strong></p> | <p>requiert Windows Server 2008.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 



### <a name="see-also"></a>Voir aussi

[JetGetThreadStats](./jetgetthreadstats-function.md)
