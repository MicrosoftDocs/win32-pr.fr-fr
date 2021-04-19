---
description: Copie le contenu d’un bloc de mémoire source vers un bloc de mémoire de destination et prend en charge les blocs de mémoire source et de destination qui se chevauchent.
ms.assetid: D374F14D-24C7-4771-AD40-3AC37E7A2D2F
title: Fonction RtlMoveMemory (WDM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlMoveMemory
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 65f8c8490224213e0bef27fab5239a21eca24344
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517186"
---
# <a name="rtlmovememory-function"></a><span data-ttu-id="e6932-103">RtlMoveMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="e6932-103">RtlMoveMemory function</span></span>

<span data-ttu-id="e6932-104">Copie le contenu d’un bloc de mémoire source vers un bloc de mémoire de destination et prend en charge les blocs de mémoire source et de destination qui se chevauchent.</span><span class="sxs-lookup"><span data-stu-id="e6932-104">Copies the contents of a source memory block to a destination memory block, and supports overlapping source and destination memory blocks.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6932-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6932-105">Syntax</span></span>


```C++
VOID RtlMoveMemory(
  _Out_       VOID UNALIGNED *Destination,
  _In_  const VOID UNALIGNED *Source,
  _In_        SIZE_T         Length
);
```



## <a name="parameters"></a><span data-ttu-id="e6932-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6932-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6932-107">*Destination* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6932-107">*Destination* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6932-108">Pointeur vers le bloc de mémoire de destination dans lequel copier les octets.</span><span class="sxs-lookup"><span data-stu-id="e6932-108">A pointer to the destination memory block to copy the bytes to.</span></span>

</dd> <dt>

<span data-ttu-id="e6932-109">*Source* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6932-109">*Source* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6932-110">Pointeur vers le bloc de mémoire source à partir duquel copier les octets.</span><span class="sxs-lookup"><span data-stu-id="e6932-110">A pointer to the source memory block to copy the bytes from.</span></span>

</dd> <dt>

<span data-ttu-id="e6932-111">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6932-111">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6932-112">Nombre d’octets à copier de la source vers la destination.</span><span class="sxs-lookup"><span data-stu-id="e6932-112">The number of bytes to copy from the source to the destination.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6932-113">Valeur de retour</span><span class="sxs-lookup"><span data-stu-id="e6932-113">Return value</span></span>

<span data-ttu-id="e6932-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="e6932-114">None</span></span>

## <a name="remarks"></a><span data-ttu-id="e6932-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e6932-115">Remarks</span></span>

<span data-ttu-id="e6932-116">Le bloc de mémoire source, qui est défini par la *source* et la *longueur*, peut chevaucher le bloc de mémoire de destination, qui est défini par la *destination* et la *longueur*.</span><span class="sxs-lookup"><span data-stu-id="e6932-116">The source memory block, which is defined by *Source* and *Length*, can overlap the destination memory block, which is defined by *Destination* and *Length*.</span></span>

<span data-ttu-id="e6932-117">La routine [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) s’exécute plus rapidement que **RtlMoveMemory**, mais **RtlCopyMemory** requiert que les blocs de mémoire source et de destination ne se chevauchent pas.</span><span class="sxs-lookup"><span data-stu-id="e6932-117">The [**RtlCopyMemory**](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory) routine runs faster than **RtlMoveMemory**, but **RtlCopyMemory** requires that the source and destination memory blocks do not overlap.</span></span>

<span data-ttu-id="e6932-118">Les appelants de **RtlMoveMemory** peuvent s’exécuter à n’importe quel niveau IRQL si les blocs de mémoire source et de destination se trouvent dans la mémoire système non paginée.</span><span class="sxs-lookup"><span data-stu-id="e6932-118">Callers of **RtlMoveMemory** can be running at any IRQL if the source and destination memory blocks are in nonpaged system memory.</span></span> <span data-ttu-id="e6932-119">Dans le cas contraire, l’appelant doit s’exécuter au niveau IRQL <= APC \_ .</span><span class="sxs-lookup"><span data-stu-id="e6932-119">Otherwise, the caller must be running at IRQL <= APC\_LEVEL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6932-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6932-120">Requirements</span></span>



| <span data-ttu-id="e6932-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6932-121">Requirement</span></span> | <span data-ttu-id="e6932-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6932-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6932-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6932-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6932-124">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6932-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="e6932-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6932-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6932-126">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6932-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="e6932-127">Plateforme cible</span><span class="sxs-lookup"><span data-stu-id="e6932-127">Target platform</span></span><br/>          | <dl> <span data-ttu-id="e6932-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="e6932-128"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="e6932-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6932-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6932-130"><dt>WDM. h (inclure WDM. h, Ntddk. h ou Ntifs. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6932-130"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="e6932-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6932-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e6932-132"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6932-132"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="e6932-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e6932-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6932-134"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6932-134"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="e6932-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6932-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6932-136">**RtlCopyMemory**</span><span class="sxs-lookup"><span data-stu-id="e6932-136">**RtlCopyMemory**</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-rtlcopymemory)
</dt> </dl>

 

 
