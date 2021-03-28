---
description: Les fonctions suivantes sont utilisées avec les pinceaux.
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: Fonctions de pinceau (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528395"
---
# <a name="brush-functions-windows-gdi"></a><span data-ttu-id="3d63b-103">Fonctions de pinceau (Windows GDI)</span><span class="sxs-lookup"><span data-stu-id="3d63b-103">Brush Functions (Windows GDI)</span></span>

<span data-ttu-id="3d63b-104">Les fonctions suivantes sont utilisées avec les pinceaux.</span><span class="sxs-lookup"><span data-stu-id="3d63b-104">The following functions are used with brushes.</span></span>



| <span data-ttu-id="3d63b-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="3d63b-105">Function</span></span>                                                   | <span data-ttu-id="3d63b-106">Description</span><span class="sxs-lookup"><span data-stu-id="3d63b-106">Description</span></span>                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="3d63b-107">**CreateBrushIndirect**</span><span class="sxs-lookup"><span data-stu-id="3d63b-107">**CreateBrushIndirect**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | <span data-ttu-id="3d63b-108">Crée un pinceau avec un style, une couleur et un motif spécifiés</span><span class="sxs-lookup"><span data-stu-id="3d63b-108">Creates a brush with a specified style, color, and pattern</span></span> |
| [<span data-ttu-id="3d63b-109">**CreateDIBPatternBrushPt**</span><span class="sxs-lookup"><span data-stu-id="3d63b-109">**CreateDIBPatternBrushPt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | <span data-ttu-id="3d63b-110">Crée un pinceau avec le modèle à partir d’un DIB</span><span class="sxs-lookup"><span data-stu-id="3d63b-110">Creates a brush with the pattern from a DIB</span></span>                |
| [<span data-ttu-id="3d63b-111">**CreateHatchBrush**</span><span class="sxs-lookup"><span data-stu-id="3d63b-111">**CreateHatchBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | <span data-ttu-id="3d63b-112">Crée un pinceau avec un motif hachuré et une couleur</span><span class="sxs-lookup"><span data-stu-id="3d63b-112">Creates a brush with a hatch pattern and color</span></span>             |
| [<span data-ttu-id="3d63b-113">**CreatePatternBrush**</span><span class="sxs-lookup"><span data-stu-id="3d63b-113">**CreatePatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | <span data-ttu-id="3d63b-114">Crée un pinceau avec un modèle bitmap</span><span class="sxs-lookup"><span data-stu-id="3d63b-114">Creates a brush with a bitmap pattern</span></span>                      |
| [<span data-ttu-id="3d63b-115">**CreateSolidBrush**</span><span class="sxs-lookup"><span data-stu-id="3d63b-115">**CreateSolidBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | <span data-ttu-id="3d63b-116">Crée un pinceau avec une couleur unie</span><span class="sxs-lookup"><span data-stu-id="3d63b-116">Creates a brush with a solid color</span></span>                         |
| [<span data-ttu-id="3d63b-117">**GetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="3d63b-117">**GetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | <span data-ttu-id="3d63b-118">Obtient l’origine du pinceau pour un contexte de périphérique (Device Context)</span><span class="sxs-lookup"><span data-stu-id="3d63b-118">Gets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="3d63b-119">**GetSysColorBrush**</span><span class="sxs-lookup"><span data-stu-id="3d63b-119">**GetSysColorBrush**</span></span>](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | <span data-ttu-id="3d63b-120">Obtient un handle vers un pinceau qui correspond à un index de couleur</span><span class="sxs-lookup"><span data-stu-id="3d63b-120">Gets a handle to a brush that corresponds to a color index</span></span> |
| [<span data-ttu-id="3d63b-121">**PatBlt**</span><span class="sxs-lookup"><span data-stu-id="3d63b-121">**PatBlt**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | <span data-ttu-id="3d63b-122">Peint un rectangle</span><span class="sxs-lookup"><span data-stu-id="3d63b-122">Paints a rectangle</span></span>                                         |
| [<span data-ttu-id="3d63b-123">**SetBrushOrgEx**</span><span class="sxs-lookup"><span data-stu-id="3d63b-123">**SetBrushOrgEx**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | <span data-ttu-id="3d63b-124">Définit l’origine du pinceau pour un contexte de périphérique (Device Context)</span><span class="sxs-lookup"><span data-stu-id="3d63b-124">Sets the brush origin for a device context</span></span>                 |
| [<span data-ttu-id="3d63b-125">**SetDCBrushColor**</span><span class="sxs-lookup"><span data-stu-id="3d63b-125">**SetDCBrushColor**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | <span data-ttu-id="3d63b-126">Définit la couleur actuelle du pinceau du contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="3d63b-126">Sets the current device context brush color.</span></span>               |



 

## <a name="obsolete-functions"></a><span data-ttu-id="3d63b-127">Fonctions obsolètes</span><span class="sxs-lookup"><span data-stu-id="3d63b-127">Obsolete Functions</span></span>

<span data-ttu-id="3d63b-128">Les fonctions suivantes sont fournies uniquement à des fins de compatibilité avec les versions 16 bits de Windows.</span><span class="sxs-lookup"><span data-stu-id="3d63b-128">The following functions are provided only for compatibility with 16-bit versions of Windows.</span></span>

[<span data-ttu-id="3d63b-129">**CreateDIBPatternBrush**</span><span class="sxs-lookup"><span data-stu-id="3d63b-129">**CreateDIBPatternBrush**</span></span>](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



