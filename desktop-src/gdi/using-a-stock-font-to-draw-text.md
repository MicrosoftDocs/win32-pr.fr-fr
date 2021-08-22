---
description: Le système fournit six polices boursières.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Utilisation d’une police stock pour dessiner du texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468329"
---
# <a name="using-a-stock-font-to-draw-text"></a>Utilisation d’une police stock pour dessiner du texte

Le système fournit six polices boursières. Une police stockée est une police logique qu’une application peut obtenir en appelant la fonction [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) et en spécifiant la police demandée. La liste suivante contient les valeurs que vous pouvez spécifier pour obtenir une police de stock.



| Valeur                 | Signification                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_police ANSI fixe \_     | spécifie une police à espacement fixe basée sur le jeu de caractères Windows. Une police courier est généralement utilisée.                                                                                                                                                                                                |
| \_police ANSI var \_       | spécifie une police proportionnelle basée sur le jeu de caractères Windows. MS Sans Serif est généralement utilisé.                                                                                                                                                                                              |
| \_police par défaut de l’appareil \_ | Spécifie la police par défaut pour l’appareil spécifié. Il s’agit généralement de la police système pour les périphériques d’affichage. Toutefois, pour certaines imprimantes matricielles, il s’agit d’une police qui réside sur l’appareil. (L’impression avec cette police est généralement plus rapide que l’impression avec une police bitmap téléchargée).    |
| \_police OEM fixe \_      | Spécifie une police à espacement fixe basée sur un jeu de caractères OEM. Pour les ordinateurs IBM et compatibles, la police OEM est basée sur le jeu de caractères IBM PC.                                                                                                                                                 |
| \_police système          | Spécifie la police système. il s’agit d’une police proportionnelle basée sur le jeu de caractères Windows, qui est utilisée par le système d’exploitation pour afficher des titres de fenêtre, des noms de menu et du texte dans les boîtes de dialogue. La police système est toujours disponible. D’autres polices ne sont disponibles que si elles ont été installées. |
| \_police système fixe \_   | Spécifie une police à espacement fixe compatible avec la police système dans les versions antérieures de Windows.                                                                                                                                                                                                        |



 

Pour plus d’informations sur les polices, consultez [à propos des polices](about-fonts.md).

L’exemple suivant récupère un handle vers la police stock variable, le sélectionne dans un contexte de périphérique, puis écrit une chaîne à l’aide de la police suivante :


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



Si d’autres polices stock ne sont pas disponibles, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) retourne un handle à la police système ( \_ police système). Vous devez utiliser des polices stock uniquement si le mode de mappage du contexte de périphérique de votre application est de MM de \_ texte.

 

 



