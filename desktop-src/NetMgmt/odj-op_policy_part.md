---
title: OP_POLICY_PART
description: Définition du OP_POLICY_PART IDL
ms.assetid: 3988b298-b21d-4476-bfa5-ac606bcbd6c8
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: ef0e3b96ce564ed7ff8e2ce0886e33ca474a1cf8
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383175"
---
# <a name="op_policy_part-structure"></a><span data-ttu-id="4bcd2-103">Structure OP_POLICY_PART</span><span class="sxs-lookup"><span data-stu-id="4bcd2-103">OP_POLICY_PART structure</span></span>

<span data-ttu-id="4bcd2-104">Contient un tableau de structures OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="4bcd2-104">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bcd2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bcd2-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_PART
{
    ULONG                                       cElementLists;
    [size_is(cElementLists)]
                        POP_POLICY_ELEMENT_LIST pElementLists;
    OP_BLOB                                     Extension;
} OP_POLICY_PART, *POP_POLICY_PART;
```

## <a name="members"></a><span data-ttu-id="4bcd2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="4bcd2-106">Members</span></span>

### <a name="celementlists"></a><span data-ttu-id="4bcd2-107">cElementLists</span><span class="sxs-lookup"><span data-stu-id="4bcd2-107">cElementLists</span></span>

<span data-ttu-id="4bcd2-108">Contient le nombre d’éléments dans pElementLists.</span><span class="sxs-lookup"><span data-stu-id="4bcd2-108">Contains the number of elements in pElementLists.</span></span>

### <a name="pelementlists"></a><span data-ttu-id="4bcd2-109">pElementLists</span><span class="sxs-lookup"><span data-stu-id="4bcd2-109">pElementLists</span></span>

<span data-ttu-id="4bcd2-110">Contient un tableau de structures OP_POLICY_ELEMENT_LIST.</span><span class="sxs-lookup"><span data-stu-id="4bcd2-110">Contains an array of OP_POLICY_ELEMENT_LIST structures.</span></span>

### <a name="extension"></a><span data-ttu-id="4bcd2-111">Extension</span><span class="sxs-lookup"><span data-stu-id="4bcd2-111">Extension</span></span>

<span data-ttu-id="4bcd2-112">Réservé pour une utilisation ultérieure et doit contenir uniquement des zéros.</span><span class="sxs-lookup"><span data-stu-id="4bcd2-112">Reserved for future use and must contain all zeros.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bcd2-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bcd2-113">See also</span></span>

[<span data-ttu-id="4bcd2-114">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="4bcd2-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="4bcd2-115">**Liste des éléments de la \_ stratégie op \_ \_**</span><span class="sxs-lookup"><span data-stu-id="4bcd2-115">**OP\_POLICY\_ELEMENT\_LIST**</span></span>](odj-op_policy_element_list.md)
