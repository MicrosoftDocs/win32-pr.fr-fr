---
description: Un contexte de périphérique de fenêtre permet à une application de dessiner n’importe où dans une fenêtre, y compris la zone non cliente.
ms.assetid: 7b3c6352-51d5-4fdf-82c2-7a28194f607f
title: Fenêtre Affichage des contextes de périphérique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfed34646323114ffcfb7753331b1b5c305a7a0c01a475795a7918f6e5a2dd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965089"
---
# <a name="window-display-device-contexts"></a>Fenêtre Affichage des contextes de périphérique

Un *contexte de périphérique de fenêtre* permet à une application de dessiner n’importe où dans une fenêtre, y compris la zone non cliente. Les contextes de périphérique Windows sont généralement utilisés par les applications qui traitent les messages [**WM \_ NCPAINT**](wm-ncpaint.md) et [**WM \_ NCACTIVATE**](../winmsg/wm-ncactivate.md) pour Windows avec des zones non clientes personnalisées. L’utilisation d’un contexte de périphérique Windows n’est pas recommandée à d’autres fins.

Une application peut récupérer un contexte de périphérique Windows à l’aide de la fonction [**GetWindowDC**](/windows/desktop/api/Winuser/nf-winuser-getwindowdc) ou [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) avec l' \_ option de fenêtre DCX spécifiée. La fonction récupère un contexte de périphérique Windows à partir du cache du contexte de périphérique d’affichage. Une fenêtre qui utilise un contexte de périphérique Windows doit le libérer après avoir dessiné à l’aide de la fonction [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) dès que possible. Les contextes de périphérique Windows proviennent toujours du cache ; les \_ styles de classe CS OWNDC et CS \_ CLASSDC n’affectent pas le contexte de périphérique.

Quand une application récupère un contexte de périphérique Windows, le système définit l’origine de l’appareil dans l’angle supérieur gauche de la fenêtre au lieu de l’angle supérieur gauche de la zone cliente. Il définit également la zone de découpage pour inclure la fenêtre entière, pas seulement la zone cliente. Le système définit les valeurs d’attribut actuelles d’un contexte de périphérique Windows avec les mêmes valeurs par défaut qu’un contexte de périphérique courant. Une application peut modifier les valeurs d’attribut, mais le système ne conserve pas les modifications apportées lors de la libération du contexte de périphérique.

 

 
