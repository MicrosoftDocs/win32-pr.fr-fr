---
description: Mélangeurs personnalisés
ms.assetid: a0af318d-9ac2-43f9-8934-f28c472256a6
title: Mélangeurs personnalisés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac7e56c578a7081de7c71ae3abaf9fc45d085827
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519241"
---
# <a name="custom-mixers"></a>Mélangeurs personnalisés

Cette rubrique explique comment écrire un mélangeur personnalisé pour le convertisseur vidéo amélioré (EVR). Vous pouvez utiliser un mélangeur personnalisé avec le Media Foundation récepteur de média EVR ou le filtre EVR DirectShow. Pour plus d’informations sur les mélangeurs et les présentateurs, consultez [amélioration du rendu vidéo](enhanced-video-renderer.md).

Le mélangeur est une transformation de Media Foundation (MFT) avec une ou plusieurs entrées (le flux de référence et les sous-flux) et une sortie. Le flux d’entrée reçoit des exemples de en amont. Le flux de sortie remet des exemples au présentateur. Le EVR est chargé d’appeler [**IMFTransform ::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) sur le mélangeur, et le présenteur est chargé d’appeler [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).

Au minimum, un mélangeur EVR doit implémenter les interfaces suivantes :



| Interface                                                                | Description                                                                                      |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)                                     | Fournit la fonctionnalité MFT de base.                                                                 |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permet au mélangeur d’extraire des interfaces à partir du EVR.                                                |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Permet au mélangeur d’extraire des interfaces à partir du EVR.                                                |
| [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)                                   | Utilisé pour exposer l’attribut prenant en charge la prise en [**\_ \_ \_ charge Direct3D MF**](mf-sa-d3d-aware-attribute.md) à EVR. |



 

Éventuellement, une table MFT peut implémenter l’une des interfaces suivantes :



| Interface                                                | Description                                                                                                                                          |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Requis pour lire du contenu protégé.                                                                                                                  |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                   | Expose des interfaces telles que [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) et [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) à l’application. |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)             | Permet au gestionnaire de qualité d’ajuster la qualité vidéo.                                                                                             |
| [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)       | Permet à l’application de mélanger une image bitmap statique sur la vidéo.                                                                                       |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mappe les coordonnées sur l’image vidéo de sortie à des coordonnées sur l’image vidéo d’entrée.                                                                  |
| [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)           | Expose certaines fonctionnalités de traitement vidéo DXVA à l’application.                                                                                      |



 

La négociation de format avec le mélangeur fonctionne comme suit :

1.  EVR définit le type de média sur le flux de référence.
2.  EVR appelle [**IMFVideoPresenter ::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) sur le présenteur avec le message **MFVP \_ \_ INVALIDATEMEDIATYPE** .

3.  Le présentateur définit le type de média sur le flux de sortie de la console.
4.  EVR définit le type de média sur les sous-flux.

Si le type de média sur le flux de référence change, les autres types de supports de la console de mixage ne sont plus valides. La méthode [**IMFTransform ::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) du mélangeur échoue et retourne la **\_ modification du \_ \_ flux \_ de transformation MF E**. Le présenteur ne doit rien faire à ce stade. Le EVR lancera à nouveau le processus de négociation de format.

Quand un flux d’entrée atteint la fin du flux, EVR appelle [**IMFTransform ::P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage) sur le mixer avec la [**\_ \_ fin de la notification de message MFT \_ de la fin \_ du \_ flux**](mft-message-notify-end-of-stream.md).

Le mélangeur envoie les événements suivants au EVR à l’aide de l’interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) du EVR. Cette interface est documentée dans la documentation du kit de développement logiciel (SDK) DirectShow.



| Événement                                            | Description                            |
|--------------------------------------------------|----------------------------------------|
| [**\_exemple EC \_ requis**](../directshow/ec-sample-needed.md) | Le mélangeur requiert un nouvel exemple d’entrée. |



 

Le EVR peut appeler [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) sur le mélangeur avant le démarrage de la diffusion en continu. Le mélangeur ne doit pas faire échouer ces appels. Au lieu de cela, elle doit remplir la surface de sortie avec des pixels noirs. Le mélangeur doit continuer à remplir les échantillons de sortie en couleur jusqu’à ce qu’il reçoive un message de la [**diffusion en \_ \_ \_ \_ continu de la notification par message MFT**](mft-message-notify-begin-streaming.md) ou que la méthode [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) soit appelée. Si la console de mixage reçoit un message de [**\_ fin de \_ \_ \_ diffusion de message MFT**](mft-message-notify-end-streaming.md) , elle doit revenir en mode de remplissage des couleurs.

## <a name="implementing-imfvideodeviceid"></a>Implémentation de IMFVideoDeviceID

L’interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contient une méthode, [**GetDeviceID**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid), qui retourne un GUID de périphérique. Le GUID de l’appareil garantit que le présentateur et le mélangeur utilisent des technologies compatibles. Si les GUID d’appareil ne correspondent pas, l’initialisation du EVR échoue.

Le mélangeur et le présentateur standard utilisent Direct3D 9, avec le GUID d’appareil égal à IID \_ IDirect3DDevice9. Si vous envisagez d’utiliser votre présentateur personnalisé avec le mélangeur standard, le GUID de l’appareil du présentateur doit être IID \_ IDirect3DDevice9. Si vous remplacez les deux composants, vous pouvez définir un nouveau GUID d’appareil.

## <a name="implementing-imftopologyservicelookupclient"></a>Implémentation de IMFTopologyServiceLookupClient

Le mixer doit implémenter l’interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) . Avant le début de la diffusion en continu, EVR appelle [**IMFTopologyServiceLookupClient :: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) et transmet un pointeur vers l’interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) du EVR. Le mélangeur utilise ce pointeur pour récupérer les pointeurs d’interface à partir de EVR.

Au minimum, le mélangeur doit interroger l’interface suivante :

-   [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink)

Quand EVR appelle [**IMFTopologyServiceLookupClient :: ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers), le mixer doit libérer tous les pointeurs obtenus à partir de l’appel à [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers).

## <a name="mixer-attributes"></a>Attributs du mélangeur

Un mélangeur doit prendre en charge les attributs suivants.



| Attribut                                                                        | Description                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Compatible avec la prise en \_ \_ charge Direct3D MF \_**](mf-sa-d3d-aware-attribute.md)                          | Spécifie si le mélangeur prend en charge l’accélération vidéo DirectX (DXVA).                                                                                                                                                                               |
| [**\_nombre d' \_ \_ échantillons requis As MF \_**](mf-sa-required-sample-count-attribute.md) | Nombre d’échantillons vidéo que le EVR doit allouer pour chaque flux de mixage. Cet attribut s’applique aux flux individuels. Utilisez le magasin d’attributs retourné par [**IMFTransform :: GetInputStreamAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreamattributes). |



 

## <a name="setting-the-mixer-on-the-evr"></a>Définition du mélangeur sur le EVR

Pour définir une fonction de mixage personnalisé sur le EVR, appelez [**IMFVideoRenderer :: InitializeRenderer**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer). Le filtre DirectShow EVR et le récepteur multimédia EVR implémentent cette méthode.

**Objet d’activation EVR**. Si vous utilisez l’objet d’activation EVR, vous pouvez fournir un mélangeur personnalisé en définissant l’un des attributs suivants sur l’objet d’activation EVR :



| Attribut                                                                                                 | Description                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**activer \_ le \_ \_ \_ MÉLANGEur vidéo \_ personnalisé MF activé**](mf-activate-custom-video-mixer-activate-attribute.md) | Pointeur vers un objet d’activation pour le mixer. L’objet d’activation doit implémenter l’interface [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) . |
| [**\_activer le \_ \_ CLSID du \_ MÉLANGEur vidéo personnalisé \_ MF**](mf-activate-custom-video-mixer-clsid-attribute.md)       | CLSID du mélangeur.                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> </dl>

 

 
