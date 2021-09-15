---
title: OP_JOINPROV3_PART
description: Définition du OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127517753"
---
# <a name="op_joinprov3_part-structure"></a>Structure OP_JOINPROV3_PART

Contient des informations supplémentaires utilisées pour la configuration d’un client joint à un domaine.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a>Membres

### <a name="rid"></a>RID

Doit être défini sur l’identificateur relatif du SID du compte d’ordinateur

### <a name="lpsid"></a>lpSid

Doit être défini sur le SID du compte d’ordinateur sous forme de chaîne.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)
