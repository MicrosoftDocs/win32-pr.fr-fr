---
description: Chaque affichage physique est représenté par un handle de moniteur de type HMONITOR.
ms.assetid: c43c1401-52d3-485e-a418-205df5737040
title: HMONITOR et le contexte de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afb727457c388710b19d8f22bef8f65d76e9d8c5c27b0ec7dfcbf55a4acea3b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119558749"
---
# <a name="hmonitor-and-the-device-context"></a>HMONITOR et le contexte de périphérique

Chaque affichage physique est représenté par un handle de moniteur de type **HMONITOR**. Un **HMONITOR** valide est garanti être non null. Un affichage physique a le même **HMONITOR** , à condition qu’il fasse partie du bureau. Lorsqu’un message **WM \_ DISPLAYCHANGE** est envoyé, toute analyse peut être supprimée du bureau et son **HMONITOR** devient non valide ou ses paramètres sont modifiés. Par conséquent, une application doit vérifier si tous les **HMONITORS** sont valides lorsque ce message est envoyé.

Toute fonction qui retourne un contexte de périphérique d’affichage (DC) retourne normalement un contrôleur de l’écran principal. Pour obtenir le contrôleur de l’autre moniteur, utilisez la fonction [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors) . Vous pouvez utiliser le nom de l’appareil à partir de la fonction [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) pour créer un contrôleur de périphérique avec [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca). Toutefois, si la fonction, telle que [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), obtient un DC pour une fenêtre qui s’étend sur plusieurs affichages, le contrôleur de périphérique s’étend également sur les deux affichages.

 

 



