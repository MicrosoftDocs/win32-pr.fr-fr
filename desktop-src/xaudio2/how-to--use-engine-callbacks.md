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
# <a name="how-to-use-engine-callbacks"></a><span data-ttu-id="9314f-103">Procédure : utiliser des rappels de moteur</span><span class="sxs-lookup"><span data-stu-id="9314f-103">How to: Use Engine Callbacks</span></span>

<span data-ttu-id="9314f-104">Vous pouvez notifier le code client XAudio2 des événements de moteur en inscrivant une instance d’une classe qui implémente l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) avec le moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="9314f-104">You can notify the XAudio2 client code of engine events by registering an instance of a class implementing the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface with the XAudio2 engine.</span></span> <span data-ttu-id="9314f-105">Cela permet au code client XAudio2 de suivre le moment où le traitement audio se produit et le moment où il doit redémarrer le moteur en cas d’erreur critique.</span><span class="sxs-lookup"><span data-stu-id="9314f-105">This allows the XAudio2 client code to keep track of when audio processing is occurring, and when to restart the engine in the event of a critical error.</span></span>

## <a name="to-use-an-engine-callback"></a><span data-ttu-id="9314f-106">Pour utiliser un rappel de moteur</span><span class="sxs-lookup"><span data-stu-id="9314f-106">To use an engine callback</span></span>

<span data-ttu-id="9314f-107">Les étapes suivantes inscrivent un objet pour gérer les événements du moteur.</span><span class="sxs-lookup"><span data-stu-id="9314f-107">The following steps register an object to handle engine events.</span></span>

1.  <span data-ttu-id="9314f-108">Créez une classe qui hérite de l’interface [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) .</span><span class="sxs-lookup"><span data-stu-id="9314f-108">Create a class that inherits from the [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) interface.</span></span>

    <span data-ttu-id="9314f-109">Toutes les méthodes de [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) sont purement virtuelles et doivent être définies.</span><span class="sxs-lookup"><span data-stu-id="9314f-109">All methods of [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) are purely virtual and must be defined.</span></span> <span data-ttu-id="9314f-110">La méthode d’intérêt dans cet exemple est [**IXAudio2EngineCallback :: OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), qui définit un indicateur qui signale à la boucle de jeu principale qu’une erreur critique s’est produite.</span><span class="sxs-lookup"><span data-stu-id="9314f-110">The method of interest in this example is [**IXAudio2EngineCallback::OnCriticalError**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-oncriticalerror), which sets a flag to signal the main game loop that a critical error has occurred.</span></span> <span data-ttu-id="9314f-111">Les méthodes restantes, [**IXAudio2EngineCallback :: OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) et [**IXAudio2EngineCallback :: OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), sont des stubs dans cet exemple.</span><span class="sxs-lookup"><span data-stu-id="9314f-111">The remaining methods, [**IXAudio2EngineCallback::OnProcessingPassStart**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassstart) and [**IXAudio2EngineCallback::OnProcessingPassEnd**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2enginecallback-onprocessingpassend), are stubs in this example.</span></span>

    ```
    class EngineCallback : public IXAudio2EngineCallback
    {
        void OnProcessingPassEnd () {}
        void OnProcessingPassStart() {}
        void OnCriticalError (HRESULT Error) {}
    };
    ```

    

2.  <span data-ttu-id="9314f-112">Utilisez [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) pour créer une instance du moteur XAudio2.</span><span class="sxs-lookup"><span data-stu-id="9314f-112">Use [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) to create an instance of the XAudio2 engine.</span></span>

    ```
    if ( FAILED(hr = XAudio2Create( &pXAudio2, 0, XAUDIO2_DEFAULT_PROCESSOR ) ) )
        return hr;
    ```

    

3.  <span data-ttu-id="9314f-113">Utilisez [**IXAudio2 :: RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) pour enregistrer le rappel du moteur.</span><span class="sxs-lookup"><span data-stu-id="9314f-113">Use [**IXAudio2::RegisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) to register the engine callback.</span></span>

    ```
    pXAudio2->RegisterForCallbacks( &engineCallback );
    ```

    

4.  <span data-ttu-id="9314f-114">Si vous n’avez plus besoin du rappel du moteur, appelez [**IXAudio2 :: UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span><span class="sxs-lookup"><span data-stu-id="9314f-114">If you don't need the engine callback any more, call [**IXAudio2::UnregisterForCallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-unregisterforcallbacks).</span></span>

    ```
    pXAudio2->UnregisterForCallbacks( &engineCallback );
    ```

    

## <a name="related-topics"></a><span data-ttu-id="9314f-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9314f-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9314f-116">Rappels</span><span class="sxs-lookup"><span data-stu-id="9314f-116">Callbacks</span></span>](callbacks.md)
</dt> <dt>

[<span data-ttu-id="9314f-117">Rappels XAudio2</span><span class="sxs-lookup"><span data-stu-id="9314f-117">XAudio2 Callbacks</span></span>](xaudio2-callbacks.md)
</dt> <dt>

[<span data-ttu-id="9314f-118">Guide de programmation XAudio2</span><span class="sxs-lookup"><span data-stu-id="9314f-118">XAudio2 Programming Guide</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="9314f-119">Procédure : créer un graphique de traitement audio de base</span><span class="sxs-lookup"><span data-stu-id="9314f-119">How to: Build a Basic Audio Processing Graph</span></span>](how-to--build-a-basic-audio-processing-graph.md)
</dt> <dt>

[<span data-ttu-id="9314f-120">Procédure : diffuser un son en continu à partir du disque</span><span class="sxs-lookup"><span data-stu-id="9314f-120">How to: Stream a Sound from Disk</span></span>](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
