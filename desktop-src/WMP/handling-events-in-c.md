---
title: Gestion des événements en C++
description: Gestion des événements en C++
ms.assetid: 5d9eb1c7-7022-4442-b67a-6a96fe5ce97f
keywords:
- Lecteur Windows Media, C++
- Windows Media Player Object Model, C++
- modèle objet, C++
- Windows Media Player Mobile, C++
- Contrôle ActiveX du lecteur Windows Media, C++
- Windows Media Player Mobile, contrôle ActiveX, C++
- Contrôle ActiveX, C++
- Incorporation de programmes C++
- incorporation, programmes C++
- Contrôle ActiveX du lecteur Windows Media, gestion des événements
- Windows Media Player Mobile contrôle ActiveX, gestion des événements
- Contrôle ActiveX, gestion des événements
- événements, C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16cbef547ab2604244c5c204707a08eb87a6b70a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100745"
---
# <a name="handling-events-in-c"></a><span data-ttu-id="a7b82-116">Gestion des événements en C++</span><span class="sxs-lookup"><span data-stu-id="a7b82-116">Handling Events in C++</span></span>

<span data-ttu-id="a7b82-117">Vous pouvez recevoir des événements du lecteur Windows Media de deux manières.</span><span class="sxs-lookup"><span data-stu-id="a7b82-117">You can receive events from Windows Media Player in two ways.</span></span>

-   <span data-ttu-id="a7b82-118">Via **IDispatch** à l’aide de l’interface **\_ WMPOCXEvents** .</span><span class="sxs-lookup"><span data-stu-id="a7b82-118">Through **IDispatch** by using the **\_WMPOCXEvents** interface.</span></span> <span data-ttu-id="a7b82-119">Il s’agit de l’interface à utiliser pour la plupart des scénarios d’incorporation.</span><span class="sxs-lookup"><span data-stu-id="a7b82-119">This is the interface to use for most embedding scenarios.</span></span>
-   <span data-ttu-id="a7b82-120">Via l’interface **IWMPEvents** .</span><span class="sxs-lookup"><span data-stu-id="a7b82-120">Through the **IWMPEvents** interface.</span></span> <span data-ttu-id="a7b82-121">Cette interface est disponible lorsque votre code est connecté au lecteur en mode complet, par exemple lors de la communication à distance du contrôle du lecteur Windows Media ou dans un plug-in d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7b82-121">This interface is available when your code is connected to the full mode Player, such as when remoting the Windows Media Player control or in a UI plug-in.</span></span>

<span data-ttu-id="a7b82-122">Dans chaque scénario, vous commencez à écouter des événements à l’aide de points de connexion COM.</span><span class="sxs-lookup"><span data-stu-id="a7b82-122">In each scenario, you start listening to events by using COM connection points.</span></span>

<span data-ttu-id="a7b82-123">L’exemple de code suivant utilise trois variables membres :</span><span class="sxs-lookup"><span data-stu-id="a7b82-123">The following example code uses three member variables:</span></span>


```C++
CComPtr<IWMPPlayer>         m_spWMPPlayer;
CComPtr<IConnectionPoint>   m_spConnectionPoint;
DWORD                       m_dwAdviseCookie;

```



<span data-ttu-id="a7b82-124">Pour récupérer un point de connexion, vous commencez par **QueryInterface** pour le conteneur de point de connexion.</span><span class="sxs-lookup"><span data-stu-id="a7b82-124">To retrieve a connection point, you first **QueryInterface** for the connection point container.</span></span>


```C++
HRESULT  hr = S_OK;
// Smart pointer to IConnectionPointContainer
CComPtr<IConnectionPointContainer>  spConnectionContainer;

hr = m_spWMPPlayer->QueryInterface(&spConnectionContainer);

```



<span data-ttu-id="a7b82-125">Ensuite, demandez le point de connexion de l’interface d’événement que vous souhaitez utiliser.</span><span class="sxs-lookup"><span data-stu-id="a7b82-125">Next, request the connection point for the event interface you want to use.</span></span> <span data-ttu-id="a7b82-126">L’exemple de code suivant tente d’abord d’utiliser **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7b82-126">The following example code first attempts to use **IWMPEvents**.</span></span> <span data-ttu-id="a7b82-127">Si cette interface n’est pas disponible, elle utilise **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7b82-127">If that interface isn't available, it uses **\_WMPOCXEvents**.</span></span>


```C++
// Test whether the control supports the IWMPEvents interface.
if(SUCCEEDED(hr))
{
    hr = spConnectionContainer->FindConnectionPoint(__uuidof(IWMPEvents), &m_spConnectionPoint);
    if (FAILED(hr))
    {
        // If not, try the _WMPOCXEvents interface, which uses IDispatch.
        hr = spConnectionContainer->FindConnectionPoint(__uuidof(_WMPOCXEvents), &m_spConnectionPoint);
    }
}

```



<span data-ttu-id="a7b82-128">Enfin, appelez **IConnectionPoint :: Advise** pour demander des événements.</span><span class="sxs-lookup"><span data-stu-id="a7b82-128">Finally, call **IConnectionPoint::Advise** to request events.</span></span>


```C++
if(SUCCEEDED(hr))
{
    hr = m_spConnectionPoint->Advise(this, &m_dwAdviseCookie);
}

```



<span data-ttu-id="a7b82-129">Dans l’exemple précédent, le premier paramètre suppose que la classe appelante implémente à la fois **IWMPEvents** et **\_ WMPOCXEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7b82-129">In the preceding example, the first parameter assumes that the calling class implements both **IWMPEvents** and **\_WMPOCXEvents**.</span></span> <span data-ttu-id="a7b82-130">Le deuxième paramètre est une valeur de retour que vous utilisez pour arrêter d’écouter des événements, par exemple lorsque votre programme s’arrête, à l’aide d’un code similaire à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="a7b82-130">The second parameter is a return value that you use to stop listening to events, such as when your program exits, using code similar to the following:</span></span>


```C++
// Stop listening to events
if (m_spConnectionPoint)
{
    if (0 != m_dwAdviseCookie)
        m_spConnectionPoint->Unadvise(m_dwAdviseCookie);
        m_spConnectionPoint.Release();
}

```



<span data-ttu-id="a7b82-131">L’implémentation des gestionnaires d’événements pour **IWMPEvents** et **\_ WMPOCXEvents** diffère.</span><span class="sxs-lookup"><span data-stu-id="a7b82-131">Implementing the event handlers for **IWMPEvents** and **\_WMPOCXEvents** differs.</span></span> <span data-ttu-id="a7b82-132">Pour **IWMPEvents**, vous devez implémenter une fonction pour gérer chaque événement défini par l’interface, même si vous n’envisagez pas d’utiliser l’événement.</span><span class="sxs-lookup"><span data-stu-id="a7b82-132">For **IWMPEvents**, you must implement a function to handle every event defined by the interface, even if you don't intend to use the event.</span></span>


```C++
// IWMPEvents methods
void STDMETHODCALLTYPE OpenStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE PlayStateChange( long NewState ){ return; }
void STDMETHODCALLTYPE AudioLanguageChange( long LangID ){ return; }
// And so on...

```



<span data-ttu-id="a7b82-133">Pour implémenter des gestionnaires **\_ WMPOCXEvents** , vous devez utiliser **IDispatch :: Invoke**, qui est une implémentation de gestionnaire d’événements unique pour tous les événements qui se produisent sur l’interface **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="a7b82-133">To implement **\_WMPOCXEvents** handlers, you must use **IDispatch::Invoke**, which is a single event handler implementation for all the events happening on the **IDispatch** interface.</span></span> <span data-ttu-id="a7b82-134">Cela signifie que vous pouvez choisir de gérer uniquement certains événements et d’en ignorer d’autres.</span><span class="sxs-lookup"><span data-stu-id="a7b82-134">This means that you can choose to handle only certain events and ignore others.</span></span> <span data-ttu-id="a7b82-135">L’exemple de code suivant montre un gestionnaire **\_ WMPOCXEvents** , à l’aide de **Invoke**, qui gère uniquement les événements **OpenStateChange** et **PlayStateChange** :</span><span class="sxs-lookup"><span data-stu-id="a7b82-135">The following example code shows a **\_WMPOCXEvents** handler, using **Invoke**, that handles only the **OpenStateChange** and **PlayStateChange** events:</span></span>


```C++
HRESULT CMyClass::Invoke(
    DISPID  dispIdMember,      
    REFIID  riid,              
    LCID  lcid,                
    WORD  wFlags,              
    DISPPARAMS FAR*  pDispParams,  
    VARIANT FAR*  pVarResult,  
    EXCEPINFO FAR*  pExcepInfo,  
    unsigned int FAR*  puArgErr )
{
    if (!pDispParams)
        return E_POINTER;

    if (pDispParams->cNamedArgs != 0)
        return DISP_E_NONAMEDARGS;

    HRESULT hr = DISP_E_MEMBERNOTFOUND;

    switch (dispIdMember)
    {
        case DISPID_WMPCOREEVENT_OPENSTATECHANGE:
            OpenStateChange(pDispParams->rgvarg[0].lVal /* NewState */ );
            break;

        case DISPID_WMPCOREEVENT_PLAYSTATECHANGE:
            PlayStateChange(pDispParams->rgvarg[0].lVal /* NewState */);
            break;

        // Other cases can handle additional events by using DISPIDs.
    }

    return( hr );
}

```



<span data-ttu-id="a7b82-136">Dans l’exemple de code précédent, chaque cas appelle simplement via le gestionnaire **IWMPEvents** pour l’événement correspondant.</span><span class="sxs-lookup"><span data-stu-id="a7b82-136">In the preceding example code, each case simply calls through to the **IWMPEvents** handler for the corresponding event.</span></span> <span data-ttu-id="a7b82-137">Si votre code gère uniquement **\_ WMPOCXEvents**, vous pouvez simplement appeler une fonction personnalisée ou gérer l’événement Inline après l’instruction **case** .</span><span class="sxs-lookup"><span data-stu-id="a7b82-137">If your code only handles **\_WMPOCXEvents**, you can simply call a custom function or handle the event inline after the **case** statement.</span></span>

## <a name="receiving-events-from-windows-media-player-10-mobile"></a><span data-ttu-id="a7b82-138">Réception d’événements du lecteur Windows Media 10 mobile</span><span class="sxs-lookup"><span data-stu-id="a7b82-138">Receiving Events from Windows Media Player 10 Mobile</span></span>

<span data-ttu-id="a7b82-139">Le contrôle mobile du lecteur Windows Media 10 ne prend en charge que la réception de certains événements via **\_ WMPOCXEvents** et **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7b82-139">The Windows Media Player 10 Mobile control only supports receiving certain events through **\_WMPOCXEvents** and **IWMPEvents**.</span></span> <span data-ttu-id="a7b82-140">Pour plus d’informations, consultez la documentation de **IWMPEvents**.</span><span class="sxs-lookup"><span data-stu-id="a7b82-140">For more information, please see the documentation for **IWMPEvents**.</span></span>

## <a name="samples"></a><span data-ttu-id="a7b82-141">Exemples</span><span class="sxs-lookup"><span data-stu-id="a7b82-141">Samples</span></span>

<span data-ttu-id="a7b82-142">Le package d’installation du lecteur Windows Media installe un exemple qui illustre la gestion des événements.</span><span class="sxs-lookup"><span data-stu-id="a7b82-142">The Windows Media Player setup package installs a sample that demonstrates event handling.</span></span> <span data-ttu-id="a7b82-143">Pour plus d’informations, consultez l’exemple WMPHost.</span><span class="sxs-lookup"><span data-stu-id="a7b82-143">See the WMPHost sample for more information.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7b82-144">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7b82-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7b82-145">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="a7b82-145">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="a7b82-146">**Utilisation du contrôle du lecteur Windows Media dans un programme C++**</span><span class="sxs-lookup"><span data-stu-id="a7b82-146">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




