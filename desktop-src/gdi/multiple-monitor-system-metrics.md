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
# <a name="multiple-monitor-system-metrics"></a>Métriques système à plusieurs moniteurs

La fonction [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) retourne des valeurs pour le moniteur principal, à l’exception de SM \_ CXMAXTRACK et SM \_ CYMAXTRACK, qui font référence à l’ensemble du bureau. Les métriques suivantes sont identiques pour tous les pilotes de périphérique : SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Les fonctionnalités d’affichage suivantes sont identiques pour toutes les analyses : LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) a également des constantes qui font uniquement référence à un système à plusieurs écrans. SM \_ XVIRTUALSCREEN et SM \_ YVIRTUALSCREEN identifient l’angle supérieur gauche de l’écran virtuel, les \_ CYVIRTUALSCREEN SM CXVIRTUALSCREEN et SM \_ sont les mesures verticale et horizontale de l’écran virtuel, le SM \_ CMONITORS est le nombre d’écrans reliés au bureau et \_ le SM SAMEDISPLAYFORMAT indique si tous les moniteurs du Bureau ont le même format de couleur.

Pour obtenir des informations sur un moniteur d’affichage unique ou sur tous les moniteurs d’affichage d’un ordinateur de bureau, utilisez EnumDisplayMonitors. Le rectangle de la fenêtre du Bureau retourné par [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) ou [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) est toujours égal au rectangle de l’analyse principale, pour la compatibilité avec les applications existantes. Ainsi, le résultat de


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



sera :


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Pour modifier la zone de travail d’une analyse, appelez [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) avec SPI \_ SETWORKAREA et *pvParam* pointant vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) située sur le moniteur souhaité. Si *pvParam* a la **valeur null**, la zone de travail de l’analyse principale est modifiée. L’utilisation \_ de SPI GETWORKAREA retourne toujours la zone de travail de l’analyse principale. Pour obtenir la zone de travail d’une analyse autre que l’écran principal, appelez [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
