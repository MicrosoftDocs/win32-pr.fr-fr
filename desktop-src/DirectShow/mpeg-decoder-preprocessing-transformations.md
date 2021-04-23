---
description: Transformations de prétraitement du décodeur MPEG
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Transformations de prétraitement du décodeur MPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908897"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a><span data-ttu-id="8c931-103">Transformations de prétraitement du décodeur MPEG</span><span class="sxs-lookup"><span data-stu-id="8c931-103">MPEG Decoder Preprocessing Transformations</span></span>

<span data-ttu-id="8c931-104">**Bandes et PanScan**</span><span class="sxs-lookup"><span data-stu-id="8c931-104">**Letterbox and PanScan**</span></span>

<span data-ttu-id="8c931-105">L’image 4x3 peut être formée en remplissant le haut et le bas de l’image (appelée « image de la zone de bandes »), soit en extrayant une partie 4x3 de l’image (appelée image PanScan).</span><span class="sxs-lookup"><span data-stu-id="8c931-105">The 4x3 image can be formed by either padding the top and bottom of the image (referred to as a Letterbox image) or by extracting a 4x3 portion of the image (referred to as a PanScan image).</span></span> <span data-ttu-id="8c931-106">Les flux des menus et des sous-images sont superposés au-dessus de l’image vidéo finale.</span><span class="sxs-lookup"><span data-stu-id="8c931-106">The menus and subpicture streams are overlaid on top of the final video image.</span></span> <span data-ttu-id="8c931-107">Les images de rapport 16 x 9 sont stockées dans un format anamorphique 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-107">The 16x9 ratio images are stored in a 4x3 anamorphic format.</span></span> <span data-ttu-id="8c931-108">L’étirement de la vidéo source 720 x 480 de l’aspect 4x3 anamorphique en un proportions 16 x 9 forme l’image de l’aspect 16 x 9 d’origine.</span><span class="sxs-lookup"><span data-stu-id="8c931-108">Stretching the anamorphic 4x3 aspect ratio 720x480 source video to a 16x9 aspect ratio forms the original 16x9 aspect image.</span></span>

<span data-ttu-id="8c931-109">Vous trouverez ci-dessous une description de l’affichage correct de chacun des modes et de leurs points de vue :</span><span class="sxs-lookup"><span data-stu-id="8c931-109">Below is a description of how to correctly display each of the modes and their highlights:</span></span>

-   <span data-ttu-id="8c931-110">**Panoramique :** Vidéo source étirée dans la plus grande zone 16 x 9 de la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-110">**Widescreen:** The source video stretched into the largest 16x9 area of the output window.</span></span> <span data-ttu-id="8c931-111">Les surbrillances sont relatives à l’intérieur de la zone 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="8c931-111">The highlights are relative to the inside of the 16x9 area.</span></span> <span data-ttu-id="8c931-112">Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="8c931-112">Black bars should be added to either the top and bottom or to the sides to maintain a 16x9 area.</span></span>
-   <span data-ttu-id="8c931-113">**Analyse panoramique :** À partir de la vidéo 16 x 9, utilisez le décalage horizontal fourni dans le flux MPEG2 pour extraire une sous-fenêtre 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-113">**Pan Scan:** From the 16x9 video, use the horizontal offset provided in the MPEG2 stream to extract a 4x3 subwindow.</span></span> <span data-ttu-id="8c931-114">Placez la sous-fenêtre 4x3 dans la zone 4x3 la plus grande de la fenêtre cliente de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-114">Place the 4x3 subwindow into the largest 4x3 area of the output client window.</span></span> <span data-ttu-id="8c931-115">Les coordonnées de la surbrillance sont relatives à la fenêtre de sortie 4x3 et n’ont aucune relation avec la vidéo 16 x 9 source.</span><span class="sxs-lookup"><span data-stu-id="8c931-115">The highlight's coordinates are relative to the 4x3 output window and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="8c931-116">Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-116">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>
-   <span data-ttu-id="8c931-117">**Bandes de bandes :** Calculez la plus grande zone 4x3 de la fenêtre sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-117">**Letterbox:** Compute the largest 4x3 area of the output window.</span></span> <span data-ttu-id="8c931-118">Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-118">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span> <span data-ttu-id="8c931-119">La vidéo 4x3 anamorphique source (représentant une image 16 x 9) est placée dans la plus grande sous-fenêtre 16 x 9 à l’intérieur de la zone 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-119">The source anamorphic 4x3 video (representing a 16x9 image) is placed in the largest 16x9 subwindow inside of the 4x3 area.</span></span> <span data-ttu-id="8c931-120">Des barres noires doivent être ajoutées en haut et en bas de la sous-fenêtre pour tenir à jour une zone 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="8c931-120">Black bars should be added to the top and bottom of the subwindow to maintain a 16x9 area.</span></span> <span data-ttu-id="8c931-121">Les coordonnées de la surbrillance sont relatives à la zone 4x3 et n’ont aucune relation avec la vidéo 16 x 9 source.</span><span class="sxs-lookup"><span data-stu-id="8c931-121">The highlight's coordinates are relative to the 4x3 area and have no relationship to the source 16x9 video.</span></span> <span data-ttu-id="8c931-122">Un disque peut spécifier une mise en surbrillance qui se trouve en dehors de la zone 16 x 9 (mais toujours dans la fenêtre 4x3).</span><span class="sxs-lookup"><span data-stu-id="8c931-122">It is possible for a disk to specify a highlight that lies outside of the 16x9 area (but still in the 4x3 window).</span></span> <span data-ttu-id="8c931-123">Pour 4x3 vidéo, la vidéo est placée dans la zone de sortie 4x3 la plus grande de la fenêtre cliente de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-123">For 4x3 video, the video is placed in the largest 4x3 output area of the output client window.</span></span> <span data-ttu-id="8c931-124">Les barres noires doivent être ajoutées à la partie supérieure et inférieure, ou aux côtés pour maintenir une zone 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-124">Black bars should be added to either the top and bottom or to the sides to maintain a 4x3 area.</span></span>

<span data-ttu-id="8c931-125">**Prétraitement MPEG avec le navigateur DVD et VMR**</span><span class="sxs-lookup"><span data-stu-id="8c931-125">**MPEG preprocessing with the DVD Navigator and VMR**</span></span>

<span data-ttu-id="8c931-126">Actuellement, le décodeur reçoit un type de \_ média vidéo MPEG2 de format \_ (dont le bloc de format pointe vers une structure [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) ).</span><span class="sxs-lookup"><span data-stu-id="8c931-126">Currently, the decoder is passed a FORMAT\_MPEG2\_VIDEO media type (whose format block points to a [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) structure).</span></span> <span data-ttu-id="8c931-127">Sur les broches de sortie, le décodeur produit un \_ type de média VIDEOINFO2 format, dont le bloc de format pointe vers une structure [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) .</span><span class="sxs-lookup"><span data-stu-id="8c931-127">On the output pins, the decoder produces a FORMAT\_VideoInfo2 media type, whose format block points to a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure.</span></span> <span data-ttu-id="8c931-128">Le champ **dwReserved** de la structure a été renommé en indicateurs **dwControls** .</span><span class="sxs-lookup"><span data-stu-id="8c931-128">The structure's **dwReserved** field has been renamed to **dwControls** flags.</span></span>

<span data-ttu-id="8c931-129">Le membre **dwControlFlags** contient maintenant les nouveaux bits.</span><span class="sxs-lookup"><span data-stu-id="8c931-129">The **dwControlFlags** member will now contain the new bits.</span></span>



| <span data-ttu-id="8c931-130">Étiquette</span><span class="sxs-lookup"><span data-stu-id="8c931-130">Label</span></span> | <span data-ttu-id="8c931-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="8c931-131">Value</span></span> |
|--------------------------|------------|
| <span data-ttu-id="8c931-132">AMCONTROL \_ utilisé</span><span class="sxs-lookup"><span data-stu-id="8c931-132">AMCONTROL\_USED</span></span>          | <span data-ttu-id="8c931-133">0x00000001</span><span class="sxs-lookup"><span data-stu-id="8c931-133">0x00000001</span></span> |
| <span data-ttu-id="8c931-134">AMCONTROL \_ \_ à \_ 4x3</span><span class="sxs-lookup"><span data-stu-id="8c931-134">AMCONTROL\_PAD\_TO\_4x3</span></span>  | <span data-ttu-id="8c931-135">0x00000002</span><span class="sxs-lookup"><span data-stu-id="8c931-135">0x00000002</span></span> |
| <span data-ttu-id="8c931-136">AMCONTROL \_ \_ à \_ 16 x 9</span><span class="sxs-lookup"><span data-stu-id="8c931-136">AMCONTROL\_PAD\_TO\_16x9</span></span> | <span data-ttu-id="8c931-137">0x00000004</span><span class="sxs-lookup"><span data-stu-id="8c931-137">0x00000004</span></span> |



 

<span data-ttu-id="8c931-138">AMCONTROL \_ utilisé est utilisé pour tester si ces nouveaux indicateurs sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8c931-138">AMCONTROL\_USED is used to test whether these new flags are supported.</span></span> <span data-ttu-id="8c931-139">Un filtre source doit définir l' \_ indicateur AMCONTROL utilisé et voir si QueryAccept (MediaType) parvient au code pin en aval.</span><span class="sxs-lookup"><span data-stu-id="8c931-139">A source filter should set the AMCONTROL\_USED flag and see if QueryAccept(MediaType) succeeds on the downstream pin.</span></span> <span data-ttu-id="8c931-140">Si elle est rejetée, les indicateurs AMCONTROL ne peuvent pas être utilisés et dwReserved1 doit avoir la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="8c931-140">If it is rejected, then the AMCONTROL flags cannot be used and dwReserved1 must be set to 0.</span></span>

<span data-ttu-id="8c931-141">AMCONTROL \_ Pad \_ à \_ 4x3 indique que l’image doit être remplie et affichée dans une zone de 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-141">AMCONTROL\_PAD\_TO\_4x3 indicates that the image should be padded and displayed in a 4x3 area.</span></span>

<span data-ttu-id="8c931-142">AMCONTROL \_ Pad \_ à \_ 16 x 9 indique que l’image doit être remplie et affichée dans une zone de 16 x 9.</span><span class="sxs-lookup"><span data-stu-id="8c931-142">AMCONTROL\_PAD\_TO\_16x9 indicates that the image should be padded and displayed in a 16x9 area.</span></span>

<span data-ttu-id="8c931-143">Le décodeur doit soit copier, soit traiter en aveugle les bits.</span><span class="sxs-lookup"><span data-stu-id="8c931-143">The decoder should either blindly copy or process the bits.</span></span> <span data-ttu-id="8c931-144">Si le décodeur exécute cadre lui-même, il doit modifier les proportions de pixels, remplir l’image et supprimer les bits AMCONTROL correspondants \_ \* .</span><span class="sxs-lookup"><span data-stu-id="8c931-144">If the decoder performs letterboxing itself, then it must alter the pixel aspect ratio, pad the image and remove the corresponding AMCONTROL\_\* bits.</span></span>

<span data-ttu-id="8c931-145">MPEG2VIDEOINFO. dwFlags contient désormais trois indicateurs pour contrôler le mode d’affichage du contenu :</span><span class="sxs-lookup"><span data-stu-id="8c931-145">The MPEG2VIDEOINFO.dwFlags now contains three flags for controlling for controlling how the content should be displayed:</span></span>

-   <span data-ttu-id="8c931-146">`AMMPEG2_DoPanScan (0x00000001)`: Si cet indicateur est défini, le décodeur vidéo MPEG-2 doit rogner l’image de sortie en fonction de vecteurs d’analyse panoramique dans l’extension d’affichage des images \_ \_ et modifier les proportions de l’image en 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-146">`AMMPEG2_DoPanScan (0x00000001)`: If this flag is set, the MPEG-2 video decoder should crop the output image based on pan-scan vectors in picture\_display\_extension and change the picture aspect ratio to 4x3.</span></span> <span data-ttu-id="8c931-147">VMR ne doit pas recevoir un exemple 16 x 9 avec cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8c931-147">The VMR should not receive a 16x9 sample with this flag.</span></span> <span data-ttu-id="8c931-148">Une implémentation simple peut modifier le rectangle source pour indiquer une région source largeur 540 avec un bord gauche égal au décalage d’affichage dans l’extension d’affichage de l’image \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8c931-148">A simple implementation might alter the source rectangle to indicate a 540 wide source region with a left edge equal to the display offset in the picture\_display\_extension.</span></span>
-   <span data-ttu-id="8c931-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: Lorsqu’un décodeur matériel affiche ce flux dans une sortie vidéo (généralement un connecteur SVIDEO sur la carte), il doit appliquer les règles d’affichage d’un exemple 16 x 9 sur un 4x3 Display.</span><span class="sxs-lookup"><span data-stu-id="8c931-149">`AMMPEG2_LetterboxAnalogOut (0x00000020)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should apply the rules for displaying a 16x9 sample on a 4x3 display.</span></span>

    <span data-ttu-id="8c931-150">Un décodeur logiciel (ou un décodeur matériel produisant une sortie envoyée à VMR) a deux options lors du traitement des images :</span><span class="sxs-lookup"><span data-stu-id="8c931-150">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing images:</span></span>

    1.  <span data-ttu-id="8c931-151">Ignorez cet indicateur et passez le contenu VideoInfoHeader2 à VMR (l' \_ indicateur AMCONTROL Pad \_ to \_ 4x3 sera déjà défini par le [navigateur DVD](dvd-navigator-filter.md) sur l’exemple).</span><span class="sxs-lookup"><span data-stu-id="8c931-151">Ignore this flag and pass the VideoInfoHeader2 contents to the VMR (the AMCONTROL\_PAD\_TO\_4x3 flag will already be set by the [DVD Navigator](dvd-navigator-filter.md) on the sample).</span></span> <span data-ttu-id="8c931-152">VMR rencontre un exemple de vidéo 16 x 9 avec le bloc AMCONTROL \_ \_ pour l' \_ indicateur 4x3 et un flux de sous-image 4x3.</span><span class="sxs-lookup"><span data-stu-id="8c931-152">The VMR will encounter a 16x9 video sample with the AMCONTROL\_PAD\_TO\_4x3 flag set and a 4x3 subpicture stream.</span></span> <span data-ttu-id="8c931-153">L’application doit définir les rectangles de destination normalisés de sortie des deux flux pour qu’ils aient la même largeur.</span><span class="sxs-lookup"><span data-stu-id="8c931-153">The application must set the output normalized destination rectangles of the two streams to be the same width.</span></span>
    2.  <span data-ttu-id="8c931-154">Convertissez le flux anamorphique en image 4x3 en complétant le haut et le bas de l’image et en définissant les proportions de l’image sur 4x3 (voir la zone de la zone de rapport au-dessus), puis en supprimant le \_ bloc AMCONTROL \_ à \_ 4X3 bit du VIDEOINFOHEADER2.</span><span class="sxs-lookup"><span data-stu-id="8c931-154">Convert the anamorphic stream to a 4x3 image by padding the top and bottom of the image and setting the image aspect ratio to 4x3 (see Letterbox above) and removing the AMCONTROL\_PAD\_TO\_4x3 bit from the VIDEOINFOHEADER2.</span></span>

    <span data-ttu-id="8c931-155">Les décodeurs DirectXVA qui mélangent les flux vidéo et sous-image doivent traiter cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="8c931-155">DirectXVA decoders that blend the video and subpicture streams will have to process this flag.</span></span> <span data-ttu-id="8c931-156">Si le matériel ne peut pas mettre à l’échelle la sous-image fusionnée, le décodeur doit produire un flux de sous-image séparé pour VMR à mélanger avec la vidéo.</span><span class="sxs-lookup"><span data-stu-id="8c931-156">If the hardware cannot scale the blended subpicture, then the decoder should produce a separate subpicture stream for the VMR to blend with the video.</span></span>

-   <span data-ttu-id="8c931-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: Lorsqu’un décodeur matériel affiche ce flux dans une sortie vidéo (généralement un connecteur SVIDEO sur la carte), il doit supposer un affichage 16 x 9 (anamorphique).</span><span class="sxs-lookup"><span data-stu-id="8c931-157">`AMMPEG2_WidescreenAnalogOut (0x00000200)`: When a hardware decoder displays this stream to a video output (usually an SVIDEO connector on the card), it should assume a 16x9 (anamorphic) display.</span></span>

    <span data-ttu-id="8c931-158">Un décodeur logiciel (ou un décodeur matériel produisant une sortie envoyée à VMR) a deux options lors du traitement d’une image anamorphique :</span><span class="sxs-lookup"><span data-stu-id="8c931-158">A software decoder (or a hardware decoder producing output sent to the VMR) has two options when processing an anamorphic image:</span></span>

    1.  <span data-ttu-id="8c931-159">Ignorez cet indicateur et copiez le contenu VideoInfoHeader2 dans VMR.</span><span class="sxs-lookup"><span data-stu-id="8c931-159">Ignore this flag and copy the VideoInfoHeader2 contents to the VMR.</span></span> <span data-ttu-id="8c931-160">VMR remplira les images 4x3 à 16 x 9 s’ils disposent du \_ Pad AMCONTROL \_ pour \_ 16 x 9 défini.</span><span class="sxs-lookup"><span data-stu-id="8c931-160">The VMR will pad 4x3 images to 16x9 if they have the AMCONTROL\_PAD\_TO\_16x9 set.</span></span>
    2.  <span data-ttu-id="8c931-161">Remplissez l’image de sortie sur une image 16 x 9 et supprimez le \_ bloc AMCONTROL \_ pour \_ 16 x 9 bit.</span><span class="sxs-lookup"><span data-stu-id="8c931-161">Pad the output image to a 16x9 image and remove the AMCONTROL\_PAD\_TO\_16x9 bit.</span></span>

<span data-ttu-id="8c931-162">La plupart des décodeurs doivent utiliser **GetMediaType** pour détecter une modification de média sur la broche d’entrée et copier le contenu de **VIDEOINFOHEADER2** (contenu dans **MPEG2INFOHEADER**) sur la broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-162">Most decoders should use **GetMediaType** to detect a media change on the input pin and copy the **VIDEOINFOHEADER2** contents (contained in the **MPEG2INFOHEADER**) to the output pin.</span></span> <span data-ttu-id="8c931-163">Ils ne traiteront probablement que le bit PanScan.</span><span class="sxs-lookup"><span data-stu-id="8c931-163">They will probably only process the PanScan bit.</span></span>

<span data-ttu-id="8c931-164">L’exemple de code suivant montre comment copier le contenu **VIDEOINFOHEADER2** d’une broche d’entrée vers une broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="8c931-164">The following example code shows how to copy the **VIDEOINFOHEADER2** contents from an input pin to an output pin.</span></span>


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



