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
# <a name="op_policy_element-structure"></a><span data-ttu-id="e7426-103">Structure OP_POLICY_ELEMENT</span><span class="sxs-lookup"><span data-stu-id="e7426-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="e7426-104">Définit une clé de Registre et un nom de valeur, un type et une valeur qui doivent être configurés sous cette clé.</span><span class="sxs-lookup"><span data-stu-id="e7426-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7426-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7426-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="e7426-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e7426-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="e7426-107">pKeyPath</span><span class="sxs-lookup"><span data-stu-id="e7426-107">pKeyPath</span></span>

<span data-ttu-id="e7426-108">Contient le chemin d’accès de la clé de registre.</span><span class="sxs-lookup"><span data-stu-id="e7426-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="e7426-109">pValueName</span><span class="sxs-lookup"><span data-stu-id="e7426-109">pValueName</span></span>

<span data-ttu-id="e7426-110">Contient le nom de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="e7426-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="e7426-111">ulValueType</span><span class="sxs-lookup"><span data-stu-id="e7426-111">ulValueType</span></span>

<span data-ttu-id="e7426-112">Contient l’une des valeurs des [types de valeur de Registre](../sysinfo/registry-value-types.md).</span><span class="sxs-lookup"><span data-stu-id="e7426-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="e7426-113">cbValueData</span><span class="sxs-lookup"><span data-stu-id="e7426-113">cbValueData</span></span>

<span data-ttu-id="e7426-114">Contient la taille de pValueData en octets.</span><span class="sxs-lookup"><span data-stu-id="e7426-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="e7426-115">ulValueType</span><span class="sxs-lookup"><span data-stu-id="e7426-115">ulValueType</span></span>

<span data-ttu-id="e7426-116">Contient la valeur de la valeur de registre.</span><span class="sxs-lookup"><span data-stu-id="e7426-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7426-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7426-117">See also</span></span>

[<span data-ttu-id="e7426-118">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="e7426-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)