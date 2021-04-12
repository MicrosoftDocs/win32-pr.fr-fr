---
title: Hébergement du contrôle du lecteur Windows Media dans une application Windows
description: Hébergement du contrôle du lecteur Windows Media dans une application Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Lecteur Windows Media, incorporer un contrôle ActiveX
- Modèle objet du lecteur Windows Media, incorporer un contrôle ActiveX
- modèle objet, incorporer un contrôle ActiveX
- Windows Media Player Mobile, incorporer un contrôle ActiveX
- Contrôle ActiveX du lecteur Windows Media, incorporation
- Windows Media Player Mobile, contrôle ActiveX, incorporation
- Contrôle ActiveX, incorporation
- Windows Media Player, programmes Windows
- Windows Media Player Object Model, programmes Windows
- modèle objet, programmes Windows
- Windows Media Player Mobile, programmes Windows
- Windows Media Player ActiveX Control, programmes Windows
- Windows Media Player Mobile contrôle ActiveX, programmes Windows
- Contrôle ActiveX, programmes Windows
- Incorporation de programmes basés sur Windows
- incorporation, programmes Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310766"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="b83af-119">Hébergement du contrôle du lecteur Windows Media dans une application Windows</span><span class="sxs-lookup"><span data-stu-id="b83af-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="b83af-120">Pour utiliser le contrôle ActiveX du lecteur Windows Media (y compris l’interface utilisateur) dans un programme Windows, vous devez fournir un conteneur de contrôles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b83af-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="b83af-121">ATL fournit la classe **CAxWindow** pour fournir les fonctionnalités de la fenêtre hôte ActiveX.</span><span class="sxs-lookup"><span data-stu-id="b83af-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="b83af-122">Pour héberger le contrôle du lecteur Windows Media à l’aide de la classe **CAxWindow** , procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="b83af-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="b83af-123">Incluez les en-têtes suivants :</span><span class="sxs-lookup"><span data-stu-id="b83af-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="b83af-124">Déclarez les variables membres, comme suit :</span><span class="sxs-lookup"><span data-stu-id="b83af-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="b83af-125">Lorsque votre fenêtre d’application est créée, appelez **AtlAxWinInit**, qui est requis lors de l’utilisation de la fenêtre hôte ActiveX ATL.</span><span class="sxs-lookup"><span data-stu-id="b83af-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="b83af-126">Déclarez les variables locales pour les codes de retour et pour contenir le pointeur vers l’interface de la fenêtre hôte :</span><span class="sxs-lookup"><span data-stu-id="b83af-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="b83af-127">Créez la fenêtre hôte :</span><span class="sxs-lookup"><span data-stu-id="b83af-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="b83af-128">Récupérez le pointeur d’interface de la fenêtre hôte :</span><span class="sxs-lookup"><span data-stu-id="b83af-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="b83af-129">Créez le contrôle du lecteur Windows Media dans la fenêtre hôte à l’aide de l’ID de classe :</span><span class="sxs-lookup"><span data-stu-id="b83af-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="b83af-130">Récupérez le pointeur d’interface **IWMPPlayer** :</span><span class="sxs-lookup"><span data-stu-id="b83af-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="b83af-131">Lorsque vous écrivez votre propre code, veillez à vérifier les erreurs dans chaque code de retour **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b83af-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="b83af-132">Pour obtenir un exemple complet illustrant comment héberger le contrôle Windows Media Player ActiveX à l’aide de la classe **CAxWindow** , consultez l’exemple WMPHost.</span><span class="sxs-lookup"><span data-stu-id="b83af-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="b83af-133">Hébergement du contrôle mobile du lecteur Windows Media 10 dans Windows CE</span><span class="sxs-lookup"><span data-stu-id="b83af-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="b83af-134">Microsoft eMbedded Visual C++ 4,0 et le kit de développement logiciel (SDK) Pocket PC 2003 ou le kit de développement logiciel (SDK) Smartphone 2003 doivent être installés lors du développement d’applications basées sur Windows CE qui hébergent un contrôle mobile Windows Media Player 10.</span><span class="sxs-lookup"><span data-stu-id="b83af-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="b83af-135">En outre, contrairement à ATL pour Windows, ATL pour Windows CE ne prend pas en charge le modèle de thread cloisonné.</span><span class="sxs-lookup"><span data-stu-id="b83af-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="b83af-136">Par conséquent, vous devez rechercher toutes les instances de cloisonnement Threading dans votre projet ATL et les modifier pour utiliser le Threading libre.</span><span class="sxs-lookup"><span data-stu-id="b83af-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b83af-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b83af-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b83af-138">**Exemples**</span><span class="sxs-lookup"><span data-stu-id="b83af-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="b83af-139">**Utilisation du contrôle du lecteur Windows Media dans un programme C++**</span><span class="sxs-lookup"><span data-stu-id="b83af-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




