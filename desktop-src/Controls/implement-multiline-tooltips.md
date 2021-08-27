---
title: Comment implémenter des info-bulles multilignes
description: Les info-bulles multilignes autorisent l’affichage du texte sur plusieurs lignes.
ms.assetid: 62B10B44-C1C2-4C86-8648-AE6B606BACBB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd0d9f4172b256d2e6b72fb59ace4dc377fa3a0061e3ee0e6c0f234a74aad06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085623"
---
# <a name="how-to-implement-multiline-tooltips"></a>Comment implémenter des info-bulles multilignes

Les info-bulles multilignes autorisent l’affichage du texte sur plusieurs lignes.

Ils sont pris en charge par la [version 4,70](common-control-versions.md) et les versions ultérieures des contrôles communs. Votre application crée une info-bulle multiligne en envoyant un message [**atténuation \_ SETMAXTIPWIDTH**](ttm-setmaxtipwidth.md) , en spécifiant la largeur du rectangle d’affichage. Le texte qui dépasse cette largeur est renvoyé à la ligne suivante au lieu d’élargir la zone d’affichage. La hauteur du rectangle est augmentée autant que nécessaire pour accueillir les lignes supplémentaires. Le contrôle ToolTip encapsule les lignes automatiquement, ou vous pouvez utiliser une combinaison retour chariot/saut de ligne, \\ r \\ n, pour forcer les sauts de ligne à des emplacements particuliers.

L’illustration suivante montre l’affichage qui en résulte.

![capture d’écran d’une boîte de dialogue avec une info-bulle contenant du texte organisé comme un paragraphe à plusieurs lignes](images/tt-multiline.png)

> [!Note]  
> La mémoire tampon de texte spécifiée par le membre **szText** de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) peut contenir uniquement 80 caractères. Si vous devez utiliser une chaîne plus longue, pointez le membre **lpszText** de **NMTTDISPINFO** vers une mémoire tampon contenant le texte souhaité.

 

## <a name="what-you-need-to-know"></a>Bon à savoir

### <a name="technologies"></a>Technologies

-   [Windows Commandes](window-controls.md)

### <a name="prerequisites"></a>Prérequis

-   C/C++
-   Windows Programmation de l’interface utilisateur

## <a name="instructions"></a>Instructions

### <a name="implement-multiline-tooltips"></a>Implémenter des info-bulles multilignes

Le fragment de code suivant est un exemple de gestionnaire de notification [ \_ GETDISPINFO ttn](ttn-getdispinfo.md) simple. Il active une info-bulle multiligne en définissant le rectangle d’affichage sur 150 pixels. Un saut de ligne manuel est inséré après le premier mot pour montrer que les sauts de ligne peuvent être difficiles et souples.


```C++
    case WM_NOTIFY:
    {
        switch (((LPNMHDR)lParam)->code)
        {
        case TTN_GETDISPINFO:
            LPNMTTDISPINFO pInfo = (LPNMTTDISPINFO)lParam;
            SendMessage(pInfo->hdr.hwndFrom, TTM_SETMAXTIPWIDTH, 0, 150);
            wcscpy_s(pInfo->szText, ARRAYSIZE(pInfo->szText), 
                L"This\nis a very long text string " \
                L"that must be broken into several lines.");
            break;
        }
        break;
    }
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation des contrôles ToolTip](using-tooltip-contro.md)
</dt> </dl>

 

 




