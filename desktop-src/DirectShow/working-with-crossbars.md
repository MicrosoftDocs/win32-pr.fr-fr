---
description: Utilisation des conversions
ms.assetid: 6e8ee9c3-6776-498b-ad38-36f8172a27ae
title: Utilisation des conversions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53686250b423c0bed245650be604fd8ec4b6a6ce713e5cde8582c66c8c4dc88f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964439"
---
# <a name="working-with-crossbars"></a>Utilisation des conversions

Si une carte de capture vidéo a plusieurs entrées physiques, ou si elle prend en charge plusieurs chemins d’accès matériels pour les données, le graphique de filtre peut contenir le filtre de la barre d' [affichage vidéo analogique](analog-video-crossbar-filter.md). le générateur de Graph de Capture ajoute automatiquement ce filtre si nécessaire. il sera amont du filtre de capture. Selon le matériel, le graphique de filtre peut contenir plusieurs instances du filtre de la barre.

Le filtre de distributeur expose l’interface [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar) , que vous pouvez utiliser pour acheminer une entrée particulière vers une sortie particulière. Par exemple, une carte vidéo peut avoir un connecteur coaxial et une entrée S-Video. Celles-ci sont représentées en tant que broches d’entrée sur le filtre de la barre. Pour sélectionner une entrée, acheminez la broche d’entrée correspondante vers la broche de sortie du distributeur, à l’aide de la méthode [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

Pour rechercher des filtres de barre dans le graphique, vous pouvez utiliser la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) pour rechercher des filtres qui prennent en charge **IAMCrossbar**. Par exemple, le code suivant recherche deux transformateurs :


```C++
// Search upstream for a crossbar.
IAMCrossbar *pXBar1 = NULL;
hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pSrc,
        IID_IAMCrossbar, (void**)&pXBar1);
if (SUCCEEDED(hr)) 
{
    // Found one crossbar. Get its IBaseFilter interface.
    IBaseFilter *pFilter = NULL;
    hr = pXBar1->QueryInterface(IID_IBaseFilter, (void**)&pFilter);
    if (SUCCEEDED(hr)) 
    {
        // Search upstream for another crossbar.
        IAMCrossbar *pXBar2 = NULL;
        hr = pBuild->FindInterface(&LOOK_UPSTREAM_ONLY, NULL, pFilter,
                 IID_IAMCrossbar, (void**)&pXBar2);
        pFilter->Release();

        if (SUCCEEDED(hr))
        {
            /* ... */
            pXBar2->Release();
        }
    }
    pXBar1->Release();
}
```



Pour une approche plus généralisée, consultez la classe CCrossbar dans l' [exemple AMCAP](amcap-sample.md).

Une fois que vous avez un pointeur vers l’interface **IAMCrossbar** , vous pouvez obtenir des informations sur le filtre de la barre, y compris le type physique de chaque pin, et la matrice de laquelle les broches d’entrée peuvent être routées vers les broches de sortie.

-   Pour déterminer le type de connecteur physique auquel correspond un code confidentiel, appelez la méthode [**IAMCrossbar :: obtenir \_ CrossbarPinInfo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_crossbarpininfo) . La méthode retourne un membre de l’énumération [**PhysicalConnectorType**](/windows/win32/api/strmif/ne-strmif-physicalconnectortype) . Par exemple, un code confidentiel S-Video retourne la valeur PhysConn \_ Video \_ SVIDEO.

    La méthode d' **extraction \_ CrossbarInfo** indique également si deux broches sont liées les unes aux autres. Par exemple, un code confidentiel vidéo peut être associé à un code confidentiel audio. Les broches associées ont le même sens du code confidentiel et font généralement partie du même connecteur ou de la même prise physique sur la carte.

-   Pour déterminer si vous pouvez acheminer une broche d’entrée vers une broche de sortie particulière, appelez la méthode [**IAMCrossbar :: CanRoute**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-canroute) .
-   Pour déterminer le routage actuel entre les codes confidentiels, appelez la méthode [**IAMCrossbar :: obtenir \_ IsRoutedTo**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-get_isroutedto) .

Les méthodes précédentes spécifient toutes les broches par numéro d’index, les broches de sortie et les broches d’entrée étant indexées à partir de zéro. Appelez la méthode **IAMCrossbar :: obtenir \_ PinCounts** pour rechercher le nombre de broches sur le filtre.

Par exemple, le code suivant affiche des informations sur un filtre de barre transversale dans la fenêtre de console :


```C++
// Helper function to associate a name with the type.
const char * GetPhysicalPinName(long lType)
{
    switch (lType) 
    {
    case PhysConn_Video_Tuner:            return "Video Tuner";
    case PhysConn_Video_Composite:        return "Video Composite";
    case PhysConn_Video_SVideo:           return "S-Video";
    case PhysConn_Video_RGB:              return "Video RGB";
    case PhysConn_Video_YRYBY:            return "Video YRYBY";
    case PhysConn_Video_SerialDigital:    return "Video Serial Digital";
    case PhysConn_Video_ParallelDigital:  return "Video Parallel Digital"; 
    case PhysConn_Video_SCSI:             return "Video SCSI";
    case PhysConn_Video_AUX:              return "Video AUX";
    case PhysConn_Video_1394:             return "Video 1394";
    case PhysConn_Video_USB:              return "Video USB";
    case PhysConn_Video_VideoDecoder:     return "Video Decoder";
    case PhysConn_Video_VideoEncoder:     return "Video Encoder";
        
    case PhysConn_Audio_Tuner:            return "Audio Tuner";
    case PhysConn_Audio_Line:             return "Audio Line";
    case PhysConn_Audio_Mic:              return "Audio Microphone";
    case PhysConn_Audio_AESDigital:       return "Audio AES/EBU Digital";
    case PhysConn_Audio_SPDIFDigital:     return "Audio S/PDIF";
    case PhysConn_Audio_SCSI:             return "Audio SCSI";
    case PhysConn_Audio_AUX:              return "Audio AUX";
    case PhysConn_Audio_1394:             return "Audio 1394";
    case PhysConn_Audio_USB:              return "Audio USB";
    case PhysConn_Audio_AudioDecoder:     return "Audio Decoder";
        
    default:                              return "Unknown Type";
    }    
}

void DisplayCrossbarInfo(IAMCrossbar *pXBar)
{
    HRESULT hr;
    long cOutput = -1, cInput = -1;
    hr = pXBar->get_PinCounts(&cOutput, &cInput);

    for (long i = 0; i < cOutput; i++)
    {
        long lRelated = -1, lType = -1, lRouted = -1;

        hr = pXBar->get_CrossbarPinInfo(FALSE, i, &lRelated, &lType);
        hr = pXBar->get_IsRouted(i, &lRouted);

        printf("Output pin %d: %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated out: %d, Routed in: %d\n", lRelated, lRouted);
        printf("\tSwitching Matrix: ");

        for (long j = 0; j < cInput; j++)
        {
            hr = pXBar->CanRoute(i, j);
            printf("%d-%s", j, (S_OK == hr ? "Yes" : "No"));
        }
        printf("\n\n");
    }

    for (i = 0; i < cInput; i++)
    {
        long lRelated = -1, lType = -1;

        hr = pXBar->get_CrossbarPinInfo(TRUE, i, &lRelated, &lType);

        printf("Input pin %d - %s\n", i, GetPhysicalPinName(lType));
        printf("\tRelated in: %d\n", lRelated);
    }
}
```



Pour une carte hypothétique, cette fonction peut produire la sortie suivante :


```C++
Output pin 0: S-Video
    Related out: 2, Routed in: 0
    Switching Matrix: 0-Yes 1-No 2-No 3-No
Output pin 1 - Video Tuner
    Related out: 2, Routed in: 1
    Switching Matrix: 0-No 1-Yes 2-No 3-No
Output pin 2 - Audio decoder
    Related out: 1, Routed in: -1
    Switching Matrix: 0-No 1-No 2-Yes 3-Yes

Input pin 0 - S-Video
    Related in: 2
Input pin 1 - Video Tuner
    Related in: 3
Input pin 2 - Audio line
    Related in: 0
Input pin 3 - Audio tuner
    Related in: 1
```



Du côté de la sortie, le S-Video et le tuner vidéo sont tous deux liés au décodeur audio. Du côté de l’entrée, le tuner vidéo est lié au tuner audio et la vidéo S est associée à la ligne audio dans. L’entrée S-Video est routée vers la sortie S-Video ; et l’entrée du syntoniseur vidéo est acheminée vers la sortie du tuner vidéo. Actuellement, rien n’est routé vers le décodeur audio, mais la ligne audio dans ou le tuner audio peuvent être routés vers celui-ci.

Vous pouvez modifier le routage existant en appelant la méthode [**IAMCrossbar :: route**](/windows/desktop/api/Strmif/nf-strmif-iamcrossbar-route) .

 

 



