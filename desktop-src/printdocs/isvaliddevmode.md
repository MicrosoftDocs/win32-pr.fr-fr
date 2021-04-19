---
description: La fonction IsValidDevmode vérifie que le contenu d’une structure DEVMODE est valide.
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: IsValidDevmode, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534128"
---
# <a name="isvaliddevmode-function"></a><span data-ttu-id="a466e-103">IsValidDevmode fonction)</span><span class="sxs-lookup"><span data-stu-id="a466e-103">IsValidDevmode function</span></span>

<span data-ttu-id="a466e-104">La fonction **IsValidDevmode** vérifie que le contenu d’une structure DEVMODE est valide.</span><span class="sxs-lookup"><span data-stu-id="a466e-104">The **IsValidDevmode** function verifies that the contents of a DEVMODE structure are valid.</span></span>

## <a name="syntax"></a><span data-ttu-id="a466e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a466e-105">Syntax</span></span>


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a><span data-ttu-id="a466e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a466e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a466e-107">*pDevmode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a466e-107">*pDevmode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a466e-108">Pointeur vers le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) à valider.</span><span class="sxs-lookup"><span data-stu-id="a466e-108">A pointer to the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) to validate.</span></span>

</dd> <dt>

<span data-ttu-id="a466e-109">*DevmodeSize*</span><span class="sxs-lookup"><span data-stu-id="a466e-109">*DevmodeSize*</span></span> 
</dt> <dd>

<span data-ttu-id="a466e-110">Taille en octets de la mémoire tampon d’octets en entrée.</span><span class="sxs-lookup"><span data-stu-id="a466e-110">The size in bytes of the input byte buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a466e-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a466e-111">Return value</span></span>

<span data-ttu-id="a466e-112">**True** si [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) est structurellement valide.</span><span class="sxs-lookup"><span data-stu-id="a466e-112">**TRUE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is structurally valid.</span></span> <span data-ttu-id="a466e-113">Si des erreurs mineures sont détectées, la fonction les corrige et retourne la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="a466e-113">If minor errors are found the function will fix them and return **TRUE**.</span></span>

<span data-ttu-id="a466e-114">**False**, si le [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) présente un ou plusieurs problèmes structurels significatifs.</span><span class="sxs-lookup"><span data-stu-id="a466e-114">**FALSE**, if the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) has one or more significant structural problems.</span></span> <span data-ttu-id="a466e-115">Par exemple, son membre **dmSize** est mal aligné ou spécifie une mémoire tampon qui est trop petite.</span><span class="sxs-lookup"><span data-stu-id="a466e-115">For example, its **dmSize** member is misaligned or specifies a buffer that is too small.</span></span> <span data-ttu-id="a466e-116">**False** également si **PDevmode** a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="a466e-116">Also, **FALSE** if **pDevmode** is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a466e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="a466e-117">Remarks</span></span>

<span data-ttu-id="a466e-118">Aucun champ de pilote d’imprimante privée de l' [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) n’est activé, mais uniquement les champs publics.</span><span class="sxs-lookup"><span data-stu-id="a466e-118">No private printer driver fields of the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) are checked, only the public fields.</span></span>

<span data-ttu-id="a466e-119">Les appelants doivent utiliser **dmSize** + **dmDriverExtra** pour **DevmodeSize** uniquement s’ils peuvent garantir que la taille de la mémoire tampon d’entrée est au moins égale à celle du grand.</span><span class="sxs-lookup"><span data-stu-id="a466e-119">Callers should use **dmSize**+**dmDriverExtra** for **DevmodeSize** only if they can guarantee that the input buffer size is at least that big.</span></span> <span data-ttu-id="a466e-120">Étant donné que la [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) est généralement des données non fiables, les valeurs qui se trouvent dans la mémoire tampon d’entrée au niveau des offsets **dmSize** et **dmDriverExtra** sont également non fiables.</span><span class="sxs-lookup"><span data-stu-id="a466e-120">Since the [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) is generally untrusted data, the values that are in the input buffer at the **dmSize** and **dmDriverExtra** offsets are also untrusted.</span></span>

<span data-ttu-id="a466e-121">Cette fonction est exécutable dans Least-Privileged contexte de compte d’utilisateur (LUA).</span><span class="sxs-lookup"><span data-stu-id="a466e-121">This function is executable in Least-Privileged User Account (LUA) context.</span></span>

## <a name="requirements"></a><span data-ttu-id="a466e-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a466e-122">Requirements</span></span>



| <span data-ttu-id="a466e-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a466e-123">Requirement</span></span> | <span data-ttu-id="a466e-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a466e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a466e-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a466e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a466e-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a466e-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a466e-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a466e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a466e-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a466e-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a466e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a466e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a466e-130"><dt>Winspool. h</dt></span><span class="sxs-lookup"><span data-stu-id="a466e-130"><dt>Winspool.h</dt></span></span> </dl>   |
| <span data-ttu-id="a466e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a466e-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="a466e-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a466e-132"><dt>Winspool.lib</dt></span></span> </dl> |
| <span data-ttu-id="a466e-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a466e-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a466e-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a466e-134"><dt>Winspool.drv</dt></span></span> </dl> |
| <span data-ttu-id="a466e-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a466e-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a466e-136">**IsValidDevmodeW** (Unicode) et **IsValidDevmodeA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a466e-136">**IsValidDevmodeW** (Unicode) and **IsValidDevmodeA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a466e-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a466e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a466e-138">Impression</span><span class="sxs-lookup"><span data-stu-id="a466e-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a466e-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a466e-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a466e-140">**DEVMODE**</span><span class="sxs-lookup"><span data-stu-id="a466e-140">**DEVMODE**</span></span>](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




