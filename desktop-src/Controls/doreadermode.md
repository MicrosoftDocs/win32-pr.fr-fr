---
title: DoReaderMode fonction)
description: Active le mode lecteur dans une fenêtre.
ms.assetid: 8f898cdd-c907-430a-8287-15d88390c756
keywords:
- Contrôles Windows de la fonction DoReaderMode
topic_type:
- apiref
api_name:
- DoReaderMode
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5f5c5863e804cd4bbaab651447e4c6f22dc24a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479469"
---
# <a name="doreadermode-function"></a><span data-ttu-id="4086d-104">DoReaderMode fonction)</span><span class="sxs-lookup"><span data-stu-id="4086d-104">DoReaderMode function</span></span>

<span data-ttu-id="4086d-105">\[**DoReaderMode** est disponible via Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="4086d-105">\[**DoReaderMode** is available through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="4086d-106">Elle n’est peut-être pas disponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="4086d-106">It may be unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="4086d-107">Active le mode lecteur dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4086d-107">Enables reader mode in a window.</span></span>

## <a name="syntax"></a><span data-ttu-id="4086d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4086d-108">Syntax</span></span>


```C++
void WINAPI DoReaderMode(
  _In_ PREADERMODEINFO prmi
);
```



## <a name="parameters"></a><span data-ttu-id="4086d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4086d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4086d-110">*PRMI* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4086d-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4086d-111">Type : **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="4086d-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="4086d-112">Pointeur vers une structure [**READERMODEINFO**](readermodeinfo.md) qui contient les informations d’initialisation pour le mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="4086d-112">A pointer to a [**READERMODEINFO**](readermodeinfo.md) structure that contains initialization information for the reader mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4086d-113">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="4086d-113">Return value</span></span>

<span data-ttu-id="4086d-114">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="4086d-114">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4086d-115">Notes</span><span class="sxs-lookup"><span data-stu-id="4086d-115">Remarks</span></span>

<span data-ttu-id="4086d-116">Le mode lecteur est activé via des appareils pris en charge par un clic de souris, généralement à l’aide d’un troisième bouton de la souris ou d’une roulette de défilement.</span><span class="sxs-lookup"><span data-stu-id="4086d-116">Reader mode is activated through supported devices by a mouse click, typically using a third mouse button or scroll wheel.</span></span> <span data-ttu-id="4086d-117">Le déplacement suivant de la souris dans une zone spécifiée fait défiler le contenu de cette zone plutôt que de déplacer un pointeur.</span><span class="sxs-lookup"><span data-stu-id="4086d-117">Subsequent mouse movement in a specified area scrolls that area's contents rather than moving a pointer.</span></span> <span data-ttu-id="4086d-118">En dehors de cette zone, le pointeur de la souris est affiché et fonctionne normalement.</span><span class="sxs-lookup"><span data-stu-id="4086d-118">Outside of that area, the mouse pointer is displayed and operates normally.</span></span> <span data-ttu-id="4086d-119">Un deuxième clic sur le bouton ou la roulette de défilement libère l’appareil du mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="4086d-119">A second click of the button or scroll wheel releases the device from reader mode.</span></span>

> [!Note]  
> <span data-ttu-id="4086d-120">Cette fonction n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="4086d-120">This function is not declared in any public header.</span></span> <span data-ttu-id="4086d-121">Pour l’utiliser, vous devez y accéder en tant qu’ordinal 383 à partir de Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="4086d-121">To use it, you must access it as ordinal 383 from Comctl32.dll.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4086d-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4086d-122">Requirements</span></span>



| <span data-ttu-id="4086d-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4086d-123">Requirement</span></span> | <span data-ttu-id="4086d-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="4086d-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4086d-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4086d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4086d-126">Windows Vista, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4086d-126">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="4086d-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4086d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4086d-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4086d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4086d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="4086d-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4086d-130"><dt>Comctl32.dll (version 4,72 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="4086d-130"><dt>Comctl32.dll (version 4.72 or later)</dt></span></span> </dl> |



 

 





