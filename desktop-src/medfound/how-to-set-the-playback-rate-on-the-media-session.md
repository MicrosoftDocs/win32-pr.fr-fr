---
description: Comment définir la vitesse de lecture sur la session multimédia
ms.assetid: 3663b63f-127c-49fc-923a-d05521fe3d35
title: Comment définir la vitesse de lecture sur la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deed8bf480bba1bf1e7d86a41a75b8f41f61046b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761371"
---
# <a name="how-to-set-the-playback-rate-on-the-media-session"></a><span data-ttu-id="c10de-103">Comment définir la vitesse de lecture sur la session multimédia</span><span class="sxs-lookup"><span data-stu-id="c10de-103">How to Set the Playback Rate on the Media Session</span></span>

<span data-ttu-id="c10de-104">Pour implémenter une fonctionnalité de lecture telle que l’avance rapide et le rembobinage, les applications peuvent avoir besoin de modifier la vitesse de lecture d’un flux de média.</span><span class="sxs-lookup"><span data-stu-id="c10de-104">To implement playback functionality such as fast forward and rewind, applications may need to change the playback rate for a media stream.</span></span> <span data-ttu-id="c10de-105">Media Foundation fournit le service de contrôle de la fréquence que les applications doivent utiliser pour définir la vitesse de lecture dynamiquement.</span><span class="sxs-lookup"><span data-stu-id="c10de-105">Media Foundation provides the rate control service that the applications must use to set the playback rate dynamically.</span></span>

<span data-ttu-id="c10de-106">Avant de définir la vitesse de lecture, une application doit vérifier si la vitesse est prise en charge par la source du média.</span><span class="sxs-lookup"><span data-stu-id="c10de-106">Before setting the playback rate, an application should check whether the rate is supported by the media source.</span></span> <span data-ttu-id="c10de-107">Pour plus d’informations sur l’interrogation des tarifs pris en charge, consultez [Comment déterminer les tarifs pris en charge](how-to-determine-supported-rates.md).</span><span class="sxs-lookup"><span data-stu-id="c10de-107">For information about querying for supported rates, see [How to Determine Supported Rates](how-to-determine-supported-rates.md).</span></span>

<span data-ttu-id="c10de-108">Pour plus d’informations sur les taux de lecture, consultez [à propos](about-rate-control.md)de la gestion des taux.</span><span class="sxs-lookup"><span data-stu-id="c10de-108">For information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-set-the-playback-rate"></a><span data-ttu-id="c10de-109">Pour définir la vitesse de lecture</span><span class="sxs-lookup"><span data-stu-id="c10de-109">To set the playback rate</span></span>

1.  <span data-ttu-id="c10de-110">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’objet de contrôle de vitesse à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="c10de-110">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the rate control object from the Media Session.</span></span>

    <span data-ttu-id="c10de-111">Les applications qui appellent [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) doivent garantir les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="c10de-111">Applications calling [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) must ensure the following:</span></span>

    -   <span data-ttu-id="c10de-112">Le paramètre *punkObject* contient un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé.</span><span class="sxs-lookup"><span data-stu-id="c10de-112">The *punkObject* parameter contains an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer.</span></span>
    -   <span data-ttu-id="c10de-113">L’objet de contrôle de la fréquence reçu dans le paramètre *ppvObject* est libéré pour éviter les fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c10de-113">The rate control object received in the *ppvObject* parameter is released to avoid memory leaks.</span></span>

2.  <span data-ttu-id="c10de-114">Appelez la méthode [**IMFRateControl :: ses**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) pour définir la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="c10de-114">Call the [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) method to set the playback rate.</span></span> <span data-ttu-id="c10de-115">Une **fois** le terminé de manière asynchrone, l’application reçoit l’événement [MESessionRateChanged](mesessionratechanged.md) .</span><span class="sxs-lookup"><span data-stu-id="c10de-115">After **SetRate** completes asynchronously, the application receives the [MESessionRateChanged](mesessionratechanged.md) event.</span></span>

## <a name="example"></a><span data-ttu-id="c10de-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="c10de-116">Example</span></span>

<span data-ttu-id="c10de-117">Le code suivant montre comment [**définir la vitesse**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) de lecture en appelant la méthode.</span><span class="sxs-lookup"><span data-stu-id="c10de-117">The following code shows how to set the playback rate by calling the [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) method.</span></span>


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



<span data-ttu-id="c10de-118">L’application doit être arrêtée ou suspendue avant de pouvoir effectuer une transition d’un taux négatif ou zéro à un taux positif.</span><span class="sxs-lookup"><span data-stu-id="c10de-118">The application must be stopped or paused before it can make a transition from a negative or zero rate to a positive rate.</span></span> <span data-ttu-id="c10de-119">Pour plus d’informations sur ces États, consultez Guide pratique [pour contrôler les États de présentation](how-to-control-presentation-states.md).</span><span class="sxs-lookup"><span data-stu-id="c10de-119">For information about these states, see [How to Control Presentation States](how-to-control-presentation-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c10de-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c10de-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c10de-121">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="c10de-121">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="c10de-122">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="c10de-122">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="c10de-123">Recherche, avance rapide et lecture inversée</span><span class="sxs-lookup"><span data-stu-id="c10de-123">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



