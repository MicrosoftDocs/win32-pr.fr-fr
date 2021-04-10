---
title: Capture de Still-Image
description: Capture de Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- Message WM_CAP_GRAB_FRAME_NOSTOP
- Message WM_CAP_GRAB_FRAME
- capGrabFrameNoStop macro)
- capGrabFrame macro)
- Message WM_CAP_EDIT_COPY
- capEditCopy macro)
- Message WM_CAP_FILE_SAVEDIB
- capFileSaveDIB macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100669"
---
# <a name="still-image-capture"></a><span data-ttu-id="1792b-111">Capture de Still-Image</span><span class="sxs-lookup"><span data-stu-id="1792b-111">Still-Image Capture</span></span>

<span data-ttu-id="1792b-112">Si vous souhaitez capturer une image en tant qu’image fixe, vous pouvez utiliser le message de [**\_ \_ \_ trame**](wm-cap-grab-frame.md) de trame de manipulation de l’embout de la [**\_ \_ \_ plage \_ WM**](wm-cap-grab-frame-nostop.md) (ou la macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) ou [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ) pour capturer l’image numérisée dans une mémoire tampon de frame interne.</span><span class="sxs-lookup"><span data-stu-id="1792b-112">If you want to capture a single frame as a still image, you can use the [**WM\_CAP\_GRAB\_FRAME\_NOSTOP**](wm-cap-grab-frame-nostop.md) or [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message (or the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) or [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro) to capture the digitized image in an internal frame buffer.</span></span> <span data-ttu-id="1792b-113">Vous pouvez geler l’affichage sur l’image capturée à l’aide du cadre de manipulation de l' \_ embout WM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1792b-113">You can freeze the display on the captured image by using WM\_CAP\_GRAB\_FRAME.</span></span> <span data-ttu-id="1792b-114">Dans le cas contraire, utilisez WM \_ Cap- \_ \_ frame \_ nostop.</span><span class="sxs-lookup"><span data-stu-id="1792b-114">Otherwise, use WM\_CAP\_GRAB\_FRAME\_NOSTOP.</span></span>

<span data-ttu-id="1792b-115">Une fois capturés, vous pouvez copier l’image pour une utilisation par d’autres applications.</span><span class="sxs-lookup"><span data-stu-id="1792b-115">Once captured, you can copy the image for use by other applications.</span></span> <span data-ttu-id="1792b-116">Vous pouvez copier une image à partir de la mémoire tampon de frame dans le presse-papiers à l’aide du message [**WM \_ Cap \_ Edit \_ Copy**](wm-cap-edit-copy.md) (ou de la macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ).</span><span class="sxs-lookup"><span data-stu-id="1792b-116">You can copy an image from the frame buffer to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="1792b-117">Vous pouvez également copier l’image à partir de la mémoire tampon de frame vers une image bitmap indépendante du périphérique (DIB) à l’aide du message [**\_ \_ \_ SAVEDIB de fichier WM**](wm-cap-file-savedib.md) (ou de la macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).</span><span class="sxs-lookup"><span data-stu-id="1792b-117">You can also copy the image from the frame buffer to a device-independent bitmap (DIB) by using the [**WM\_CAP\_FILE\_SAVEDIB**](wm-cap-file-savedib.md) message (or the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro).</span></span>

<span data-ttu-id="1792b-118">Votre application peut également utiliser les deux messages de capture d’image unique pour modifier un frame de séquence par cadre, ou pour créer une séquence de photographie temporelle.</span><span class="sxs-lookup"><span data-stu-id="1792b-118">Your application can also use the two single-frame capture messages to edit a sequence frame by frame, or to create a time-lapse photography sequence.</span></span>

 

 




