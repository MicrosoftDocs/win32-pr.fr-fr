---
title: Séquences d’images
description: Séquences d’images
ms.assetid: fbfb944c-a927-4c92-b3d6-2f8c278408e6
keywords:
- DrawDib, séquences d’images
- DrawDib, séquence de bitmaps
- DrawDibDraw fonction)
- DrawDibBegin fonction)
- DrawDibEnd fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ac063cb2e9697b3b95045b95c9cc759a562197b56f10ff86a076ddcfa9a72cf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688790"
---
# <a name="sequences-of-images"></a>Séquences d’images

Vous pouvez afficher une séquence de bitmaps avec les mêmes dimensions et formats à l’aide de la fonction [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) avec la fonction [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) . **DrawDibBegin** améliore l’efficacité de **DrawDibDraw** en préparant le contrôleur de l’DrawDib pour le dessin.

> [!Note]  
> Si votre application n’utilise pas [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) l’exécute implicitement avant le dessin. Si votre application utilise **DrawDibBegin** avant **DrawDibDraw**, **DrawDibDraw** n’a pas besoin de traiter la fonction et d’attendre qu’elle se termine.

 

La fonction [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) fournit [**DRAWDIBDRAW**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) avec le DC drawdib, le handle DC, l’adresse de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) et les dimensions du rectangle source et de destination. Lorsque vous affichez une séquence de bitmaps, **DrawDibDraw** vérifie les valeurs de ces éléments pour chaque image de la séquence. Si **DrawDibDraw** détecte des modifications apportées à l’un de ces éléments, il appelle de nouveau **DrawDibBegin** de manière implicite pour ajuster les paramètres du contrôleur de service DrawDib.

Après avoir utilisé [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin), vous pouvez dessiner la séquence d’images à l’aide de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) et en spécifiant un ou plusieurs indicateurs en fonction de vos besoins. Spécifiez **le \_ même indicateur \_ HDC** tant que le handle de contrôleur de périphérique n’a pas changé. Spécifiez l' \_ \_ indicateur de dessin DDF, lorsque les paramètres suivants pour **DrawDibDraw** n’ont pas changé : l’adresse de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) et les dimensions du rectangle source et de destination.

Vous pouvez mettre à jour les indicateurs définis avec [**DrawDibBegin**](/windows/desktop/api/Vfw/nf-vfw-drawdibbegin) à l’aide de la fonction [**DrawDibEnd**](/windows/desktop/api/Vfw/nf-vfw-drawdibend) suivie d’un autre appel à **DrawDibBegin**. Utilisez ensuite **DrawDibEnd** pour effacer le DC DrawDib des paramètres et indicateurs actuels. L’appel suivant à **DrawDibBegin** réinitialise le contrôleur de périphérique DrawDib avec les indicateurs et paramètres appropriés. Vous pouvez également mettre à jour les indicateurs d’un contrôleur de DrawDib à l’aide de **DrawDibBegin** sans **DrawDibEnd**. Pour ce faire, vous devez modifier au moins l’un des paramètres suivants simultanément avec les indicateurs : l’adresse de la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) , ou les dimensions du rectangle source ou de destination.

Vous pouvez augmenter l’efficacité de [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) pour les opérations de streaming de données qui utilisent des images compressées, telles que la lecture d’un clip vidéo, à l’aide des fonctions [**DrawDibStart**](/windows/desktop/api/Vfw/nf-vfw-drawdibstart) et [**DrawDibStop**](/windows/desktop/api/Vfw/nf-vfw-drawdibstop) . La fonction **DrawDibStart** prépare le DC DrawDib à recevoir un flux d’images en envoyant un message au gestionnaire de compression vidéo (VCM). Une fois la diffusion en continu terminée, **DrawDibStop** envoie un message à VCM indiquant qu’il peut libérer les ressources qu’il a allouées pour l’opération de diffusion en continu des données. Pour plus d’informations sur VCM, consultez [Video Compression Manager](video-compression-manager.md).

> [!Note]  
> Vous devez spécifier la largeur et la hauteur des rectangles sources et de destination dans votre application. Toutefois, vous n’avez pas besoin de spécifier les origines des rectangles. Votre application peut redéfinir les origines dans [**DrawDibDraw**](/windows/desktop/api/Vfw/nf-vfw-drawdibdraw) pour utiliser différentes parties de l’image ou pour mettre à jour différentes parties de l’affichage.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rendu d’image](image-rendering.md)
</dt> </dl>

 

 