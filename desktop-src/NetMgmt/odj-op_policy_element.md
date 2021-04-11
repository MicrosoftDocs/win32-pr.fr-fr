---
title: OP_POLICY_ELEMENT
description: Définition du OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316907"
---
# <a name="op_policy_element-structure"></a>Structure OP_POLICY_ELEMENT

Définit une clé de Registre et un nom de valeur, un type et une valeur qui doivent être configurés sous cette clé.

## <a name="syntax"></a>Syntaxe

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a>Membres

### <a name="pkeypath"></a>pKeyPath

Contient le chemin d’accès de la clé de registre.

### <a name="pvaluename"></a>pValueName

Contient le nom de la valeur de registre.

### <a name="ulvaluetype"></a>ulValueType

Contient l’une des valeurs des [types de valeur de Registre](../sysinfo/registry-value-types.md).

### <a name="cbvaluedata"></a>cbValueData

Contient la taille de pValueData en octets.

### <a name="ulvaluetype"></a>ulValueType

Contient la valeur de la valeur de registre.

## <a name="see-also"></a>Voir aussi

[**Définitions IDL de jonction de domaine hors connexion**](odj-idl.md)