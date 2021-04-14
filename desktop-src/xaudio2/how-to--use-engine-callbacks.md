---
description: Vous pouvez notifier le code client XAudio2 des événements de moteur en inscrivant une instance d’une classe qui implémente l’interface IXAudio2EngineCallback avec le moteur XAudio2.
ms.assetid: 006a8cb6-c24c-f7d1-9e8b-9cb2baa046c0
title: 'Procédure : utiliser des rappels de moteur'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04adec0efd0625157740488d70be7896688d1176
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393744"
---
# <a name="how-to-use-engine-callbacks"></a>Procédure : utiliser des rappels de moteur

Vous pouvez notifier le code client XAudio2 des événements de moteur en inscrivant une instance d’une classe qui implémente l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) avec le moteur XAudio2. Cela permet au code client XAudio2 de suivre le moment où le traitement audio se produit et le moment où il doit redémarrer le moteur en cas d’erreur critique.

## <a name="to-use-an-engine-callback"></a>Pour utiliser un rappel de moteur

Les étapes suivantes inscrivent un objet pour gérer les événements du moteur.

1.  Créez une classe qui hérite de l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .

    Toutes les méthodes de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sont purement virtuelles et doivent être définies. La méthode d’intérêt dans cet exemple est [**IXAudio2EngineCallback :: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), qui définit un indicateur qui signale à la boucle de jeu principale qu’une erreur critique s’est produite. Les méthodes restantes, [**IXAudio2EngineCallback :: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) et [**IXAudio2EngineCallback :: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sont des stubs dans cet exemple.

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  Utilisez [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) pour créer une instance du moteur XAudio2.

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  Utilisez [**IXAudio2 :: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) pour enregistrer le rappel du moteur.

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  Si vous n’avez plus besoin du rappel du moteur, appelez [**IXAudio2 :: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Rappels](callbacks.md)
</dt> <dt>

[Rappels XAudio2](xaudio2-callbacks.md)
</dt> <dt>

[Guide de programmation XAudio2](programming-guide.md)
</dt> <dt>

[Procédure : créer un graphique de traitement audio de base](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[Procédure : diffuser un son en continu à partir du disque](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
