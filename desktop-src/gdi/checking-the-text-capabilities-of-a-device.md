---
description: Vous pouvez utiliser les fonctions EnumFonts et EnumFontFamilies pour énumérer les polices disponibles dans un contexte de périphérique de mémoire compatible avec l’imprimante.
ms.assetid: d68de203-2d5f-4a28-bb57-1dda9fcb078a
title: Vérification des fonctionnalités de texte d’un appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fd1a4ddc0c678c775c6c068216e60ead234d757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991273"
---
# <a name="checking-the-text-capabilities-of-a-device"></a><span data-ttu-id="110f0-103">Vérification des fonctionnalités de texte d’un appareil</span><span class="sxs-lookup"><span data-stu-id="110f0-103">Checking the Text Capabilities of a Device</span></span>

<span data-ttu-id="110f0-104">Vous pouvez utiliser les fonctions [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) et [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) pour énumérer les polices disponibles dans un contexte de périphérique de mémoire compatible avec l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="110f0-104">You can use the [EnumFonts](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa) and [EnumFontFamilies](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa) functions to enumerate the fonts that are available in a printer-compatible memory device context.</span></span> <span data-ttu-id="110f0-105">Vous pouvez également utiliser la fonction [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) pour récupérer des informations sur les fonctionnalités de texte d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="110f0-105">You can also use the [GetDeviceCaps](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) function to retrieve information about the text capabilities of a device.</span></span> <span data-ttu-id="110f0-106">En appelant la fonction [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) avec l’index NUMFONTS, vous pouvez déterminer le nombre minimal de polices prises en charge par une imprimante.</span><span class="sxs-lookup"><span data-stu-id="110f0-106">By calling the [**GetDeviceCaps**](/windows/win32/api/wingdi/nf-wingdi-getdevicecaps) function with the NUMFONTS index, you can determine the minimum number of fonts supported by a printer.</span></span> <span data-ttu-id="110f0-107">(Une imprimante peut prendre en charge plus de polices que ce qui est spécifié dans la valeur de retour de **GetDeviceCaps** avec l’index NUMFONTS.) À l’aide de l’index TEXTCAPS, vous pouvez identifier la plupart des fonctionnalités de texte de l’appareil spécifié.</span><span class="sxs-lookup"><span data-stu-id="110f0-107">(An individual printer may support more fonts than specified in the return value from **GetDeviceCaps** with the NUMFONTS index.) By using the TEXTCAPS index, you can identify many of the text capabilities of the specified device.</span></span>

 

 
