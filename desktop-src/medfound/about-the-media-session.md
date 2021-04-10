---
description: À propos de la session multimédia
ms.assetid: 09f50b11-0e0a-42b6-a7bf-bb0135343351
title: À propos de la session multimédia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc490e63f623fb3c2d5efde5a80f1988566f9345
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953342"
---
# <a name="about-the-media-session"></a><span data-ttu-id="ae374-103">À propos de la session multimédia</span><span class="sxs-lookup"><span data-stu-id="ae374-103">About the Media Session</span></span>

<span data-ttu-id="ae374-104">La session multimédia expose l’interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="ae374-104">The Media Session exposes the [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) interface.</span></span> <span data-ttu-id="ae374-105">Il existe deux façons de créer la session multimédia, selon que votre application prendra en charge le contenu protégé :</span><span class="sxs-lookup"><span data-stu-id="ae374-105">There are two ways to create the Media Session, depending on whether your application will support protected content:</span></span>

-   <span data-ttu-id="ae374-106">Si votre application ne prend pas en charge le contenu protégé, vous pouvez créer la session multimédia en appelant [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span><span class="sxs-lookup"><span data-stu-id="ae374-106">If your application does not support protected content, you can create the Media Session by calling the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession).</span></span> <span data-ttu-id="ae374-107">Cette fonction crée la session multimédia à l’intérieur du processus d’application.</span><span class="sxs-lookup"><span data-stu-id="ae374-107">This function creates the Media Session inside the application process.</span></span>
-   <span data-ttu-id="ae374-108">Pour prendre en charge le contenu protégé, créez la session multimédia en appelant [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="ae374-108">To support protected content, create the Media Session by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="ae374-109">Cette fonction crée la session multimédia à l’intérieur du processus PMP (Protected Media Path).</span><span class="sxs-lookup"><span data-stu-id="ae374-109">This function creates the Media Session inside the Protected Media Path (PMP) process.</span></span> <span data-ttu-id="ae374-110">L’application reçoit un pointeur vers un objet proxy qui marshale les appels de méthode à travers la limite de processus.</span><span class="sxs-lookup"><span data-stu-id="ae374-110">The application receives a pointer to a proxy object that marshals method calls across the process boundary.</span></span> <span data-ttu-id="ae374-111">Notez que la session de média PMP peut être utilisée pour lire du contenu clair, ainsi que du contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="ae374-111">Note that the PMP Media Session can be used to play clear content, as well as protected content.</span></span>

<span data-ttu-id="ae374-112">Toute application qui utilise la session multimédia suit les étapes générales suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae374-112">Any application that uses the Media Session will follow these general steps:</span></span>

1.  <span data-ttu-id="ae374-113">Créer une topologie.</span><span class="sxs-lookup"><span data-stu-id="ae374-113">Create a topology.</span></span>
2.  <span data-ttu-id="ae374-114">Met en file d’attente la topologie sur la session multimédia en appelant [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="ae374-114">Queue the topology on the Media Session by calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>
3.  <span data-ttu-id="ae374-115">Contrôlez le workflow de données en appelant [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession ::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)ou [**IMFMediaSession :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="ae374-115">Control the flow of data by calling [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause), or [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span>
4.  <span data-ttu-id="ae374-116">Avant de quitter l’application, appelez [**IMFMediaSession :: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) pour fermer la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae374-116">Before the application exits, call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the Media Session.</span></span>
5.  <span data-ttu-id="ae374-117">Arrêtez toutes les sources multimédias créées par l’application, en appelant [**IMFMediaSource :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span><span class="sxs-lookup"><span data-stu-id="ae374-117">Shut down any media sources that the application created, by calling [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown).</span></span>
6.  <span data-ttu-id="ae374-118">Arrêtez la session multimédia en appelant [**IMFMediaSession :: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="ae374-118">Shut down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span>

<span data-ttu-id="ae374-119">Lors de l’utilisation de la session multimédia, l’application ne doit pas démarrer, suspendre ou arrêter directement la source du média.</span><span class="sxs-lookup"><span data-stu-id="ae374-119">When using the Media Session, the application should not directly start, pause, or stop the media source.</span></span> <span data-ttu-id="ae374-120">Toutes les modifications d’État doivent être lancées en appelant les méthodes [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) .</span><span class="sxs-lookup"><span data-stu-id="ae374-120">All state changes must be initiated by calling [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) methods.</span></span> <span data-ttu-id="ae374-121">Les changements d’État dans la source du média sont gérés par la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae374-121">State changes in the media source are handled by the Media Session.</span></span>

<span data-ttu-id="ae374-122">De nombreux autres détails dépendent des fonctionnalités spécifiques de votre application.</span><span class="sxs-lookup"><span data-stu-id="ae374-122">Many other details will depend on the specific functionality of your application.</span></span>

## <a name="protected-content"></a><span data-ttu-id="ae374-123">Contenu protégé</span><span class="sxs-lookup"><span data-stu-id="ae374-123">Protected Content</span></span>

<span data-ttu-id="ae374-124">Pour lire du contenu protégé, vous devez créer la session multimédia à l’intérieur du chemin d’accès de média protégé (PMP), en appelant [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span><span class="sxs-lookup"><span data-stu-id="ae374-124">To play protected content, you must create the Media Session inside the protected media path (PMP), by calling [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession).</span></span> <span data-ttu-id="ae374-125">Cette fonction crée une instance de la session multimédia à l’intérieur de l’PMP et retourne un pointeur vers un objet proxy qui marshale les interfaces à travers la limite de processus.</span><span class="sxs-lookup"><span data-stu-id="ae374-125">This function creates an instance of the Media Session inside the PMP and returns a pointer to a proxy object that marshals interfaces across the process boundary.</span></span>

<span data-ttu-id="ae374-126">Dans la plupart des aspects, l’utilisation de la session multimédia à l’intérieur du PMP est transparente pour l’application.</span><span class="sxs-lookup"><span data-stu-id="ae374-126">In most respects, using the Media Session inside the PMP is transparent to the application.</span></span> <span data-ttu-id="ae374-127">Toutefois, l’application peut avoir besoin d’appeler certaines actions qui permettent à l’utilisateur de lire le contenu.</span><span class="sxs-lookup"><span data-stu-id="ae374-127">However, the application might need to invoke certain actions that enable the user to play the content.</span></span> <span data-ttu-id="ae374-128">Par exemple, l’utilisateur peut avoir besoin d’obtenir une licence DRM.</span><span class="sxs-lookup"><span data-stu-id="ae374-128">For example, the user might need to obtain a DRM license.</span></span> <span data-ttu-id="ae374-129">Media Foundation définit un mécanisme générique pour ces actions à l’aide de l’interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) .</span><span class="sxs-lookup"><span data-stu-id="ae374-129">Media Foundation defines a generic mechanism for these actions using the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface.</span></span>

<span data-ttu-id="ae374-130">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="ae374-130">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="ae374-131">Chemin du média protégé</span><span class="sxs-lookup"><span data-stu-id="ae374-131">Protected Media Path</span></span>](protected-media-path.md)
-   [<span data-ttu-id="ae374-132">Comment lire des fichiers multimédias protégés</span><span class="sxs-lookup"><span data-stu-id="ae374-132">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)

## <a name="presentation-clock"></a><span data-ttu-id="ae374-133">Horloge de présentation</span><span class="sxs-lookup"><span data-stu-id="ae374-133">Presentation Clock</span></span>

<span data-ttu-id="ae374-134">La session multimédia gère tous les aspects de l’horloge de présentation :</span><span class="sxs-lookup"><span data-stu-id="ae374-134">The Media Session manages all aspects of the presentation clock:</span></span>

-   <span data-ttu-id="ae374-135">Création de l’horloge de présentation.</span><span class="sxs-lookup"><span data-stu-id="ae374-135">Creating the presentation clock.</span></span>

-   <span data-ttu-id="ae374-136">Sélection de la source de temps.</span><span class="sxs-lookup"><span data-stu-id="ae374-136">Selecting the time source.</span></span>

-   <span data-ttu-id="ae374-137">Notification des récepteurs de médias sur l’horloge</span><span class="sxs-lookup"><span data-stu-id="ae374-137">Notifying the media sinks about the clock</span></span>

-   <span data-ttu-id="ae374-138">Le démarrage, l’arrêt et la suspension de l’horloge, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="ae374-138">Starting, stopping, and pausing the clock as necessary.</span></span>

-   <span data-ttu-id="ae374-139">Arrêt de l’horloge.</span><span class="sxs-lookup"><span data-stu-id="ae374-139">Shutting down the clock.</span></span>

<span data-ttu-id="ae374-140">Pour obtenir un pointeur vers l’horloge de présentation, appelez [**IMFMediaSession :: GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="ae374-140">To get a pointer to the presentation clock, call [**IMFMediaSession::GetClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) on the Media Session.</span></span> <span data-ttu-id="ae374-141">L’horloge de présentation ne retourne pas d’heure valide tant que la session multimédia n’envoie pas l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec l' \_ \_ indicateur prêt TOPOSTATUS Ready.</span><span class="sxs-lookup"><span data-stu-id="ae374-141">The presentation clock does not return a valid time until the Media Session sends the [MESessionTopologyStatus](mesessiontopologystatus.md) event with the MF\_TOPOSTATUS\_READY flag.</span></span> <span data-ttu-id="ae374-142">Jusqu’à présent, **GetClock** retourne MF \_ E \_ Clock \_ no \_ Time \_ source.</span><span class="sxs-lookup"><span data-stu-id="ae374-142">Until then, **GetClock** returns MF\_E\_CLOCK\_NO\_TIME\_SOURCE.</span></span>

<span data-ttu-id="ae374-143">Une application qui utilise la session de média ne doit jamais démarrer, arrêter ou suspendre l’horloge de la présentation ; modifier la fréquence d’horloge ; ou arrêtez l’horloge.</span><span class="sxs-lookup"><span data-stu-id="ae374-143">An application that uses the Media Session should never start, stop, or pause the presentation clock; change the clock rate; or shut down the clock.</span></span>

<span data-ttu-id="ae374-144">Lorsque l’application appelle [**IMFMediaSession :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), la session multimédia démarre l’horloge de la présentation avec une heure de début égale à la position de départ spécifiée dans la méthode **Start** .</span><span class="sxs-lookup"><span data-stu-id="ae374-144">When the application calls [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start), the Media Session starts the presentation clock with a starting time equal to the starting position specified in the **Start** method.</span></span> <span data-ttu-id="ae374-145">Pour plus d’informations sur la session multimédia, consultez [session multimédia](media-session.md).</span><span class="sxs-lookup"><span data-stu-id="ae374-145">For more information about the Media Session, see [Media Session](media-session.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae374-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae374-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae374-147">Session multimédia</span><span class="sxs-lookup"><span data-stu-id="ae374-147">Media Session</span></span>](media-session.md)
</dt> </dl>

 

 



