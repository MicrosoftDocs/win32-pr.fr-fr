---
description: Cette rubrique contient les sections suivantes.
ms.assetid: 0522ccbf-e754-470a-8199-004fcbaa927d
title: Présentation de DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 324a5be26aade17385a6ab0b7d347015497a2a3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481088"
---
# <a name="dxgi-overview"></a>Présentation de DXGI

Microsoft DirectX Graphics infrastructure (DXGI) reconnaît que certaines parties des graphiques évoluent plus lentement que d’autres. L’objectif principal de DXGI est de gérer les tâches de bas niveau qui peuvent être indépendantes du runtime Graphics DirectX. DXGI fournit une infrastructure commune pour les futurs composants graphiques. le premier composant qui tire parti de DXGI est Microsoft Direct3D 10.

Dans les versions précédentes de Direct3D, les tâches de bas niveau telles que l’énumération des périphériques matériels, la présentation des frames rendus à une sortie, le contrôle de la valeur gamma et la gestion d’une transition en plein écran étaient incluses dans le runtime Direct3D. Ces tâches sont maintenant implémentées dans DXGI.

L’objectif de DXGI est de communiquer avec le pilote en mode noyau et le matériel système, comme indiqué dans le diagramme suivant.

![diagramme de la communication entre les applications, DXGI, et les pilotes et le matériel](images/dxgi-dll.png)

Une application peut accéder directement à DXGI, ou appeler les API Direct3D dans D3D11 \_ 1. h, d3d11. h, D3D10 \_ 1. h ou d3d10. h, qui gère les communications avec DXGI pour vous. Vous pouvez utiliser DXGI directement si votre application doit énumérer des appareils ou contrôler la façon dont les données sont présentées à une sortie.

Cette rubrique contient les sections suivantes.

-   [Énumération des adaptateurs](#enumerating-adapters)
    -   [Nouvelles informations sur l’énumération des adaptateurs pour Windows 8](#new-info-about-enumerating-adapters-for-windows-8)
-   [Présentation](#presentation)
    -   [Créer une chaîne de permutation](#create-a-swap-chain)
    -   [Soins et alimentation de la chaîne de permutation](#care-and-feeding-of-the-swap-chain)
    -   [Gérer le redimensionnement de fenêtre](#handling-window-resizing)
    -   [Choix de la sortie et de la taille DXGI](#choosing-the-dxgi-output-and-size)
    -   [Débogage en mode Full-Screen](#debugging-in-full-screen-mode)
    -   [Destruction d’une chaîne de permutation](#destroying-a-swap-chain)
    -   [Utilisation d’une analyse pivotée](#using-a-rotated-monitor)
    -   [Modes de basculement](#switching-modes)
    -   [Conseil sur les performances plein écran](#full-screen-performance-tip)
    -   [Considérations multithread](#multithread-considerations)
-   [DXGI les réponses de DLLMain](#dxgi-responses-from-dllmain)
-   [Modifications apportées à DXGI 1,1](#dxgi-11-changes)
-   [Modifications apportées à DXGI 1,2](#dxgi-12-changes)
-   [Rubriques connexes](#related-topics)

Pour connaître les formats pris en charge par le matériel Direct3D 11 :

-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,1](hardware-support-for-direct3d-12-1-formats.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 12,0](hardware-support-for-direct3d-12-0-formats.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,1](format-support-for-direct3d-11-1-feature-level-hardware.md)
-   [Prise en charge du format DXGI pour le matériel de niveau de fonctionnalité Direct3D 11,0](format-support-for-direct3d-11-0-feature-level-hardware.md)
-   [Prise en charge matérielle pour les formats Direct3D 10Level9](/previous-versions//ff471324(v=vs.85))
-   [Prise en charge du matériel pour les formats Direct3D 10,1](/previous-versions//cc627091(v=vs.85))
-   [Prise en charge matérielle pour les formats Direct3D 10](/previous-versions//cc627090(v=vs.85))

## <a name="enumerating-adapters"></a>Énumération des adaptateurs

Un adaptateur est une abstraction du matériel et des fonctionnalités logicielles de votre ordinateur. Il y a généralement de nombreux adaptateurs sur votre ordinateur. Certains périphériques sont implémentés dans le matériel (comme votre carte vidéo) et d’autres sont implémentés dans le logiciel (comme le rastériseur de référence Direct3D). Les adaptateurs implémentent les fonctionnalités utilisées par une application graphique. Le diagramme suivant illustre un système avec un seul ordinateur, deux cartes (cartes vidéo) et trois moniteurs de sortie.

![diagramme d’un ordinateur avec deux cartes vidéo et trois moniteurs](images/dxgi-terms.png)

Lors de l’énumération de ces éléments matériels, DXGI crée une interface [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) pour chaque sortie (ou analyse) et une interface [**IDXGIAdapter2**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgiadapter2) pour chaque carte vidéo (même s’il s’agit d’une carte vidéo intégrée à une carte mère). L’énumération est effectuée à l’aide d’un appel d’interface [**IDXGIFactory**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) , [**IDXGIFactory :: EnumAdapters**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-enumadapters), pour retourner un jeu d’interfaces [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) qui représentent le matériel vidéo.

DXGI 1,1 a ajouté l’interface [**IDXGIFactory1**](/windows/win32/api/DXGI/nn-dxgi-idxgifactory1) . [**IDXGIFactory1 :: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) retourne un jeu d’interfaces [**IDXGIAdapter1**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter1) qui représente le matériel vidéo.

Si vous souhaitez sélectionner des fonctionnalités matérielles vidéo spécifiques quand vous utilisez des API Direct3D, nous vous recommandons d’appeler de manière itérative la fonction [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) ou [**D3D11CreateDeviceAndSwapChain**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain) avec chaque descripteur d’adaptateur et [niveau de fonctionnalité](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md)matérielle possible. Cette fonction s’exécute correctement si le niveau de fonctionnalité est pris en charge par l’adaptateur spécifié.

### <a name="new-info-about-enumerating-adapters-for-windows-8"></a>Nouvelles informations sur l’énumération des adaptateurs pour Windows 8

À compter de Windows 8, un adaptateur appelé « pilote de rendu de base Microsoft » est toujours présent. Cet adaptateur a un ID de **0x1414** et un DeviceID de **0x8C**. La valeur [**\_ \_ \_ logicielle**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) de l’indicateur de l’adaptateur DXGI est également définie dans le membre **Flags** de sa structure DESC2 de l' [**\_ adaptateur \_ dxgi**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_adapter_desc2) . Cet adaptateur est un appareil de rendu uniquement qui n’a pas de sortie d’affichage. DXGI ne retourne jamais l' [**\_ appareil d’erreur dxgi \_ \_ supprimé**](dxgi-error.md) pour cet adaptateur.

Si le pilote d’affichage d’un ordinateur ne fonctionne pas ou est désactivé, l’adaptateur principal (**null**) de l’ordinateur peut également être appelé « pilote de rendu de base Microsoft ». Toutefois, cet adaptateur a des sorties et n’a pas de valeur de logiciel pour l’indicateur de l' [**\_ adaptateur \_ \_ dxgi**](/windows/win32/api/dxgi/ne-dxgi-dxgi_adapter_flag) . Le système d’exploitation et les applications utilisent cet adaptateur par défaut. Si un pilote d’affichage est installé ou activé, les applications peuvent recevoir l' [**\_ appareil d’erreur dxgi \_ \_ supprimé**](dxgi-error.md) pour cet adaptateur, puis recommencer l’énumération des adaptateurs.

Quand la carte d’affichage principale d’un ordinateur est la « carte d’affichage de base Microsoft » (adaptateur de[déviation](../direct3d11/overviews-direct3d-11-devices-create-warp.md) ), cet ordinateur possède également un deuxième adaptateur. Ce deuxième adaptateur est le périphérique de rendu uniquement qui n’a pas de sortie d’affichage et pour lequel DXGI ne retourne jamais [**dxgi \_ périphérique d’erreur \_ \_ supprimé**](dxgi-error.md).

Si vous souhaitez utiliser la distorsion pour le rendu, le calcul ou d’autres tâches longues, nous vous recommandons d’utiliser l’appareil de rendu uniquement. Vous pouvez obtenir un pointeur vers l’appareil de rendu uniquement en appelant la méthode [**IDXGIFactory1 :: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) . Vous créez également l’appareil de rendu uniquement lorsque vous spécifiez la [**Warp de type de \_ pilote \_ \_ D3D**](/windows/win32/api/d3dcommon/ne-d3dcommon-d3d_driver_type) dans le paramètre *DriverType* de [**D3D11CreateDevice**](/windows/win32/api/d3d11/nf-d3d11-d3d11createdevice) , car l’appareil Warp utilise également l’adaptateur de Warping-only.

## <a name="presentation"></a>Présentation

Le travail de votre application consiste à afficher des frames et à demander à DXGI de présenter ces frames à la sortie. Si deux mémoires tampons sont disponibles pour l’application, elles peuvent afficher une seule mémoire tampon tout en en présentant une autre. L’application peut nécessiter plus de deux mémoires tampons en fonction du temps nécessaire au rendu d’un frame ou de la fréquence d’images souhaitée pour la présentation. L’ensemble de mémoires tampons créé est appelé chaîne de permutation, comme illustré ici.

![illustration d’une chaîne de permutation](images/dxgi-swap-chain.png)

-   [Créer une chaîne de permutation](#create-a-swap-chain)
-   [Soins et alimentation de la chaîne de permutation](#care-and-feeding-of-the-swap-chain)
-   [Gérer le redimensionnement de fenêtre](#handling-window-resizing)
-   [Choix de la sortie et de la taille DXGI](#choosing-the-dxgi-output-and-size)
-   [Débogage en mode Full-Screen](#debugging-in-full-screen-mode)
-   [Destruction d’une chaîne de permutation](#destroying-a-swap-chain)
-   [Utilisation d’une analyse pivotée](#using-a-rotated-monitor)
-   [Modes de basculement](#switching-modes)
-   [Conseil sur les performances plein écran](#full-screen-performance-tip)
-   [Considérations multithread](#multithread-considerations)

Une chaîne de permutation possède un tampon d’avant et une ou plusieurs mémoires tampons d’arrière-plan. Chaque application crée sa propre chaîne de permutation. Pour maximiser la vitesse de présentation des données dans une sortie, une chaîne de permutation est presque toujours créée dans la mémoire d’un sous-système d’affichage, comme indiqué dans l’illustration suivante.

![illustration d’un sous-système d’affichage](images/dxgi-adapter.png)

Le sous-système d’affichage (qui est souvent une carte vidéo mais qui peut être implémenté sur une carte mère) contient un GPU, un convertisseur numérique-analogique (DAC) et la mémoire. La chaîne de permutation est allouée dans cette mémoire pour accélérer la présentation. Le sous-système d’affichage présente les données dans la mémoire tampon d’avant de la sortie.

Une chaîne de permutation est configurée pour dessiner en mode plein écran ou en fenêtre, ce qui évite d’avoir à savoir si une sortie est en mode fenêtre ou plein écran. Une chaîne de permutation en mode plein écran peut optimiser les performances en basculant la résolution d’affichage.

### <a name="create-a-swap-chain"></a>Créer une chaîne d’échange

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 10 : Direct3D 10 est le premier composant graphique à utiliser DXGI. DXGI présente des comportements de chaîne de permutation différents.<br/>
<ul>
<li>Dans DXGI, une chaîne de permutation est liée à une fenêtre lorsque la chaîne de permutation est créée. Cette modification améliore les performances et économise de la mémoire. Les versions précédentes de Direct3D permettaient à la chaîne de permutation de modifier la fenêtre à laquelle la chaîne de permutation est liée.</li>
<li>Dans DXGI, une chaîne de permutation est liée à un périphérique de rendu à la création. L’objet d’appareil que les fonctions de création de périphérique Direct3D retournent implémente l’interface <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown"><strong>IUnknown</strong></a> . Vous pouvez appeler <a href="/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)"><strong>QueryInterface</strong></a> pour Rechercher l’interface <a href="/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgidevice2"><strong>IDXGIDevice2</strong></a> correspondante de l’appareil. Une modification apportée au périphérique de rendu requiert la recréation de la chaîne de permutation.</li>
<li><p>Dans DXGI, les effets d’échange disponibles sont DXGI_SWAP_EFFECT_DISCARD et DXGI_SWAP_EFFECT_SEQUENTIAL. À compter de Windows 8, l’effet d’échange DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL est également disponible. Le tableau suivant montre un mappage de l’effet Direct3D 9 à DXGI swap. </p>
<table>
<thead>
<tr class="header">
<th>D3D9 l’effet d’échange</th>
<th>DXGI l’effet d’échange</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DSWAPEFFECT_DISCARD</td>
<td>DXGI_SWAP_EFFECT_DISCARD</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_COPY</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL avec 1 tampon</td>
</tr>
<tr class="odd">
<td>D3DSWAPEFFECT_FLIP</td>
<td>DXGI_SWAP_EFFECT_SEQUENTIAL avec au moins 2 tampons</td>
</tr>
<tr class="even">
<td>D3DSWAPEFFECT_FLIPEX</td>
<td>DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL avec au moins 2 tampons</td>
</tr>
</tbody>
</table>
<p></p>
<p> </p></li>
</ul></td>
</tr>
</tbody>
</table>



 

Les mémoires tampons d’une chaîne de permutation sont créées à une taille particulière et dans un format particulier. L’application spécifie ces valeurs (ou vous pouvez hériter de la taille de la fenêtre cible) au démarrage, puis peut éventuellement les modifier au fur et à mesure que la taille de la fenêtre change en réponse à l’entrée utilisateur ou aux événements du programme.

Une fois que vous avez créé la chaîne de permutation, vous souhaiterez généralement afficher des images dans celle-ci. Voici un fragment de code qui configure un contexte Direct3D pour le rendu dans une chaîne de permutation. Ce code extrait une mémoire tampon de la chaîne de permutation, crée un affichage de rendu-cible à partir de cette mémoire tampon, puis le définit sur l’appareil :


```
ID3D11Resource * pBB;
ThrowFailure( pSwapChain->GetBuffer(0, __uuidof(pBB),    
  reinterpret_cast<void**>(&pBB)), "Couldn't get back buffer");
ID3D11RenderTargetView * pView;
ThrowFailure( pD3D11Device->CreateRenderTargetView(pBB, NULL, &pView), 
  "Couldn't create view" );
pD3D11DeviceContext->OMSetRenderTargets(1, &pView, 0);
        
```



Une fois que votre application a rendu un frame dans une mémoire tampon de chaîne d’échange, appelez [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1). L’application peut ensuite effectuer le rendu de l’image suivante.

### <a name="care-and-feeding-of-the-swap-chain"></a>Soins et alimentation de la chaîne de permutation

Une fois que vous avez rendu votre image, appelez [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) et Go Affichez l’image suivante. Il s’agit de l’étendue de votre responsabilité.

Si vous avez précédemment appelé [**IDXGIFactory :: MakeWindowAssociation**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-makewindowassociation), l’utilisateur peut appuyer sur la combinaison de touches Alt-Enter et dxgi passera votre application entre le mode fenêtre et le mode plein écran. **IDXGIFactory :: MakeWindowAssociation** est recommandé, car un mécanisme de contrôle standard pour l’utilisateur est fortement souhaité.

Si vous n’avez pas besoin d’écrire davantage de code que celui qui a été décrit, quelques étapes simples peuvent rendre votre application plus réactive. La considération la plus importante est le redimensionnement des mémoires tampons de la chaîne d’échange en réponse au redimensionnement de la fenêtre de sortie. Naturellement, le meilleur itinéraire de l’application consiste à répondre à la taille de WM \_ et à appeler [**IDXGISwapChain :: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers), en passant la taille contenue dans les paramètres du message. Ce comportement fait évidemment que votre application réponde bien à l’utilisateur lorsqu’il fait glisser les bordures de la fenêtre, mais c’est aussi exactement ce qui permet une transition en plein écran lisse. Votre fenêtre reçoit un message de \_ taille WM à chaque fois qu’une telle transition se produit, et l’appel de **IDXGISwapChain :: ResizeBuffers** est l’occasion pour la chaîne de permutation de réallouer le stockage des mémoires tampons pour une présentation optimale. C’est la raison pour laquelle l’application doit libérer toutes les références qu’elle possède sur les mémoires tampons existantes avant d’appeler **IDXGISwapChain :: ResizeBuffers**.

L’échec de l’appel de [**IDXGISwapChain :: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) en réponse au basculement en mode plein écran (le plus naturellement, en réponse à \_ la taille de WM), peut empêcher l’optimisation de la rotation, où dxgi peut simplement permuter la mémoire tampon affichée, plutôt que de copier les données d’un plein écran.

[**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) vous indique si votre fenêtre de sortie est entièrement bloqués via **dxgi \_ Status \_ bloqués**. Dans ce cas, nous vous recommandons de passer en mode veille (en appelant **IDXGISwapChain1 ::P resent1** avec le **\_ \_ test dxgi présent**), car les ressources utilisées pour le rendu du frame sont gaspillées. L’utilisation de **dxgi \_ présente un \_ test** empêchera la présentation de toutes les données pendant que le contrôle d’occlusion est toujours en cours d’exécution. Une fois **IDXGISwapChain1 ::P resent1** retourne S \_ OK, vous devez quitter le mode veille ; n’utilisez pas le code de retour pour basculer en mode veille, car cela peut permettre à la chaîne de permutation de quitter le mode plein écran.

Le runtime Direct3D 11,1, qui est disponible à partir de Windows 8, fournit une chaîne de permutation de modèle (autrement dit, une chaîne de permutation qui a l' [**effet d’échange dxgi retourne une valeur \_ \_ \_ \_ séquentielle**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) définie dans le membre **SwapEffect** de la chaîne d’échange [**dxgi \_ \_ \_ desc**](/windows/win32/api/DXGI/ns-dxgi-dxgi_swap_chain_desc) ou dxgi chaîne de permutation [**\_ \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Lorsque vous présentez des frames dans une sortie avec une chaîne de permutation-modèle, DXGI dissocie la mémoire tampon d’arrière-plan de tous les emplacements d’état de pipeline, comme une cible de rendu de fusion de sortie, qui écrivent dans la mémoire tampon d’arrière-plan 0. Par conséquent, nous vous recommandons d’appeler [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-omsetrendertargets) immédiatement avant d’effectuer le rendu dans la mémoire tampon d’arrière-plan. Par exemple, n’appelez pas **OMSetRenderTargets** , puis effectuez le calcul du nuanceur de calcul qui n’finit pas par le rendu de la ressource. Pour plus d’informations sur les chaînes de permutation-modèle et leurs avantages, consultez [dxgi Flip Model](dxgi-flip-model.md).

> [!NOTE]  
> Dans Direct3D 10 et Direct3D 11, vous n’avez pas besoin d’appeler [**IDXGISwapChain :: GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer) pour récupérer la mémoire tampon d’arrière-plan 0 après avoir appelé [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) , car pour des raisons pratiques, les identités des mémoires tampons d’arrière-plan changent. Cela ne se produit pas dans Direct3D 12, et votre application doit à la place suivre manuellement les index de mémoire tampon d’arrière-plan.

### <a name="handling-window-resizing"></a>Gérer le redimensionnement de fenêtre

Vous pouvez utiliser la méthode [**IDXGISwapChain :: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) pour gérer le redimensionnement de fenêtre. Avant d’appeler **ResizeBuffers**, vous devez libérer toutes les références en suspens aux mémoires tampons de la chaîne d’échange. L’objet qui contient généralement une référence à la mémoire tampon d’une chaîne de permutation est une vue de rendu-cible.

L’exemple de code suivant montre comment appeler [**ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) à partir du gestionnaire WindowProc pour les \_ messages de taille WM :


```
    case WM_SIZE:
        if (g_pSwapChain)
        {
            g_pd3dDeviceContext->OMSetRenderTargets(0, 0, 0);

            // Release all outstanding references to the swap chain's buffers.
            g_pRenderTargetView->Release();

            HRESULT hr;
            // Preserve the existing buffer count and format.
            // Automatically choose the width and height to match the client rect for HWNDs.
            hr = g_pSwapChain->ResizeBuffers(0, 0, 0, DXGI_FORMAT_UNKNOWN, 0);
                                            
            // Perform error handling here!

            // Get buffer and create a render-target-view.
            ID3D11Texture2D* pBuffer;
            hr = g_pSwapChain->GetBuffer(0, __uuidof( ID3D11Texture2D),
                                         (void**) &pBuffer );
            // Perform error handling here!

            hr = g_pd3dDevice->CreateRenderTargetView(pBuffer, NULL,
                                                     &g_pRenderTargetView);
            // Perform error handling here!
            pBuffer->Release();

            g_pd3dDeviceContext->OMSetRenderTargets(1, &g_pRenderTargetView, NULL );

            // Set up the viewport.
            D3D11_VIEWPORT vp;
            vp.Width = width;
            vp.Height = height;
            vp.MinDepth = 0.0f;
            vp.MaxDepth = 1.0f;
            vp.TopLeftX = 0;
            vp.TopLeftY = 0;
            g_pd3dDeviceContext->RSSetViewports( 1, &vp );
        }
        return 1;
```



### <a name="choosing-the-dxgi-output-and-size"></a>Choix de la sortie et de la taille DXGI

Par défaut, DXGI choisit la sortie qui contient la plus grande partie de la zone cliente de la fenêtre. Il s’agit de la seule option disponible pour DXGI lorsqu’elle s’affiche en plein écran en réponse à Alt-Entrée. Si l’application choisit de passer en mode plein écran par lui-même, elle peut appeler [**IDXGISwapChain :: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) et passer un [**IDXGIOutput1**](/windows/win32/api/DXGI1_2/nn-dxgi1_2-idxgioutput1) explicite (ou **null**, si l’application est heureux de laisser dxgi décider).

Pour redimensionner la sortie en mode plein écran ou dans une fenêtre, nous vous recommandons d’appeler [**IDXGISwapChain :: ResizeTarget**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizetarget), car cette méthode redimensionne également la fenêtre cible. Étant donné que la fenêtre cible est redimensionnée, le système d’exploitation envoie la **\_ taille de WM** et votre code appellera naturellement [**IDXGISwapChain :: ResizeBuffers**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) dans la réponse. Il s’agit donc d’un gaspillage de l’effort pour redimensionner vos mémoires tampons, puis de redimensionner ensuite la cible.

### <a name="debugging-in-full-screen-mode"></a>Débogage en mode plein écran

Une chaîne de permutation DXGI abandonne le mode plein écran uniquement lorsque cela est absolument nécessaire. Cela signifie que vous pouvez déboguer une application en plein écran à l’aide de plusieurs moniteurs, à condition que la fenêtre de débogage ne chevauche pas la fenêtre cible de la chaîne de permutation. Vous pouvez également empêcher le basculement du mode en ne définissant pas l’indicateur de commutateur de la **\_ chaîne d’échange dxgi \_ \_ \_ allow \_ mode \_** .

Si le basculement de mode est autorisé, une chaîne de permutation abandonnera le mode plein écran chaque fois que sa fenêtre de sortie sera bloqués par une autre fenêtre. Le contrôle d’occlusion est effectué pendant [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)ou par un thread distinct dont l’objectif est de surveiller si l’application ne répond plus (et n’appelle plus **IDXGISwapChain1 ::P resent1**). Pour désactiver la capacité du thread distinct à provoquer un basculement, définissez la clé de Registre suivante sur une valeur différente de zéro.

**\\Logiciel HKCU \\ Microsoft \\ dxgi \\ DisableFullscreenWatchdog**

### <a name="destroying-a-swap-chain"></a>Destruction d’une chaîne de permutation

Vous ne pouvez pas libérer une chaîne de permutation en mode plein écran, car cela risque de créer une contention de thread (ce qui entraîne la levée d’une exception non continuable par DXGI). Avant de libérer une chaîne de permutation, passez tout d’abord en mode fenêtre (à l’aide de [**IDXGISwapChain :: SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate)( **false**, **null** )), puis appelez [**IUnknown :: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release).

### <a name="using-a-rotated-monitor"></a>Utilisation d’une analyse pivotée

Une application n’a pas besoin de se soucier de l’orientation du moniteur, DXGI fera pivoter une mémoire tampon de chaîne d’échange pendant la présentation, si nécessaire. Bien entendu, cette rotation supplémentaire peut avoir un impact sur les performances. Pour de meilleures performances, prenez en charge la rotation dans votre application en procédant comme suit :

-   Utilisez l' **\_ indicateur de chaîne d’échange dxgi \_ \_ \_ NONPREROTATED**. Cela indique à DXGI que l’application produit une image pivotée (par exemple, en modifiant sa matrice de projection). Une chose à noter, cet indicateur est uniquement valide en mode plein écran.
-   Allouez chaque mémoire tampon de chaîne d’échange dans sa taille pivotée. Utilisez [**IDXGIOutput :: GetDesc**](/windows/win32/api/DXGI/nf-dxgi-idxgioutput-getdesc) pour récupérer ces valeurs, si nécessaire.

En effectuant la rotation dans votre application, DXGI effectue simplement une copie au lieu d’une copie et d’une rotation.

Le runtime Direct3D 11,1, qui est disponible à partir de Windows 8, fournit une chaîne de permutation de modèle (autrement dit, une chaîne de permutation qui a l' [**effet d’échange dxgi retourne une valeur \_ \_ \_ \_ séquentielle**](/windows/win32/api/DXGI/ne-dxgi-dxgi_swap_effect) définie dans le membre **SwapEffect** de la [**chaîne de \_ permutation dxgi \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Pour optimiser les optimisations de présentation disponibles avec une chaîne de permutation-modèle, nous vous recommandons de faire en sorte que vos applications orientent le contenu pour correspondre à la sortie particulière sur laquelle le contenu réside lorsque ce contenu occupe entièrement la sortie. Pour plus d’informations sur les chaînes de permutation-modèle et leurs avantages, consultez [dxgi Flip Model](dxgi-flip-model.md).

### <a name="switching-modes"></a>Modes de basculement

La chaîne de permutation DXGI peut modifier le mode d’affichage d’une sortie lors d’une transition en plein écran. Pour activer la modification du mode d’affichage automatique, vous devez spécifier le **\_ \_ \_ \_ \_ \_ commutateur du mode allow de l’indicateur de chaîne d’échange dxgi** dans la description de la chaîne d’échange. Si le mode d’affichage change automatiquement, DXGI choisit le mode le plus modeste (la taille et la résolution ne changent pas, mais la profondeur de couleur peut être). Le redimensionnement des tampons de chaîne d’échange n’entraîne pas de basculement de mode. La chaîne de permutation fait une promesse implicite que si vous choisissez une mémoire tampon d’arrière-plan qui correspond exactement à un mode d’affichage pris en charge par la sortie cible, elle bascule sur ce mode d’affichage lors de l’entrée en mode plein écran sur cette sortie. Par conséquent, vous choisissez un mode d’affichage en choisissant la taille et le format de la mémoire tampon d’arrière-plan.

### <a name="full-screen-performance-tip"></a>Conseil sur les performances plein écran

Quand vous appelez [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) sur une application en plein écran, la chaîne de permutation retourne (par opposition à BLITS) le contenu de la mémoire tampon d’arrière-plan dans la mémoire tampon d’arrière-plan. Cela nécessite la création de la chaîne de permutation à l’aide d’un mode d’affichage énuméré (spécifié dans la [**\_ chaîne de permutation dxgi \_ \_ DESC1**](/windows/win32/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1)). Si vous ne parvenez pas à énumérer les modes d’affichage ou si vous spécifiez incorrectement le mode d’affichage dans la description, la chaîne de permutation peut effectuer un transfert de bloc de bits (BitBlt) à la place. Le BitBlt provoque une copie d’étirement supplémentaire, ainsi qu’une augmentation de l’utilisation de la mémoire vidéo et est difficile à détecter. Pour éviter ce problème, énumérez les modes d’affichage et initialisez correctement la description de la chaîne de permutation avant de créer la chaîne de permutation. Cela permet de garantir des performances optimales lors du basculement en mode plein écran et d’éviter la surcharge de mémoire supplémentaire.

### <a name="multithread-considerations"></a>Considérations multithread

Quand vous utilisez DXGI dans une application avec plusieurs threads, vous devez veiller à éviter de créer un interblocage, où deux threads différents attendent l’un l’autre. Il existe deux situations dans lesquelles cela peut se produire.

-   Le thread de rendu n’est pas le thread de pompe de messages.
-   Le thread qui exécute une API DXGI n’est pas le même que celui qui a créé la fenêtre.

Veillez à ne jamais attendre le thread de pompe de messages sur le thread de rendu quand vous utilisez des chaînes d’échange plein écran. Par exemple, l’appel de [**IDXGISwapChain1 ::P resent1**](/windows/win32/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) (à partir du thread de rendu) peut entraîner l’attente du thread de rendu sur le thread de pompe de messages. Quand une modification du mode se produit, ce scénario est possible si **Present1** appelle :: SetWindowPos () ou :: SetWindowStyle () et que l’une ou l’autre de ces méthodes appelle :: SendMessage (). Dans ce scénario, si le thread de pompe de messages a une section critique qui le protège ou si le thread de rendu est bloqué, les deux threads se bloquent.

Pour plus d’informations sur l’utilisation de DXGI avec plusieurs threads, consultez [Multithreading et dxgi](../direct3d11/overviews-direct3d-11-render-multi-thread-intro.md).

## <a name="dxgi-responses-from-dllmain"></a>DXGI les réponses de DLLMain

Étant donné qu’une fonction [**DllMain**](../dlls/dllmain.md) ne peut pas garantir l’ordre de chargement et de déchargement des dll, il est recommandé que la fonction **DllMain** de votre application n’appelle pas les fonctions ou méthodes Direct3D ou dxgi, y compris les fonctions ou les méthodes qui créent ou libèrent des objets. Si la fonction **DllMain** de votre application appelle un composant particulier, ce composant peut appeler une autre dll qui n’est pas présente sur le système d’exploitation, ce qui entraîne l’arrêt du système d’exploitation. Direct3D et DXGI peuvent charger un ensemble de dll, généralement un ensemble de pilotes, qui diffère d’un ordinateur à l’ordinateur. Par conséquent, même si votre application ne se bloque pas sur vos ordinateurs de développement et de test lorsque sa fonction **DllMain** appelle des fonctions ou des méthodes Direct3D ou dxgi, elle peut se bloquer lorsqu’elle s’exécute sur un autre ordinateur.

Pour vous empêcher de créer une application susceptible de provoquer le blocage du système d’exploitation, DXGI fournit les réponses suivantes dans les situations spécifiées :

-   Si la fonction [**DllMain**](../dlls/dllmain.md) de votre application libère sa dernière référence à une fabrique DXGI, DXGI lève une exception.
-   Si la fonction [**DllMain**](../dlls/dllmain.md) de votre application crée une fabrique DXGI, DXGI retourne un code d’erreur.

## <a name="dxgi-11-changes"></a>Modifications apportées à DXGI 1,1

Nous avons ajouté les fonctionnalités suivantes dans DXGI 1,1.

-   Prise en charge des surfaces partagées synchronisées

    Les surfaces partagées synchronisées pour Direct3D 10,1 et Direct3D 11 permettent un partage des surfaces de lecture et d’écriture efficace entre plusieurs périphériques Direct3D (le partage entre les appareils Direct3D 10 et Direct3D 11 est possible). Consultez [**IDXGIKeyedMutex :: AcquireSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-acquiresync) et [**IDXGIKeyedMutex :: ReleaseSync**](/windows/win32/api/DXGI/nf-dxgi-idxgikeyedmutex-releasesync).

-   Prise en charge des couleurs élevées

    Prend en charge \_ le \_ format dxgi R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM.

-   [**IDXGIDevice1 :: SetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-setmaximumframelatency) et [ **IDXGIDevice1 :: GetMaximumFrameLatency**](/windows/win32/api/DXGI/nf-dxgi-idxgidevice1-getmaximumframelatency)
-   [**IDXGIFactory1 :: EnumAdapters1**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory1-enumadapters1) énumère les adaptateurs locaux sans moniteurs ou sorties attachés, ainsi que les adaptateurs avec des sorties attachées. Le premier adaptateur retourné sera l’adaptateur local sur lequel le bureau principal est affiché.
-   Prise en charge du format BGRA

    DXGI \_ format \_ B8G8R8A8 \_ UNORM et dxgi \_ format \_ B8G8R8A8 \_ UNORM \_ sRGB, consultez [**IDXGISurface1 :: GetDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-getdc) et [**IDXGISurface1 :: ReleaseDC**](/windows/win32/api/DXGI/nf-dxgi-idxgisurface1-releasedc).

## <a name="dxgi-12-changes"></a>Modifications apportées à DXGI 1,2

Nous avons ajouté les fonctionnalités suivantes dans DXGI 1,2.

-   Chaîne d’échange stéréo
-   [Chaîne d’échange Flip-Model](dxgi-flip-model.md)
-   Présentation optimisée (défilement, rectangles modifiés et rotation)
-   Amélioration des ressources partagées et de la synchronisation
-   [Duplication des postes de travail](desktop-dup-api.md)
-   Utilisation optimisée de la mémoire vidéo
-   Prise en charge des formats de 16 bits par pixel (BPP) (DXGI \_ format \_ B5G6R5 \_ UNORM, DXGI \_ format \_ B5G5R5A1 \_ UNORM, DXGI \_ format \_ \_ B4G4R4A4 UNORM)
-   API de débogage

Pour plus d’informations sur DXGI 1,2, consultez [améliorations apportées à DXGI 1,2](dxgi-1-2-improvements.md).

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
