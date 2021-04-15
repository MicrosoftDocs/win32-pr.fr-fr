---
title: Vue d’ensemble des miniatures DWM
description: Gestionnaire de fenêtrage (DWM) permet d’afficher les représentations miniatures des fenêtres d’application.
ms.assetid: 6d71fcda-0cf0-463c-8c60-0415109d154f
keywords:
- Gestionnaire de fenêtrage (DWM), miniatures
- DWM (Gestionnaire de fenêtrage), miniatures
- Gestionnaire de fenêtrage (DWM), relations de miniatures
- DWM (Gestionnaire de fenêtrage), relations de miniatures
- miniatures
- relations de miniatures
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3e0f1e6875e447a18ff5e63d703460ff909b25
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/04/2021
ms.locfileid: "104556128"
---
# <a name="dwm-thumbnail-overview"></a><span data-ttu-id="aa336-109">Vue d’ensemble des miniatures DWM</span><span class="sxs-lookup"><span data-stu-id="aa336-109">DWM Thumbnail Overview</span></span>

<span data-ttu-id="aa336-110">Gestionnaire de fenêtrage (DWM) permet d’afficher les représentations miniatures des fenêtres d’application.</span><span class="sxs-lookup"><span data-stu-id="aa336-110">Desktop Window Manager (DWM) enables the display of thumbnail representations of application windows.</span></span> <span data-ttu-id="aa336-111">Il ne s’agit pas d’instantanés statiques d’une fenêtre, mais qui sont plutôt dynamiques, des connexions constantes entre une fenêtre source de miniatures et un emplacement sur une fenêtre de destination qui reçoit le rendu de miniatures dynamiques.</span><span class="sxs-lookup"><span data-stu-id="aa336-111">These are not static snapshots of a window, but are instead dynamic, constant connections between a thumbnail source window and a location on a destination window that receives the live thumbnail rendering.</span></span> <span data-ttu-id="aa336-112">Cela permet d’obtenir un aperçu rapide des applications en cours d’exécution en pointant sur l’application dans la barre des tâches ou en utilisant le mouvement de touche ALT-TAB pour voir et basculer rapidement vers une application.</span><span class="sxs-lookup"><span data-stu-id="aa336-112">This allows a quick view of running applications by hovering over the application on the taskbar or using the ALT-TAB key gesture to see and quickly switch to an application.</span></span>

<span data-ttu-id="aa336-113">L’image suivante illustre la miniature de Windows Vista en direct qui s’affiche lorsque vous pointez sur l’application dans la barre des tâches.</span><span class="sxs-lookup"><span data-stu-id="aa336-113">The following image illustrates the Windows Vista live thumbnail seen when you hover over the application on the taskbar.</span></span>

![Capture d’écran montrant la miniature D W M affichée lorsque vous pointez sur une application dans la barre des tâches.](images/dwm-livethumbnail.png)

<span data-ttu-id="aa336-115">L’image suivante illustre le Flip (onglet ALT) de Windows Vista activé par DWM.</span><span class="sxs-lookup"><span data-stu-id="aa336-115">The following image illustrates the Windows Vista Flip (ALT-TAB) enabled by DWM.</span></span>

![capture d’écran de l’onglet Alt activé pour DWM](images/dwm-flip.png)

> [!Note]  
> <span data-ttu-id="aa336-117">Les miniatures DWM n’autorisent pas les développeurs à créer des applications telles que la fonctionnalité Flip3D (onglet touche Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="aa336-117">DWM thumbnails do not enable developers to create applications like the Windows Vista Flip3D (WINKEY-TAB) feature.</span></span> <span data-ttu-id="aa336-118">Les miniatures sont rendues directement dans la fenêtre de destination en 2D.</span><span class="sxs-lookup"><span data-stu-id="aa336-118">Thumbnails are rendered directly to the destination window in 2-D.</span></span>

 

## <a name="dwm-thumbnail-relationships"></a><span data-ttu-id="aa336-119">Relations des miniatures DWM</span><span class="sxs-lookup"><span data-stu-id="aa336-119">DWM Thumbnail Relationships</span></span>

<span data-ttu-id="aa336-120">Pour afficher des miniatures dans votre application, vous devez d’abord établir une relation entre une fenêtre source et une fenêtre de destination.</span><span class="sxs-lookup"><span data-stu-id="aa336-120">To display thumbnails in your application, you must first establish a relationship between a source window and a destination window.</span></span> <span data-ttu-id="aa336-121">Pour ce faire, appelez la fonction [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="aa336-121">This is done by calling the [**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) function.</span></span>

<span data-ttu-id="aa336-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) n’affiche pas de miniature sur la fenêtre de destination, mais crée simplement la relation et fournit la poignée de miniature.</span><span class="sxs-lookup"><span data-stu-id="aa336-122">[**DwmRegisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmregisterthumbnail) does not render a thumbnail on the destination window but merely creates the relationship and provides the thumbnail handle.</span></span> <span data-ttu-id="aa336-123">La miniature est rendue une fois que les [**\_ \_ Propriétés de miniature DWM**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) ont été définies et que la fonction [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) a été appelée.</span><span class="sxs-lookup"><span data-stu-id="aa336-123">The thumbnail is rendered after the [**DWM\_THUMBNAIL\_PROPERTIES**](/windows/desktop/api/Dwmapi/ns-dwmapi-dwm_thumbnail_properties) have been set and the [**DwmUpdateThumbnailProperties**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmupdatethumbnailproperties) function has been called.</span></span> <span data-ttu-id="aa336-124">Les appels suivants à **DwmUpdateThumbnailProperties** mettent à jour la miniature avec un nouvel ensemble de propriétés.</span><span class="sxs-lookup"><span data-stu-id="aa336-124">Subsequent calls to **DwmUpdateThumbnailProperties** update the thumbnail with a new set of properties.</span></span> <span data-ttu-id="aa336-125">Le DWM fournit également la fonction d’assistance [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) pour obtenir la taille de la fenêtre source à partir de la miniature.</span><span class="sxs-lookup"><span data-stu-id="aa336-125">The DWM also provides the helper function [**DwmQueryThumbnailSourceSize**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize) to obtain the size of the source window from the thumbnail.</span></span>

<span data-ttu-id="aa336-126">Pour mettre fin à une relation de miniatures, appelez la fonction [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) .</span><span class="sxs-lookup"><span data-stu-id="aa336-126">To end a thumbnail relationship, call the [**DwmUnregisterThumbnail**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmunregisterthumbnail) function.</span></span>

<span data-ttu-id="aa336-127">L’exemple suivant montre comment créer un releationship avec le bureau Windows et l’afficher dans une application.</span><span class="sxs-lookup"><span data-stu-id="aa336-127">The following example demonstrates how to create a releationship with the Windows desktop and display it in an application.</span></span>


```
HRESULT hr = S_OK;
HTHUMBNAIL thumbnail = NULL;

// Register the thumbnail
hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
if (SUCCEEDED(hr))
{
    // Specify the destination rectangle size
    RECT dest = {0,50,100,150};

    // Set the thumbnail properties for use
    DWM_THUMBNAIL_PROPERTIES dskThumbProps;
    dskThumbProps.dwFlags = DWM_TNP_SOURCECLIENTAREAONLY | DWM_TNP_VISIBLE | DWM_TNP_OPACITY | DWM_TNP_RECTDESTINATION;
    dskThumbProps.fSourceClientAreaOnly = FALSE; 
    dskThumbProps.fVisible = TRUE;
    dskThumbProps.opacity = (255 * 70)/100;
    dskThumbProps.rcDestination = dest;

    // Display the thumbnail
    hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
    if (SUCCEEDED(hr))
    {
        // ...
    }
}
return hr;
```



## <a name="related-topics"></a><span data-ttu-id="aa336-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa336-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa336-129">Vue d’ensemble du Gestionnaire de fenêtres du Bureau</span><span class="sxs-lookup"><span data-stu-id="aa336-129">Desktop Window Manager Overview</span></span>](dwm-overview.md)
</dt> <dt>

[<span data-ttu-id="aa336-130">Activer et contrôler la composition du Gestionnaire de fenêtrage</span><span class="sxs-lookup"><span data-stu-id="aa336-130">Enable and Control DWM Composition</span></span>](composition-ovw.md)
</dt> <dt>

[<span data-ttu-id="aa336-131">Considérations sur les performances et meilleures pratiques</span><span class="sxs-lookup"><span data-stu-id="aa336-131">Performance Considerations and Best Practices</span></span>](bestpractices-ovw.md)
</dt> </dl>

 

 




