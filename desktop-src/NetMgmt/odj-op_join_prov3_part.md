---
title: OP_JOINPROV3_PART
description: Définition du OP_JOINPROV3_PART IDL
ms.assetid: 1d8bbfcf-c08e-4bc8-b569-0496703f2d67
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 81c8f53f55a8d5a284f969cbde539b0c34406903
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "104383168"
---
# <a name="op_joinprov3_part-structure"></a><span data-ttu-id="5d96f-103">Structure OP_JOINPROV3_PART</span><span class="sxs-lookup"><span data-stu-id="5d96f-103">OP_JOINPROV3_PART structure</span></span>

<span data-ttu-id="5d96f-104">Contient des informations supplémentaires utilisées pour la configuration d’un client joint à un domaine.</span><span class="sxs-lookup"><span data-stu-id="5d96f-104">Contains additional information used for configuring a client joined to a domain.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d96f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d96f-105">Syntax</span></span>

```C++
typedef struct _OP_JOINPROV3_PART
{
    DWORD Rid;
    [string] wchar_t *lpSid;
} OP_JOINPROV3_PART, *POP_JOINPROV3_PART;
```

## <a name="members"></a><span data-ttu-id="5d96f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="5d96f-106">Members</span></span>

### <a name="rid"></a><span data-ttu-id="5d96f-107">RID</span><span class="sxs-lookup"><span data-stu-id="5d96f-107">Rid</span></span>

<span data-ttu-id="5d96f-108">Doit être défini sur l’identificateur relatif du SID du compte d’ordinateur</span><span class="sxs-lookup"><span data-stu-id="5d96f-108">Must be set to the Relative Identifier of the machine account’s SID</span></span>

### <a name="lpsid"></a><span data-ttu-id="5d96f-109">lpSid</span><span class="sxs-lookup"><span data-stu-id="5d96f-109">lpSid</span></span>

<span data-ttu-id="5d96f-110">Doit être défini sur le SID du compte d’ordinateur sous forme de chaîne.</span><span class="sxs-lookup"><span data-stu-id="5d96f-110">Must be set to the SID of the machine account in string form.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d96f-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d96f-111">See also</span></span>

[<span data-ttu-id="5d96f-112">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="5d96f-112">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
