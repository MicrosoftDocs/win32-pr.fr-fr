---
description: Dessiner du texte
ms.assetid: 8a06f659-4e08-4738-b7a9-956b599c1344
title: texte de dessin (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52508e5a0825a3f43a62f5cce7905a767513f007555eb430c26dbc2d914f372
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062269"
---
# <a name="drawing-text-windows-gdi"></a>texte de dessin (Windows GDI)

Une fois qu’une application a sélectionné la police appropriée, définit les options de mise en forme de texte requises et calcule les valeurs de largeur et de hauteur de caractère nécessaires pour une chaîne de texte, elle peut commencer à dessiner des caractères et des symboles en appelant l’une des fonctions de sortie de texte :

-   [DrawText](/windows/desktop/api/Winuser/nf-winuser-drawtext)
-   [DrawTextEx](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)
-   [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)
-   [PolyTextOut](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)
-   [TabbedTextOut](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)
-   [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta)

Quand une application appelle l’une de ces fonctions, le système d’exploitation passe l’appel au moteur Graphics, qui à son tour passe l’appel au pilote de périphérique approprié. Au niveau du pilote de périphérique, tous ces appels sont pris en charge par un ou plusieurs appels à la fonction [ExtTextOut](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta) ou [TextOut](/windows/desktop/api/Wingdi/nf-wingdi-textouta) du pilote. Une application effectue l’exécution la plus rapide en appelant [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta), qui est rapidement converti en appel **ExtTextOut** pour l’appareil. Toutefois, il existe des instances lorsqu’une application doit appeler l’une des trois autres fonctions ; par exemple, pour dessiner plusieurs lignes de texte dans les bordures d’une zone rectangulaire spécifiée, il est plus efficace d’appeler [**DrawText**](/windows/win32/api/winuser/nf-winuser-drawtext). Pour créer une table multicolonne avec des colonnes de texte justifiées, il est plus efficace d’appeler [**TabbedTextOut**](/windows/win32/api/winuser/nf-winuser-tabbedtextouta).

 

 
