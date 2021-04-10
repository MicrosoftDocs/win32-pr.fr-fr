---
title: Palettes
description: Palettes
ms.assetid: ee048f9a-3036-40dc-a6d7-f612b9ef767c
keywords:
- DrawDib, palettes
- DrawDibRealize fonction)
- DrawDibDraw fonction)
- DrawDibSetPalette fonction)
- DrawDibGetPalette fonction)
- DrawDibChangePalette fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5935831d8996c424a386f86082282f9cf7c1c12
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940947"
---
# <a name="palettes"></a>Palettes

Les fonctions DrawDib requièrent qu’une application réponde à deux messages orientés palette : [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) et [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged). Si votre application ne prend pas en charge la palette, vous devez ajouter un gestionnaire pour chacun de ces messages. Pour plus d’informations sur le traitement des messages **WM \_ QUERYNEWPALETTE** et **WM \_ PALETTECHANGED** , consultez [Ajout de gestionnaires de messages de palette](adding-palette-message-handlers.md).

Vous pouvez réaliser la palette DrawDib actuelle sur le contrôleur de l’objet à l’aide de la fonction [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) . Vous devez vous rendre compte de la palette en réponse au message [**WM \_ QUERYNEWPALETTE**](/windows/desktop/gdi/wm-querynewpalette) ou [**WM \_ PALETTECHANGED**](/windows/desktop/gdi/wm-palettechanged) , ou lorsque vous vous préparez à afficher une séquence d’images à l’aide de la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) .

Vous pouvez dessiner une image mappée à une autre palette à l’aide de la fonction [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) . Cette fonction force le contrôleur de DrawDib à utiliser la palette spécifiée, ce qui peut affecter la qualité de l’image. Par exemple, une application qui prend en charge la palette peut avoir réalisé une palette et doit empêcher DrawDib de réaliser sa propre palette. L’application peut utiliser **DrawDibSetPalette** pour notifier les DrawDib de la palette à utiliser.

Vous pouvez obtenir un descripteur de la palette de premier plan actuelle à l’aide de la fonction [**DrawDibGetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibgetpalette) . Si votre application utilise la palette de premier plan actuelle, elle n’utilise pas l’exclusivité de la palette et une autre application peut invalider le handle de palette. Votre application ne doit pas libérer la palette lorsque vous avez fini de l’utiliser. La libération de la palette pourrait invalider le handle de palette pour une autre application.

Vous pouvez préparer DrawDib à recevoir de nouvelles valeurs de couleur pour sa palette à l’aide de la fonction [**DrawDibChangePalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibchangepalette) . Dans le code suivant **DrawDibChangePalette**, vous affectez de nouvelles valeurs pour la table des couleurs de la palette. Si l’indicateur d' **\_ animation DDF** n’est pas défini dans le DC DrawDib quand vous appelez **DrawDibChangePalette**, vous pouvez appliquer les modifications de la palette à l’aide de [**DrawDibRealize**](/windows/desktop/api/Vfw/nf-vfw-drawdibrealize) pour réaliser la palette. Vous pouvez ensuite utiliser [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) pour redessiner l’image. Si l’indicateur d' **\_ animation DDF** est défini dans le DC DrawDib, vous pouvez animer la palette et les couleurs de la bitmap affichée à l’aide de **DrawDibDraw** ou **DrawDibRealize**. Vous pouvez mettre à jour l’indicateur d' **\_ animation DDF** à l’aide des fonctions [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) et [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) .

> [!Note]  
> Si vous libérez la palette DrawDib alors qu’elle est sélectionnée par un contrôleur de service, une erreur GDI (Graphics Device Interface) peut se produire lorsque le DC utilise la palette. Au lieu de cela, votre application doit utiliser [**DrawDibSetPalette**](/windows/desktop/api/Vfw/nf-vfw-drawdibsetpalette) pour modifier le contrôleur de périphérique DrawDib afin d’utiliser la palette par défaut ou une autre palette.

 

Les fonctions [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend), [**DrawDibClose**](/windows/desktop/api/Vfw/nf-vfw-drawdibclose)et [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) peuvent libérer la palette DrawDib. Toutefois, ces fonctions ne doivent être utilisées que lorsque la palette n’a pas été sélectionnée par le contrôleur de périphérique. La fonction DrawDibDraw peut également libérer la palette lorsqu’elle utilise le même DC DrawDib, mais spécifie différents paramètres de dessin (*lpbi*, *dxDst*, *dyDst*, *dxSrc* ou *dySrc*) ou un format différent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’image](image-rendering.md)
</dt> </dl>

 

 