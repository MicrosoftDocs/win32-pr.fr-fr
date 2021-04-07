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
# <a name="setting-deinterlace-preferences"></a>Définition des préférences de désentrelacement

Le convertisseur de mixage vidéo (VMR) prend en charge l’entrelacement accéléré par le matériel, ce qui améliore la qualité de rendu de la vidéo entrelacée. Les fonctionnalités exactes disponibles dépendent du matériel sous-jacent. L’application peut interroger les fonctionnalités de désentrelacement du matériel et définir des préférences de désentrelacement par le biais de l’interface [**IVMRDeinterlaceControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) ou de l’interface [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9). L’entrelacement est effectué sur une base par flux.

Il existe une différence importante dans le comportement de l’entrelacement entre VMR-7 et VMR-9. Sur les systèmes où le matériel graphique ne prend pas en charge le désentrelacement avancé, VMR-7 peut revenir à la superposition matérielle et lui demander d’utiliser une désentrelacement de style BOB. Dans ce cas, bien que VMR signale 30fps, la vidéo est en fait rendue à 60 bascule par seconde.

Sauf dans le cas de VMR-7 utilisant la superposition matérielle, la désentrelacement est effectuée par le mixer de VMR. Le mélangeur utilise l’interface de pilote de périphérique (DDI) désentrelacement de DirectX Video Acceleration (DXVA) pour effectuer la désentrelacement. Cette interface DDI ne peut pas être appelée par les applications et les applications ne peuvent pas remplacer la fonctionnalité de désentrelacement de VMR. Toutefois, une application peut sélectionner le mode de désentrelacement souhaité, comme décrit dans cette section.

> [!Note]  
> Cette section décrit les méthodes **IVMRDeinterlaceControl9** , mais les versions VMR-7 sont presque identiques.

 

Pour obtenir les capacités de désentrelacement d’un flux vidéo, procédez comme suit :

1.  Remplissez une structure [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) avec une description du flux vidéo. Les détails du remplissage de cette structure sont fournis ultérieurement.
2.  Transmettez la structure à la méthode [**IVMRDeinterlaceControl9 :: GetNumberOfDeinterlaceModes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) . Appelez la méthode à deux reprises. Le premier appel retourne le nombre de modes de désentrelacement que le matériel prend en charge pour le format spécifié. Allouez un tableau de GUID de cette taille et appelez à nouveau la méthode, en passant l’adresse du tableau. Le deuxième appel remplit le tableau avec des GUID. Chaque GUID identifie un mode de désentrelacement.
3.  Pour obtenir le fonctionnalités d’un mode particulier, appelez la méthode [**IVMRDeinterlaceControl9 :: GetDeinterlaceModeCaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) . Transmettez la même structure **VMR9VideoDesc** , ainsi que l’un des GUID du tableau. La méthode remplit une structure [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) avec les fonctionnalités du mode.

Le code suivant illustre ces étapes :


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



L’application peut désormais définir le mode de désentrelacement pour le flux, à l’aide des méthodes suivantes :

-   La méthode [**SetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) définit le mode par défaut. Utilisez le GUID \_ null pour désactiver l’entrelacement.
-   La méthode [**SetDeinterlacePrefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) spécifie le comportement si le mode demandé n’est pas disponible.
-   La méthode [**GetDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) retourne le mode par défaut que vous définissez.
-   La méthode [**GetActualDeinterlaceMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) retourne le mode réel en cours d’utilisation, qui peut être un mode de secours, si le mode par défaut n’est pas disponible.

Les pages de référence de méthode fournissent plus d’informations.

**Utilisation de la structure VMR9VideoDesc**

Dans la procédure indiquée précédemment, la première étape consiste à remplir une structure **VMR9VideoDesc** avec une description du flux vidéo. Commencez par obtenir le type de média du flux vidéo. Pour ce faire, vous pouvez appeler [**IPIN :: ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) sur la broche d’entrée du filtre VMR. Vérifiez ensuite si le flux vidéo est entrelacé. Seuls les formats [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) peuvent être entrelacés. Si le type de format est \_ VIDEOINFO format, il doit s’agir d’une trame progressive. Si le type de format est \_ VIDEOINFO2 format, recherchez l’indicateur ISINTERLACED AMINTERLACE dans le champ **dwInterlaceFlags** \_ . La présence de cet indicateur indique que la vidéo est entrelacée.

Supposons que la variable **pBMI** est un pointeur vers la structure [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) dans le bloc de format. Définissez les valeurs suivantes dans la structure **VMR9VideoDesc** :

-   **dwSize nul**: définissez ce champ sur `sizeof(VMR9VideoDesc)` .
-   **dwSampleWidth**: définissez ce champ sur `pBMI->biWidth` .
-   **dwSampleHeight**: définissez ce champ sur `abs(pBMI->biHeight)` .
-   **SampleFormat**: ce champ décrit les caractéristiques d’entrelacement du type de média. Vérifiez le champ **dwInterlaceFlags** dans la structure **VIDEOINFOHEADER2** et affectez à **SampleFormat** la valeur équivalente à l’indicateur [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) . Une fonction d’assistance pour effectuer cette opération est indiquée ci-dessous.
-   **InputSampleFreq**: ce champ indique la fréquence d’entrée, qui peut être calculée à partir du champ **AvgTimePerFrame** de la structure **VIDEOINFOHEADER2** . Dans le cas général, affectez à **dwNumerator** la valeur 10 millions et à **DwDenominator** la valeur **AvgTimePerFrame**. Toutefois, vous pouvez également vérifier les fréquences d’images connues suivantes :

    | Temps moyen par frame | Fréquence d’images (FPS) | Monnaie | Dénominateur |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59,94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29,97 (NTSC)     | 30000     | 1001        |
    | 417188                 | 23,97 (NTSC)     | 24 000     | 1001        |
    | 200000                 | 50,00 (PAL)      | 50        | 1           |
    | 400000                 | 25,00 (PAL)      | 25        | 1           |
    | 416667                 | 24,00 (film)     | 24        | 1           |

    

     

-   **OutputFrameFreq**: ce champ indique la fréquence de sortie, qui peut être calculée à partir de la valeur **InputSampleFreq** et des caractéristiques d’entrelacement du flux d’entrée :
    -   Définissez **OutputFrameFreq. dwDenominator** égal à **InputSampleFreq. dwDenominator**.
    -   Si la vidéo d’entrée est entrelacée, définissez **OutputFrameFreq. dwNumerator** sur 2 x **InputSampleFreq. dwNumerator**. (Après désentrelacement, la fréquence d’images est doublée.) Sinon, définissez la valeur sur **InputSampleFreq. dwNumerator**.
-   **dwFourCC**: définissez ce champ sur `pBMI->biCompression` .

La fonction d’assistance suivante convertit les indicateurs AMINTERLACE \_ *X* en valeurs [**\_ SampleFormat VMR9**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) :


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



 

 



