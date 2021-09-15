---
description: Comment définir la vitesse de lecture sur la session multimédia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Comment définir la vitesse de lecture sur la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413044"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a>Comment définir la vitesse de lecture sur la session multimédia

Pour implémenter une fonctionnalité de lecture telle que l’avance rapide et le rembobinage, les applications peuvent avoir besoin de modifier la vitesse de lecture d’un flux de média. Media Foundation fournit le service de contrôle de la fréquence que les applications doivent utiliser pour définir la vitesse de lecture dynamiquement.

Avant de définir la vitesse de lecture, une application doit vérifier si la vitesse est prise en charge par la source du média. Pour plus d’informations sur l’interrogation des tarifs pris en charge, consultez [Comment déterminer les tarifs pris en charge](how-to-determine-supported-rates.md).

Pour plus d’informations sur les taux de lecture, consultez [à propos](about-rate-control.md)de la gestion des taux.

## <a name="to-set-the-playback-rate"></a>Pour définir la vitesse de lecture

1.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’objet de contrôle de vitesse à partir de la session multimédia.

    Les applications qui appellent [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) doivent garantir les éléments suivants :

    -   Le paramètre *punkObject* contient un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé.
    -   L’objet de contrôle de la fréquence reçu dans le paramètre *ppvObject* est libéré pour éviter les fuites de mémoire.

2.  Appelez la méthode [**IMFRateControl :: ses**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) pour définir la vitesse de lecture. Une **fois** le terminé de manière asynchrone, l’application reçoit l’événement [MESessionRateChanged](mesessionratechanged.md) .

## <a name="example"></a>Exemple

Le code suivant montre comment [**définir la vitesse**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) de lecture en appelant la méthode.


```C++
///////////////////////////////////////////////////////////////////////
//  Name: SetPlaybackRate
//  Description: 
//      Gets the rate control service from Media Session.
//      Sets the playback rate to the specified rate.
//  Parameter:
//      pMediaSession: [in] Media session object to query.
//      rateRequested: [in] Playback rate to set.
//      bThin: [in] Indicates whether to use thinning.
///////////////////////////////////////////////////////////////////////

HRESULT SetPlaybackRate(
          IMFMediaSession *pMediaSession, 
          float rateRequested, 
          BOOL bThin)
{
    HRESULT hr = S_OK;
    IMFRateControl *pRateControl = NULL;

    // Get the rate control object from the Media Session.
    hr = MFGetService( 
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE, 
           IID_IMFRateControl, 
           (void**) &pRateControl ); 

    // Set the playback rate.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( bThin, rateRequested); 
    }

    // Clean up.
    SAFE_RELEASE(pRateControl );

    return hr;
}
```



L’application doit être arrêtée ou suspendue avant de pouvoir effectuer une transition d’un taux négatif ou zéro à un taux positif. Pour plus d’informations sur ces États, consultez Guide pratique [pour contrôler les États de présentation](how-to-control-presentation-states.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> <dt>

[recherche, Avance rapide et la lecture inversée](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



