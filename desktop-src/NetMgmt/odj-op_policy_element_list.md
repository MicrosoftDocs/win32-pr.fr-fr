---
title: OP_POLICY_ELEMENT_LIST
description: Définition du OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 1fde1bb1d2794be4fd1bf799282a0257b78ae213453566208ff64bcf7a312654
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796860"
---
# <a name="op_policy_element_list-structure"></a>Structure OP_POLICY_ELEMENT_LIST

Définit une clé de Registre racine et un tableau d’éléments de clé de Registre à configurer sous cette clé.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a>Membres

### <a name="psource"></a>pSource

Contient le chemin d’accès du fichier stratégie de groupe à partir duquel les éléments contenus ont été issus.

### <a name="ulrootkeyid"></a>ulRootKeyId

Contient l’identificateur de la clé de Registre racine ; doit être défini sur HKEY_LOCAL_MACHINE.

### <a name="celements"></a>cElements

Contient le nombre d’éléments dans les papelements.

### <a name="pelements"></a>papelements

Contient un tableau d’éléments OP_POLICY_ELEMENT.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)

[**OP ( \_ élément de stratégie) \_**](odj-op_policy_element.md)
