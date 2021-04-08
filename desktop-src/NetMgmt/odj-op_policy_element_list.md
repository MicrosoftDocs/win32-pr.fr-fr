---
title: OP_POLICY_ELEMENT_LIST
description: Définition du OP_POLICY_ELEMENT_LIST IDL
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "103734700"
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
