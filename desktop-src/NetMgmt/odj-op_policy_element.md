---
title: OP_POLICY_ELEMENT
description: Définition du OP_POLICY_ELEMENT IDL
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 74e81f09f4d45d42f5e9df585b88051ac1e96e8cd33e4c15807701e61825b43b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983383"
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