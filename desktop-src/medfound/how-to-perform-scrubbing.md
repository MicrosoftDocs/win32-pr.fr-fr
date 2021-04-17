---
description: Comment effectuer un nettoyage
ms.assetid: 3cf56caf-5c6d-4318-811a-c8bdc1959148
title: Comment effectuer un nettoyage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dad1f06cb6abe6a570fd85407028450651e32a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527687"
---
# <a name="how-to-perform-scrubbing"></a><span data-ttu-id="4b3a1-103">Comment effectuer un nettoyage</span><span class="sxs-lookup"><span data-stu-id="4b3a1-103">How to Perform Scrubbing</span></span>

<span data-ttu-id="4b3a1-104">Le nettoyage est effectué pour rechercher instantanément des points spécifiques dans un fichier en interagissant avec une représentation visuelle du temps, telle qu’une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-104">Scrubbing is performed to instantaneously seek to specific points within a file by interacting with a visual representation of time, such as a scrollbar.</span></span> <span data-ttu-id="4b3a1-105">Dans Media Foundation, le nettoyage signifie la recherche sur un fichier et l’obtention d’une trame mise à jour.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-105">In Media Foundation, scrubbing means seeking on a file and getting one updated frame.</span></span>

<span data-ttu-id="4b3a1-106">Pour plus d’informations sur le nettoyage, consultez [à propos du contrôle du taux](about-rate-control.md).</span><span class="sxs-lookup"><span data-stu-id="4b3a1-106">For information about scrubbing, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-perform-scrubbing"></a><span data-ttu-id="4b3a1-107">Pour effectuer un nettoyage</span><span class="sxs-lookup"><span data-stu-id="4b3a1-107">To perform scrubbing</span></span>

1.  <span data-ttu-id="4b3a1-108">Appelez [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) pour récupérer l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="4b3a1-108">Call [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) to get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the [Media Session](media-session.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="4b3a1-109">N’obtient pas l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) à partir de la source du média.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-109">Do not get the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface from the media source.</span></span> <span data-ttu-id="4b3a1-110">Récupérez toujours l’interface à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-110">Always get the interface from the Media Session.</span></span>

     

2.  <span data-ttu-id="4b3a1-111">Appelez [**IMFRateControl ::**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) se. pour définir la vitesse de lecture sur zéro.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-111">Call [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) to set the playback rate to zero.</span></span> <span data-ttu-id="4b3a1-112">Pour plus d’informations sur l’appel de cette méthode, consultez [comment définir la vitesse de lecture sur la session multimédia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="4b3a1-112">For more information about calling this method, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>
3.  <span data-ttu-id="4b3a1-113">Créez une position de recherche dans un **PROPVARIANT** en spécifiant l’heure de présentation de la recherche dans un type **MFTIME** .</span><span class="sxs-lookup"><span data-stu-id="4b3a1-113">Create a seek position in a **PROPVARIANT** by specifying the presentation time to seek to in a **MFTIME** type.</span></span>
4.  <span data-ttu-id="4b3a1-114">Appelez [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) avec la position de recherche pour démarrer la lecture.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-114">Call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) with the seek position to start playback.</span></span>
5.  <span data-ttu-id="4b3a1-115">Lorsque l’opération de nettoyage est terminée, la session multimédia envoie un événement [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="4b3a1-115">When the scrub operation is complete, the Media Session sends an [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event.</span></span> <span data-ttu-id="4b3a1-116">Attendez que cet événement soit [**redémarré**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour une autre opération de nettoyage.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-116">Wait for this event before calling [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) again for another scrubbing operation.</span></span>

## <a name="example"></a><span data-ttu-id="4b3a1-117">Exemple</span><span class="sxs-lookup"><span data-stu-id="4b3a1-117">Example</span></span>

<span data-ttu-id="4b3a1-118">L’exemple de code suivant montre comment effectuer un nettoyage.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-118">The following code example shows how to perform scrubbing.</span></span>


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



<span data-ttu-id="4b3a1-119">Une opération de nettoyage réussi génère l’événement [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) une fois que tous les récepteurs de flux ont été mis à jour avec le nouveau Frame et que l’opération de nettoyage s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-119">A successful scrubbing operation generates the [MESessionScrubSampleComplete](mesessionscrubsamplecomplete.md) event after all the stream sinks are updated with the new frame and the scrubbing operation completes successfully.</span></span> <span data-ttu-id="4b3a1-120">Le nettoyage d’un fichier vidéo affiche le frame auquel il a été fait, mais ne génère pas de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="4b3a1-120">Scrubbing a video file displays the frame that was seeked to, but does not generate an audio output.</span></span>

<span data-ttu-id="4b3a1-121">L’application peut effectuer une exécution pas à pas en définissant la vitesse de lecture sur zéro, puis en passant un **PROPVARIANT** défini sur **VT \_ vide** dans l’appel à [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span><span class="sxs-lookup"><span data-stu-id="4b3a1-121">The application can perform frame stepping by setting the playback rate to zero and then passing a **PROPVARIANT** that is set to **VT\_EMPTY** in the call to [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b3a1-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b3a1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b3a1-123">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="4b3a1-123">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="4b3a1-124">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="4b3a1-124">Rate Control</span></span>](rate-control.md)
</dt> </dl>

 

 



