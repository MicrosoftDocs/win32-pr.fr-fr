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
# <a name="configure-the-video-quality"></a>Configurer la qualité vidéo

Cette rubrique décrit comment une application peut modifier par programme les paramètres de l’image et de l’appareil photo sur un appareil de capture vidéo.

-   [Paramètres de ProcAmp](#procamp-settings)
-   [Paramètres de la caméra](#camera-settings)
-   [Rubriques connexes](#related-topics)

## <a name="procamp-settings"></a>Paramètres de ProcAmp

Les caméras vidéo Windows Driver Model (WDM) peuvent prendre en charge des propriétés qui contrôlent la qualité de l’image :

-   Compensation du rétroéclairage
-   Luminosité
-   Comparez
-   Maîtrise
-   Gamma
-   Teinte
-   Saturation
-   Netteté
-   Balance des blancs

Ces propriétés sont contrôlées par le biais de l’interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) . Utilisez cette interface comme suit :

1.  Appelez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le filtre de capture de l’interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .
2.  Pour chaque propriété que vous souhaitez définir, appelez la méthode [**IAMVideoProcAmp :: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) . Les propriétés sont spécifiées par l’énumération [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) . Si la méthode **GetRange** échoue, cela signifie que l’appareil photo ne prend pas en charge cette propriété particulière.
3.  Si [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) parvient, elle retourne la plage des valeurs prises en charge pour la propriété, la valeur par défaut et l’incrément minimal.
4.  Pour obtenir la valeur actuelle d’une propriété, appelez [**IAMVideoProcAmp :: obtenir**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Pour définir une propriété, appelez la méthode [**IAMVideoProcAmp :: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) . Pour restaurer la valeur par défaut d’une propriété, appelez [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) pour rechercher la valeur par défaut et passer cette valeur à la méthode **Set** .

Vous n’avez pas besoin d’arrêter le graphique de filtre lorsque vous définissez les propriétés.

Le code suivant configure un contrôle TrackBar afin qu’il puisse être utilisé pour définir la luminosité. La plage du TrackBar correspond à la plage de luminosité prise en charge par l’appareil et la position du TrackBar correspond au paramètre de luminosité initiale de l’appareil.


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



## <a name="camera-settings"></a>Paramètres de la caméra

L’interface [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) est similaire à [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), mais contrôle diverses positions sur l’appareil photo lui-même :

-   Exposition :
-   Priorité
-   Iris
-   Panoramique
-   Group
-   Tilt
-   Zoom

Pour utiliser cette interface, suivez les mêmes étapes que celles utilisées pour [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):

1.  Interrogez le filtre de capture pour [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).
2.  Appelez [**IAMCameraControl :: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) pour rechercher les paramètres pris en charge, ainsi que la plage possible pour chaque paramètre.
3.  Appelez [**IAMCameraControl :: obtenir**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) pour obtenir la valeur actuelle d’un paramètre.
4.  Appelez [**IAMCameraControl :: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) pour définir la valeur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Configuration d’un périphérique de capture vidéo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
