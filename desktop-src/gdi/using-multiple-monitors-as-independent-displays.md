---
description: Lorsque vous utilisez plusieurs écrans comme des affichages indépendants, le bureau contient un affichage ou un ensemble d’affichages.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Utilisation de plusieurs moniteurs comme affichages indépendants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973626"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="0cc30-103">Utilisation de plusieurs moniteurs comme affichages indépendants</span><span class="sxs-lookup"><span data-stu-id="0cc30-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="0cc30-104">Lorsque vous utilisez plusieurs écrans comme des affichages indépendants, le bureau contient un affichage ou un ensemble d’affichages.</span><span class="sxs-lookup"><span data-stu-id="0cc30-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="0cc30-105">Cet ensemble d’affichages comprend toujours l’analyse principale et se comporte comme indiqué dans les autres sections de cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="0cc30-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="0cc30-106">Une application peut utiliser n’importe quelle autre analyse comme un affichage indépendant.</span><span class="sxs-lookup"><span data-stu-id="0cc30-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="0cc30-107">L’utilisation d’autres moniteurs comme des affichages indépendants n’est pas prise en charge sur les pilotes qui sont implémentés sur le modèle WDDM (Windows Display Driver Model).</span><span class="sxs-lookup"><span data-stu-id="0cc30-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="0cc30-108">Le gestionnaire de fenêtres ne sait rien des affichages indépendants.</span><span class="sxs-lookup"><span data-stu-id="0cc30-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="0cc30-109">Ils sont entièrement contrôlés par l’application et aucune fonction du gestionnaire de fenêtrage n’est disponible pour l’application (tous les appels du gestionnaire de fenêtres passent automatiquement à l’affichage principal).</span><span class="sxs-lookup"><span data-stu-id="0cc30-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="0cc30-110">Chaque affichage indépendant a sa propre origine et ses coordonnées horizontales et verticales, et est accessible via les fonctions GDI telles que [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) ou les fonctions DirectX telles que **DirectDrawCreate**.</span><span class="sxs-lookup"><span data-stu-id="0cc30-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="0cc30-111">Pour localiser les affichages indépendants, appelez [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) et recherchez les affichages qui n’ont pas de \_ périphérique d’affichage \_ attaché \_ à \_ l’indicateur de bureau dans la structure du [**\_ périphérique d’affichage**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="0cc30-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="0cc30-112">Une application peut ouvrir un affichage en appelant</span><span class="sxs-lookup"><span data-stu-id="0cc30-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="0cc30-113">Dans cet appel, le paramètre *lpszDisplayName* est l’un des noms d’appareil retournés par [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) et *lpDevMode* est une description du mode graphique de cet appareil.</span><span class="sxs-lookup"><span data-stu-id="0cc30-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="0cc30-114">Le HDC qui en résulte peut être utilisé pour effectuer une opération graphique sur l’appareil.</span><span class="sxs-lookup"><span data-stu-id="0cc30-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



