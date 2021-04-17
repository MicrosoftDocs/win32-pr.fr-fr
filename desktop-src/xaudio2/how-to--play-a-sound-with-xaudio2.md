---
description: Cette rubrique décrit les étapes minimales requises pour lire des données audio précédemment chargées dans XAudio2.
ms.assetid: 5172b31c-d2af-45aa-5bd4-b62502f3c047
title: 'Procédure : lire un son avec XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18ee2636ae9b6513dba9a479d63e0fd14be2c198
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526883"
---
# <a name="how-to-play-a-sound-with-xaudio2"></a><span data-ttu-id="12599-103">Procédure : lire un son avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="12599-103">How to: Play a Sound with XAudio2</span></span>

<span data-ttu-id="12599-104">Cette rubrique décrit les étapes minimales requises pour lire des données audio précédemment chargées dans XAudio2.</span><span class="sxs-lookup"><span data-stu-id="12599-104">This topic describes the minimum steps required to play previously-loaded audio data in XAudio2.</span></span> <span data-ttu-id="12599-105">Après l’initialisation de XAudio2 (voir [Comment : initialiser XAudio2](how-to--initialize-xaudio2.md)) et charger les données audio (voir procédure [: chargement des fichiers de données audio dans XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), vous pouvez lire un son en créant une voix source et en lui transmettant des données audio.</span><span class="sxs-lookup"><span data-stu-id="12599-105">After you initialize XAudio2 (see [How to: Initialize XAudio2](how-to--initialize-xaudio2.md)) and load the audio data (see How to: [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md)), you can play a sound by creating a source voice and passing audio data to it.</span></span>

## <a name="to-play-a-sound"></a><span data-ttu-id="12599-106">Pour émettre un signal sonore</span><span class="sxs-lookup"><span data-stu-id="12599-106">To play a sound</span></span>

1.  <span data-ttu-id="12599-107">Initialisez le moteur XAudio2 en suivant les étapes décrites dans [How to : Initialize XAudio2](how-to--initialize-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="12599-107">Initialize the XAudio2 engine by following the steps described in [How to: Initialize XAudio2](how-to--initialize-xaudio2.md).</span></span>
2.  <span data-ttu-id="12599-108">Remplissez une structure de [**\_ mémoire tampon**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) et XAUDIO2 en suivant les étapes décrites dans [Comment : charger des fichiers de données audio dans XAUDIO2](how-to--load-audio-data-files-in-xaudio2.md).</span><span class="sxs-lookup"><span data-stu-id="12599-108">Populate a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) and [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) structure by following the steps described in [How to: Load Audio Data Files in XAudio2](how-to--load-audio-data-files-in-xaudio2.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="12599-109">Selon le format des données audio, vous devrez peut-être utiliser une plus grande structure de données contenant une structure [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) à la place d’un **WAVEFORMATEX**.</span><span class="sxs-lookup"><span data-stu-id="12599-109">Depending on the format of the audio data, you may need to use a larger data structure containing a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure in place of a **WAVEFORMATEX**.</span></span> <span data-ttu-id="12599-110">Pour plus d’informations, consultez la page de référence de **WAVEFORMATEX** .</span><span class="sxs-lookup"><span data-stu-id="12599-110">See the **WAVEFORMATEX** reference page for more information.</span></span>

     

3.  <span data-ttu-id="12599-111">Créez une voix source en appelant la méthode [**IXAudio2 :: CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) sur une instance du moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="12599-111">Create a source voice by calling the [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice) method on an instance of the XAudio2 engine.</span></span> <span data-ttu-id="12599-112">Le format de la voix est spécifié par les valeurs définies dans une structure [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) .</span><span class="sxs-lookup"><span data-stu-id="12599-112">The format of the voice is specified by the values set in a [**WAVEFORMATEX**](/windows/win32/api/mmreg/ns-mmreg-waveformatex) structure.</span></span>
    ```
    IXAudio2SourceVoice* pSourceVoice;
    if( FAILED(hr = pXAudio2->CreateSourceVoice( &pSourceVoice, (WAVEFORMATEX*)&wfx ) ) ) return hr;
    ```

    

4.  <span data-ttu-id="12599-113">Soumettez [**une \_ mémoire tampon XAUDIO2**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) à la voix source à l’aide de la fonction [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="12599-113">Submit an [**XAUDIO2\_BUFFER**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_buffer) to the source voice using the function [**SubmitSourceBuffer**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-submitsourcebuffer).</span></span>
    ```
    if( FAILED(hr = pSourceVoice->SubmitSourceBuffer( &buffer ) ) )
        return hr;
    ```

    

    > [!Note]  
    > <span data-ttu-id="12599-114">Les exemples de données audio auxquels les points de la *mémoire tampon* sont toujours « détenus » par l’application et qui doivent rester alloués et accessibles jusqu’à ce que le son s’arrête.</span><span class="sxs-lookup"><span data-stu-id="12599-114">The audio sample data to which *buffer* points is still 'owned' by the app and must remain allocated and accessible until the sound stops playing.</span></span>

     

5.  <span data-ttu-id="12599-115">Utilisez la fonction [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) pour démarrer la voix source.</span><span class="sxs-lookup"><span data-stu-id="12599-115">Use the [**Start**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2sourcevoice-start) function to start the source voice.</span></span> <span data-ttu-id="12599-116">Dans la mesure où toutes les voix XAudio2 envoient leur sortie à la voix de mastérisation par défaut, l’audio de la voix source rend automatiquement le périphérique audio sélectionné lors de l’initialisation.</span><span class="sxs-lookup"><span data-stu-id="12599-116">Since all XAudio2 voices send their output to the mastering voice by default, audio from the source voice automatically makes its way to the audio device selected at initialization.</span></span> <span data-ttu-id="12599-117">Dans un graphique audio plus complexe, la voix source doit spécifier la voix à laquelle sa sortie doit être envoyée.</span><span class="sxs-lookup"><span data-stu-id="12599-117">In a more complicated audio graph, the source voice would have to specify the voice to which its output should be sent.</span></span>
    ```
    if ( FAILED(hr = pSourceVoice->Start( 0 ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="12599-118">Notes pour les applications du Windows Store</span><span class="sxs-lookup"><span data-stu-id="12599-118">Notes for Windows Store apps</span></span>

<span data-ttu-id="12599-119">Nous vous recommandons d’utiliser un [pointeur intelligent](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) pour gérer la durée de vie des objets XAUDIO2 de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="12599-119">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="12599-120">Pour les applications du Windows Store, vous pouvez utiliser le modèle de pointeur intelligent [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) à partir de la bibliothèque de modèles C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="12599-120">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```
Microsoft::WRL::ComPtr<IXAudio2SourceVoice> SourceVoice;
HRESULT hr;
if( FAILED(hr = pXAudio2->CreateSourceVoice( &SourceVoice, (WAVEFORMATEX*)&wfx ) ) )
    throw Platform::Exception::CreateException(hr); 

if( FAILED(hr = SourceVoice->SubmitSourceBuffer( &buffer ) ) )
    throw Platform::Exception::CreateException(hr); 

if ( FAILED(hr = SourceVoice->Start( 0 ) ) )
    throw Platform::Exception::CreateException(hr);
```



> [!Note]  
> <span data-ttu-id="12599-121">Assurez-vous que tous les pointeurs intelligents vers les objets XAUDIO2 sont entièrement libérés avant de libérer l’objet [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="12599-121">Ensure that all smart pointers to XAUDIO2 objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="12599-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="12599-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12599-123">XAudio2 Prise en main</span><span class="sxs-lookup"><span data-stu-id="12599-123">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="12599-124">Procédure : initialiser XAudio2</span><span class="sxs-lookup"><span data-stu-id="12599-124">How to: Initialize XAudio2</span></span>](how-to--initialize-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="12599-125">Procédure : charger des fichiers de données audio dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="12599-125">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> </dl>

 

 
