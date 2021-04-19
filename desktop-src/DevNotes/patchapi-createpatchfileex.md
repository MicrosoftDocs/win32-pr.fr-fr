---
description: Crée un delta entre le fichier source spécifié et le fichier cible spécifié.
title: CreatePatchFileExA/W, fonction
ms.topic: reference
ms.date: 04/17/2020
ms.keywords: CreatePatchFileExA, CreatePatchFileExW
req.header: patchapi.h
req.dll: mspatchc.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePatchFileExW
api_type:
- DllExport
api_location:
- mspatchc.dll
ms.openlocfilehash: c84be2d859a780e46e7e940aa4a7e7da5296f0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532719"
---
# <a name="createpatchfileexaw-function"></a><span data-ttu-id="77569-103">CreatePatchFileExA/W, fonction</span><span class="sxs-lookup"><span data-stu-id="77569-103">CreatePatchFileExA/W function</span></span>

<span data-ttu-id="77569-104">Les fonctions **CreatePatchFileExA** et **CreatePatchFileExW** créent un delta entre le fichier source spécifié et le fichier cible spécifié.</span><span class="sxs-lookup"><span data-stu-id="77569-104">The **CreatePatchFileExA** and **CreatePatchFileExW** functions create a delta between the specified source file and the specified target file.</span></span> <span data-ttu-id="77569-105">Les fichiers source et cible sont fournis sous forme de chemins d’accès.</span><span class="sxs-lookup"><span data-stu-id="77569-105">Both the source and the target files are provided as paths.</span></span> <span data-ttu-id="77569-106">Le delta de sortie est également écrit dans un chemin d’accès fourni.</span><span class="sxs-lookup"><span data-stu-id="77569-106">The output delta is also written to a provided path.</span></span> <span data-ttu-id="77569-107">Ces fonctions fournissent des rapports de progression pendant le processus de création.</span><span class="sxs-lookup"><span data-stu-id="77569-107">These functions provide progress reporting during the create process.</span></span>

## <a name="syntax"></a><span data-ttu-id="77569-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77569-108">Syntax</span></span>

```cpp
BOOL  PATCHAPI  CreatePatchFileExA(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCTSTR                   NewFileName,
    LPCTSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );

BOOL  PATCHAPI  CreatePatchFileExW(
    ULONG                     OldFileCount,
    PPATCH_OLD_FILE_INFO_A    OldFileInfoArray,
    LPCWSTR                   NewFileName,
    LPCWSTR                   PatchFileName,
    ULONG                     OptionFlags,
    PPATCH_OPTION_DATA        OptionData,
    PPATCH_PROGRESS_CALLBACK  ProgressCallback,
    PVOID                     CallbackContext
    );
```

## <a name="parameters"></a><span data-ttu-id="77569-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77569-109">Parameters</span></span>

<span data-ttu-id="77569-110">*OldFileCount*</span><span class="sxs-lookup"><span data-stu-id="77569-110">*OldFileCount*</span></span>

<span data-ttu-id="77569-111">Nombre total de fichiers sources.</span><span class="sxs-lookup"><span data-stu-id="77569-111">The total number of source files.</span></span> <span data-ttu-id="77569-112">Utilisé pour créer des deltas sur plusieurs fichiers sources (255 maximum).</span><span class="sxs-lookup"><span data-stu-id="77569-112">Used to create deltas against multiple source files (maximum 255).</span></span>

<span data-ttu-id="77569-113">*OldFileInfoArray*</span><span class="sxs-lookup"><span data-stu-id="77569-113">*OldFileInfoArray*</span></span>

<span data-ttu-id="77569-114">Pointeur vers le tableau d’informations du fichier source.</span><span class="sxs-lookup"><span data-stu-id="77569-114">Pointer to source file information array.</span></span>

<span data-ttu-id="77569-115">*NewFileName*</span><span class="sxs-lookup"><span data-stu-id="77569-115">*NewFileName*</span></span>

<span data-ttu-id="77569-116">Nom du fichier cible.</span><span class="sxs-lookup"><span data-stu-id="77569-116">The name of the target file.</span></span>

<span data-ttu-id="77569-117">*PatchFileName*</span><span class="sxs-lookup"><span data-stu-id="77569-117">*PatchFileName*</span></span>

<span data-ttu-id="77569-118">Nom du Delta créé.</span><span class="sxs-lookup"><span data-stu-id="77569-118">The name of the delta that is created.</span></span>

<span data-ttu-id="77569-119">*OptionFlags*</span><span class="sxs-lookup"><span data-stu-id="77569-119">*OptionFlags*</span></span>

<span data-ttu-id="77569-120">Indicateurs de création.</span><span class="sxs-lookup"><span data-stu-id="77569-120">Creation flags.</span></span>

<span data-ttu-id="77569-121">*ProgressCallback*</span><span class="sxs-lookup"><span data-stu-id="77569-121">*ProgressCallback*</span></span>

<span data-ttu-id="77569-122">Pointeur vers le rappel de progression défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="77569-122">Pointer to application-defined progress callback.</span></span>

<span data-ttu-id="77569-123">*CallbackContext*</span><span class="sxs-lookup"><span data-stu-id="77569-123">*CallbackContext*</span></span>

<span data-ttu-id="77569-124">Pointeur vers le contexte défini par l’application.</span><span class="sxs-lookup"><span data-stu-id="77569-124">Pointer to application-defined context.</span></span>

## <a name="return-value"></a><span data-ttu-id="77569-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="77569-125">Return value</span></span>

<span data-ttu-id="77569-126">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="77569-126">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="77569-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77569-127">Requirements</span></span>

| <span data-ttu-id="77569-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77569-128">Requirement</span></span> | <span data-ttu-id="77569-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="77569-129">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77569-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="77569-130">Header</span></span> | <span data-ttu-id="77569-131">patchapi. h</span><span class="sxs-lookup"><span data-stu-id="77569-131">patchapi.h</span></span> |
| <span data-ttu-id="77569-132">DLL</span><span class="sxs-lookup"><span data-stu-id="77569-132">DLL</span></span> | <span data-ttu-id="77569-133">mspatchc.dll</span><span class="sxs-lookup"><span data-stu-id="77569-133">mspatchc.dll</span></span> |
| <span data-ttu-id="77569-134">Unicode</span><span class="sxs-lookup"><span data-stu-id="77569-134">Unicode</span></span> | <span data-ttu-id="77569-135">Implémenté en tant que CreatePatchFileExW (Unicode) et CreatePatchFileExA (ANSI)</span><span class="sxs-lookup"><span data-stu-id="77569-135">Implemented as CreatePatchFileExW (Unicode) and CreatePatchFileExA (ANSI)</span></span> |

## <a name="see-also"></a><span data-ttu-id="77569-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77569-136">See also</span></span>

[<span data-ttu-id="77569-137">PatchAPI</span><span class="sxs-lookup"><span data-stu-id="77569-137">PatchAPI</span></span>](patchapi.md)
