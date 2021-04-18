---
description: Comment contrôler les États de présentation
ms.assetid: 978373ef-b2a4-4035-b889-e28a037c0ab5
title: Comment contrôler les États de présentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a82fe0363a27b9c6f5c054b73ca409835a3dff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536341"
---
# <a name="how-to-control-presentation-states"></a><span data-ttu-id="97846-103">Comment contrôler les États de présentation</span><span class="sxs-lookup"><span data-stu-id="97846-103">How to Control Presentation States</span></span>

<span data-ttu-id="97846-104">La session multimédia fournit un contrôle de transport, tel que la modification des États de présentation (lecture, pause et arrêt dans un scénario de lecture de style playlist).</span><span class="sxs-lookup"><span data-stu-id="97846-104">The Media Session provides transport control such as changing presentation states (Play, Pause, and Stop in a playlist-style playback scenario).</span></span> <span data-ttu-id="97846-105">Cette rubrique décrit les méthodes de session multimédia qu’une application doit appeler pour modifier l’état de lecture.</span><span class="sxs-lookup"><span data-stu-id="97846-105">This topic describes Media Session methods that an application should call to change the playback state.</span></span>

<span data-ttu-id="97846-106">Le tableau suivant répertorie les transitions d’état de présentation valides.</span><span class="sxs-lookup"><span data-stu-id="97846-106">The following table shows the valid presentation state transitions.</span></span>



| <span data-ttu-id="97846-107">Transition d'état</span><span class="sxs-lookup"><span data-stu-id="97846-107">State transition</span></span> | <span data-ttu-id="97846-108">Description</span><span class="sxs-lookup"><span data-stu-id="97846-108">Description</span></span>                                                                                |
|------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="97846-109">Lecture > pause</span><span class="sxs-lookup"><span data-stu-id="97846-109">Play -> Pause</span></span> | <span data-ttu-id="97846-110">L’horloge de la présentation se fige.</span><span class="sxs-lookup"><span data-stu-id="97846-110">The presentation clock freezes.</span></span>                                                            |
| <span data-ttu-id="97846-111">Lecture > arrêter</span><span class="sxs-lookup"><span data-stu-id="97846-111">Play -> Stop</span></span>  | <span data-ttu-id="97846-112">L’horloge de la présentation est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="97846-112">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="97846-113">Pause-> de lecture</span><span class="sxs-lookup"><span data-stu-id="97846-113">Pause -> Play</span></span> | <span data-ttu-id="97846-114">L’horloge de la présentation reprend à partir du moment où elle figée pendant la lecture pour suspendre la transition.</span><span class="sxs-lookup"><span data-stu-id="97846-114">The presentation clock resumes from the time it froze during the Play to Pause transition.</span></span> |
| <span data-ttu-id="97846-115">Interrompre-> arrêter</span><span class="sxs-lookup"><span data-stu-id="97846-115">Pause -> Stop</span></span> | <span data-ttu-id="97846-116">L’horloge de la présentation est réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="97846-116">The presentation clock is reset.</span></span>                                                           |
| <span data-ttu-id="97846-117">Lecture ></span><span class="sxs-lookup"><span data-stu-id="97846-117">Stop -> Play</span></span>  | <span data-ttu-id="97846-118">L’horloge de présentation commence au début de la présentation.</span><span class="sxs-lookup"><span data-stu-id="97846-118">The presentation clock starts from the beginning of the presentation.</span></span>                      |
| <span data-ttu-id="97846-119">Arrêter > suspendre</span><span class="sxs-lookup"><span data-stu-id="97846-119">Stop -> Pause</span></span> | <span data-ttu-id="97846-120">Non autorisé.</span><span class="sxs-lookup"><span data-stu-id="97846-120">Not allowed.</span></span>                                                                               |



 

## <a name="to-change-presentation-states"></a><span data-ttu-id="97846-121">Pour modifier les États de présentation</span><span class="sxs-lookup"><span data-stu-id="97846-121">To change presentation states</span></span>

-   <span data-ttu-id="97846-122">Appelez la méthode [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) pour suspendre la lecture.</span><span class="sxs-lookup"><span data-stu-id="97846-122">Call the [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause) method to pause playback.</span></span>

    ```C++
    hr = pMediaSession->Pause();
    ```

    

    <span data-ttu-id="97846-123">Avant d’appeler cette méthode, l’application doit appeler la méthode [**IMFMediaSession :: GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) pour déterminer si la source du média prend en charge l’État pause.</span><span class="sxs-lookup"><span data-stu-id="97846-123">Before calling this method, the application must call the [**IMFMediaSession::GetSessionCapabilities**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getsessioncapabilities) method to discover whether the media source supports the Pause state.</span></span> <span data-ttu-id="97846-124">Si c’est le cas, cette méthode retourne **MFSESSIONCAP \_ Pause** dans le paramètre *pdwCaps* .</span><span class="sxs-lookup"><span data-stu-id="97846-124">If it does, this method returns **MFSESSIONCAP\_PAUSE** in the *pdwCaps* parameter.</span></span>

    <span data-ttu-id="97846-125">Suspendre arrête temporairement la session multimédia, l’horloge de présentation et le récepteur de flux pour la présentation actuelle.</span><span class="sxs-lookup"><span data-stu-id="97846-125">Pause temporarily stops the Media Session, the presentation clock, and the stream sink for the current presentation.</span></span> <span data-ttu-id="97846-126">Une fois l’appel terminé, l’application reçoit un événement [MESessionPaused](mesessionpaused.md) .</span><span class="sxs-lookup"><span data-stu-id="97846-126">After the call completes successfully, the application receives a [MESessionPaused](mesessionpaused.md) event.</span></span>

-   <span data-ttu-id="97846-127">Appelez la méthode [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) pour arrêter la lecture.</span><span class="sxs-lookup"><span data-stu-id="97846-127">Call the [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) method to stop playback.</span></span>

    ```C++
    hr = pMediaSession->Stop();
    ```

    

    <span data-ttu-id="97846-128">Cette méthode arrête la session multimédia en arrêtant la source du média, les horloges correspondantes et les récepteurs de flux.</span><span class="sxs-lookup"><span data-stu-id="97846-128">This method stops the Media Session by stopping the media source, the corresponding clocks, and stream sinks.</span></span> <span data-ttu-id="97846-129">Si la session multimédia contrôle la [source de Sequencer](sequencer-source.md), les sources natives sous-jacentes sont arrêtées par la source de Sequencer.</span><span class="sxs-lookup"><span data-stu-id="97846-129">If the Media Session is controlling the [Sequencer Source](sequencer-source.md), the underlying native sources are stopped by the sequencer source.</span></span> <span data-ttu-id="97846-130">Une fois la session multimédia arrêtée, l’application reçoit un événement [MESessionStopped](mesessionstopped.md) .</span><span class="sxs-lookup"><span data-stu-id="97846-130">After the Media Session is stopped, the application receives a [MESessionStopped](mesessionstopped.md) event.</span></span>

-   <span data-ttu-id="97846-131">Appelez la méthode [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) pour démarrer la lecture ou rechercher une nouvelle position.</span><span class="sxs-lookup"><span data-stu-id="97846-131">Call the [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method to start playback or seek to a new position.</span></span>

    ```C++
    hr = pMediaSession->Start(NULL, &var);
    ```

    

    <span data-ttu-id="97846-132">Cette méthode démarre la session multimédia à partir des États pause et arrêt.</span><span class="sxs-lookup"><span data-stu-id="97846-132">This method starts the Media Session from Pause and Stop states.</span></span> <span data-ttu-id="97846-133">La session multimédia est responsable de la configuration du workflow dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="97846-133">The Media Session is responsible for setting up the data flow in the pipeline.</span></span> <span data-ttu-id="97846-134">Cette méthode indique à la session multimédia de démarrer l’horloge de la présentation.</span><span class="sxs-lookup"><span data-stu-id="97846-134">This method instructs the Media Session to start the presentation clock.</span></span> <span data-ttu-id="97846-135">Après cet appel, la session multimédia envoie un événement [MESessionStarted](mesessionstarted.md) à l’application.</span><span class="sxs-lookup"><span data-stu-id="97846-135">After this call, Media Session sends a [MESessionStarted](mesessionstarted.md) event to the application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97846-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="97846-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97846-137">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="97846-137">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



