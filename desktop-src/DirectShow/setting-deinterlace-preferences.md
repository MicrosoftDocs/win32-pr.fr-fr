---
description: Définition des préférences de désentrelacement
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Définition des préférences de désentrelacement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745405"
---
# <a name="setting-deinterlace-preferences"></a><span data-ttu-id="13159-103">Définition des préférences de désentrelacement</span><span class="sxs-lookup"><span data-stu-id="13159-103">Setting Deinterlace Preferences</span></span>

<span data-ttu-id="13159-104">Le convertisseur de mixage vidéo (VMR) prend en charge l’entrelacement accéléré par le matériel, ce qui améliore la qualité de rendu de la vidéo entrelacée.</span><span class="sxs-lookup"><span data-stu-id="13159-104">The Video Mixing Renderer (VMR) supports hardware-accelerated deinterlacing, which improves rendering quality for interlaced video.</span></span> <span data-ttu-id="13159-105">Les fonctionnalités exactes disponibles dépendent du matériel sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="13159-105">The exact features that are available depend on the underlying hardware.</span></span> <span data-ttu-id="13159-106">L’application peut interroger les fonctionnalités de désentrelacement du matériel et définir des préférences de désentrelacement par le biais de l’interface [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) ou de l’interface [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9).</span><span class="sxs-lookup"><span data-stu-id="13159-106">The application can query for the hardware deinterlacing capabilities and set deinterlacing preferences through the [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) interface (VMR-7) or [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) interface (VMR-9).</span></span> <span data-ttu-id="13159-107">L’entrelacement est effectué sur une base par flux.</span><span class="sxs-lookup"><span data-stu-id="13159-107">Deinterlacing is performed on a per-stream basis.</span></span>

<span data-ttu-id="13159-108">Il existe une différence importante dans le comportement de l’entrelacement entre VMR-7 et VMR-9.</span><span class="sxs-lookup"><span data-stu-id="13159-108">There is one important difference in interlacing behavior between the VMR-7 and the VMR-9.</span></span> <span data-ttu-id="13159-109">Sur les systèmes où le matériel graphique ne prend pas en charge le désentrelacement avancé, VMR-7 peut revenir à la superposition matérielle et lui demander d’utiliser une désentrelacement de style BOB.</span><span class="sxs-lookup"><span data-stu-id="13159-109">On systems where the graphics hardware doesn't support advanced deinterlacing, the VMR-7 can fall back to the hardware overlay and instruct it to use a BOB style deinterlace.</span></span> <span data-ttu-id="13159-110">Dans ce cas, bien que VMR signale 30fps, la vidéo est en fait rendue à 60 bascule par seconde.</span><span class="sxs-lookup"><span data-stu-id="13159-110">In this case, although the VMR is reporting 30fps the video is actually being rendered at 60 flips per second.</span></span>

<span data-ttu-id="13159-111">Sauf dans le cas de VMR-7 utilisant la superposition matérielle, la désentrelacement est effectuée par le mixer de VMR.</span><span class="sxs-lookup"><span data-stu-id="13159-111">Except in the case of the VMR-7 using hardware overlay, deinterlacing is performed by the VMR's mixer.</span></span> <span data-ttu-id="13159-112">Le mélangeur utilise l’interface de pilote de périphérique (DDI) désentrelacement de DirectX Video Acceleration (DXVA) pour effectuer la désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="13159-112">The mixer uses the DirectX Video Acceleration (DXVA) deinterlacing device driver interface (DDI) to perform the deinterlacing.</span></span> <span data-ttu-id="13159-113">Cette interface DDI ne peut pas être appelée par les applications et les applications ne peuvent pas remplacer la fonctionnalité de désentrelacement de VMR.</span><span class="sxs-lookup"><span data-stu-id="13159-113">This DDI is not callable by applications, and applications cannot replace the VMR's deinterlacing functionality.</span></span> <span data-ttu-id="13159-114">Toutefois, une application peut sélectionner le mode de désentrelacement souhaité, comme décrit dans cette section.</span><span class="sxs-lookup"><span data-stu-id="13159-114">However, an application can select the desired deinterlacing mode, as described in this section.</span></span>

> [!Note]  
> <span data-ttu-id="13159-115">Cette section décrit les méthodes **IVMRDeinterlaceControl9** , mais les versions VMR-7 sont presque identiques.</span><span class="sxs-lookup"><span data-stu-id="13159-115">This section describes the **IVMRDeinterlaceControl9** methods, but the VMR-7 versions are almost identical.</span></span>

 

<span data-ttu-id="13159-116">Pour obtenir les capacités de désentrelacement d’un flux vidéo, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="13159-116">To get the deinterlacing capabilities for a video stream, do the following:</span></span>

1.  <span data-ttu-id="13159-117">Remplissez une structure [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) avec une description du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="13159-117">Fill in a [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) structure with a description of the video stream.</span></span> <span data-ttu-id="13159-118">Les détails du remplissage de cette structure sont fournis ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="13159-118">Details of how to fill in this structure are given later.</span></span>
2.  <span data-ttu-id="13159-119">Transmettez la structure à la méthode [**IVMRDeinterlaceControl9 :: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) .</span><span class="sxs-lookup"><span data-stu-id="13159-119">Pass the structure to the [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) method.</span></span> <span data-ttu-id="13159-120">Appelez la méthode à deux reprises.</span><span class="sxs-lookup"><span data-stu-id="13159-120">Call the method twice.</span></span> <span data-ttu-id="13159-121">Le premier appel retourne le nombre de modes de désentrelacement que le matériel prend en charge pour le format spécifié.</span><span class="sxs-lookup"><span data-stu-id="13159-121">The first call returns the number of deinterlace modes the hardware supports for the specified format.</span></span> <span data-ttu-id="13159-122">Allouez un tableau de GUID de cette taille et appelez à nouveau la méthode, en passant l’adresse du tableau.</span><span class="sxs-lookup"><span data-stu-id="13159-122">Allocate an array of GUIDs of this size, and call the method again, passing in the address of the array.</span></span> <span data-ttu-id="13159-123">Le deuxième appel remplit le tableau avec des GUID.</span><span class="sxs-lookup"><span data-stu-id="13159-123">The second call fills the array with GUIDs.</span></span> <span data-ttu-id="13159-124">Chaque GUID identifie un mode de désentrelacement.</span><span class="sxs-lookup"><span data-stu-id="13159-124">Each GUID identifies one deinterlacing mode.</span></span>
3.  <span data-ttu-id="13159-125">Pour obtenir le fonctionnalités d’un mode particulier, appelez la méthode [**IVMRDeinterlaceControl9 :: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) .</span><span class="sxs-lookup"><span data-stu-id="13159-125">To get the capabiltiies of a particular mode, call the [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) method.</span></span> <span data-ttu-id="13159-126">Transmettez la même structure **VMR9VideoDesc** , ainsi que l’un des GUID du tableau.</span><span class="sxs-lookup"><span data-stu-id="13159-126">Pass in the same **VMR9VideoDesc** structure, along with one of the GUIDs from the array.</span></span> <span data-ttu-id="13159-127">La méthode remplit une structure [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) avec les fonctionnalités du mode.</span><span class="sxs-lookup"><span data-stu-id="13159-127">The method fills a [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) structure with the mode capabilities.</span></span>

<span data-ttu-id="13159-128">Le code suivant illustre ces étapes :</span><span class="sxs-lookup"><span data-stu-id="13159-128">The following code shows these steps:</span></span>


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



<span data-ttu-id="13159-129">L’application peut désormais définir le mode de désentrelacement pour le flux, à l’aide des méthodes suivantes :</span><span class="sxs-lookup"><span data-stu-id="13159-129">Now the application can set the deinterlacing mode for the stream, using the following methods:</span></span>

-   <span data-ttu-id="13159-130">La méthode [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) définit le mode par défaut.</span><span class="sxs-lookup"><span data-stu-id="13159-130">The [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) method sets the preferred mode.</span></span> <span data-ttu-id="13159-131">Utilisez le GUID \_ null pour désactiver l’entrelacement.</span><span class="sxs-lookup"><span data-stu-id="13159-131">Use GUID\_NULL to turn off deinterlacing.</span></span>
-   <span data-ttu-id="13159-132">La méthode [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) spécifie le comportement si le mode demandé n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="13159-132">The [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) method specifies the behavior if the requested mode is not available.</span></span>
-   <span data-ttu-id="13159-133">La méthode [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) retourne le mode par défaut que vous définissez.</span><span class="sxs-lookup"><span data-stu-id="13159-133">The [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) method returns the preferred mode that you set.</span></span>
-   <span data-ttu-id="13159-134">La méthode [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) retourne le mode réel en cours d’utilisation, qui peut être un mode de secours, si le mode par défaut n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="13159-134">The [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) method returns the actual mode in use, which might be a fallback mode, if the preferred mode is not available.</span></span>

<span data-ttu-id="13159-135">Les pages de référence de méthode fournissent plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="13159-135">The method reference pages give more information.</span></span>

<span data-ttu-id="13159-136">**Utilisation de la structure VMR9VideoDesc**</span><span class="sxs-lookup"><span data-stu-id="13159-136">**Using the VMR9VideoDesc Structure**</span></span>

<span data-ttu-id="13159-137">Dans la procédure indiquée précédemment, la première étape consiste à remplir une structure **VMR9VideoDesc** avec une description du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="13159-137">In the procedure given previously, the first step is to fill in a **VMR9VideoDesc** structure with a description of the video stream.</span></span> <span data-ttu-id="13159-138">Commencez par obtenir le type de média du flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="13159-138">Start by getting the media type of the video stream.</span></span> <span data-ttu-id="13159-139">Pour ce faire, vous pouvez appeler [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) sur la broche d’entrée du filtre VMR.</span><span class="sxs-lookup"><span data-stu-id="13159-139">You can do this by calling [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) on the VMR filter's input pin.</span></span> <span data-ttu-id="13159-140">Vérifiez ensuite si le flux vidéo est entrelacé.</span><span class="sxs-lookup"><span data-stu-id="13159-140">Then confirm whether the video stream is interlaced.</span></span> <span data-ttu-id="13159-141">Seuls les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) peuvent être entrelacés.</span><span class="sxs-lookup"><span data-stu-id="13159-141">Only [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats can be interlaced.</span></span> <span data-ttu-id="13159-142">Si le type de format est \_ VIDEOINFO format, il doit s’agir d’une trame progressive.</span><span class="sxs-lookup"><span data-stu-id="13159-142">If the format type is FORMAT\_VideoInfo, it must be a progressive frame.</span></span> <span data-ttu-id="13159-143">Si le type de format est \_ VIDEOINFO2 format, recherchez l’indicateur ISINTERLACED AMINTERLACE dans le champ **dwInterlaceFlags** \_ .</span><span class="sxs-lookup"><span data-stu-id="13159-143">If the format type is FORMAT\_VideoInfo2, check the **dwInterlaceFlags** field for the AMINTERLACE\_IsInterlaced flag.</span></span> <span data-ttu-id="13159-144">La présence de cet indicateur indique que la vidéo est entrelacée.</span><span class="sxs-lookup"><span data-stu-id="13159-144">The presence of this flag indicates the video is interlaced.</span></span>

<span data-ttu-id="13159-145">Supposons que la variable **pBMI** est un pointeur vers la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="13159-145">Assume that the variable **pBMI** is a pointer to the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure in the format block.</span></span> <span data-ttu-id="13159-146">Définissez les valeurs suivantes dans la structure **VMR9VideoDesc** :</span><span class="sxs-lookup"><span data-stu-id="13159-146">Set the following values in the **VMR9VideoDesc** structure:</span></span>

-   <span data-ttu-id="13159-147">**dwSize nul**: définissez ce champ sur `sizeof(VMR9VideoDesc)` .</span><span class="sxs-lookup"><span data-stu-id="13159-147">**dwSize**: Set this field to `sizeof(VMR9VideoDesc)`.</span></span>
-   <span data-ttu-id="13159-148">**dwSampleWidth**: définissez ce champ sur `pBMI->biWidth` .</span><span class="sxs-lookup"><span data-stu-id="13159-148">**dwSampleWidth**: Set this field to `pBMI->biWidth`.</span></span>
-   <span data-ttu-id="13159-149">**dwSampleHeight**: définissez ce champ sur `abs(pBMI->biHeight)` .</span><span class="sxs-lookup"><span data-stu-id="13159-149">**dwSampleHeight**: Set this field to `abs(pBMI->biHeight)`.</span></span>
-   <span data-ttu-id="13159-150">**SampleFormat**: ce champ décrit les caractéristiques d’entrelacement du type de média.</span><span class="sxs-lookup"><span data-stu-id="13159-150">**SampleFormat**: This field describes the interlace characteristics of the media type.</span></span> <span data-ttu-id="13159-151">Vérifiez le champ **dwInterlaceFlags** dans la structure **VIDEOINFOHEADER2** et affectez à **SampleFormat** la valeur équivalente à l’indicateur [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) .</span><span class="sxs-lookup"><span data-stu-id="13159-151">Check the **dwInterlaceFlags** field in the **VIDEOINFOHEADER2** structure, and set **SampleFormat** equal to the equivalent [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) flag.</span></span> <span data-ttu-id="13159-152">Une fonction d’assistance pour effectuer cette opération est indiquée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="13159-152">A helper function to do this is given below.</span></span>
-   <span data-ttu-id="13159-153">**InputSampleFreq**: ce champ indique la fréquence d’entrée, qui peut être calculée à partir du champ **AvgTimePerFrame** de la structure **VIDEOINFOHEADER2** .</span><span class="sxs-lookup"><span data-stu-id="13159-153">**InputSampleFreq**: This field gives the input frequency, which can be calculated from the **AvgTimePerFrame** field in the **VIDEOINFOHEADER2** structure.</span></span> <span data-ttu-id="13159-154">Dans le cas général, affectez à **dwNumerator** la valeur 10 millions et à **DwDenominator** la valeur **AvgTimePerFrame**.</span><span class="sxs-lookup"><span data-stu-id="13159-154">In the general case, set **dwNumerator** to 10000000, and set **dwDenominator** to **AvgTimePerFrame**.</span></span> <span data-ttu-id="13159-155">Toutefois, vous pouvez également vérifier les fréquences d’images connues suivantes :</span><span class="sxs-lookup"><span data-stu-id="13159-155">However, you can also check for some well-known frame rates:</span></span>

    | <span data-ttu-id="13159-156">Temps moyen par frame</span><span class="sxs-lookup"><span data-stu-id="13159-156">Average time per frame</span></span> | <span data-ttu-id="13159-157">Fréquence d’images (FPS)</span><span class="sxs-lookup"><span data-stu-id="13159-157">Frame rate (fps)</span></span> | <span data-ttu-id="13159-158">Monnaie</span><span class="sxs-lookup"><span data-stu-id="13159-158">Numerator</span></span> | <span data-ttu-id="13159-159">Dénominateur</span><span class="sxs-lookup"><span data-stu-id="13159-159">Denominator</span></span> |
    |------------------------|------------------|-----------|-------------|
    | <span data-ttu-id="13159-160">166833</span><span class="sxs-lookup"><span data-stu-id="13159-160">166833</span></span>                 | <span data-ttu-id="13159-161">59,94 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="13159-161">59.94 (NTSC)</span></span>     | <span data-ttu-id="13159-162">60000</span><span class="sxs-lookup"><span data-stu-id="13159-162">60000</span></span>     | <span data-ttu-id="13159-163">1001</span><span class="sxs-lookup"><span data-stu-id="13159-163">1001</span></span>        |
    | <span data-ttu-id="13159-164">333667</span><span class="sxs-lookup"><span data-stu-id="13159-164">333667</span></span>                 | <span data-ttu-id="13159-165">29,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="13159-165">29.97 (NTSC)</span></span>     | <span data-ttu-id="13159-166">30000</span><span class="sxs-lookup"><span data-stu-id="13159-166">30000</span></span>     | <span data-ttu-id="13159-167">1001</span><span class="sxs-lookup"><span data-stu-id="13159-167">1001</span></span>        |
    | <span data-ttu-id="13159-168">417188</span><span class="sxs-lookup"><span data-stu-id="13159-168">417188</span></span>                 | <span data-ttu-id="13159-169">23,97 (NTSC)</span><span class="sxs-lookup"><span data-stu-id="13159-169">23.97 (NTSC)</span></span>     | <span data-ttu-id="13159-170">24 000</span><span class="sxs-lookup"><span data-stu-id="13159-170">24000</span></span>     | <span data-ttu-id="13159-171">1001</span><span class="sxs-lookup"><span data-stu-id="13159-171">1001</span></span>        |
    | <span data-ttu-id="13159-172">200000</span><span class="sxs-lookup"><span data-stu-id="13159-172">200000</span></span>                 | <span data-ttu-id="13159-173">50,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="13159-173">50.00 (PAL)</span></span>      | <span data-ttu-id="13159-174">50</span><span class="sxs-lookup"><span data-stu-id="13159-174">50</span></span>        | <span data-ttu-id="13159-175">1</span><span class="sxs-lookup"><span data-stu-id="13159-175">1</span></span>           |
    | <span data-ttu-id="13159-176">400000</span><span class="sxs-lookup"><span data-stu-id="13159-176">400000</span></span>                 | <span data-ttu-id="13159-177">25,00 (PAL)</span><span class="sxs-lookup"><span data-stu-id="13159-177">25.00 (PAL)</span></span>      | <span data-ttu-id="13159-178">25</span><span class="sxs-lookup"><span data-stu-id="13159-178">25</span></span>        | <span data-ttu-id="13159-179">1</span><span class="sxs-lookup"><span data-stu-id="13159-179">1</span></span>           |
    | <span data-ttu-id="13159-180">416667</span><span class="sxs-lookup"><span data-stu-id="13159-180">416667</span></span>                 | <span data-ttu-id="13159-181">24,00 (film)</span><span class="sxs-lookup"><span data-stu-id="13159-181">24.00 (Film)</span></span>     | <span data-ttu-id="13159-182">24</span><span class="sxs-lookup"><span data-stu-id="13159-182">24</span></span>        | <span data-ttu-id="13159-183">1</span><span class="sxs-lookup"><span data-stu-id="13159-183">1</span></span>           |

    

     

-   <span data-ttu-id="13159-184">**OutputFrameFreq**: ce champ indique la fréquence de sortie, qui peut être calculée à partir de la valeur **InputSampleFreq** et des caractéristiques d’entrelacement du flux d’entrée :</span><span class="sxs-lookup"><span data-stu-id="13159-184">**OutputFrameFreq**: This field gives the output frequency, which can be calculated from the **InputSampleFreq** value and the interleaving characteristics of the input stream:</span></span>
    -   <span data-ttu-id="13159-185">Définissez **OutputFrameFreq. dwDenominator** égal à **InputSampleFreq. dwDenominator**.</span><span class="sxs-lookup"><span data-stu-id="13159-185">Set **OutputFrameFreq.dwDenominator** equal to **InputSampleFreq.dwDenominator**.</span></span>
    -   <span data-ttu-id="13159-186">Si la vidéo d’entrée est entrelacée, définissez **OutputFrameFreq. dwNumerator** sur 2 x **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="13159-186">If the input video is interleaved, set **OutputFrameFreq.dwNumerator** to 2 x **InputSampleFreq.dwNumerator**.</span></span> <span data-ttu-id="13159-187">(Après désentrelacement, la fréquence d’images est doublée.) Sinon, définissez la valeur sur **InputSampleFreq. dwNumerator**.</span><span class="sxs-lookup"><span data-stu-id="13159-187">(After deinterlacing, the frame rate is doubled.) Otherwise, set the value to **InputSampleFreq.dwNumerator**.</span></span>
-   <span data-ttu-id="13159-188">**dwFourCC**: définissez ce champ sur `pBMI->biCompression` .</span><span class="sxs-lookup"><span data-stu-id="13159-188">**dwFourCC**: Set this field to `pBMI->biCompression`.</span></span>

<span data-ttu-id="13159-189">La fonction d’assistance suivante convertit les indicateurs AMINTERLACE \_ *X* en valeurs [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :</span><span class="sxs-lookup"><span data-stu-id="13159-189">The following helper function converts AMINTERLACE\_*X* flags to [**VMR9\_SampleFormat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) values:</span></span>


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



