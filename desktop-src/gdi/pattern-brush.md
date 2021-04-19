---
description: Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB). Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.
ms.assetid: 0de89a6f-d9c7-4f33-8088-c24a48a3ceee
title: Pinceau de motif
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66d39dd499d6a95b3fb61624b2aab8b421f51c34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987698"
---
# <a name="pattern-brush"></a><span data-ttu-id="205b3-104">Pinceau de motif</span><span class="sxs-lookup"><span data-stu-id="205b3-104">Pattern Brush</span></span>

<span data-ttu-id="205b3-105">Un pinceau de modèle (ou personnalisé) est créé à partir d’une bitmap définie par l’application ou d’une bitmap indépendante du périphérique (DIB).</span><span class="sxs-lookup"><span data-stu-id="205b3-105">A pattern (or custom) brush is created from an application-defined bitmap or device-independent bitmap (DIB).</span></span> <span data-ttu-id="205b3-106">Les rectangles suivants ont été peints à l’aide de différents pinceaux de modèle.</span><span class="sxs-lookup"><span data-stu-id="205b3-106">The following rectangles were painted by using different pattern brushes.</span></span>

![Illustration montrant trois zones, chacune remplie d’un modèle différent](images/csbru-05.png)

<span data-ttu-id="205b3-108">Pour créer un pinceau de motif logique, une application doit d’abord créer une image bitmap.</span><span class="sxs-lookup"><span data-stu-id="205b3-108">To create a logical pattern brush, an application must first create a bitmap.</span></span> <span data-ttu-id="205b3-109">Après la création de l’image bitmap, l’application peut créer le pinceau de modèle logique en appelant la fonction [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) ou [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) , en fournissant un handle qui identifie la bitmap (ou DIB).</span><span class="sxs-lookup"><span data-stu-id="205b3-109">After creating the bitmap, the application can create the logical pattern brush by calling the [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush) or [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) function, supplying a handle that identifies the bitmap (or DIB).</span></span> <span data-ttu-id="205b3-110">Les pinceaux qui apparaissent dans l’illustration précédente ont été créés à partir d’images bitmap monochrome.</span><span class="sxs-lookup"><span data-stu-id="205b3-110">The brushes that appear in the preceding illustration were created from monochrome bitmaps.</span></span> <span data-ttu-id="205b3-111">Pour obtenir une description des bitmaps, des DIB et des fonctions qui les créent, consultez [bitmaps](bitmaps.md).</span><span class="sxs-lookup"><span data-stu-id="205b3-111">For a description of bitmaps, DIBs, and the functions that create them, see [Bitmaps](bitmaps.md).</span></span>

 

 



