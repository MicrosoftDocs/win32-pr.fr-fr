---
description: Utilise le Delta et la source (fournis sous forme de mémoires tampons) pour créer une nouvelle copie des données cibles. Les données de sortie sont retournées dans une mémoire tampon allouée par MSDelta.
title: ApplyDeltaB function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: ApplyDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplyDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 368788ba894064aa8ac3f8c9711f987a32f306af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541445"
---
# <a name="applydeltab-function"></a><span data-ttu-id="edaaa-104">ApplyDeltaB function</span><span class="sxs-lookup"><span data-stu-id="edaaa-104">ApplyDeltaB function</span></span>

<span data-ttu-id="edaaa-105">Utilise le Delta et la source (fournis sous forme de mémoires tampons) pour créer une nouvelle copie des données cibles.</span><span class="sxs-lookup"><span data-stu-id="edaaa-105">Uses the delta and source (provided as buffers) to create a new copy of the target data.</span></span> <span data-ttu-id="edaaa-106">Les données de sortie sont retournées dans une mémoire tampon allouée par MSDelta.</span><span class="sxs-lookup"><span data-stu-id="edaaa-106">The output data is returned in an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="edaaa-107">Vous devez appeler [DeltaFree](msdelta-deltafree.md) pour libérer la mémoire tampon de sortie une fois cette fonction terminée.</span><span class="sxs-lookup"><span data-stu-id="edaaa-107">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

> [!NOTE]
> <span data-ttu-id="edaaa-108">Si le delta spécifié a été créé à l’aide de [PatchAPI](patchapi.md)et que l’indicateur [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) est défini, MSDelta appellera PatchAPI pour appliquer le delta.</span><span class="sxs-lookup"><span data-stu-id="edaaa-108">If the specified delta was created using [PatchAPI](patchapi.md), and the [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) flag is set, MSDelta will call PatchAPI to apply the delta.</span></span>

## <a name="syntax"></a><span data-ttu-id="edaaa-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="edaaa-109">Syntax</span></span>

```cpp
BOOL  WINAPI  ApplyDeltaB(
    DELTA_FLAG_TYPE  ApplyFlags,
    DELTA_INPUT      Source,
    DELTA_INPUT      Delta,
    LPDELTA_OUTPUT   lpTarget
   );
```

## <a name="parameters"></a><span data-ttu-id="edaaa-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="edaaa-110">Parameters</span></span>

<span data-ttu-id="edaaa-111">*ApplyFlags*</span><span class="sxs-lookup"><span data-stu-id="edaaa-111">*ApplyFlags*</span></span>

<span data-ttu-id="edaaa-112">dans [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) ou [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span><span class="sxs-lookup"><span data-stu-id="edaaa-112">[in] Either [DELTA_FLAG_NONE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) or [DELTA_APPLY_FLAG_ALLOW_PA19](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags).</span></span>

<span data-ttu-id="edaaa-113">*Source*</span><span class="sxs-lookup"><span data-stu-id="edaaa-113">*Source*</span></span>

<span data-ttu-id="edaaa-114">dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données sources.</span><span class="sxs-lookup"><span data-stu-id="edaaa-114">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="edaaa-115">*Delta*</span><span class="sxs-lookup"><span data-stu-id="edaaa-115">*Delta*</span></span>

<span data-ttu-id="edaaa-116">dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données Delta.</span><span class="sxs-lookup"><span data-stu-id="edaaa-116">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the delta data.</span></span>

<span data-ttu-id="edaaa-117">*lpTarget*</span><span class="sxs-lookup"><span data-stu-id="edaaa-117">*lpTarget*</span></span>

<span data-ttu-id="edaaa-118">à Pointeur vers la structure [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) dans laquelle la cible doit être écrite.</span><span class="sxs-lookup"><span data-stu-id="edaaa-118">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the target is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="edaaa-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="edaaa-119">Return value</span></span>

<span data-ttu-id="edaaa-120">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="edaaa-120">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="edaaa-121">Quand la fonction retourne **false**, vous pouvez appeler [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour recevoir le code d’erreur système Win32 correspondant.</span><span class="sxs-lookup"><span data-stu-id="edaaa-121">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="edaaa-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="edaaa-122">Requirements</span></span>

| <span data-ttu-id="edaaa-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="edaaa-123">Requirement</span></span> | <span data-ttu-id="edaaa-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="edaaa-124">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="edaaa-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="edaaa-125">Header</span></span> | <span data-ttu-id="edaaa-126">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="edaaa-126">msdelta.h</span></span> |
| <span data-ttu-id="edaaa-127">DLL</span><span class="sxs-lookup"><span data-stu-id="edaaa-127">DLL</span></span> | <span data-ttu-id="edaaa-128">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="edaaa-128">msdelta.dll</span></span> |
| <span data-ttu-id="edaaa-129">Unicode</span><span class="sxs-lookup"><span data-stu-id="edaaa-129">Unicode</span></span> | <span data-ttu-id="edaaa-130">Non applicable</span><span class="sxs-lookup"><span data-stu-id="edaaa-130">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="edaaa-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="edaaa-131">See also</span></span>

[<span data-ttu-id="edaaa-132">MSDelta</span><span class="sxs-lookup"><span data-stu-id="edaaa-132">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="edaaa-133">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="edaaa-133">DeltaFree</span></span>](msdelta-deltafree.md)
