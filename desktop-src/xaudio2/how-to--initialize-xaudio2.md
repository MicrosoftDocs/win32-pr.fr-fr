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
# <a name="how-to-initialize-xaudio2"></a>Procédure : initialiser XAudio2

XAudio2 est initialisé pour la lecture audio en créant une instance du moteur XAudio2 et en créant une voix de mastérisation.

**Pour initialiser XAudio2**

1.  Vérifiez que vous avez initialisé COM. Pour une application du Windows Store, cette opération est effectuée dans le cadre de l’initialisation du Windows Runtime. Sinon, utilisez [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex).

    ```
    HRESULT hr;
    hr = CoInitializeEx( nullptr, COINIT_MULTITHREADED );
    if (FAILED(hr))
        return hr;
    ```



2.  Utilisez la fonction [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) pour créer une instance du moteur XAudio2.

    ```
    IXAudio2* pXAudio2 = nullptr;
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Utilisez la méthode [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) pour créer une voix de mastérisation.

    Les voix de mastérisation encapsulent un périphérique audio. Il s’agit de la destination ultime de tout son qui traverse un graphique audio.

    ```
    IXAudio2MasteringVoice* pMasterVoice = nullptr;
    if ( FAILED(hr = pXAudio2->CreateMasteringVoice( &pMasterVoice ) ) )
        return hr;
    ```

    

## <a name="notes-for-windows-store-apps"></a>Notes pour les applications du Windows Store

Nous vous recommandons d’utiliser un [pointeur intelligent](/previous-versions/visualstudio/visual-studio-2012/hh279674(v=vs.110)) pour gérer la durée de vie des objets XAUDIO2 de façon sécurisée. Pour les applications du Windows Store, vous pouvez utiliser le modèle de pointeur intelligent [**ComPtr**](/previous-versions/visualstudio/visual-studio-2012/br244983(v=vs.110)) à partir de la bibliothèque de modèles C++ Windows Runtime (WRL).


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
> Assurez-vous que tous les objets enfants XAUDIO2 sont entièrement libérés avant de libérer l’objet [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) .

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[XAudio2 Prise en main](getting-started.md)
</dt> <dt>

[Procédure : charger des fichiers de données audio dans XAudio2](how-to--load-audio-data-files-in-xaudio2.md)
</dt> <dt>

[Procédure : lire un son avec XAudio2](how-to--play-a-sound-with-xaudio2.md)
</dt> </dl>

 

 
