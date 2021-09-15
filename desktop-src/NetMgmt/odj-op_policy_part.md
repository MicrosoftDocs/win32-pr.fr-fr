---
title: OP_POLICY_PART
description: Définition du OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517736"
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
