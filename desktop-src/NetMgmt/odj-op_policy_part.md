---
title: OP_POLICY_PART
description: Définition du OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 8ad479c2e24d8c38e87a2100658be2afcf37d70d321e99433e3b05a3af35fa60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911479"
---
# <a name="op_policy_part-structure"></a>Structure OP_POLICY_PART

Contient un tableau de structures OP_POLICY_ELEMENT_LIST.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a>Membres

### <a name="celementlists"></a>cElementLists

Contient le nombre d’éléments dans pElementLists.

### <a name="pelementlists"></a>pElementLists

Contient un tableau de structures OP_POLICY_ELEMENT_LIST.

### <a name="extension"></a>Extension

Réservé pour une utilisation ultérieure et doit contenir uniquement des zéros.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**Liste des éléments de la \_ stratégie op \_ \_**](odj-op_policy_element_list.md)
