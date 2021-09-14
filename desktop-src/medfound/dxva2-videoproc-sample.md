---
description: Montre comment utiliser le traitement vidéo DXVA.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: Exemple de DXVA2_VideoProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8fc4be1bad6a3955af255cb083a4595ecedfd30
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127220881"
---
# <a name="dxva2_videoproc-sample"></a>\_Exemple DXVA2 VideoProc

Montre comment utiliser le [traitement vidéo DXVA](dxva-video-processing.md).

Cet exemple génère par programmation une vidéo avec un flux principal et un sous-flux. Le flux principal affiche des barres de couleur SMPTE et le sous-flux est un rectangle semi-transparent. La vidéo est ensuite traitée et affichée à l’aide d’un processeur vidéo DXVA. L’utilisateur peut modifier les valeurs alpha planaires, les rectangles source et de destination, les réglages de couleur et l’espace colorimétrique.

![capture d’écran de l' \- exemple dxva2 videoproc](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces DXVA suivantes :

-   [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a>Usage

l' \_ exemple DXVA2 VideoProc génère une application Windows.

Options de ligne de commande :



| Option | Description                                                                          |
|--------|--------------------------------------------------------------------------------------|
| -hh    | Force l’application à utiliser un périphérique Direct3D matériel et un périphérique DXVA matériel. |
| -HS    | Force l’application à utiliser un périphérique Direct3D matériel et un périphérique DXVA logiciel. |
| -ss    | Force l’application à utiliser un périphérique Direct3D logiciel et un périphérique DXVA logiciel. |



 

Commandes du clavier :



| Clé       | Description                                             |
|-----------|---------------------------------------------------------|
| Alt+Entrée | Basculer entre le mode fenêtre et le mode plein écran.      |
| F1-F8     | Entrez l’un des modes répertoriés dans le tableau suivant.    |
| FIN       | Activez ou désactivez la journalisation du débogage des frames supprimés. |
| Origine      | Réinitialisation d’un paramètre à sa valeur initiale.                 |



 

Chacune des touches de fonction F1 à F8 bascule vers un mode dans lequel les touches de direction peuvent être utilisées pour ajuster un paramètre de rendu particulier. En outre, la couleur du sous-flux change.




| Clé | Description | 
|-----|-------------|
| F1 | Ajustez les valeurs alpha.<br /><ul><li>HAUT : Augmentez l’alpha planaire des deux flux.</li><li>Baisse : diminuez l’alpha planaire des deux flux.</li><li>RIGHT : augmentez le pixel alpha du sous-flux.</li><li>GAUCHE : diminuez le pixel alpha du sous-flux.</li></ul>Couleur de sous-flux : blanc<br /> | 
| F2 | Ajustez la zone source du flux principal (zoom).<br /><ul><li>HAUT : augmentez verticalement (zoom avant).</li><li>VERS le dessous : diminue verticalement (zoom arrière).</li><li>RIGHT : augmenter horizontalement (zoom avant).</li><li>GAUCHE : diminue horizontalement (zoom arrière).</li></ul>Couleur de sous-flux : rouge<br /> | 
| F3 | Déplacez la zone source du flux principal.<br /><ul><li>HAUT : vers le haut.</li><li>Descendre : descendre.</li><li>RIGHT : déplacer vers la droite.</li><li>GAUCHE : déplacer vers la gauche.</li></ul>Couleur de sous-flux : jaune<br /> | 
| F4 | Ajustez la zone de destination du flux principal.<br /><ul><li>HAUT : augmente verticalement.</li><li>VERS le dessous : diminue verticalement.</li><li>RIGHT : augmenter horizontalement.</li><li>GAUCHE : diminue horizontalement.</li></ul>Couleur de sous-flux : vert<br /> | 
| F5 | Déplacez la zone de destination du flux principal.<br /><ul><li>HAUT : vers le haut.</li><li>Descendre : descendre.</li><li>RIGHT : déplacer vers la droite.</li><li>GAUCHE : déplacer vers la gauche.</li></ul>Couleur de sous-flux : cyan<br /> | 
| F6 | Modifiez l’espace colorimétrique ou couleur d’arrière-plan.<br /><ul><li>Haut, vers le haut : parcourir les espaces de couleurs.</li><li>DROITE, gauche : parcourir les couleurs d’arrière-plan.</li></ul>Couleur de sous-flux : bleue<br /> | 
| F7 | Ajustez la luminosité et le contraste.<br /><ul><li>HAUT : augmentez la luminosité.</li><li>Baisse : réduire la luminosité.</li><li>RIGHT : augmenter le contraste.</li><li>GAUCHE : diminuer le contraste.</li></ul>Couleur de sous-flux : magenta<br /> | 
| F8 | Ajustez la teinte et la saturation.<br /><ul><li>HAUT : augmentez la teinte.</li><li>Baisse : diminuer la teinte.</li><li>RIGHT : augmenter la saturation.</li><li>GAUCHE : diminuer la saturation.</li></ul>Couleur de sous-flux : noir<br /> | 




 

Dans chaque mode, l’appui sur la touche origine rétablit les valeurs initiales des paramètres de ce mode.

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Accélération vidéo DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Traitement vidéo DXVA](dxva-video-processing.md)
</dt> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




