---
description: Utilisation des contrôles d’affichage vidéo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Utilisation des contrôles d’affichage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313666"
---
# <a name="using-the-video-display-controls"></a>Utilisation des contrôles d’affichage vidéo

L’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) contrôle la manière dont le convertisseur vidéo amélioré (EVR) affiche la vidéo à l’intérieur d’une fenêtre d’application. cette interface peut être utilisée dans DirectShow ou Media Foundation. En interne, les contrôles d’affichage vidéo sont fournis par le présentateur par défaut de EVR. Si vous écrivez un présentateur personnalisé, vous pouvez fournir la même interface ou définir une interface personnalisée.

la méthode correcte pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) varie selon que vous utilisez la version DirectShow du EVR ou la version Media Foundation. Pour le Media Foundation EVR, cela dépend également de l’utilisation directe du EVR ou de son utilisation par le biais de la session multimédia (qui est plus courante).

Pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , procédez comme suit :

1.  Obtient un pointeur vers l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .

    -   si vous utilisez le filtre DirectShow EVR, appelez **QueryInterface** sur le filtre.

    -   Si vous utilisez directement le récepteur multimédia EVR, appelez **QueryInterface** sur le récepteur multimédia.

    -   Si vous utilisez la session multimédia, appelez **QueryInterface** sur la session multimédia.

2.  Si vous utilisez la session de média, attendez que la session multimédia envoie l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec la valeur d’État MF \_ TOPOSTATUS \_ Ready. (Ignorez cette étape dans le cas contraire).

3.  Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour accéder à l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . L’identificateur de service est un \_ service de rendu vidéo Mr \_ \_ .

Vous pouvez utiliser l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pour effectuer les tâches suivantes :

-   Définissez la fenêtre de découpage.

-   Définissez les rectangles source et de destination.

-   Mettez à jour la fenêtre vidéo en réponse aux messages de fenêtre.

-   Activer ou désactiver le mode plein écran.

## <a name="clipping-window"></a>Fenêtre de découpage

L’application doit fournir une fenêtre dans laquelle le EVR dessine la vidéo. Pour définir la fenêtre de découpage, appelez [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) avec un handle vers la fenêtre d’application.

Si vous créez le récepteur multimédia EVR par le biais de son objet d’activation, cette étape n’est pas nécessaire. L’objet d’activation appelle automatiquement [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)à l’aide du handle de fenêtre que vous avez fourni dans la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .

## <a name="source-and-destination-rectangles"></a>Rectangles de source et de destination

Pendant la lecture, le présentateur prend une partie de l’image vidéo composite et la dessine dans une zone de la fenêtre vidéo. La partie de l’image composite est le *rectangle source*, tandis que la zone de la fenêtre vidéo est le *rectangle de destination*.

Le rectangle source est défini à l’aide de coordonnées normalisées où le point (0,0, 0,0) correspond à l’angle supérieur gauche de la vidéo, et (1,0, 1,0) correspond au coin inférieur droit de la vidéo. Le rectangle source peut être n’importe quelle région dans ce rectangle. Le rectangle de destination est spécifié en pixels, par rapport à la zone cliente de la fenêtre. Le rectangle source par défaut est la totalité de l’image, et le rectangle de destination par défaut est un rectangle vide.

Pour définir les rectangles source et de destination, appelez [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Si vous créez le récepteur multimédia EVR par le biais de son objet d’activation, cette étape n’est pas nécessaire. L’objet d’activation définit automatiquement le rectangle de destination comme étant la totalité de la zone cliente de la fenêtre. Toutefois, vous devez appeler [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) si vous souhaitez modifier le rectangle source ou définir un autre rectangle de destination.

## <a name="window-messages"></a>Messages de fenêtre

Pendant la lecture, votre application doit répondre à certains messages de fenêtre, comme suit :

-   WM \_ Paint : appelez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) pour repeindre la vidéo. Évitez également de peindre sur le rectangle de destination pendant que la vidéo est lue, car cela peut provoquer un scintillement.

-   \_Taille du WM : vous devrez peut-être appeler [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) pour redimensionner le rectangle de destination.

contrairement au filtre de convertisseur de mixage vidéo (VMR) dans DirectShow, il n’est pas nécessaire d’avertir le EVR quand vous recevez un \_ message DISPLAYCHANGE WM.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 



