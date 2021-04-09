---
description: Utilisation des contrôles d’affichage vidéo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Utilisation des contrôles d’affichage vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753828"
---
# <a name="using-the-video-display-controls"></a><span data-ttu-id="002ba-103">Utilisation des contrôles d’affichage vidéo</span><span class="sxs-lookup"><span data-stu-id="002ba-103">Using the Video Display Controls</span></span>

<span data-ttu-id="002ba-104">L’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) contrôle la manière dont le convertisseur vidéo amélioré (EVR) affiche la vidéo à l’intérieur d’une fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="002ba-104">The [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface controls how the enhanced video renderer (EVR) displays video inside an application window.</span></span> <span data-ttu-id="002ba-105">Cette interface peut être utilisée dans DirectShow ou Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="002ba-105">This interface can be used in either DirectShow or Media Foundation.</span></span> <span data-ttu-id="002ba-106">En interne, les contrôles d’affichage vidéo sont fournis par le présentateur par défaut de EVR.</span><span class="sxs-lookup"><span data-stu-id="002ba-106">Internally, the video display controls are provided by the EVR's default presenter.</span></span> <span data-ttu-id="002ba-107">Si vous écrivez un présentateur personnalisé, vous pouvez fournir la même interface ou définir une interface personnalisée.</span><span class="sxs-lookup"><span data-stu-id="002ba-107">If you write a custom presenter, you can provide the same interface or define a custom interface.</span></span>

<span data-ttu-id="002ba-108">La méthode correcte pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) varie selon que vous utilisez la version DIRECTSHOW de EVR ou la version Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="002ba-108">The correct way to get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface depends on whether you are using the DirectShow version of the EVR or the Media Foundation version.</span></span> <span data-ttu-id="002ba-109">Pour le Media Foundation EVR, cela dépend également de l’utilisation directe du EVR ou de son utilisation par le biais de la session multimédia (qui est plus courante).</span><span class="sxs-lookup"><span data-stu-id="002ba-109">For the Media Foundation EVR, it also depends on whether you are using the EVR directly or using it through the Media Session (which is more typical).</span></span>

<span data-ttu-id="002ba-110">Pour obtenir un pointeur vers l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="002ba-110">To get a pointer to the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface, do the following:</span></span>

1.  <span data-ttu-id="002ba-111">Obtient un pointeur vers l’interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .</span><span class="sxs-lookup"><span data-stu-id="002ba-111">Get a pointer to the [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) interface.</span></span>

    -   <span data-ttu-id="002ba-112">Si vous utilisez le filtre DirectShow EVR, appelez **QueryInterface** sur le filtre.</span><span class="sxs-lookup"><span data-stu-id="002ba-112">If you are using the DirectShow EVR filter, call **QueryInterface** on the filter.</span></span>

    -   <span data-ttu-id="002ba-113">Si vous utilisez directement le récepteur multimédia EVR, appelez **QueryInterface** sur le récepteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="002ba-113">If you are using the EVR media sink directly, call **QueryInterface** on the media sink.</span></span>

    -   <span data-ttu-id="002ba-114">Si vous utilisez la session multimédia, appelez **QueryInterface** sur la session multimédia.</span><span class="sxs-lookup"><span data-stu-id="002ba-114">If you are using the Media Session, call **QueryInterface** on the Media Session.</span></span>

2.  <span data-ttu-id="002ba-115">Si vous utilisez la session de média, attendez que la session multimédia envoie l’événement [MESessionTopologyStatus](mesessiontopologystatus.md) avec la valeur d’État MF \_ TOPOSTATUS \_ Ready.</span><span class="sxs-lookup"><span data-stu-id="002ba-115">If you are using the Media Session, wait for the Media Session to send the [MESessionTopologyStatus](mesessiontopologystatus.md) event with a status value of MF\_TOPOSTATUS\_READY.</span></span> <span data-ttu-id="002ba-116">(Ignorez cette étape dans le cas contraire).</span><span class="sxs-lookup"><span data-stu-id="002ba-116">(Skip this step otherwise.)</span></span>

3.  <span data-ttu-id="002ba-117">Appelez [**IMFGetService :: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) pour accéder à l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) .</span><span class="sxs-lookup"><span data-stu-id="002ba-117">Call [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) to get the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface.</span></span> <span data-ttu-id="002ba-118">L’identificateur de service est un \_ service de rendu vidéo Mr \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="002ba-118">The service identifier is MR\_VIDEO\_RENDER\_SERVICE.</span></span>

<span data-ttu-id="002ba-119">Vous pouvez utiliser l’interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pour effectuer les tâches suivantes :</span><span class="sxs-lookup"><span data-stu-id="002ba-119">You can use the [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) interface to perform the following tasks:</span></span>

-   <span data-ttu-id="002ba-120">Définissez la fenêtre de découpage.</span><span class="sxs-lookup"><span data-stu-id="002ba-120">Set the clipping window.</span></span>

-   <span data-ttu-id="002ba-121">Définissez les rectangles source et de destination.</span><span class="sxs-lookup"><span data-stu-id="002ba-121">Set the source and destination rectangles.</span></span>

-   <span data-ttu-id="002ba-122">Mettez à jour la fenêtre vidéo en réponse aux messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="002ba-122">Update the video window in response to window messages.</span></span>

-   <span data-ttu-id="002ba-123">Activer ou désactiver le mode plein écran.</span><span class="sxs-lookup"><span data-stu-id="002ba-123">Enable or disable full-screen mode.</span></span>

## <a name="clipping-window"></a><span data-ttu-id="002ba-124">Fenêtre de découpage</span><span class="sxs-lookup"><span data-stu-id="002ba-124">Clipping Window</span></span>

<span data-ttu-id="002ba-125">L’application doit fournir une fenêtre dans laquelle le EVR dessine la vidéo.</span><span class="sxs-lookup"><span data-stu-id="002ba-125">The application must provide a window where the EVR draws the video.</span></span> <span data-ttu-id="002ba-126">Pour définir la fenêtre de découpage, appelez [**IMFVideoDisplayControl :: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) avec un handle vers la fenêtre d’application.</span><span class="sxs-lookup"><span data-stu-id="002ba-126">To set the clipping window, call [**IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) with a handle to the application window.</span></span>

<span data-ttu-id="002ba-127">Si vous créez le récepteur multimédia EVR par le biais de son objet d’activation, cette étape n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="002ba-127">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="002ba-128">L’objet d’activation appelle automatiquement [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)à l’aide du handle de fenêtre que vous avez fourni dans la fonction [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="002ba-128">The activation object automatically calls [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), using the window handle that you provided in the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span>

## <a name="source-and-destination-rectangles"></a><span data-ttu-id="002ba-129">Rectangles de source et de destination</span><span class="sxs-lookup"><span data-stu-id="002ba-129">Source and Destination Rectangles</span></span>

<span data-ttu-id="002ba-130">Pendant la lecture, le présentateur prend une partie de l’image vidéo composite et la dessine dans une zone de la fenêtre vidéo.</span><span class="sxs-lookup"><span data-stu-id="002ba-130">During playback, the presenter takes a portion of the composited video image and draws it onto an area of the video window.</span></span> <span data-ttu-id="002ba-131">La partie de l’image composite est le *rectangle source*, tandis que la zone de la fenêtre vidéo est le *rectangle de destination*.</span><span class="sxs-lookup"><span data-stu-id="002ba-131">The portion of the composited image is the *source rectangle*, and the area of the video window is the *destination rectangle*.</span></span>

<span data-ttu-id="002ba-132">Le rectangle source est défini à l’aide de coordonnées normalisées où le point (0,0, 0,0) correspond à l’angle supérieur gauche de la vidéo, et (1,0, 1,0) correspond au coin inférieur droit de la vidéo.</span><span class="sxs-lookup"><span data-stu-id="002ba-132">The source rectangle is defined using normalized coordinates where the point (0.0, 0.0) corresponds to the upper left corner of the video, and (1.0, 1.0) corresponds to the lower right corner of the video.</span></span> <span data-ttu-id="002ba-133">Le rectangle source peut être n’importe quelle région dans ce rectangle.</span><span class="sxs-lookup"><span data-stu-id="002ba-133">The source rectangle can be any region within this rectangle.</span></span> <span data-ttu-id="002ba-134">Le rectangle de destination est spécifié en pixels, par rapport à la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="002ba-134">The destination rectangle is specified in pixels, relative to the client area of the window.</span></span> <span data-ttu-id="002ba-135">Le rectangle source par défaut est la totalité de l’image, et le rectangle de destination par défaut est un rectangle vide.</span><span class="sxs-lookup"><span data-stu-id="002ba-135">The default source rectangle is the entire image, and the default destination rectangle is an empty rectangle.</span></span>

<span data-ttu-id="002ba-136">Pour définir les rectangles source et de destination, appelez [**IMFVideoDisplayControl :: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span><span class="sxs-lookup"><span data-stu-id="002ba-136">To set the source and destination rectangles, call [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).</span></span>

<span data-ttu-id="002ba-137">Si vous créez le récepteur multimédia EVR par le biais de son objet d’activation, cette étape n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="002ba-137">If you create the EVR media sink through its activation object, this step is not required.</span></span> <span data-ttu-id="002ba-138">L’objet d’activation définit automatiquement le rectangle de destination comme étant la totalité de la zone cliente de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="002ba-138">The activation object automatically sets the destination rectangle equal to the entire client area of the window.</span></span> <span data-ttu-id="002ba-139">Toutefois, vous devez appeler [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) si vous souhaitez modifier le rectangle source ou définir un autre rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="002ba-139">However, you should call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) if you want to change the source rectangle or set a different destination rectangle.</span></span>

## <a name="window-messages"></a><span data-ttu-id="002ba-140">Messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="002ba-140">Window Messages</span></span>

<span data-ttu-id="002ba-141">Pendant la lecture, votre application doit répondre à certains messages de fenêtre, comme suit :</span><span class="sxs-lookup"><span data-stu-id="002ba-141">During playback, your application should respond to certain window messages, as follows:</span></span>

-   <span data-ttu-id="002ba-142">WM \_ Paint : appelez [**IMFVideoDisplayControl :: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) pour repeindre la vidéo.</span><span class="sxs-lookup"><span data-stu-id="002ba-142">WM\_PAINT: Call [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) to repaint the video.</span></span> <span data-ttu-id="002ba-143">Évitez également de peindre sur le rectangle de destination pendant que la vidéo est lue, car cela peut provoquer un scintillement.</span><span class="sxs-lookup"><span data-stu-id="002ba-143">Also, avoid painting over the destination rectangle while video is playing, because this can cause flickering.</span></span>

-   <span data-ttu-id="002ba-144">\_Taille du WM : vous devrez peut-être appeler [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) pour redimensionner le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="002ba-144">WM\_SIZE: You might need to call [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) to resize the destination rectangle.</span></span>

<span data-ttu-id="002ba-145">Contrairement au filtre de convertisseur de mixage vidéo (VMR) dans DirectShow, il n’est pas nécessaire d’avertir le EVR quand vous recevez un \_ message WM DISPLAYCHANGE.</span><span class="sxs-lookup"><span data-stu-id="002ba-145">Unlike the Video Mixing Renderer (VMR) filter in DirectShow, you do not have to notify the EVR when you receive a WM\_DISPLAYCHANGE message.</span></span>

## <a name="related-topics"></a><span data-ttu-id="002ba-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="002ba-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="002ba-147">Convertisseur vidéo amélioré</span><span class="sxs-lookup"><span data-stu-id="002ba-147">Enhanced Video Renderer</span></span>](enhanced-video-renderer.md)
</dt> </dl>

 

 



