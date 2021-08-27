---
description: 'En savoir plus sur : structure JET_SNPROG'
title: Structure JET_SNPROG
TOCTitle: JET_SNPROG Structure
ms:assetid: 8b4224e4-ad4d-440f-8915-8eb43b0885f0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269328(v=EXCHG.10)
ms:contentKeyID: 32765618
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
ms.openlocfilehash: ab132d203ca2dc81e2ed3c3d8a0ce25c76a2cc71
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987732"
---
# <a name="jet_snprog-structure"></a>Structure JET_SNPROG


_**S’applique à :** Windows | Windows Serveurs_

## <a name="jet_snprog-structure"></a>Structure JET_SNPROG

La structure **JET_SNPROG** contient des informations sur la progression d’une opération de longue durée. Lorsque la fonction de rappel est appelée pour notifier l’état de l’opération et que l’opération est toujours en cours, le dernier paramètre de la fonction de rappel est un pointeur vers une structure de **JET_SNPROG** .

```cpp
    typedef struct {
      unsigned long cbStruct;
      unsigned long cunitDone;
      unsigned long cunitTotal;
    } JET_SNPROG;
```

### <a name="members"></a>Membres

**cbStruct**

Taille de la structure **JET_SNPROG** , en octets. Cette valeur confirme la présence des champs suivants.

**cunitDone**

Nombre d’unités de travail déjà terminées pendant la fonction de longue durée.

**cunitTotal**

Nombre d’unités de travail qui doivent être terminées. Cette valeur doit toujours être supérieure ou égale à **cunitDone**.

### <a name="requirements"></a>Configuration requise


| Condition requise | Valeur |
|------------|----------|
| <p><strong>Client</strong></p> | <p>requiert Windows Vista, Windows XP ou Windows 2000 Professional.</p> | 
| <p><strong>Serveur</strong></p> | <p>nécessite Windows server 2008, Windows server 2003 ou Windows 2000 server.</p> | 
| <p><strong>En-tête</strong></p> | <p>Déclaré dans esent. h.</p> | 


