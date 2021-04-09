---
description: Ces valeurs sont utilisées avec ImmGetCompositionString et la \_ composition de l’IME WM \_ .
ms.assetid: 14087598-8041-4e02-a168-f5538a437be0
title: Valeurs de chaîne de composition IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c5b3935329e56f015cdb08a764e1660142a067a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862918"
---
# <a name="ime-composition-string-values"></a><span data-ttu-id="45a20-103">Valeurs de chaîne de composition IME</span><span class="sxs-lookup"><span data-stu-id="45a20-103">IME Composition String Values</span></span>

<span data-ttu-id="45a20-104">Ces valeurs sont utilisées avec [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) et [**la \_ \_ composition de l’IME WM**](wm-ime-composition.md).</span><span class="sxs-lookup"><span data-stu-id="45a20-104">These values are used with [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) and [**WM\_IME\_COMPOSITION**](wm-ime-composition.md).</span></span>



| <span data-ttu-id="45a20-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="45a20-105">Value</span></span>                 | <span data-ttu-id="45a20-106">Description</span><span class="sxs-lookup"><span data-stu-id="45a20-106">Description</span></span>                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="45a20-107">comfromateurs \_ gc</span><span class="sxs-lookup"><span data-stu-id="45a20-107">GCS\_COMPATTR</span></span>         | <span data-ttu-id="45a20-108">Récupérez ou mettez à jour l’attribut de la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-108">Retrieve or update the attribute of the composition string.</span></span>                                |
| <span data-ttu-id="45a20-109">catalogues globaux \_ COMPCLAUSE</span><span class="sxs-lookup"><span data-stu-id="45a20-109">GCS\_COMPCLAUSE</span></span>       | <span data-ttu-id="45a20-110">Récupère ou met à jour les informations de clause de la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-110">Retrieve or update clause information of the composition string.</span></span>                           |
| <span data-ttu-id="45a20-111">catalogues globaux \_ COMPREADATTR</span><span class="sxs-lookup"><span data-stu-id="45a20-111">GCS\_COMPREADATTR</span></span>     | <span data-ttu-id="45a20-112">Récupérez ou mettez à jour les attributs de la chaîne de lecture de la composition actuelle.</span><span class="sxs-lookup"><span data-stu-id="45a20-112">Retrieve or update the attributes of the reading string of the current composition.</span></span>        |
| <span data-ttu-id="45a20-113">catalogues globaux \_ COMPREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="45a20-113">GCS\_COMPREADCLAUSE</span></span>   | <span data-ttu-id="45a20-114">Récupère ou met à jour les informations de clause de la chaîne de lecture de la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-114">Retrieve or update the clause information of the reading string of the composition string.</span></span> |
| <span data-ttu-id="45a20-115">catalogues globaux \_ COMPREADSTR</span><span class="sxs-lookup"><span data-stu-id="45a20-115">GCS\_COMPREADSTR</span></span>      | <span data-ttu-id="45a20-116">Récupère ou met à jour la chaîne de lecture de la composition actuelle.</span><span class="sxs-lookup"><span data-stu-id="45a20-116">Retrieve or update the reading string of the current composition.</span></span>                          |
| <span data-ttu-id="45a20-117">catalogues globaux \_ COMPSTR</span><span class="sxs-lookup"><span data-stu-id="45a20-117">GCS\_COMPSTR</span></span>          | <span data-ttu-id="45a20-118">Récupérez ou mettez à jour la chaîne de composition actuelle.</span><span class="sxs-lookup"><span data-stu-id="45a20-118">Retrieve or update the current composition string.</span></span>                                         |
| <span data-ttu-id="45a20-119">catalogues globaux \_ CURSORPOS</span><span class="sxs-lookup"><span data-stu-id="45a20-119">GCS\_CURSORPOS</span></span>        | <span data-ttu-id="45a20-120">Récupère ou met à jour la position du curseur dans la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-120">Retrieve or update the cursor position in composition string.</span></span>                              |
| <span data-ttu-id="45a20-121">catalogues globaux \_ DELTASTART</span><span class="sxs-lookup"><span data-stu-id="45a20-121">GCS\_DELTASTART</span></span>       | <span data-ttu-id="45a20-122">Récupère ou met à jour la position de départ de toutes les modifications dans la chaîne de composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-122">Retrieve or update the starting position of any changes in composition string.</span></span>             |
| <span data-ttu-id="45a20-123">catalogues globaux \_ RESULTCLAUSE</span><span class="sxs-lookup"><span data-stu-id="45a20-123">GCS\_RESULTCLAUSE</span></span>     | <span data-ttu-id="45a20-124">Récupère ou met à jour les informations de clause de la chaîne de résultat.</span><span class="sxs-lookup"><span data-stu-id="45a20-124">Retrieve or update clause information of the result string.</span></span>                                |
| <span data-ttu-id="45a20-125">catalogues globaux \_ RESULTREADCLAUSE</span><span class="sxs-lookup"><span data-stu-id="45a20-125">GCS\_RESULTREADCLAUSE</span></span> | <span data-ttu-id="45a20-126">Récupère ou met à jour les informations de clause de la chaîne de lecture.</span><span class="sxs-lookup"><span data-stu-id="45a20-126">Retrieve or update clause information of the reading string.</span></span>                               |
| <span data-ttu-id="45a20-127">catalogues globaux \_ RESULTREADSTR</span><span class="sxs-lookup"><span data-stu-id="45a20-127">GCS\_RESULTREADSTR</span></span>    | <span data-ttu-id="45a20-128">Récupérez ou mettez à jour la chaîne de lecture.</span><span class="sxs-lookup"><span data-stu-id="45a20-128">Retrieve or update the reading string.</span></span>                                                     |
| <span data-ttu-id="45a20-129">GC \_ RESULTSTR</span><span class="sxs-lookup"><span data-stu-id="45a20-129">GCS\_RESULTSTR</span></span>        | <span data-ttu-id="45a20-130">Récupérez ou mettez à jour la chaîne du résultat de la composition.</span><span class="sxs-lookup"><span data-stu-id="45a20-130">Retrieve or update the string of the composition result.</span></span>                                   |



 

 

 



