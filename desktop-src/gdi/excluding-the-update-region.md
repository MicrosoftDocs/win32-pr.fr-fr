---
description: La fonction ExcludeUpdateRgn exclut la région de mise à jour de la zone de découpage pour le contexte de périphérique d’affichage.
ms.assetid: e652122b-a3b7-4d1b-8afd-9648d5ee3d42
title: Exclusion de la région de mise à jour
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7be39b948e61fc06c7f7005d15c1163cef0068f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034222"
---
# <a name="excluding-the-update-region"></a><span data-ttu-id="d8e03-103">Exclusion de la région de mise à jour</span><span class="sxs-lookup"><span data-stu-id="d8e03-103">Excluding the Update Region</span></span>

<span data-ttu-id="d8e03-104">La fonction [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) exclut la région de mise à jour de la zone de découpage pour le contexte de périphérique d’affichage.</span><span class="sxs-lookup"><span data-stu-id="d8e03-104">The [**ExcludeUpdateRgn**](/windows/desktop/api/Winuser/nf-winuser-excludeupdatergn) function excludes the update region from the clipping region for the display device context.</span></span> <span data-ttu-id="d8e03-105">Cette fonction est utile lors du dessin dans une fenêtre autre que lors du \_ traitement d’un message de peinture WM.</span><span class="sxs-lookup"><span data-stu-id="d8e03-105">This function is useful when drawing in a window other than when a WM\_PAINT message is processing.</span></span> <span data-ttu-id="d8e03-106">Il empêche le dessin dans les zones qui seront mises à jour pendant le prochain \_ message de peinture WM.</span><span class="sxs-lookup"><span data-stu-id="d8e03-106">It prevents drawing in the areas that will be updated during the next WM\_PAINT message.</span></span>

 

 



