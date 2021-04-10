---
description: XAudio2 est initialisé pour la lecture audio en créant une instance du moteur XAudio2 et en créant une voix de mastérisation.
ms.assetid: 4db2e7fc-0a87-0344-a07c-3abf2b21af32
title: 'Procédure : initialiser XAudio2'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4a613c1ae2b7c3a7f0c55ab5349a0a605aaeb2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862950"
---
# <a name="how-to-initialize-xaudio2"></a><span data-ttu-id="f932d-103">Procédure : initialiser XAudio2</span><span class="sxs-lookup"><span data-stu-id="f932d-103">How to: Initialize XAudio2</span></span>

<span data-ttu-id="f932d-104">XAudio2 est initialisé pour la lecture audio en créant une instance du moteur XAudio2 et en créant une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="f932d-104">XAudio2 is initialized for audio playback by creating an instance of the XAudio2 engine, and creating a mastering voice.</span></span>

<span data-ttu-id="f932d-105">**Pour initialiser XAudio2**</span><span class="sxs-lookup"><span data-stu-id="f932d-105">**To initialize XAudio2**</span></span>

1.  <span data-ttu-id="f932d-106">Vérifiez que vous avez initialisé COM.</span><span class="sxs-lookup"><span data-stu-id="f932d-106">Make sure you have initialized COM.</span></span> <span data-ttu-id="f932d-107">Pour une application du Windows Store, cette opération est effectuée dans le cadre de l’initialisation du Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="f932d-107">For a Windows Store app, this is done as part of initializing the Windows Runtime.</span></span> <span data-ttu-id="f932d-108">Sinon, utilisez [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="f932d-108">Otherwise, use [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  <span data-ttu-id="f932d-109">Utilisez la fonction [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) pour créer une instance du moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="f932d-109">Use the [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) function to create an instance of the XAudio2 engine.</span></span>

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="f932d-110">Utilisez la méthode [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) pour créer une voix de mastérisation.</span><span class="sxs-lookup"><span data-stu-id="f932d-110">Use the [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) method to create a mastering voice.</span></span>

    <span data-ttu-id="f932d-111">Les voix de mastérisation encapsulent un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="f932d-111">The mastering voices encapsulates an audio device.</span></span> <span data-ttu-id="f932d-112">Il s’agit de la destination ultime de tout son qui traverse un graphique audio.</span><span class="sxs-lookup"><span data-stu-id="f932d-112">It is the ultimate destination for all audio that passes through an audio graph.</span></span>

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a><span data-ttu-id="f932d-113">Notes pour les applications du Windows Store</span><span class="sxs-lookup"><span data-stu-id="f932d-113">Notes for Windows Store apps</span></span>

<span data-ttu-id="f932d-114">Nous vous recommandons d’utiliser un [pointeur intelligent](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) pour gérer la durée de vie des objets XAUDIO2 de façon sécurisée.</span><span class="sxs-lookup"><span data-stu-id="f932d-114">We recommend that you make use of a [smart pointer](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) to manage the lifetime of XAUDIO2 objects in an exception safe manner.</span></span> <span data-ttu-id="f932d-115">Pour les applications du Windows Store, vous pouvez utiliser le modèle de pointeur intelligent [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) à partir de la bibliothèque de modèles C++ Windows Runtime (WRL).</span><span class="sxs-lookup"><span data-stu-id="f932d-115">For Windows Store apps, you can use the [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) smart pointer template from the Windows Runtime C++ Template Library (WRL).</span></span>


```C++
Microsoft::WRL::ComPtr<IXAudio2> XAudio2;
HRESULT hr;
if ( FAILED(hr = XAudio2Create( &XAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
    throw Platform::Exception::CreateException(hr);

IXAudio2MasteringVoice* pMasterVoice = nullptr;
if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
    return hr;
```



> [!Note]  
> <span data-ttu-id="f932d-116">Assurez-vous que tous les objets enfants XAUDIO2 sont entièrement libérés avant de libérer l’objet [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .</span><span class="sxs-lookup"><span data-stu-id="f932d-116">Ensure that all XAUDIO2 child objects are fully released before you release the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) object.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f932d-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f932d-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f932d-118">XAudio2 Prise en main</span><span class="sxs-lookup"><span data-stu-id="f932d-118">XAudio2 Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="f932d-119">Procédure : charger des fichiers de données audio dans XAudio2</span><span class="sxs-lookup"><span data-stu-id="f932d-119">How to: Load Audio Data Files in XAudio2</span></span>](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[<span data-ttu-id="f932d-120">Procédure : lire un son avec XAudio2</span><span class="sxs-lookup"><span data-stu-id="f932d-120">How to: Play a Sound with XAudio2</span></span>](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
