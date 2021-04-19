---
description: Crée un delta entre la source et la cible (fourni sous forme de mémoires tampons) et retourne le delta de sortie comme une mémoire tampon allouée par MSDelta.
title: CreateDeltaB function
ms.topic: reference
ms.date: 12/03/2020
ms.keywords: CreateDeltaB
req.header: msdelta.h
req.dll: msdelta.dll
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateDeltaB
api_type:
- DllExport
api_location:
- msdelta.dll
ms.openlocfilehash: a2142f26499514c24967e5334d782c2dee559cd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523480"
---
# <a name="createdeltab-function"></a><span data-ttu-id="5e03a-103">CreateDeltaB function</span><span class="sxs-lookup"><span data-stu-id="5e03a-103">CreateDeltaB function</span></span>

<span data-ttu-id="5e03a-104">Crée un delta entre la source et la cible (fourni sous forme de mémoires tampons) et retourne le delta de sortie comme une mémoire tampon allouée par MSDelta.</span><span class="sxs-lookup"><span data-stu-id="5e03a-104">Creates a delta between the source and target (provided as buffers) and returns the output delta as an MSDelta-allocated buffer.</span></span>

> [!NOTE]
> <span data-ttu-id="5e03a-105">Vous devez appeler [DeltaFree](msdelta-deltafree.md) pour libérer la mémoire tampon de sortie une fois cette fonction terminée.</span><span class="sxs-lookup"><span data-stu-id="5e03a-105">You must call [DeltaFree](msdelta-deltafree.md) to free the output buffer after this function has completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e03a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5e03a-106">Syntax</span></span>

```cpp
BOOL  WINAPI  CreateDeltaB(
           DELTA_FILE_TYPE  FileTypeSet,
           DELTA_FLAG_TYPE  SetFlags,
           DELTA_FLAG_TYPE  ResetFlags,
           DELTA_INPUT      Source,
           DELTA_INPUT      Target,
           DELTA_INPUT      SourceOptions,
           DELTA_INPUT      TargetOptions,
           DELTA_INPUT      GlobalOptions,
    const  FILETIME        *lpTargetFileTime,
           ALG_ID           HashAlgId,
           LPDELTA_OUTPUT   lpDelta
    );
```

## <a name="parameters"></a><span data-ttu-id="5e03a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5e03a-107">Parameters</span></span>

<span data-ttu-id="5e03a-108">*FileTypeSet*</span><span class="sxs-lookup"><span data-stu-id="5e03a-108">*FileTypeSet*</span></span>

<span data-ttu-id="5e03a-109">dans Valeur [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) qui indique le type de fichier à utiliser pour le processus de création.</span><span class="sxs-lookup"><span data-stu-id="5e03a-109">[in] The [DELTA_FILE_TYPE](/previous-versions/bb417345(v=msdn.10)#file-type-sets) value that indicates the file type set to be used for the create process.</span></span>

<span data-ttu-id="5e03a-110">*SetFlags*</span><span class="sxs-lookup"><span data-stu-id="5e03a-110">*SetFlags*</span></span>

<span data-ttu-id="5e03a-111">dans Une ou plusieurs valeurs [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) qui spécifient les indicateurs à utiliser pendant le processus de création, en plus des indicateurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="5e03a-111">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the flags to be used during the create process, in addition to the default flags.</span></span>

<span data-ttu-id="5e03a-112">*ResetFlags*</span><span class="sxs-lookup"><span data-stu-id="5e03a-112">*ResetFlags*</span></span>

<span data-ttu-id="5e03a-113">dans Une ou plusieurs valeurs [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) qui spécifient les indicateurs par défaut à réinitialiser au cours du processus de création.</span><span class="sxs-lookup"><span data-stu-id="5e03a-113">[in] One or more [DELTA_FLAG_TYPE](/previous-versions/bb417345(v=msdn.10)#delta_flag_type-flags) values that specify the default flags to be reset during the create process.</span></span>

<span data-ttu-id="5e03a-114">*Source*</span><span class="sxs-lookup"><span data-stu-id="5e03a-114">*Source*</span></span>

<span data-ttu-id="5e03a-115">dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données sources.</span><span class="sxs-lookup"><span data-stu-id="5e03a-115">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the source data.</span></span>

<span data-ttu-id="5e03a-116">*Cible*</span><span class="sxs-lookup"><span data-stu-id="5e03a-116">*Target*</span></span>

<span data-ttu-id="5e03a-117">dans Structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) contenant un pointeur vers la mémoire tampon contenant les données cibles.</span><span class="sxs-lookup"><span data-stu-id="5e03a-117">[in] A [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure containing a pointer to the buffer containing the target data.</span></span>

<span data-ttu-id="5e03a-118">*SourceOptions*</span><span class="sxs-lookup"><span data-stu-id="5e03a-118">*SourceOptions*</span></span>

<span data-ttu-id="5e03a-119">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="5e03a-119">[in] Reserved.</span></span> <span data-ttu-id="5e03a-120">Passer une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec la valeur *modifiable* définie à **false**, *lpStart* défini sur **null** et *uSize* défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="5e03a-120">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="5e03a-121">*TargetOptions*</span><span class="sxs-lookup"><span data-stu-id="5e03a-121">*TargetOptions*</span></span>

<span data-ttu-id="5e03a-122">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="5e03a-122">[in] Reserved.</span></span> <span data-ttu-id="5e03a-123">Passer une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec la valeur *modifiable* définie à **false**, *lpStart* défini sur **null** et *uSize* défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="5e03a-123">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *Editable* set to **FALSE**, *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="5e03a-124">*GlobalOptions*</span><span class="sxs-lookup"><span data-stu-id="5e03a-124">*GlobalOptions*</span></span>

<span data-ttu-id="5e03a-125">[in] Réservée.</span><span class="sxs-lookup"><span data-stu-id="5e03a-125">[in] Reserved.</span></span> <span data-ttu-id="5e03a-126">Transmettez une structure [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) avec *LpStart* défini sur **null** et *uSize* défini sur 0.</span><span class="sxs-lookup"><span data-stu-id="5e03a-126">Pass a [DELTA_INPUT](/previous-versions/bb417345(v=msdn.10)#delta-input-structure) structure with *lpStart* set to **NULL** and *uSize* set to 0.</span></span>

<span data-ttu-id="5e03a-127">*lpTargetFileTime*</span><span class="sxs-lookup"><span data-stu-id="5e03a-127">*lpTargetFileTime*</span></span>

<span data-ttu-id="5e03a-128">dans L’horodatage défini sur le fichier cible après Delta s’applique.</span><span class="sxs-lookup"><span data-stu-id="5e03a-128">[in] The time stamp set on the target file after delta apply.</span></span> <span data-ttu-id="5e03a-129">Si la **valeur est null**, l’horodatage cible sera l’heure actuelle pendant le processus de création.</span><span class="sxs-lookup"><span data-stu-id="5e03a-129">If **NULL**, the target timestamp will be the current time during the create process.</span></span>

<span data-ttu-id="5e03a-130">*HashAlgId*</span><span class="sxs-lookup"><span data-stu-id="5e03a-130">*HashAlgId*</span></span>

<span data-ttu-id="5e03a-131">dans ALG_ID de l’algorithme à utiliser pour générer la signature cible.</span><span class="sxs-lookup"><span data-stu-id="5e03a-131">[in] ALG_ID of the algorithm to be used to generate the target signature.</span></span> <span data-ttu-id="5e03a-132">Certaines valeurs spéciales sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="5e03a-132">Some special values are:</span></span>

- <span data-ttu-id="5e03a-133">0 = aucune signature</span><span class="sxs-lookup"><span data-stu-id="5e03a-133">0 = No signature</span></span>
- <span data-ttu-id="5e03a-134">32 = CRC de 32 bits défini dans msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="5e03a-134">32 = 32-bit CRC defined in msdelta.dll</span></span>

<span data-ttu-id="5e03a-135">*lpDelta*</span><span class="sxs-lookup"><span data-stu-id="5e03a-135">*lpDelta*</span></span>

<span data-ttu-id="5e03a-136">à Pointeur vers la structure [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) dans laquelle le delta doit être écrit.</span><span class="sxs-lookup"><span data-stu-id="5e03a-136">[out] Pointer to the [DELTA_OUTPUT](/previous-versions/bb417345(v=msdn.10)#delta-output-structure) structure where the delta is to be written.</span></span>

## <a name="return-value"></a><span data-ttu-id="5e03a-137">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5e03a-137">Return value</span></span>

<span data-ttu-id="5e03a-138">Cette fonction retourne **true** si elle est réussie ; Sinon, elle retourne **false**.</span><span class="sxs-lookup"><span data-stu-id="5e03a-138">This function returns **TRUE** if it succeeds; otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="5e03a-139">Quand la fonction retourne **false**, vous pouvez appeler [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) pour recevoir le code d’erreur système Win32 correspondant.</span><span class="sxs-lookup"><span data-stu-id="5e03a-139">When the function returns **FALSE**, you can call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to get the corresponding Win32 system error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e03a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5e03a-140">Requirements</span></span>

| <span data-ttu-id="5e03a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5e03a-141">Requirement</span></span> | <span data-ttu-id="5e03a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="5e03a-142">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5e03a-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="5e03a-143">Header</span></span> | <span data-ttu-id="5e03a-144">msdelta. h</span><span class="sxs-lookup"><span data-stu-id="5e03a-144">msdelta.h</span></span> |
| <span data-ttu-id="5e03a-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5e03a-145">DLL</span></span> | <span data-ttu-id="5e03a-146">msdelta.dll</span><span class="sxs-lookup"><span data-stu-id="5e03a-146">msdelta.dll</span></span> |
| <span data-ttu-id="5e03a-147">Unicode</span><span class="sxs-lookup"><span data-stu-id="5e03a-147">Unicode</span></span> | <span data-ttu-id="5e03a-148">Non applicable</span><span class="sxs-lookup"><span data-stu-id="5e03a-148">Not applicable</span></span> |

## <a name="see-also"></a><span data-ttu-id="5e03a-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e03a-149">See also</span></span>

[<span data-ttu-id="5e03a-150">MSDelta</span><span class="sxs-lookup"><span data-stu-id="5e03a-150">MSDelta</span></span>](msdelta.md)

[<span data-ttu-id="5e03a-151">DeltaFree</span><span class="sxs-lookup"><span data-stu-id="5e03a-151">DeltaFree</span></span>](msdelta-deltafree.md)
