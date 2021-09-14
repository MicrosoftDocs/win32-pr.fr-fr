---
description: Cette rubrique montre comment vous pouvez définir la matrice de sortie d’une voix mono source qui produit une voix de mastérisation stéréo afin d’obtenir un panoramique entre les haut-parleurs gauche et droit.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Comment : faire pivoter un son'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225484"
---
# <a name="how-to-pan-a-sound"></a>Comment : faire pivoter un son

Cette rubrique montre comment vous pouvez définir la matrice de sortie d’une voix mono source qui produit une voix de mastérisation stéréo afin d’obtenir un panoramique entre les haut-parleurs gauche et droit.

## <a name="to-setup-panning"></a>Pour configurer le panoramique

1.  Récupérez la configuration de l’orateur à l’aide de [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  Créez un tableau pour contenir la matrice de sortie. La taille minimale de la matrice de sortie est le nombre de canaux dans la voix source multiplié par le nombre de canaux dans la voix de sortie. Dans ce cas, un tableau à huit éléments gère une sortie de la voix mono dans n’importe quel format de sortie jusqu’à 7,1 de son surround.

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  Calculez les niveaux d’envoi en fonction du panorama souhaité entre les haut-parleurs gauche et droit. Dans cet exemple, les valeurs de panoramique sont comprises entre-1 et 1 avec-1 indiquant tout le son sur le haut-parleur gauche et 1 indiquant tout le son dans le haut-parleur droit.

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  Définissez les index de la matrice de sortie correspondant aux haut-parleurs gauche et droit avec les valeurs calculées à l’étape précédente. Les haut-parleurs gauche et droit sont déterminés en examinant le masque de canal renvoyé par [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask). Étant donné que les canaux doivent toujours être encodés dans l’ordre spécifié dans la page de référence [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , il est possible de déterminer l’index de tableau correspondant à un intervenant individuel.

    ```
    switch (dwChannelMask)
    {
    case SPEAKER_MONO:
        outputMatrix[0] = 1.0;
        break;
    case SPEAKER_STEREO:
    case SPEAKER_2POINT1:
    case SPEAKER_SURROUND:
        outputMatrix[0] = left;
        outputMatrix[1] = right;
        break;
    case SPEAKER_QUAD:
        outputMatrix[0] = outputMatrix[2] = left;
        outputMatrix[1] = outputMatrix[3] = right;
        break;
    case SPEAKER_4POINT1:
        outputMatrix[ 0 ] = outputMatrix[ 3 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 4 ] = right;
        break;
    case SPEAKER_5POINT1:
    case SPEAKER_7POINT1:
    case SPEAKER_5POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = right;
        break;
    case SPEAKER_7POINT1_SURROUND:
        outputMatrix[ 0 ] = outputMatrix[ 4 ] = outputMatrix[ 6 ] = left;
        outputMatrix[ 1 ] = outputMatrix[ 5 ] = outputMatrix[ 7 ] = right;
        break;
    }
    ```

    

5.  Appliquez la matrice de sortie à la voix d’origine à l’aide de [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix). La voix d’origine est soit une voix source, soit une voix de mixage secondaire envoyée à une voix de mixage secondaire ou à une voix de mastérisation. Vous pouvez obtenir des informations sur les voix d’origine et de destination, comme le nombre de canaux, à l’aide de [**IXAudio2Voice :: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Contrôle du volume et du tangage XAudio2](volume-and-pitch-control.md)
</dt> </dl>

 

 
