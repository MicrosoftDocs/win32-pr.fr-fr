---
description: La fonction GetSystemMetrics retourne des valeurs pour le moniteur principal, à l’exception de SM \_ CXMAXTRACK et SM \_ CYMAXTRACK, qui font référence à l’ensemble du bureau.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Métriques système à plusieurs moniteurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114639"
---
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="89d66-103">Métriques système à plusieurs moniteurs</span><span class="sxs-lookup"><span data-stu-id="89d66-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="89d66-104">La fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retourne des valeurs pour le moniteur principal, à l’exception de SM \_ CXMAXTRACK et SM \_ CYMAXTRACK, qui font référence à l’ensemble du bureau.</span><span class="sxs-lookup"><span data-stu-id="89d66-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="89d66-105">Les métriques suivantes sont identiques pour tous les pilotes de périphérique : SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON.</span><span class="sxs-lookup"><span data-stu-id="89d66-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="89d66-106">Les fonctionnalités d’affichage suivantes sont identiques pour toutes les analyses : LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span><span class="sxs-lookup"><span data-stu-id="89d66-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="89d66-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) a également des constantes qui font uniquement référence à un système à plusieurs écrans.</span><span class="sxs-lookup"><span data-stu-id="89d66-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="89d66-108">SM \_ XVIRTUALSCREEN et SM \_ YVIRTUALSCREEN identifient l’angle supérieur gauche de l’écran virtuel, les \_ CYVIRTUALSCREEN SM CXVIRTUALSCREEN et SM \_ sont les mesures verticale et horizontale de l’écran virtuel, le SM \_ CMONITORS est le nombre d’écrans reliés au bureau et \_ le SM SAMEDISPLAYFORMAT indique si tous les moniteurs du Bureau ont le même format de couleur.</span><span class="sxs-lookup"><span data-stu-id="89d66-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="89d66-109">Pour obtenir des informations sur un moniteur d’affichage unique ou sur tous les moniteurs d’affichage d’un ordinateur de bureau, utilisez EnumDisplayMonitors.</span><span class="sxs-lookup"><span data-stu-id="89d66-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="89d66-110">Le rectangle de la fenêtre du Bureau retourné par [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) ou [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) est toujours égal au rectangle de l’analyse principale, pour la compatibilité avec les applications existantes.</span><span class="sxs-lookup"><span data-stu-id="89d66-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="89d66-111">Ainsi, le résultat de</span><span class="sxs-lookup"><span data-stu-id="89d66-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="89d66-112">sera :</span><span class="sxs-lookup"><span data-stu-id="89d66-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="89d66-113">Pour modifier la zone de travail d’une analyse, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ SETWORKAREA et *pvParam* pointant vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) située sur le moniteur souhaité.</span><span class="sxs-lookup"><span data-stu-id="89d66-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="89d66-114">Si *pvParam* a la **valeur null**, la zone de travail de l’analyse principale est modifiée.</span><span class="sxs-lookup"><span data-stu-id="89d66-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="89d66-115">L’utilisation \_ de SPI GETWORKAREA retourne toujours la zone de travail de l’analyse principale.</span><span class="sxs-lookup"><span data-stu-id="89d66-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="89d66-116">Pour obtenir la zone de travail d’une analyse autre que l’écran principal, appelez [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="89d66-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
