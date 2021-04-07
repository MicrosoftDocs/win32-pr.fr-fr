---
description: Cette rubrique décrit comment une application peut modifier par programme les paramètres de l’image et de l’appareil photo sur un appareil de capture vidéo.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurer la qualité vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746053"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="39ce4-103">Configurer la qualité vidéo</span><span class="sxs-lookup"><span data-stu-id="39ce4-103">Configure the Video Quality</span></span>

<span data-ttu-id="39ce4-104">Cette rubrique décrit comment une application peut modifier par programme les paramètres de l’image et de l’appareil photo sur un appareil de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="39ce4-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="39ce4-105">Paramètres de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="39ce4-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="39ce4-106">Paramètres de la caméra</span><span class="sxs-lookup"><span data-stu-id="39ce4-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="39ce4-107">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39ce4-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="39ce4-108">Paramètres de ProcAmp</span><span class="sxs-lookup"><span data-stu-id="39ce4-108">ProcAmp Settings</span></span>

<span data-ttu-id="39ce4-109">Les caméras vidéo Windows Driver Model (WDM) peuvent prendre en charge des propriétés qui contrôlent la qualité de l’image :</span><span class="sxs-lookup"><span data-stu-id="39ce4-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="39ce4-110">Compensation du rétroéclairage</span><span class="sxs-lookup"><span data-stu-id="39ce4-110">Backlight compensation</span></span>
-   <span data-ttu-id="39ce4-111">Luminosité</span><span class="sxs-lookup"><span data-stu-id="39ce4-111">Brightness</span></span>
-   <span data-ttu-id="39ce4-112">Comparez</span><span class="sxs-lookup"><span data-stu-id="39ce4-112">Contrast</span></span>
-   <span data-ttu-id="39ce4-113">Maîtrise</span><span class="sxs-lookup"><span data-stu-id="39ce4-113">Gain</span></span>
-   <span data-ttu-id="39ce4-114">Gamma</span><span class="sxs-lookup"><span data-stu-id="39ce4-114">Gamma</span></span>
-   <span data-ttu-id="39ce4-115">Teinte</span><span class="sxs-lookup"><span data-stu-id="39ce4-115">Hue</span></span>
-   <span data-ttu-id="39ce4-116">Saturation</span><span class="sxs-lookup"><span data-stu-id="39ce4-116">Saturation</span></span>
-   <span data-ttu-id="39ce4-117">Netteté</span><span class="sxs-lookup"><span data-stu-id="39ce4-117">Sharpness</span></span>
-   <span data-ttu-id="39ce4-118">Balance des blancs</span><span class="sxs-lookup"><span data-stu-id="39ce4-118">White balance</span></span>

<span data-ttu-id="39ce4-119">Ces propriétés sont contrôlées par le biais de l’interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="39ce4-120">Utilisez cette interface comme suit :</span><span class="sxs-lookup"><span data-stu-id="39ce4-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="39ce4-121">Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le filtre de capture de l’interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="39ce4-122">Pour chaque propriété que vous souhaitez définir, appelez la méthode [**IAMVideoProcAmp :: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="39ce4-123">Les propriétés sont spécifiées par l’énumération [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="39ce4-124">Si la méthode **GetRange** échoue, cela signifie que l’appareil photo ne prend pas en charge cette propriété particulière.</span><span class="sxs-lookup"><span data-stu-id="39ce4-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="39ce4-125">Si [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) parvient, elle retourne la plage des valeurs prises en charge pour la propriété, la valeur par défaut et l’incrément minimal.</span><span class="sxs-lookup"><span data-stu-id="39ce4-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="39ce4-126">Pour obtenir la valeur actuelle d’une propriété, appelez [**IAMVideoProcAmp :: obtenir**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="39ce4-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="39ce4-127">Pour définir une propriété, appelez la méthode [**IAMVideoProcAmp :: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="39ce4-128">Pour restaurer la valeur par défaut d’une propriété, appelez [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) pour rechercher la valeur par défaut et passer cette valeur à la méthode **Set** .</span><span class="sxs-lookup"><span data-stu-id="39ce4-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="39ce4-129">Vous n’avez pas besoin d’arrêter le graphique de filtre lorsque vous définissez les propriétés.</span><span class="sxs-lookup"><span data-stu-id="39ce4-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="39ce4-130">Le code suivant configure un contrôle TrackBar afin qu’il puisse être utilisé pour définir la luminosité.</span><span class="sxs-lookup"><span data-stu-id="39ce4-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="39ce4-131">La plage du TrackBar correspond à la plage de luminosité prise en charge par l’appareil et la position du TrackBar correspond au paramètre de luminosité initiale de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="39ce4-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="39ce4-132">Paramètres de la caméra</span><span class="sxs-lookup"><span data-stu-id="39ce4-132">Camera Settings</span></span>

<span data-ttu-id="39ce4-133">L’interface [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) est similaire à [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), mais contrôle diverses positions sur l’appareil photo lui-même :</span><span class="sxs-lookup"><span data-stu-id="39ce4-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="39ce4-134">Exposition :</span><span class="sxs-lookup"><span data-stu-id="39ce4-134">Exposure</span></span>
-   <span data-ttu-id="39ce4-135">Priorité</span><span class="sxs-lookup"><span data-stu-id="39ce4-135">Focus</span></span>
-   <span data-ttu-id="39ce4-136">Iris</span><span class="sxs-lookup"><span data-stu-id="39ce4-136">Iris</span></span>
-   <span data-ttu-id="39ce4-137">Panoramique</span><span class="sxs-lookup"><span data-stu-id="39ce4-137">Pan</span></span>
-   <span data-ttu-id="39ce4-138">Group</span><span class="sxs-lookup"><span data-stu-id="39ce4-138">Roll</span></span>
-   <span data-ttu-id="39ce4-139">Tilt</span><span class="sxs-lookup"><span data-stu-id="39ce4-139">Tilt</span></span>
-   <span data-ttu-id="39ce4-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="39ce4-140">Zoom</span></span>

<span data-ttu-id="39ce4-141">Pour utiliser cette interface, suivez les mêmes étapes que celles utilisées pour [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span><span class="sxs-lookup"><span data-stu-id="39ce4-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="39ce4-142">Interrogez le filtre de capture pour [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span><span class="sxs-lookup"><span data-stu-id="39ce4-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="39ce4-143">Appelez [**IAMCameraControl :: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) pour rechercher les paramètres pris en charge, ainsi que la plage possible pour chaque paramètre.</span><span class="sxs-lookup"><span data-stu-id="39ce4-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="39ce4-144">Appelez [**IAMCameraControl :: obtenir**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) pour obtenir la valeur actuelle d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="39ce4-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="39ce4-145">Appelez [**IAMCameraControl :: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) pour définir la valeur.</span><span class="sxs-lookup"><span data-stu-id="39ce4-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39ce4-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="39ce4-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39ce4-147">Configuration d’un périphérique de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="39ce4-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
