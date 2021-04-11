---
description: Comment déterminer les tarifs pris en charge
ms.assetid: 7f2b64e1-1062-4f77-b8e0-62b6d962ae8b
title: Comment déterminer les tarifs pris en charge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f67e9753604f51e85c641e616e8b69944b96618
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201802"
---
# <a name="how-to-determine-supported-rates"></a><span data-ttu-id="f85b9-103">Comment déterminer les tarifs pris en charge</span><span class="sxs-lookup"><span data-stu-id="f85b9-103">How to Determine Supported Rates</span></span>

<span data-ttu-id="f85b9-104">Avant de modifier la vitesse de lecture, une application doit vérifier si la vitesse de lecture est prise en charge par les objets dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="f85b9-104">Before changing the playback rate, an application should check whether the playback rate is supported by the objects in the pipeline.</span></span> <span data-ttu-id="f85b9-105">L’interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) fournit des méthodes pour obtenir les taux maximaux et inversés, le taux pris en charge le plus proche d’une vitesse demandée et le taux le plus lent.</span><span class="sxs-lookup"><span data-stu-id="f85b9-105">The [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) interface provides methods to get the maximum forward and reverse rates, the supported rate nearest to a requested rate, and the slowest rate.</span></span> <span data-ttu-id="f85b9-106">Chacune de ces requêtes de taux peut spécifier la direction de lecture et s’il faut utiliser l’affinage.</span><span class="sxs-lookup"><span data-stu-id="f85b9-106">Each of these rate queries can specify the playback direction and whether to use thinning.</span></span> <span data-ttu-id="f85b9-107">La vitesse de lecture exacte est interrogée à l’aide de l’interface [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) .</span><span class="sxs-lookup"><span data-stu-id="f85b9-107">The exact playback rate is queried by using the [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) interface.</span></span>

<span data-ttu-id="f85b9-108">Pour plus d’informations sur la modification des vitesses de lecture, consultez [comment définir la vitesse de lecture sur la session multimédia](how-to-set-the-playback-rate-on-the-media-session.md).</span><span class="sxs-lookup"><span data-stu-id="f85b9-108">For information about changing playback rates, see [How to Set the Playback Rate on the Media Session](how-to-set-the-playback-rate-on-the-media-session.md).</span></span>

<span data-ttu-id="f85b9-109">Pour obtenir des informations générales sur les vitesses de lecture, consultez [à propos](about-rate-control.md)de la gestion des taux.</span><span class="sxs-lookup"><span data-stu-id="f85b9-109">For general information about playback rates, see [About Rate Control](about-rate-control.md).</span></span>

## <a name="to-determine-the-current-playback-rate"></a><span data-ttu-id="f85b9-110">Pour déterminer la vitesse de lecture actuelle</span><span class="sxs-lookup"><span data-stu-id="f85b9-110">To determine the current playback rate</span></span>

1.  <span data-ttu-id="f85b9-111">Procurez-vous le service de contrôle de la vitesse à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f85b9-111">Get the rate control service from the Media Session.</span></span>

    ```C++
    IMFRateControl *pRateControl = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateControl, 
           (void**) &pRateControl );
    ```

    

    <span data-ttu-id="f85b9-112">Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="f85b9-112">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

    <span data-ttu-id="f85b9-113">L’application doit interroger le service de contrôle de la fréquence par le biais de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f85b9-113">The application must query for the rate control service through the Media Session.</span></span> <span data-ttu-id="f85b9-114">En interne, la session multimédia interroge les objets de la topologie.</span><span class="sxs-lookup"><span data-stu-id="f85b9-114">Internally, the Media Session queries the objects in the topology.</span></span>

2.  <span data-ttu-id="f85b9-115">Appelez la méthode [**IMFRateControl :: GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) pour accéder à la vitesse de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f85b9-115">Call the [**IMFRateControl::GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) method to get the current playback rate.</span></span>

    ```C++
    hr = pRateControl->GetRate(&bThin, &rate);
    ```

    

    <span data-ttu-id="f85b9-116">Le paramètre *pfThin* de [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) reçoit une valeur **bool** qui indique si le flux est actuellement éclairci.</span><span class="sxs-lookup"><span data-stu-id="f85b9-116">The *pfThin* parameter of [**GetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-getrate) receives a **BOOL** value that indicates whether the stream is currently being thinned.</span></span> <span data-ttu-id="f85b9-117">L’application doit passer la **valeur null** si elle ne souhaite pas interroger la prise en charge de l’affinement pour le flux.</span><span class="sxs-lookup"><span data-stu-id="f85b9-117">The application must pass **NULL** if it does not want to query thinning support for the stream.</span></span> <span data-ttu-id="f85b9-118">Le paramètre *pflRate* reçoit la vitesse de lecture actuelle.</span><span class="sxs-lookup"><span data-stu-id="f85b9-118">The *pflRate* parameter receives the current playback rate.</span></span>

## <a name="to-determine-the-nearest-supported-rate"></a><span data-ttu-id="f85b9-119">Pour déterminer le tarif le plus proche pris en charge</span><span class="sxs-lookup"><span data-stu-id="f85b9-119">To determine the nearest supported rate</span></span>

1.  <span data-ttu-id="f85b9-120">Procurez-vous le service support rate à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f85b9-120">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="f85b9-121">Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="f85b9-121">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="f85b9-122">Appelez la méthode [**IMFRateSupport :: IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) pour récupérer le taux pris en charge le plus proche de la vitesse de lecture demandée.</span><span class="sxs-lookup"><span data-stu-id="f85b9-122">Call the [**IMFRateSupport::IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) method to retrieve the supported rate nearest to a requested playback rate.</span></span>

    ```C++
    float rateRequested = 4.0;
    float actualRate = 0;
    hr = pRateSupport->IsRateSupported(
           TRUE, 
           rateRequested, 
           &actualRate );
    ```

    

    <span data-ttu-id="f85b9-123">L’exemple interroge si un taux de lecture de 4,0 est pris en charge avec une éclaircie.</span><span class="sxs-lookup"><span data-stu-id="f85b9-123">The example queries whether a playback rate of 4.0 is supported with thinning.</span></span> <span data-ttu-id="f85b9-124">Cela est indiqué en passant **true** dans le paramètre *fThin* de [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span><span class="sxs-lookup"><span data-stu-id="f85b9-124">This is indicated by passing **TRUE** in the *fThin* parameter of [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported).</span></span> <span data-ttu-id="f85b9-125">Si ce taux est pris en charge, *actualRate* contient la vitesse de lecture de 4,0, et l’appel est effectué avec une valeur de retour de S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f85b9-125">If this rate is supported, *actualRate* contains the playback rate of 4.0, and the call succeeds with a return value of S\_OK.</span></span> <span data-ttu-id="f85b9-126">Si la vitesse de lecture exacte n’est pas prise en charge, le tarif le plus proche pris en charge est reçu dans *actualRate*.</span><span class="sxs-lookup"><span data-stu-id="f85b9-126">If the exact playback rate is not supported, the nearest supported rate is received in *actualRate*.</span></span> <span data-ttu-id="f85b9-127">Si la fréquence n’est pas prise en charge et qu’il n’existe aucun taux de lecture le plus proche disponible, l’appel retourne un code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="f85b9-127">If the rate is not supported and there is no available nearest playback rate, the call returns an appropriate error code.</span></span>

    <span data-ttu-id="f85b9-128">Ces valeurs peuvent changer en fonction des composants de pipeline chargés.</span><span class="sxs-lookup"><span data-stu-id="f85b9-128">These values can change depending on which pipeline components are loaded.</span></span> <span data-ttu-id="f85b9-129">Par conséquent, vous devez interroger à nouveau les valeurs chaque fois que vous chargez un nouveau topololgy.</span><span class="sxs-lookup"><span data-stu-id="f85b9-129">Therefore, you should query the values again whenever you load a new topololgy.</span></span>

    <span data-ttu-id="f85b9-130">Si la vitesse de lecture souhaitée n’est pas prise en charge, l’une des options consiste à interroger chaque objet de la topologie individuellement, afin de déterminer si un composant particulier ne prend pas en charge la vitesse.</span><span class="sxs-lookup"><span data-stu-id="f85b9-130">If the desired playback rate is not supported, one option is to query each object in the topology individually, to find out if a particular component does not support the rate.</span></span> <span data-ttu-id="f85b9-131">Vous pourrez peut-être régénérer la topologie sans ce composant, puis jouer à la vitesse souhaitée.</span><span class="sxs-lookup"><span data-stu-id="f85b9-131">You might be able to rebuild the topology without this component and then play at the desired rate.</span></span> <span data-ttu-id="f85b9-132">Par exemple, si chaque composant, à l’exception du convertisseur audio, prend en charge une fréquence donnée, vous pouvez reconstruire la topologie sans la branche audio et la lire à la vitesse souhaitée sans l’audio.</span><span class="sxs-lookup"><span data-stu-id="f85b9-132">For example, if every component except the audio renderer supports a given rate, you could rebuild the topology without the audio branch and play at the desired rate without audio.</span></span>

## <a name="to-determine-the-slowest-supported-rate"></a><span data-ttu-id="f85b9-133">Pour déterminer le taux le plus lent pris en charge</span><span class="sxs-lookup"><span data-stu-id="f85b9-133">To determine the slowest supported rate</span></span>

1.  <span data-ttu-id="f85b9-134">Procurez-vous le service support rate à partir de la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="f85b9-134">Get the rate support service from the Media Session.</span></span>

    ```C++
    IMFRateSupport *pRateSupport = NULL;
    hr = MFGetService(
           pMediaSession, 
           MF_RATE_CONTROL_SERVICE,
           IID_IMFRateSupport, 
           (void**) &pRateSupport );
    ```

    

    <span data-ttu-id="f85b9-135">Transmettez un pointeur d’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) initialisé dans le paramètre *punkObject* de [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span><span class="sxs-lookup"><span data-stu-id="f85b9-135">Pass an initialized [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface pointer in the *punkObject* parameter of [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).</span></span>

2.  <span data-ttu-id="f85b9-136">Appelez la méthode [**IMFRateSupport :: GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) pour récupérer le taux le plus lent pris en charge.</span><span class="sxs-lookup"><span data-stu-id="f85b9-136">Call the [**IMFRateSupport::GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate) method to retrieve the slowest supported rate.</span></span>

    ```C++
    float slowestRate = 0;
    hr = pRateSupport->GetSlowestRate(
           MFRATE_REVERSE, 
           TRUE, 
           &slowestRate);
    ```

    

    <span data-ttu-id="f85b9-137">L’exemple interroge la vitesse de lecture inversée la plus lente avec la réduction.</span><span class="sxs-lookup"><span data-stu-id="f85b9-137">The example queries for the slowest reverse playback rate with thinning.</span></span> <span data-ttu-id="f85b9-138">Le débit de la limite inférieure est reçu dans le paramètre *slowestRate* de [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span><span class="sxs-lookup"><span data-stu-id="f85b9-138">The lower bound rate is received in *slowestRate* parameter of [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate).</span></span>

    <span data-ttu-id="f85b9-139">Si la lecture ou l’affinage inverse n’est pas pris en charge, l’appel retourne un code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="f85b9-139">If reverse playback or thinning is not supported, the call returns an appropriate error code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f85b9-140">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f85b9-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f85b9-141">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="f85b9-141">Media Session</span></span>](media-session.md)
</dt> <dt>

[<span data-ttu-id="f85b9-142">Contrôle de la fréquence</span><span class="sxs-lookup"><span data-stu-id="f85b9-142">Rate Control</span></span>](rate-control.md)
</dt> <dt>

[<span data-ttu-id="f85b9-143">Recherche, avance rapide et lecture inversée</span><span class="sxs-lookup"><span data-stu-id="f85b9-143">Seeking, Fast Forward, and Reverse Play</span></span>](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



