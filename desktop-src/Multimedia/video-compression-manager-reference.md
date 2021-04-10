---
title: Référence du gestionnaire de compression vidéo
description: Référence du gestionnaire de compression vidéo
ms.assetid: dd678b24-62af-495f-bdd6-3082c1a753dd
keywords:
- Video for Windows (VFW), Video Compression Manager (VCM)
- VFW (vidéo pour Windows), gestionnaire de compression vidéo (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801df7ecdf0f6468762c2742235d4ef627f5aee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190947"
---
# <a name="video-compression-manager-reference"></a><span data-ttu-id="cd956-105">Référence du gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="cd956-105">Video Compression Manager Reference</span></span>

<span data-ttu-id="cd956-106">Cette section décrit les fonctions, structures, messages et macros associés à VCM.</span><span class="sxs-lookup"><span data-stu-id="cd956-106">This section describes the functions, structures, messages, and macros, associated with VCM.</span></span> <span data-ttu-id="cd956-107">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="cd956-107">These elements are grouped as follows.</span></span>

## <a name="compressor-installation-and-removal"></a><span data-ttu-id="cd956-108">Installation et suppression du compresseur</span><span class="sxs-lookup"><span data-stu-id="cd956-108">Compressor Installation and Removal</span></span>

-   [<span data-ttu-id="cd956-109">**ICInstall**</span><span class="sxs-lookup"><span data-stu-id="cd956-109">**ICInstall**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icinstall)
-   [<span data-ttu-id="cd956-110">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="cd956-110">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="cd956-111">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="cd956-111">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="cd956-112">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="cd956-112">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)
-   [<span data-ttu-id="cd956-113">**ICRemove**</span><span class="sxs-lookup"><span data-stu-id="cd956-113">**ICRemove**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icremove)
-   [<span data-ttu-id="cd956-114">**ICOpenFunction**</span><span class="sxs-lookup"><span data-stu-id="cd956-114">**ICOpenFunction**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icopenfunction)

## <a name="locating-and-opening-a-compressor"></a><span data-ttu-id="cd956-115">Localisation et ouverture d’un compresseur</span><span class="sxs-lookup"><span data-stu-id="cd956-115">Locating and Opening a Compressor</span></span>

-   [<span data-ttu-id="cd956-116">**ICLocate**</span><span class="sxs-lookup"><span data-stu-id="cd956-116">**ICLocate**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iclocate)
-   [<span data-ttu-id="cd956-117">**ICOPEN**</span><span class="sxs-lookup"><span data-stu-id="cd956-117">**ICOPEN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icopen)
-   [<span data-ttu-id="cd956-118">**ICDecompressOpen**</span><span class="sxs-lookup"><span data-stu-id="cd956-118">**ICDecompressOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressopen)
-   [<span data-ttu-id="cd956-119">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="cd956-119">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="cd956-120">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="cd956-120">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="cd956-121">**ICClose**</span><span class="sxs-lookup"><span data-stu-id="cd956-121">**ICClose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icclose)

## <a name="selecting-compressors"></a><span data-ttu-id="cd956-122">Sélection de compresseurs</span><span class="sxs-lookup"><span data-stu-id="cd956-122">Selecting Compressors</span></span>

-   [<span data-ttu-id="cd956-123">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="cd956-123">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)
-   [<span data-ttu-id="cd956-124">**ICCompressorFree**</span><span class="sxs-lookup"><span data-stu-id="cd956-124">**ICCompressorFree**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorfree)
-   [<span data-ttu-id="cd956-125">**COMPVARS**</span><span class="sxs-lookup"><span data-stu-id="cd956-125">**COMPVARS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-compvars)

## <a name="configuring-compressors"></a><span data-ttu-id="cd956-126">Configuration des compresseurs</span><span class="sxs-lookup"><span data-stu-id="cd956-126">Configuring Compressors</span></span>

-   [<span data-ttu-id="cd956-127">**\_configuration ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-127">**ICM\_CONFIGURE**</span></span>](icm-configure.md)
-   [<span data-ttu-id="cd956-128">**\_GETSTATE ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-128">**ICM\_GETSTATE**</span></span>](icm-getstate.md)
-   [<span data-ttu-id="cd956-129">**de \_ la CCI.**</span><span class="sxs-lookup"><span data-stu-id="cd956-129">**ICM\_SETSTATE**</span></span>](icm-setstate.md)
-   [<span data-ttu-id="cd956-130">**ICSendMessage**</span><span class="sxs-lookup"><span data-stu-id="cd956-130">**ICSendMessage**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icsendmessage)

## <a name="compressor-information"></a><span data-ttu-id="cd956-131">Informations sur le compresseur</span><span class="sxs-lookup"><span data-stu-id="cd956-131">Compressor Information</span></span>

-   [<span data-ttu-id="cd956-132">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cd956-132">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="cd956-133">**ICINFO**</span><span class="sxs-lookup"><span data-stu-id="cd956-133">**ICINFO**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icinfo)
-   [<span data-ttu-id="cd956-134">**\_GETDEFAULTKEYFRAMERATE ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-134">**ICM\_GETDEFAULTKEYFRAMERATE**</span></span>](icm-getdefaultkeyframerate.md)
-   [<span data-ttu-id="cd956-135">**ICGetDisplayFormat**</span><span class="sxs-lookup"><span data-stu-id="cd956-135">**ICGetDisplayFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetdisplayformat)
-   [<span data-ttu-id="cd956-136">**\_GETDEFAULTQUALITY ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-136">**ICM\_GETDEFAULTQUALITY**</span></span>](icm-getdefaultquality.md)
-   [<span data-ttu-id="cd956-137">**ICM \_ à propos de**</span><span class="sxs-lookup"><span data-stu-id="cd956-137">**ICM\_ABOUT**</span></span>](icm-about.md)

## <a name="single-image-compression"></a><span data-ttu-id="cd956-138">Compression d’image unique</span><span class="sxs-lookup"><span data-stu-id="cd956-138">Single Image Compression</span></span>

-   [<span data-ttu-id="cd956-139">**ICImageCompress**</span><span class="sxs-lookup"><span data-stu-id="cd956-139">**ICImageCompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagecompress)

## <a name="sequence-compression"></a><span data-ttu-id="cd956-140">Compression de séquence</span><span class="sxs-lookup"><span data-stu-id="cd956-140">Sequence Compression</span></span>

-   [<span data-ttu-id="cd956-141">**ICSeqCompressFrame**</span><span class="sxs-lookup"><span data-stu-id="cd956-141">**ICSeqCompressFrame**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframe)
-   [<span data-ttu-id="cd956-142">**ICSeqCompressFrameStart**</span><span class="sxs-lookup"><span data-stu-id="cd956-142">**ICSeqCompressFrameStart**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframestart)
-   [<span data-ttu-id="cd956-143">**ICSeqCompressFrameEnd**</span><span class="sxs-lookup"><span data-stu-id="cd956-143">**ICSeqCompressFrameEnd**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icseqcompressframeend)

## <a name="compvars"></a><span data-ttu-id="cd956-144">COMPVARS</span><span class="sxs-lookup"><span data-stu-id="cd956-144">COMPVARS</span></span>

-   [<span data-ttu-id="cd956-145">**ICCompressorChoose**</span><span class="sxs-lookup"><span data-stu-id="cd956-145">**ICCompressorChoose**</span></span>](/windows/desktop/api/Vfw/nf-vfw-iccompressorchoose)

## <a name="image-data-compression"></a><span data-ttu-id="cd956-146">Compression des données d’image</span><span class="sxs-lookup"><span data-stu-id="cd956-146">Image Data Compression</span></span>

-   [<span data-ttu-id="cd956-147">**ICCOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="cd956-147">**ICCOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-iccompress)
-   [<span data-ttu-id="cd956-148">**FORMAT d’extraction de la \_ compression ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-148">**ICM\_COMPRESS\_GET\_FORMAT**</span></span>](icm-compress-get-format.md)
-   [<span data-ttu-id="cd956-149">**\_requête de compression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-149">**ICM\_COMPRESS\_QUERY**</span></span>](icm-compress-query.md)
-   [<span data-ttu-id="cd956-150">**taille d’extraction de la \_ compression ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-150">**ICM\_COMPRESS\_GET\_SIZE**</span></span>](icm-compress-get-size.md)
-   [<span data-ttu-id="cd956-151">**début de la \_ compression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-151">**ICM\_COMPRESS\_BEGIN**</span></span>](icm-compress-begin.md)
-   [<span data-ttu-id="cd956-152">**fin de la \_ compression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-152">**ICM\_COMPRESS\_END**</span></span>](icm-compress-end.md)

## <a name="compressor-monitoring"></a><span data-ttu-id="cd956-153">Analyse du compresseur</span><span class="sxs-lookup"><span data-stu-id="cd956-153">Compressor Monitoring</span></span>

-   [<span data-ttu-id="cd956-154">**ICSETSTATUSPROC**</span><span class="sxs-lookup"><span data-stu-id="cd956-154">**ICSETSTATUSPROC**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icsetstatusproc)

## <a name="decompressing-single-images"></a><span data-ttu-id="cd956-155">Décompression d’images uniques</span><span class="sxs-lookup"><span data-stu-id="cd956-155">Decompressing Single Images</span></span>

-   [<span data-ttu-id="cd956-156">**ICImageDecompress**</span><span class="sxs-lookup"><span data-stu-id="cd956-156">**ICImageDecompress**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icimagedecompress)

## <a name="decompressing-image-data"></a><span data-ttu-id="cd956-157">Décompression des données d’image</span><span class="sxs-lookup"><span data-stu-id="cd956-157">Decompressing Image Data</span></span>

-   [<span data-ttu-id="cd956-158">**ICDECOMPRESSEX**</span><span class="sxs-lookup"><span data-stu-id="cd956-158">**ICDECOMPRESSEX**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompressex)
-   [<span data-ttu-id="cd956-159">**ICDecompressExBegin**</span><span class="sxs-lookup"><span data-stu-id="cd956-159">**ICDecompressExBegin**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexbegin)
-   [<span data-ttu-id="cd956-160">**\_fin de DECOMPRESSEX ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-160">**ICM\_DECOMPRESSEX\_END**</span></span>](icm-decompressex-end.md)
-   [<span data-ttu-id="cd956-161">**FORMAT d’extraction de la \_ décompression ICM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-161">**ICM\_DECOMPRESS\_GET\_FORMAT**</span></span>](icm-decompress-get-format.md)
-   [<span data-ttu-id="cd956-162">**\_DÉcompresser \_ la \_ palette ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-162">**ICM\_DECOMPRESS\_GET\_PALETTE**</span></span>](icm-decompress-get-palette.md)
-   [<span data-ttu-id="cd956-163">**ICDecompressExQuery**</span><span class="sxs-lookup"><span data-stu-id="cd956-163">**ICDecompressExQuery**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdecompressexquery)
-   [<span data-ttu-id="cd956-164">**ICDECOMPRESS**</span><span class="sxs-lookup"><span data-stu-id="cd956-164">**ICDECOMPRESS**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdecompress)
-   [<span data-ttu-id="cd956-165">**début de la \_ décompression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-165">**ICM\_DECOMPRESS\_BEGIN**</span></span>](icm-decompress-begin.md)
-   [<span data-ttu-id="cd956-166">**\_fin de décompression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-166">**ICM\_DECOMPRESS\_END**</span></span>](icm-decompress-end.md)
-   [<span data-ttu-id="cd956-167">**\_requête de décompression ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-167">**ICM\_DECOMPRESS\_QUERY**</span></span>](icm-decompress-query.md)

## <a name="using-hardware-drawing-capabilities"></a><span data-ttu-id="cd956-168">Utilisation des fonctionnalités de Hardware-Drawing</span><span class="sxs-lookup"><span data-stu-id="cd956-168">Using Hardware-Drawing Capabilities</span></span>

-   [<span data-ttu-id="cd956-169">**ICGetInfo**</span><span class="sxs-lookup"><span data-stu-id="cd956-169">**ICGetInfo**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icgetinfo)
-   [<span data-ttu-id="cd956-170">**ICDRAWBEGIN**</span><span class="sxs-lookup"><span data-stu-id="cd956-170">**ICDRAWBEGIN**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdrawbegin)
-   [<span data-ttu-id="cd956-171">**\_fin de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-171">**ICM\_DRAW\_END**</span></span>](icm-draw-end.md)
-   [<span data-ttu-id="cd956-172">**\_vidage de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-172">**ICM\_DRAW\_FLUSH**</span></span>](icm-draw-flush.md)
-   [<span data-ttu-id="cd956-173">**requête ICM de \_ dessin \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-173">**ICM\_DRAW\_QUERY**</span></span>](icm-draw-query.md)
-   [<span data-ttu-id="cd956-174">**ICDrawSuggestFormat**</span><span class="sxs-lookup"><span data-stu-id="cd956-174">**ICDrawSuggestFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat)
-   [<span data-ttu-id="cd956-175">**\_début de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-175">**ICM\_DRAW\_START**</span></span>](icm-draw-start.md)
-   [<span data-ttu-id="cd956-176">**\_arrêter le dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-176">**ICM\_DRAW\_STOP**</span></span>](icm-draw-stop.md)
-   [<span data-ttu-id="cd956-177">**\_GETBUFFERSWANTED ICM**</span><span class="sxs-lookup"><span data-stu-id="cd956-177">**ICM\_GETBUFFERSWANTED**</span></span>](icm-getbufferswanted.md)
-   [<span data-ttu-id="cd956-178">**ICM- \_ créer \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-178">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="cd956-179">**ICDrawOpen**</span><span class="sxs-lookup"><span data-stu-id="cd956-179">**ICDrawOpen**</span></span>](/windows/desktop/api/Vfw/nf-vfw-icdrawopen)
-   [<span data-ttu-id="cd956-180">**ICDRAW**</span><span class="sxs-lookup"><span data-stu-id="cd956-180">**ICDRAW**</span></span>](/windows/desktop/api/Vfw/ns-vfw-icdraw)
-   [<span data-ttu-id="cd956-181">**ICM de \_ dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-181">**ICM\_DRAW\_GETTIME**</span></span>](icm-draw-gettime.md)
-   [<span data-ttu-id="cd956-182">**ICM \_ dessin \_ setTime**</span><span class="sxs-lookup"><span data-stu-id="cd956-182">**ICM\_DRAW\_SETTIME**</span></span>](icm-draw-settime.md)
-   [<span data-ttu-id="cd956-183">**\_fenêtre de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-183">**ICM\_DRAW\_WINDOW**</span></span>](icm-draw-window.md)
-   [<span data-ttu-id="cd956-184">**ICM- \_ créer \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-184">**ICM\_DRAW\_REALIZE**</span></span>](icm-draw-realize.md)
-   [<span data-ttu-id="cd956-185">**\_CHANGEPALETTE de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-185">**ICM\_DRAW\_CHANGEPALETTE**</span></span>](icm-draw-changepalette.md)
-   [<span data-ttu-id="cd956-186">**\_RENDERBUFFER de dessin ICM \_**</span><span class="sxs-lookup"><span data-stu-id="cd956-186">**ICM\_DRAW\_RENDERBUFFER**</span></span>](icm-draw-renderbuffer.md)

## <a name="related-topics"></a><span data-ttu-id="cd956-187">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cd956-187">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd956-188">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="cd956-188">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> </dl>

 

 




