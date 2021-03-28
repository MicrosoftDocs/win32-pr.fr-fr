---
description: La couleur est définie sous la forme d’une combinaison de trois couleurs primaires rouge, vert et bleu.
ms.assetid: 6e44935c-2b3b-4062-8273-f1f3e70300d2
title: Valeurs de couleur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67e46cd7ee87871c660702bed120958e7096745d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114694"
---
# <a name="color-values"></a><span data-ttu-id="422e5-103">Valeurs de couleur</span><span class="sxs-lookup"><span data-stu-id="422e5-103">Color Values</span></span>

<span data-ttu-id="422e5-104">La couleur est définie sous la forme d’une combinaison de trois couleurs primaires rouge, vert et bleu.</span><span class="sxs-lookup"><span data-stu-id="422e5-104">Color is defined as a combination of three primary colors red, green, and blue.</span></span> <span data-ttu-id="422e5-105">le système identifie une couleur en lui attribuant une valeur de couleur (parfois appelée triplet RVB), qui se compose de valeurs 3 8 bits spécifiant les intensités de ses composants de couleur.</span><span class="sxs-lookup"><span data-stu-id="422e5-105">the system identifies a color by giving it a color value (sometimes called an RGB triplet), which consists of three 8-bit values specifying the intensities of its color components.</span></span> <span data-ttu-id="422e5-106">Le noir présente l’intensité minimale pour le rouge, le vert et le bleu, donc la valeur de couleur pour le noir est (0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="422e5-106">Black has the minimum intensity for red, green, and blue, so the color value for black is (0, 0, 0).</span></span> <span data-ttu-id="422e5-107">Le blanc a l’intensité maximale pour le rouge, le vert et le bleu, donc sa valeur de couleur est (255, 255, 255).</span><span class="sxs-lookup"><span data-stu-id="422e5-107">White has the maximum intensity for red, green, and blue, so its color value is (255, 255, 255).</span></span>

> [!Note]  
> <span data-ttu-id="422e5-108">Si la correspondance des couleurs de l’image est activée, la définition de la couleur et la signification d’une valeur de couleur dépendent du type d’espace de couleurs actuellement défini pour le contexte de périphérique.</span><span class="sxs-lookup"><span data-stu-id="422e5-108">If image color matching is enabled, the definition of color and the meaning of a color value depends on the type of color space that is currently set for the device context.</span></span>

 

<span data-ttu-id="422e5-109">Le système et les applications utilisent des paramètres et des variables dont le type [COLORREF](colorref.md) permet de transmettre et de stocker des valeurs de couleur.</span><span class="sxs-lookup"><span data-stu-id="422e5-109">The system and applications use parameters and variables having the [COLORREF](colorref.md) type to pass and store color values.</span></span> <span data-ttu-id="422e5-110">Par exemple, la fonction [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) identifie la couleur de chaque stylet en affectant une valeur de couleur au membre **lopnColor** dans une structure [**logpen,**](/windows/win32/api/wingdi/ns-wingdi-logpen) .</span><span class="sxs-lookup"><span data-stu-id="422e5-110">For example, the [**EnumObjects**](/windows/desktop/api/Wingdi/nf-wingdi-enumobjects) function identifies the color of each pen by setting the **lopnColor** member in a [**LOGPEN**](/windows/win32/api/wingdi/ns-wingdi-logpen) structure to a color value.</span></span> <span data-ttu-id="422e5-111">Les applications peuvent extraire les valeurs individuelles des composants rouge, vert et bleu d’une valeur de couleur à l’aide des macros [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue)et [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) , respectivement.</span><span class="sxs-lookup"><span data-stu-id="422e5-111">Applications can extract the individual values of the red, green, and blue components from a color value by using the [**GetRValue**](/windows/desktop/api/Wingdi/nf-wingdi-getrvalue), [**GetGValue**](/windows/desktop/api/Wingdi/nf-wingdi-getgvalue), and [**GetBValue**](/windows/desktop/api/Wingdi/nf-wingdi-getbvalue) macros, respectively.</span></span> <span data-ttu-id="422e5-112">Les applications peuvent créer une valeur de couleur à partir de valeurs de composants individuels à l’aide de la macro [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) .</span><span class="sxs-lookup"><span data-stu-id="422e5-112">Applications can create a color value from individual component values by using the [**RGB**](/windows/desktop/api/Wingdi/nf-wingdi-rgb) macro.</span></span> <span data-ttu-id="422e5-113">Lors de la création ou de l’examen d’une palette logique, une application utilise la structure [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) pour définir les valeurs de couleur et pour examiner les valeurs des composants individuels.</span><span class="sxs-lookup"><span data-stu-id="422e5-113">When creating or examining a logical palette, an application uses the [**RGBQUAD**](/windows/win32/api/wingdi/ns-wingdi-rgbquad) structure to define color values and to examine individual component values.</span></span>

 

 



