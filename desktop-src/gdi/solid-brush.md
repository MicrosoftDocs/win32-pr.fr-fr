---
description: Un pinceau plein est un pinceau logique qui contient 64 pixels de la même couleur.
ms.assetid: 920014c7-d1ef-4b98-8c92-c4169be52cb9
title: Pinceau plein
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7cd7a2140ece4bf93ac6f8525be461b70e28fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973090"
---
# <a name="solid-brush"></a><span data-ttu-id="39062-103">Pinceau plein</span><span class="sxs-lookup"><span data-stu-id="39062-103">Solid Brush</span></span>

<span data-ttu-id="39062-104">Un *pinceau plein* est un pinceau logique qui contient 64 pixels de la même couleur.</span><span class="sxs-lookup"><span data-stu-id="39062-104">A *solid brush* is a logical brush that contains 64 pixels of the same color.</span></span> <span data-ttu-id="39062-105">Une application peut créer un pinceau logique solide en appelant la fonction [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) , en spécifiant la couleur du pinceau requis.</span><span class="sxs-lookup"><span data-stu-id="39062-105">An application can create a solid logical brush by calling the [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) function, specifying the color of the brush required.</span></span> <span data-ttu-id="39062-106">Après avoir créé le pinceau plein, l’application peut la sélectionner dans son contexte de périphérique et l’utiliser pour peindre des formes remplies.</span><span class="sxs-lookup"><span data-stu-id="39062-106">After creating the solid brush, the application can select it into its device context and use it to paint filled shapes.</span></span>

 

 



