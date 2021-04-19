---
description: Libère le bloc de mémoire spécifié.
title: DeltaFree function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: DeltaFree
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- DeltaFree
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: 15885cfa3e879ed6a1e85b2f9553af92d436ca71
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520957"
---
# <a name="deltafree-function"></a><span data-ttu-id="79afd-103">DeltaFree function</span><span class="sxs-lookup"><span data-stu-id="79afd-103">DeltaFree function</span></span>

<span data-ttu-id="79afd-104">Libère le bloc de mémoire spécifié.</span><span class="sxs-lookup"><span data-stu-id="79afd-104">Frees the specified memory block.</span></span> <span data-ttu-id="79afd-105">Vous devez appeler cette fonction après avoir correctement appelé [CreateDeltaB](msdelta-createdeltab.md) et [ApplyDeltaB](msdelta-applydeltab.md) pour libérer la mémoire tampon allouée par MSDelta.</span><span class="sxs-lookup"><span data-stu-id="79afd-105">You must call this function after successful calls to [CreateDeltaB](msdelta-createdeltab.md) and [ApplyDeltaB](msdelta-applydeltab.md) to free the MSDelta-allocated memory buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="79afd-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79afd-106">Syntax</span></span>

```cpp
BOOL  WINAPI  DeltaFree(
    LPVOID  lpMemory
    );
```

## <a name="parameters"></a><span data-ttu-id="79afd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79afd-107">Parameters</span></span>

<span data-ttu-id="79afd-108">*lpMemory*</span><span class="sxs-lookup"><span data-stu-id="79afd-108">*lpMemory*</span></span>

<span data-ttu-id="79afd-109">dans Bloc de mémoire à libérer.</span><span class="sxs-lookup"><span data-stu-id="79afd-109">[in] Memory block to be freed.</span></span>

## <a name="return-value"></a><span data-ttu-id="79afd-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79afd-110">Return value</span></span>

<span data-ttu-id="79afd-111">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="79afd-111">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="79afd-112">Quand la fonction retourne **false**, vous pouvez appeler [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour recevoir le code d’erreur système Win32 correspondant.</span><span class="sxs-lookup"><span data-stu-id="79afd-112">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="79afd-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79afd-113">Requirements</span></span>

| <span data-ttu-id="79afd-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79afd-114">Requirement</span></span> | <span data-ttu-id="79afd-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="79afd-115">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79afd-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="79afd-116">Header</span></span> | <span data-ttu-id="79afd-117">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="79afd-117">msdelta.h</span></span> |
| <span data-ttu-id="79afd-118">DLL</span><span class="sxs-lookup"><span data-stu-id="79afd-118">DLL</span></span> | <span data-ttu-id="79afd-119">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="79afd-119">msdelta.dll</span></span> |
| <span data-ttu-id="79afd-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="79afd-120">Unicode</span></span> | <span data-ttu-id="79afd-121">Non applicable</span><span class="sxs-lookup"><span data-stu-id="79afd-121">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="79afd-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79afd-122">See also</span></span>

[<span data-ttu-id="79afd-123">MSDelta</span><span class="sxs-lookup"><span data-stu-id="79afd-123">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="79afd-124">CreateDeltaB</span><span class="sxs-lookup"><span data-stu-id="79afd-124">CreateDeltaB</span></span>](msdelta-createdeltab.md)

[<span data-ttu-id="79afd-125">ApplyDeltaB</span><span class="sxs-lookup"><span data-stu-id="79afd-125">ApplyDeltaB</span></span>](msdelta-applydeltab.md)
