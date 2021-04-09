---
description: Cette rubrique montre comment vous pouvez définir la matrice de sortie d’une voix mono source qui produit une voix de mastérisation stéréo afin d’obtenir un panoramique entre les haut-parleurs gauche et droit.
ms.assetid: d87db173-6de0-09eb-7767-df619c88acfd
title: 'Comment : faire pivoter un son'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4136d6e30cba1e6b0bc669fef5518d2a56f868f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866482"
---
# <a name="how-to-pan-a-sound"></a><span data-ttu-id="4b044-103">Comment : faire pivoter un son</span><span class="sxs-lookup"><span data-stu-id="4b044-103">How to: Pan a Sound</span></span>

<span data-ttu-id="4b044-104">Cette rubrique montre comment vous pouvez définir la matrice de sortie d’une voix mono source qui produit une voix de mastérisation stéréo afin d’obtenir un panoramique entre les haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="4b044-104">This topic shows you how you can set the output matrix of a mono source voice that outputs to a stereo mastering voice in order to achieve panning between the left and right speakers.</span></span>

## <a name="to-setup-panning"></a><span data-ttu-id="4b044-105">Pour configurer le panoramique</span><span class="sxs-lookup"><span data-stu-id="4b044-105">To setup panning</span></span>

1.  <span data-ttu-id="4b044-106">Récupérez la configuration de l’orateur à l’aide de [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="4b044-106">Retrieve the speaker configuration using [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span>

    ```
    DWORD dwChannelMask;       
    pMasteringVoice->GetChannelMask( &dwChannelMask );       
    ```

    

2.  <span data-ttu-id="4b044-107">Créez un tableau pour contenir la matrice de sortie.</span><span class="sxs-lookup"><span data-stu-id="4b044-107">Create an array to hold the output matrix.</span></span> <span data-ttu-id="4b044-108">La taille minimale de la matrice de sortie est le nombre de canaux dans la voix source multiplié par le nombre de canaux dans la voix de sortie.</span><span class="sxs-lookup"><span data-stu-id="4b044-108">The minimum size of the output matrix is the number of channels in the source voice times the number of channels in the output voice.</span></span> <span data-ttu-id="4b044-109">Dans ce cas, un tableau à huit éléments gère une sortie de la voix mono dans n’importe quel format de sortie jusqu’à 7,1 de son surround.</span><span class="sxs-lookup"><span data-stu-id="4b044-109">In this case an eight element array will handle a mono voice outputting to any output format up to 7.1 surround sound.</span></span>

    ```
    float outputMatrix[ 8 ];
    for (int i=0; i<8; i++) outputMatrix[i] = 0;
    ```

    

3.  <span data-ttu-id="4b044-110">Calculez les niveaux d’envoi en fonction du panorama souhaité entre les haut-parleurs gauche et droit.</span><span class="sxs-lookup"><span data-stu-id="4b044-110">Calculate the send levels based on the desired panning between the left and right speakers.</span></span> <span data-ttu-id="4b044-111">Dans cet exemple, les valeurs de panoramique sont comprises entre-1 et 1 avec-1 indiquant tout le son sur le haut-parleur gauche et 1 indiquant tout le son dans le haut-parleur droit.</span><span class="sxs-lookup"><span data-stu-id="4b044-111">In this example, pan values will range from -1 to 1 with -1 indicating all sound to the left speaker and 1 indicating all sound to the right speaker.</span></span>

    ```
    // pan of -1.0 indicates all left speaker, 
    // 1.0 is all right speaker, 0.0 is split between left and right
    float left = 0.5f - pan / 2;
    float right = 0.5f + pan / 2; 
    ```

    

4.  <span data-ttu-id="4b044-112">Définissez les index de la matrice de sortie correspondant aux haut-parleurs gauche et droit avec les valeurs calculées à l’étape précédente.</span><span class="sxs-lookup"><span data-stu-id="4b044-112">Set the output matrix indices corresponding to the left and right speakers with the values calculated in the previous step.</span></span> <span data-ttu-id="4b044-113">Les haut-parleurs gauche et droit sont déterminés en examinant le masque de canal renvoyé par [**IXAudio2MasteringVoice :: GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span><span class="sxs-lookup"><span data-stu-id="4b044-113">The left and right speakers are determined by looking at the channel mask returned by [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask).</span></span> <span data-ttu-id="4b044-114">Étant donné que les canaux doivent toujours être encodés dans l’ordre spécifié dans la page de référence [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) , il est possible de déterminer l’index de tableau correspondant à un intervenant individuel.</span><span class="sxs-lookup"><span data-stu-id="4b044-114">Since the channels must always be encoded in the order specified on the [**WAVEFORMATEXTENSIBLE**](/windows-hardware/drivers/ddi/ksmedia/ns-ksmedia-waveformatextensible) reference page, it is possible to determine the array index corresponding to an individual speaker.</span></span>

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

    

5.  <span data-ttu-id="4b044-115">Appliquez la matrice de sortie à la voix d’origine à l’aide de [**IXAudio2Voice :: SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span><span class="sxs-lookup"><span data-stu-id="4b044-115">Apply the output matrix to the originating voice by using [**IXAudio2Voice::SetOutputMatrix**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-setoutputmatrix).</span></span> <span data-ttu-id="4b044-116">La voix d’origine est soit une voix source, soit une voix de mixage secondaire envoyée à une voix de mixage secondaire ou à une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="4b044-116">The originating voice will be either a source voice or a submix voice sending to either a submix voice or a mastering voice.</span></span> <span data-ttu-id="4b044-117">Vous pouvez obtenir des informations sur les voix d’origine et de destination, comme le nombre de canaux, à l’aide de [**IXAudio2Voice :: GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span><span class="sxs-lookup"><span data-stu-id="4b044-117">You can get info about the originating and destination voices, like their number of channels, by using [**IXAudio2Voice::GetVoiceDetails**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2voice-getvoicedetails).</span></span>

    ```
    // Assuming pVoice sends to pMasteringVoice

    XAUDIO2_VOICE_DETAILS VoiceDetails;
    pVoice->GetVoiceDetails(&VoiceDetails);

    XAUDIO2_VOICE_DETAILS MasterVoiceDetails;
    pMasteringVoice->GetVoiceDetails(&MasterVoiceDetails);

    pVoice->SetOutputMatrix( NULL, VoiceDetails.InputChannels, MasterVoiceDetails.InputChannels, outputMatrix );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="4b044-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b044-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b044-119">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="4b044-119">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="4b044-120">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="4b044-120">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="4b044-121">Contrôle du volume et du tangage XAudio2</span><span class="sxs-lookup"><span data-stu-id="4b044-121">XAudio2 Volume and Pitch Control</span></span>](volume-and-pitch-control.md)
</dt> </dl>

 

 
