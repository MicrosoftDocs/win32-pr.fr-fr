---
description: Comment effectuer un nettoyage
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Comment effectuer un nettoyage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab86ae39567132352592883b7441e4f325cb1b021b74e5b7a67f4a2755c3c947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118063356"
---
# <a name="how-to-perform-scrubbing"></a>Comment effectuer un nettoyage

Le nettoyage est effectué pour rechercher instantanément des points spécifiques dans un fichier en interagissant avec une représentation visuelle du temps, telle qu’une barre de défilement. Dans Media Foundation, le nettoyage signifie la recherche sur un fichier et l’obtention d’une trame mise à jour.

Pour plus d’informations sur le nettoyage, consultez [à propos du contrôle du taux](about-rate-control.md).

## <a name="to-perform-scrubbing"></a>Pour effectuer un nettoyage

1.  Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la [session multimédia](media-session.md).
    > [!Note]  
    > N’obtient pas l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la source du média. Récupérez toujours l’interface à partir de la session multimédia.

     

2.  Appelez [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se. pour définir la vitesse de lecture sur zéro. Pour plus d’informations sur l’appel de cette méthode, consultez [comment définir la vitesse de lecture sur la session multimédia](how-to-set-the-playback-rate-on-the-media-session.md).
3.  Créez une position de recherche dans un **PROPVARIANT** en spécifiant l’heure de présentation de la recherche dans un type **MFTIME** .
4.  Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) avec la position de recherche pour démarrer la lecture.
5.  Lorsque l’opération de nettoyage est terminée, la session multimédia envoie un événement [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) . Attendez que cet événement soit [**redémarré**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour une autre opération de nettoyage.

## <a name="example"></a>Exemples

L’exemple de code suivant montre comment effectuer un nettoyage.


```C++
HRESULT SkipToPosition (MFTIME SeekTime, IMFMediaSession *pMediaSession)
{
    PROPVARIANT var;
    PropVariantInit(&var);

    IMFRateControl *pRateControl = NULL;

    // Get the rate control service.
    HRESULT hr = MFGetService(pMediaSession, MF_RATE_CONTROL_SERVICE, IID_PPV_ARGS(&pRateControl));

    // Set the playback rate to zero without thinning.
    if(SUCCEEDED(hr))
    {
        hr = pRateControl ->SetRate( FALSE, 0.0F); 
    }

    // Create the Media Session start position.
    if( SeekTime == PRESENTATION_CURRENT_POSITION )
    {
        var.vt = VT_EMPTY;
    }
    else
    {
        var.vt = VT_I8;
        var.hVal.QuadPart = SeekTime;
    }

    // Start the Media Session.
    if(SUCCEEDED(hr))
    {
        hr = pMediaSession->Start( NULL, &var);
    }

// Clean up.
    SafeRelease(&pRateControl);
    PropVariantClear(&var)
    return hr;
}
```



Une opération de nettoyage réussi génère l’événement [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) une fois que tous les récepteurs de flux ont été mis à jour avec le nouveau Frame et que l’opération de nettoyage s’est terminée avec succès. Le nettoyage d’un fichier vidéo affiche le frame auquel il a été fait, mais ne génère pas de sortie audio.

L’application peut effectuer une exécution pas à pas en définissant la vitesse de lecture sur zéro, puis en passant un **PROPVARIANT** défini sur **VT \_ vide** dans l’appel à [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> </dl>

 

 



