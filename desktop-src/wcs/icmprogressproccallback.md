---
title: ICMProgressProcCallback, fonction de rappel
description: La fonction ICMProgressProcCallback est une fonction de rappel fournie par l’application qui signale la progression et permet à l’application d’annuler le traitement des couleurs.
ms.assetid: 4e0bfa4c-f0eb-4776-98d6-90d9adf71bee
keywords:
- Fonction de rappel ICMProgressProcCallback Windows Color System
topic_type:
- apiref
api_name:
- ICMProgressProcCallback
api_location:
- Icm.h
api_type:
- UserDefined
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8acf790a135a41e4eabb4a67c2498f1ed914c4c8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520783"
---
# <a name="icmprogressproccallback-callback-function"></a><span data-ttu-id="d8813-104">ICMProgressProcCallback, fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="d8813-104">ICMProgressProcCallback callback function</span></span>

<span data-ttu-id="d8813-105">La fonction **ICMProgressProcCallback** est une fonction de rappel fournie par l’application qui signale la progression et permet à l’application d’annuler le traitement des couleurs.</span><span class="sxs-lookup"><span data-stu-id="d8813-105">The **ICMProgressProcCallback** function is an application-supplied callback function that reports progress and permits the application to cancel color processing.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8813-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8813-106">Syntax</span></span>


```C++
BOOL WINAPI ICMProgressProcCallback(
   ULONG  ulMax,
   ULONG  ulCurrent,
   LPARAM ulCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="d8813-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8813-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8813-108">*ulMax*</span><span class="sxs-lookup"><span data-stu-id="d8813-108">*ulMax*</span></span> 
</dt> <dd>

<span data-ttu-id="d8813-109">Spécifie la valeur maximale du compteur de progression (utilisée pour estimer l’achèvement du traitement de la bitmap).</span><span class="sxs-lookup"><span data-stu-id="d8813-109">Specifies the maximum value of the progress counter (used to estimate completion of the bitmap processing).</span></span>

</dd> <dt>

<span data-ttu-id="d8813-110">*ulCurrent*</span><span class="sxs-lookup"><span data-stu-id="d8813-110">*ulCurrent*</span></span> 
</dt> <dd>

<span data-ttu-id="d8813-111">Spécifie la valeur actuelle du compteur de progression (lorsqu’elle est divisée par la valeur maximale, fournit une estimation approximative du pourcentage d’achèvement).</span><span class="sxs-lookup"><span data-stu-id="d8813-111">Specifies the current value of the progress counter (when divided by the maximum value, provides a rough estimate of percentage of completion).</span></span>

</dd> <dt>

<span data-ttu-id="d8813-112">*ulCallbackData*</span><span class="sxs-lookup"><span data-stu-id="d8813-112">*ulCallbackData*</span></span> 
</dt> <dd>

<span data-ttu-id="d8813-113">Spécifie les données qui sont passées par l’application à une fonction ICM2, qui la transmet ensuite à la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="d8813-113">Specifies the data which is passed by the application to an ICM2 function, which then passes it on to the callback function.</span></span> <span data-ttu-id="d8813-114">Ces données peuvent être utilisées, par exemple, pour identifier la bitmap et traiter la progression signalée.</span><span class="sxs-lookup"><span data-stu-id="d8813-114">Such data can be used, for example, to identify the bitmap and process about which progress is being reported.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8813-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d8813-115">Return value</span></span>

<span data-ttu-id="d8813-116">Cette fonction retourne la **valeur true** pour continuer le traitement de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="d8813-116">This function returns **TRUE** to continue bitmap processing.</span></span> <span data-ttu-id="d8813-117">La valeur de retour est **false** pour annuler le traitement.</span><span class="sxs-lookup"><span data-stu-id="d8813-117">The return value is **FALSE** to cancel processing.</span></span> <span data-ttu-id="d8813-118">Si le traitement est annulé, la fonction appelante retourne la valeur zéro pour indiquer un échec, même si sa mémoire tampon de sortie peut être partiellement remplie.</span><span class="sxs-lookup"><span data-stu-id="d8813-118">If processing is canceled, the calling function returns zero to indicate failure, although its output buffer may be partially filled.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8813-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d8813-119">Remarks</span></span>

<span data-ttu-id="d8813-120">Le nom de cette fonction de rappel est fourni par l’application.</span><span class="sxs-lookup"><span data-stu-id="d8813-120">The name of this callback function is supplied by the application.</span></span> <span data-ttu-id="d8813-121">Plusieurs fonctions WCS, y compris [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) et [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), appellent cette fonction régulièrement.</span><span class="sxs-lookup"><span data-stu-id="d8813-121">A number of WCS functions, including [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) and [**CheckBitmapBits**](/windows/win32/api/icm/nf-icm-checkbitmapbits), call this function periodically.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8813-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d8813-122">Requirements</span></span>



| <span data-ttu-id="d8813-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d8813-123">Requirement</span></span> | <span data-ttu-id="d8813-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d8813-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d8813-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8813-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d8813-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8813-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d8813-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d8813-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d8813-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d8813-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d8813-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="d8813-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8813-130"><dt>ICM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8813-130"><dt>Icm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8813-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8813-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8813-132">Concepts de base de la gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="d8813-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="d8813-133">Fonctions</span><span class="sxs-lookup"><span data-stu-id="d8813-133">Functions</span></span>](functions.md)
</dt> <dt>

[<span data-ttu-id="d8813-134">**TranslateBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="d8813-134">**TranslateBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-translatebitmapbits)
</dt> <dt>

[<span data-ttu-id="d8813-135">**CheckBitmapBits**</span><span class="sxs-lookup"><span data-stu-id="d8813-135">**CheckBitmapBits**</span></span>](/windows/win32/api/icm/nf-icm-checkbitmapbits)
</dt> </dl>
