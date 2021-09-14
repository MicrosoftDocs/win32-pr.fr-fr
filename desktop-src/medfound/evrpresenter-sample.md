---
description: Exemple EVRPresenter
ms.assetid: 791a9816-4c40-4683-8b32-22f73d7fe84d
title: Exemple EVRPresenter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bde85de152c41f348b1aae74a8c0d67ca746cab
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293486"
---
# <a name="evrpresenter-sample"></a>Exemple EVRPresenter

Montre comment implémenter un présentateur personnalisé pour le [convertisseur vidéo amélioré](enhanced-video-renderer.md) (EVR). le présentateur personnalisé peut être utilisé avec les DirectShow filtre EVR ou Microsoft Media Foundation récepteur EVR.

## <a name="apis-demonstrated"></a>API illustrées

Cet exemple illustre les interfaces de Media Foundation suivantes :

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient)
-   [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)
-   [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol)
-   [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)

## <a name="usage"></a>Usage

L’exemple EVRPresenter génère une DLL qui est un serveur COM pour le présentateur. Avant d’utiliser le présentateur personnalisé, vous devez inscrire la DLL.

Pour utiliser cet exemple dans Media Foundation :

1.  Générez l’exemple.
2.  EvrPresenter.dll regsvr32.
3.  Générez et exécutez l' [exemple MFPlayer](/previous-versions//bb970516(v=vs.85)).
4.  Dans le menu **fichier** , sélectionnez **ouvrir** un fichier.
5.  Dans la boîte de dialogue **ouvrir un fichier** , sélectionnez le **présentateur EVR personnalisé.**
6.  Sélectionnez un fichier pour la lecture.

Pour utiliser cet exemple dans DirectShow :

1.  Générez l’exemple.
2.  Inscrire EvrPresenter.dll.
3.  Générez et exécutez l’exemple EVRPlayer. cet exemple est fourni avec les exemples de DirectShow dans le SDK Windows.
4.  Dans le menu **fichier** , sélectionnez **EVR Presenter**.
5.  Sélectionnez un fichier pour la lecture.

## <a name="requirements"></a>Spécifications



| Produit                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

cet exemple est disponible dans [Windows le référentiel github exemples classiques](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Convertisseur vidéo amélioré](enhanced-video-renderer.md)
</dt> <dt>

[Comment écrire un présentateur EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[Exemples du kit de développement logiciel Media Foundation](media-foundation-sdk-samples.md)
</dt> </dl>

 

 
