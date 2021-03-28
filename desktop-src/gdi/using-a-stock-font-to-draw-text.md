---
description: Le système fournit six polices boursières.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Utilisation d’une police stock pour dessiner du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952765"
---
# <a name="using-a-stock-font-to-draw-text"></a><span data-ttu-id="75e94-103">Utilisation d’une police stock pour dessiner du texte</span><span class="sxs-lookup"><span data-stu-id="75e94-103">Using a Stock Font to Draw Text</span></span>

<span data-ttu-id="75e94-104">Le système fournit six polices boursières.</span><span class="sxs-lookup"><span data-stu-id="75e94-104">The system provides six stock fonts.</span></span> <span data-ttu-id="75e94-105">Une police stockée est une police logique qu’une application peut obtenir en appelant la fonction [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) et en spécifiant la police demandée.</span><span class="sxs-lookup"><span data-stu-id="75e94-105">A stock font is a logical font that an application can obtain by calling the [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) function and specifying the requested font.</span></span> <span data-ttu-id="75e94-106">La liste suivante contient les valeurs que vous pouvez spécifier pour obtenir une police de stock.</span><span class="sxs-lookup"><span data-stu-id="75e94-106">The following list contains the values that you can specify to obtain a stock font.</span></span>



| <span data-ttu-id="75e94-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="75e94-107">Value</span></span>                 | <span data-ttu-id="75e94-108">Signification</span><span class="sxs-lookup"><span data-stu-id="75e94-108">Meaning</span></span>                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75e94-109">\_police ANSI fixe \_</span><span class="sxs-lookup"><span data-stu-id="75e94-109">ANSI\_FIXED\_FONT</span></span>     | <span data-ttu-id="75e94-110">Spécifie une police à espacement fixe basée sur le jeu de caractères Windows.</span><span class="sxs-lookup"><span data-stu-id="75e94-110">Specifies a monospace font based on the Windows character set.</span></span> <span data-ttu-id="75e94-111">Une police courier est généralement utilisée.</span><span class="sxs-lookup"><span data-stu-id="75e94-111">A Courier font is typically used.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="75e94-112">\_police ANSI var \_</span><span class="sxs-lookup"><span data-stu-id="75e94-112">ANSI\_VAR\_FONT</span></span>       | <span data-ttu-id="75e94-113">Spécifie une police proportionnelle basée sur le jeu de caractères Windows.</span><span class="sxs-lookup"><span data-stu-id="75e94-113">Specifies a proportional font based on the Windows character set.</span></span> <span data-ttu-id="75e94-114">MS Sans Serif est généralement utilisé.</span><span class="sxs-lookup"><span data-stu-id="75e94-114">MS Sans Serif is typically used.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="75e94-115">\_police par défaut de l’appareil \_</span><span class="sxs-lookup"><span data-stu-id="75e94-115">DEVICE\_DEFAULT\_FONT</span></span> | <span data-ttu-id="75e94-116">Spécifie la police par défaut pour l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="75e94-116">Specifies the preferred font for the specified device.</span></span> <span data-ttu-id="75e94-117">Il s’agit généralement de la police système pour les périphériques d’affichage. Toutefois, pour certaines imprimantes matricielles, il s’agit d’une police qui réside sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75e94-117">This is typically the System font for display devices; however, for some dot-matrix printers this is a font that is resident on the device.</span></span> <span data-ttu-id="75e94-118">(L’impression avec cette police est généralement plus rapide que l’impression avec une police bitmap téléchargée).</span><span class="sxs-lookup"><span data-stu-id="75e94-118">(Printing with this font is usually faster than printing with a downloaded, bitmap font).</span></span>    |
| <span data-ttu-id="75e94-119">\_police OEM fixe \_</span><span class="sxs-lookup"><span data-stu-id="75e94-119">OEM\_FIXED\_FONT</span></span>      | <span data-ttu-id="75e94-120">Spécifie une police à espacement fixe basée sur un jeu de caractères OEM.</span><span class="sxs-lookup"><span data-stu-id="75e94-120">Specifies a monospace font based on an OEM character set.</span></span> <span data-ttu-id="75e94-121">Pour les ordinateurs IBM et compatibles, la police OEM est basée sur le jeu de caractères IBM PC.</span><span class="sxs-lookup"><span data-stu-id="75e94-121">For IBM computers and compatibles, the OEM font is based on the IBM PC character set.</span></span>                                                                                                                                                 |
| <span data-ttu-id="75e94-122">\_police système</span><span class="sxs-lookup"><span data-stu-id="75e94-122">SYSTEM\_FONT</span></span>          | <span data-ttu-id="75e94-123">Spécifie la police système.</span><span class="sxs-lookup"><span data-stu-id="75e94-123">Specifies the System font.</span></span> <span data-ttu-id="75e94-124">Il s’agit d’une police proportionnelle basée sur le jeu de caractères Windows. elle est utilisée par le système d’exploitation pour afficher des titres de fenêtre, des noms de menu et du texte dans les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="75e94-124">This is a proportional font based on the Windows character set, and is used by the operating system to display window titles, menu names, and text in dialog boxes.</span></span> <span data-ttu-id="75e94-125">La police système est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="75e94-125">The System font is always available.</span></span> <span data-ttu-id="75e94-126">D’autres polices ne sont disponibles que si elles ont été installées.</span><span class="sxs-lookup"><span data-stu-id="75e94-126">Other fonts are available only if they have been installed.</span></span> |
| <span data-ttu-id="75e94-127">\_police système fixe \_</span><span class="sxs-lookup"><span data-stu-id="75e94-127">SYSTEM\_FIXED\_FONT</span></span>   | <span data-ttu-id="75e94-128">Spécifie une police à espacement fixe compatible avec la police système dans les versions antérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="75e94-128">Specifies a monospace font compatible with the System font in early versions of Windows.</span></span>                                                                                                                                                                                                        |



 

<span data-ttu-id="75e94-129">Pour plus d’informations sur les polices, consultez [à propos des polices](about-fonts.md).</span><span class="sxs-lookup"><span data-stu-id="75e94-129">For more information on fonts, see [About Fonts](about-fonts.md).</span></span>

<span data-ttu-id="75e94-130">L’exemple suivant récupère un handle vers la police stock variable, le sélectionne dans un contexte de périphérique, puis écrit une chaîne à l’aide de la police suivante :</span><span class="sxs-lookup"><span data-stu-id="75e94-130">The following example retrieves a handle to the variable stock font, selects it into a device context, and then writes a string using that font:</span></span>


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



<span data-ttu-id="75e94-131">Si d’autres polices stock ne sont pas disponibles, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) retourne un handle à la police système ( \_ police système).</span><span class="sxs-lookup"><span data-stu-id="75e94-131">If other stock fonts are not available, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) returns a handle to the System font (SYSTEM\_FONT).</span></span> <span data-ttu-id="75e94-132">Vous devez utiliser des polices stock uniquement si le mode de mappage du contexte de périphérique de votre application est de MM de \_ texte.</span><span class="sxs-lookup"><span data-stu-id="75e94-132">You should use stock fonts only if the mapping mode for your application's device context is MM\_TEXT.</span></span>

 

 



