---
title: Boîtes de dialogue vidéo
description: Boîtes de dialogue vidéo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- Message WM_CAP_DLG_VIDEOSOURCE
- capDlgVideoSource macro)
- Message WM_CAP_DLG_VIDEOFORMAT
- capDlgVideoFormat macro)
- Message WM_CAP_DLG_VIDEODISPLAY
- capDlgVideoDisplay macro)
- Message WM_CAP_DLG_VIDEOCOMPRESSION
- capDlgVideoCompression macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106530075"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="9a011-111">Boîtes de dialogue vidéo</span><span class="sxs-lookup"><span data-stu-id="9a011-111">Video Dialog Boxes</span></span>

<span data-ttu-id="9a011-112">Chaque pilote de capture peut fournir jusqu’à quatre boîtes de dialogue pour contrôler les aspects du processus de numérisation et de capture vidéo, et pour définir des attributs de compression utilisés pour réduire la taille des données vidéo.</span><span class="sxs-lookup"><span data-stu-id="9a011-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="9a011-113">Le contenu de ces boîtes de dialogue est défini par le pilote de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="9a011-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="9a011-114">La boîte de dialogue source vidéo contrôle la sélection des canaux d’entrée vidéo et des paramètres affectant l’image vidéo en cours de numérisation dans la mémoire tampon de trame.</span><span class="sxs-lookup"><span data-stu-id="9a011-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="9a011-115">Cette boîte de dialogue énumère les types de signaux qui connectent la source vidéo à la carte de capture (généralement les entrées SVHS et composite) et fournit des contrôles pour modifier la teinte, le contraste ou la saturation.</span><span class="sxs-lookup"><span data-stu-id="9a011-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="9a011-116">Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOSOURCE**](wm-cap-dlg-videosource.md) (ou de la macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).</span><span class="sxs-lookup"><span data-stu-id="9a011-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="9a011-117">La boîte de dialogue Format vidéo contrôle la sélection des dimensions de l’image numérisée et de la profondeur de l’image, ainsi que des options de compression de la vidéo capturée.</span><span class="sxs-lookup"><span data-stu-id="9a011-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="9a011-118">Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou de la macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).</span><span class="sxs-lookup"><span data-stu-id="9a011-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="9a011-119">La boîte de dialogue affichage vidéo contrôle l’apparence de la vidéo sur le moniteur pendant la capture.</span><span class="sxs-lookup"><span data-stu-id="9a011-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="9a011-120">Les contrôles de cette boîte de dialogue n’ont aucun effet sur les données numérisées de la vidéo, mais elles peuvent affecter la présentation du signal numérisé.</span><span class="sxs-lookup"><span data-stu-id="9a011-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="9a011-121">Par exemple, les appareils de capture qui prennent en charge la superposition peuvent permettre de modifier la teinte et la saturation, la couleur de la clé ou l’alignement de la superposition.</span><span class="sxs-lookup"><span data-stu-id="9a011-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="9a011-122">Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) (ou de la macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).</span><span class="sxs-lookup"><span data-stu-id="9a011-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="9a011-123">La boîte de dialogue compression vidéo contrôle les attributs de compression vidéo postérieurs à la capture.</span><span class="sxs-lookup"><span data-stu-id="9a011-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="9a011-124">Si la boîte de dialogue est prise en charge par un pilote de capture vidéo, vous pouvez l’afficher et la mettre à jour à l’aide du message [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) (ou de la macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).</span><span class="sxs-lookup"><span data-stu-id="9a011-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




