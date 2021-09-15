---
description: Comment déterminer les tarifs pris en charge
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Comment déterminer les tarifs pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531300"
---
# <a name="how-to-determine-supported-rates"></a>Comment déterminer les tarifs pris en charge

Avant de modifier la vitesse de lecture, une application doit vérifier si la vitesse de lecture est prise en charge par les objets dans le pipeline. L’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fournit des méthodes pour obtenir les taux maximaux et inversés, le taux pris en charge le plus proche d’une vitesse demandée et le taux le plus lent. Chacune de ces requêtes de taux peut spécifier la direction de lecture et s’il faut utiliser l’affinage. La vitesse de lecture exacte est interrogée à l’aide de l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .

Pour plus d’informations sur la modification des vitesses de lecture, consultez [comment définir la vitesse de lecture sur la session multimédia](how-to-set-the-playback-rate-on-the-media-session.md).

Pour obtenir des informations générales sur les vitesses de lecture, consultez [à propos](about-rate-control.md)de la gestion des taux.

## <a name="to-determine-the-current-playback-rate"></a>Pour déterminer la vitesse de lecture actuelle

1.  Procurez-vous le service de contrôle de la vitesse à partir de la session multimédia.

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

    L’application doit interroger le service de contrôle de la fréquence par le biais de la session multimédia. En interne, la session multimédia interroge les objets de la topologie.

2.  Appelez la méthode [**IMFRateControl :: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) pour accéder à la vitesse de lecture actuelle.

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    Le paramètre *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) reçoit une valeur **bool** qui indique si le flux est actuellement éclairci. L’application doit passer la **valeur null** si elle ne souhaite pas interroger la prise en charge de l’affinement pour le flux. Le paramètre *pflRate* reçoit la vitesse de lecture actuelle.

## <a name="to-determine-the-nearest-supported-rate"></a>Pour déterminer le tarif le plus proche pris en charge

1.  Procurez-vous le service support rate à partir de la session multimédia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Appelez la méthode [**IMFRateSupport :: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) pour récupérer le taux pris en charge le plus proche de la vitesse de lecture demandée.

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    L’exemple interroge si un taux de lecture de 4,0 est pris en charge avec une éclaircie. Cela est indiqué en passant **true** dans le paramètre *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported). Si ce taux est pris en charge, *actualRate* contient la vitesse de lecture de 4,0, et l’appel est effectué avec une valeur de retour de S \_ OK. Si la vitesse de lecture exacte n’est pas prise en charge, le tarif le plus proche pris en charge est reçu dans *actualRate*. Si la fréquence n’est pas prise en charge et qu’il n’existe aucun taux de lecture le plus proche disponible, l’appel retourne un code d’erreur approprié.

    Ces valeurs peuvent changer en fonction des composants de pipeline chargés. Par conséquent, vous devez interroger à nouveau les valeurs chaque fois que vous chargez un nouveau topololgy.

    Si la vitesse de lecture souhaitée n’est pas prise en charge, l’une des options consiste à interroger chaque objet de la topologie individuellement, afin de déterminer si un composant particulier ne prend pas en charge la vitesse. Vous pourrez peut-être régénérer la topologie sans ce composant, puis jouer à la vitesse souhaitée. Par exemple, si chaque composant, à l’exception du convertisseur audio, prend en charge une fréquence donnée, vous pouvez reconstruire la topologie sans la branche audio et la lire à la vitesse souhaitée sans l’audio.

## <a name="to-determine-the-slowest-supported-rate"></a>Pour déterminer le taux le plus lent pris en charge

1.  Procurez-vous le service support rate à partir de la session multimédia.

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).

2.  Appelez la méthode [**IMFRateSupport :: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) pour récupérer le taux le plus lent pris en charge.

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    L’exemple interroge la vitesse de lecture inversée la plus lente avec la réduction. Le débit de la limite inférieure est reçu dans le paramètre *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).

    Si la lecture ou l’affinage inverse n’est pas pris en charge, l’appel retourne un code d’erreur approprié.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Session multimédia](media-session.md)
</dt> <dt>

[Contrôle de la fréquence](rate-control.md)
</dt> <dt>

[recherche, Avance rapide et la lecture inversée](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



