---
title: Toucher la couleur RVB
description: Toucher la couleur RVB
ms.assetid: b71a0a66-11aa-4a21-b78a-3bd90f80a428
keywords:
- Apparences mobiles du lecteur Windows Media, couleurs de bouton
- apparences, couleurs de bouton
- informations de référence sur les apparences, les boutons
- boutons dans les apparences, couleurs
- Référence des couleurs pour les habillages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7c69863c4197702383f729c8d7e8d30d3cb52bc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512679"
---
# <a name="hit-rgb-color"></a><span data-ttu-id="8bdff-108">Toucher la couleur RVB</span><span class="sxs-lookup"><span data-stu-id="8bdff-108">Hit RGB Color</span></span>

<span data-ttu-id="8bdff-109">Si vous utilisez des boutons de région (PushHit, ToggleHit et 2PushHit), vous devez définir la couleur qui sera utilisée par le lecteur Windows Media pour déterminer la zone d’accès de votre bouton.</span><span class="sxs-lookup"><span data-stu-id="8bdff-109">If you are using region buttons (PushHit, ToggleHit, and 2PushHit), you must define the color that Windows Media Player will use to determine the hit area of your button.</span></span> <span data-ttu-id="8bdff-110">Cette valeur doit être spécifiée à l’aide de trois entiers positifs séparés par des virgules.</span><span class="sxs-lookup"><span data-stu-id="8bdff-110">This value must be specified using three positive integers separated by commas.</span></span> <span data-ttu-id="8bdff-111">Ces entiers représentent la quantité de rouge, de vert et de bleu pour une image bitmap, et sont comprises entre 0 et 255.</span><span class="sxs-lookup"><span data-stu-id="8bdff-111">These integers represent the amount of red, green, and blue for a bitmap color, and range from 0 to 255.</span></span>

> [!Note]  
> <span data-ttu-id="8bdff-112">Les types de boutons sont déconseillés dans les habillages pour Windows Media Player 10 mobile ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="8bdff-112">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span>

 

<span data-ttu-id="8bdff-113">Vous pouvez utiliser n’importe quelle couleur pour les valeurs, mais assurez-vous que chaque bouton de région que vous définissez a une couleur unique dans le fichier image de la région et que la valeur de couleur que vous définissez ici comme nombre correspond à la couleur réelle utilisée dans l’image de la région.</span><span class="sxs-lookup"><span data-stu-id="8bdff-113">You can use any colors for the values, but be sure that each region button you define has a unique color in the Region image file and that the color value you define here as a number matches the actual color used in the Region image.</span></span>

<span data-ttu-id="8bdff-114">Le tableau suivant répertorie les couleurs typiques que vous pouvez utiliser.</span><span class="sxs-lookup"><span data-stu-id="8bdff-114">The following table shows some typical colors you might want to use.</span></span>



| <span data-ttu-id="8bdff-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="8bdff-115">Value</span></span>       | <span data-ttu-id="8bdff-116">Description</span><span class="sxs-lookup"><span data-stu-id="8bdff-116">Description</span></span> |
|-------------|-------------|
| <span data-ttu-id="8bdff-117">0, 0, 0</span><span class="sxs-lookup"><span data-stu-id="8bdff-117">0,0,0</span></span>       | <span data-ttu-id="8bdff-118">Noir</span><span class="sxs-lookup"><span data-stu-id="8bdff-118">Black</span></span>       |
| <span data-ttu-id="8bdff-119">255 255 255</span><span class="sxs-lookup"><span data-stu-id="8bdff-119">255,255,255</span></span> | <span data-ttu-id="8bdff-120">Blancs</span><span class="sxs-lookup"><span data-stu-id="8bdff-120">White</span></span>       |
| <span data-ttu-id="8bdff-121">255, 0, 0</span><span class="sxs-lookup"><span data-stu-id="8bdff-121">255,0,0</span></span>     | <span data-ttu-id="8bdff-122">Rouge</span><span class="sxs-lookup"><span data-stu-id="8bdff-122">Red</span></span>         |
| <span data-ttu-id="8bdff-123">0255, 0</span><span class="sxs-lookup"><span data-stu-id="8bdff-123">0,255,0</span></span>     | <span data-ttu-id="8bdff-124">Vert</span><span class="sxs-lookup"><span data-stu-id="8bdff-124">Green</span></span>       |
| <span data-ttu-id="8bdff-125">0, 0255</span><span class="sxs-lookup"><span data-stu-id="8bdff-125">0,0,255</span></span>     | <span data-ttu-id="8bdff-126">Bleu</span><span class="sxs-lookup"><span data-stu-id="8bdff-126">Blue</span></span>        |



 

<span data-ttu-id="8bdff-127">Si vous n’utilisez pas de boutons de région, vous devez entrer les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="8bdff-127">If you do not use region buttons, you must enter the following:</span></span>


```C++
0,0,0

```



## <a name="related-topics"></a><span data-ttu-id="8bdff-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8bdff-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bdff-129">**Boutons**</span><span class="sxs-lookup"><span data-stu-id="8bdff-129">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




