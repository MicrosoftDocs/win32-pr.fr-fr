---
title: ODJ_UNICODE_STRING
description: Définition du ODJ_UNICODE_STRING IDL
ms.assetid: a7999df0-d961-4fd7-ae5e-65ad79a9c17c
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: f1134d7b95cca6948932bf9d79fe976d6745448a
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/14/2020
ms.locfileid: "106511719"
---
# <a name="odj_unicode_string-structure"></a><span data-ttu-id="f3aec-103">Structure ODJ_UNICODE_STRING</span><span class="sxs-lookup"><span data-stu-id="f3aec-103">ODJ_UNICODE_STRING structure</span></span>

<span data-ttu-id="f3aec-104">Contient une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="f3aec-104">Contains a Unicode string.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3aec-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f3aec-105">Syntax</span></span>

```C++
typedef struct _ODJ_UNICODE_STRING
{
    USHORT Length;
    USHORT MaximumLength;
    [size_is(MaximumLength/2), length_is(Length/2)] PWSTR Buffer;
} ODJ_UNICODE_STRING, *PODJ_UNICODE_STRING;
```

## <a name="members"></a><span data-ttu-id="f3aec-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f3aec-106">Members</span></span>

### <a name="length"></a><span data-ttu-id="f3aec-107">Longueur</span><span class="sxs-lookup"><span data-stu-id="f3aec-107">Length</span></span>

<span data-ttu-id="f3aec-108">Doit être défini sur le nombre d’octets dans la mémoire tampon contenant la chaîne, à l’exclusion de la marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="f3aec-108">Must be set to the number of bytes in Buffer containing the string, not including the NULL terminator.</span></span>

### <a name="maximumlength"></a><span data-ttu-id="f3aec-109">MaximumLength</span><span class="sxs-lookup"><span data-stu-id="f3aec-109">MaximumLength</span></span>

<span data-ttu-id="f3aec-110">Elle doit être définie sur le nombre total d’octets dans la mémoire tampon, à l’exclusion de la marque de fin NULL.</span><span class="sxs-lookup"><span data-stu-id="f3aec-110">This MUST be set to the total number of bytes in Buffer, not including the NULL terminator.</span></span>

### <a name="buffer"></a><span data-ttu-id="f3aec-111">Buffer</span><span class="sxs-lookup"><span data-stu-id="f3aec-111">Buffer</span></span>

<span data-ttu-id="f3aec-112">Il doit s'agir d'une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="f3aec-112">Must be a Unicode string.</span></span>

## <a name="see-also"></a><span data-ttu-id="f3aec-113">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3aec-113">See also</span></span>

[<span data-ttu-id="f3aec-114">**Définitions IDL de jonction de domaine hors connexion**</span><span class="sxs-lookup"><span data-stu-id="f3aec-114">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
