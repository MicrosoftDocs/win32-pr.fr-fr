---
description: Extrait les informations d’en-tête d’un Delta.
title: ExtractPatchHeaderToFileA/W, fonction
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: ExtractPatchHeaderToFileA, ExtractPatchHeaderToFileW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtractPatchHeaderToFileW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: 40835a0b88558046ff9086ffcd7ec4609d1ed863
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530517"
---
# <a name="extractpatchheadertofileaw-function"></a><span data-ttu-id="84f8f-103">ExtractPatchHeaderToFileA/W, fonction</span><span class="sxs-lookup"><span data-stu-id="84f8f-103">ExtractPatchHeaderToFileA/W function</span></span>

<span data-ttu-id="84f8f-104">Les fonctions **ExtractPatchHeaderToFileA** et **ExtractPatchHeaderToFileW** extraient les informations d’en-tête d’un Delta.</span><span class="sxs-lookup"><span data-stu-id="84f8f-104">The **ExtractPatchHeaderToFileA** and **ExtractPatchHeaderToFileW** functions extract the header information from a delta.</span></span> <span data-ttu-id="84f8f-105">Le Delta est fourni sous la forme d’un chemin d’accès de fichier.</span><span class="sxs-lookup"><span data-stu-id="84f8f-105">The delta is provided as a file path.</span></span> <span data-ttu-id="84f8f-106">L’en-tête de sortie est également écrit dans un chemin d’accès fourni.</span><span class="sxs-lookup"><span data-stu-id="84f8f-106">The output header is also written to a provided path.</span></span>

## <a name="syntax"></a><span data-ttu-id="84f8f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84f8f-107">Syntax</span></span>

```cpp
BOOL  PATCHAPI  ExtractPatchHeaderToFileA(
    LPCTSTR  PatchFileName,
    LPCTSTR  PatchHeaderFileName
    );

BOOL  PATCHAPI  ExtractPatchHeaderToFileW(
    LPCWSTR  PatchFileName,
    LPCWSTR  PatchHeaderFileName
    );
```

## <a name="parameters"></a><span data-ttu-id="84f8f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="84f8f-108">Parameters</span></span>

<span data-ttu-id="84f8f-109">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="84f8f-109">*PatchFileName*</span></span>

<span data-ttu-id="84f8f-110">Nom du Delta contenant l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="84f8f-110">The name of the delta containing the header.</span></span>

<span data-ttu-id="84f8f-111">*PatchHeaderFileName*</span><span class="sxs-lookup"><span data-stu-id="84f8f-111">*PatchHeaderFileName*</span></span>

<span data-ttu-id="84f8f-112">Nom du fichier d’en-tête à créer.</span><span class="sxs-lookup"><span data-stu-id="84f8f-112">The name of the header file that is to be created.</span></span>

## <a name="return-value"></a><span data-ttu-id="84f8f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="84f8f-113">Return value</span></span>

<span data-ttu-id="84f8f-114">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="84f8f-114">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="84f8f-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="84f8f-115">Requirements</span></span>

| <span data-ttu-id="84f8f-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="84f8f-116">Requirement</span></span> | <span data-ttu-id="84f8f-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="84f8f-117">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="84f8f-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="84f8f-118">Header</span></span> | <span data-ttu-id="84f8f-119">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="84f8f-119">patchapi.h</span></span> |
| <span data-ttu-id="84f8f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="84f8f-120">DLL</span></span> | <span data-ttu-id="84f8f-121">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="84f8f-121">mspatchc.dll</span></span> |
| <span data-ttu-id="84f8f-122">Unicode</span><span class="sxs-lookup"><span data-stu-id="84f8f-122">Unicode</span></span> | <span data-ttu-id="84f8f-123">Implémenté en tant que ExtractPatchHeaderToFileW (Unicode) et ExtractPatchHeaderToFileA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="84f8f-123">Implemented as ExtractPatchHeaderToFileW (Unicode) and ExtractPatchHeaderToFileA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="84f8f-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="84f8f-124">See also</span></span>

[<span data-ttu-id="84f8f-125">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="84f8f-125">PatchAPI</span></span>](patchapi.md)
