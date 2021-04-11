---
title: Modes d’aperçu et de superposition
description: Modes d’aperçu et de superposition
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- Message WM_CAP_SET_PREVIEW
- capPreview macro)
- Message WM_CAP_SET_PREVIEWRATE
- capPreviewRate macro)
- Message WM_CAP_SET_SCALE
- capPreviewScale macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939851"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="af1a4-109">Modes d’aperçu et de superposition</span><span class="sxs-lookup"><span data-stu-id="af1a4-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="af1a4-110">Un pilote de capture peut implémenter deux méthodes pour afficher un flux vidéo entrant : le mode Aperçu et le mode superposition.</span><span class="sxs-lookup"><span data-stu-id="af1a4-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="af1a4-111">Si un pilote de capture implémente les deux méthodes, l’utilisateur peut choisir la méthode à utiliser.</span><span class="sxs-lookup"><span data-stu-id="af1a4-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="af1a4-112">Le mode aperçu transfère les images numérisées du matériel de capture à la mémoire système, puis affiche les images numérisées dans la fenêtre de capture à l’aide des fonctions GDI (Graphics Device Interface).</span><span class="sxs-lookup"><span data-stu-id="af1a4-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="af1a4-113">Les applications peuvent réduire le taux d’aperçu lorsque la fenêtre parente perd le focus et augmenter la vitesse d’aperçu lorsque la fenêtre parente obtient le focus.</span><span class="sxs-lookup"><span data-stu-id="af1a4-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="af1a4-114">Cette action améliore la réactivité générale du système, car l’opération de préversion est gourmande en ressources processeur.</span><span class="sxs-lookup"><span data-stu-id="af1a4-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="af1a4-115">Trois messages permettent de contrôler l’opération d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="af1a4-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="af1a4-116">Utilisez le message [**WM \_ Cap \_ Set \_ preview**](wm-cap-set-preview.md) pour activer ou désactiver le mode aperçu en envoyant (ou la macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="af1a4-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="af1a4-117">Utilisez le message [**WM \_ embout \_ Set \_ PREVIEWRATE**](wm-cap-set-previewrate.md) (ou la macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) pour définir la fréquence d’affichage des images en mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="af1a4-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="af1a4-118">Utilisez le message de mise à l' [**\_ \_ \_ échelle WM Cap Set**](wm-cap-set-scale.md) (ou la macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) pour activer ou désactiver la mise à l’échelle de la vidéo d’aperçu.</span><span class="sxs-lookup"><span data-stu-id="af1a4-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="af1a4-119">Lorsque l’aperçu et la mise à l’échelle sont activés, l’image vidéo capturée est étirée sur les dimensions de la fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="af1a4-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="af1a4-120">L’activation du mode aperçu désactive automatiquement le mode superposition.</span><span class="sxs-lookup"><span data-stu-id="af1a4-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="af1a4-121">Le mode superposition est une fonction matérielle qui affiche le contenu de la mémoire tampon de capture sur le moniteur sans utiliser les ressources du processeur.</span><span class="sxs-lookup"><span data-stu-id="af1a4-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="af1a4-122">Vous pouvez activer et désactiver le mode superposition en envoyant le message [**WM \_ Cap \_ Set \_ Overlay**](wm-cap-set-overlay.md) (ou la macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="af1a4-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="af1a4-123">L’activation du mode superposition désactive automatiquement le mode aperçu.</span><span class="sxs-lookup"><span data-stu-id="af1a4-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="af1a4-124">Vous pouvez également définir la position de défilement de la trame vidéo dans la zone cliente de la fenêtre de capture pour le mode aperçu ou le mode superposition en envoyant le message de [**\_ \_ \_ défilement WM Cap Set**](wm-cap-set-scroll.md) (ou la macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) à une fenêtre de capture.</span><span class="sxs-lookup"><span data-stu-id="af1a4-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




