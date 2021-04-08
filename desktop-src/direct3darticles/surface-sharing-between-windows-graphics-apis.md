---
title: Partage de surface entre les API graphiques Windows
description: Cette rubrique fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre les API graphiques Windows, notamment Direct3D 11, Direct2D, DirectWrite, Direct3D 10 et Direct3D 9Ex.
ms.assetid: 65abf33e-3d15-42ff-99bd-674f24da773e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d889797902c964e603adefc51b25039afca7d46
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730764"
---
# <a name="surface-sharing-between-windows-graphics-apis"></a>Partage de surface entre les API graphiques Windows

Cette rubrique fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre les API graphiques Windows, notamment Direct3D 11, Direct2D, DirectWrite, Direct3D 10 et Direct3D 9Ex. Si vous avez déjà une connaissance de ces API, ce document peut vous aider à utiliser plusieurs API pour effectuer un rendu sur la même surface dans une application conçue pour les systèmes d’exploitation Windows 7 ou Windows Vista. Cette rubrique présente également les meilleures pratiques et les pointeurs vers des ressources supplémentaires.

> [!Note]  
> Pour l’interopérabilité de Direct2D et DirectWrite sur le runtime DirectX 11,1, vous pouvez utiliser des [appareils Direct2D et des contextes de périphérique](/windows/desktop/Direct2D/devices-and-device-contexts) pour effectuer un rendu direct sur les périphériques Direct3D 11.

 

Cette rubrique contient les sections suivantes.

-   [Introduction](#introduction)
-   [Vue d’ensemble de l’interopérabilité des API](#api-interoperability-overview)
-   [Scénarios d’interopérabilité](#interoperability-scenarios)
    -   [Partage d’appareils Direct3D 10,1 avec Direct2D](#direct3d-101-device-sharing-with-direct2d)
    -   [DXGI 1,1 surfaces partagées synchronisées](#dxgi-11-synchronized-shared-surfaces)
    -   [Interopérabilité entre les API Direct3D 9Ex et DXGI](#interoperability-between-direct3d-9ex-and-dxgi-based-apis)
-   [Conclusion](#conclusion)

## <a name="introduction"></a>Introduction

Dans ce document, l’interopérabilité des API Windows Graphics fait référence au partage de la même surface de rendu par différentes API. Ce type d’interopérabilité permet aux applications de créer des affichages attrayants en tirant parti de plusieurs API graphiques Windows et de faciliter la migration vers de nouvelles technologies en conservant la compatibilité avec les API existantes.

Dans Windows 7 (et Windows Vista SP2 avec Windows 7 Interop Pack, Vista 7IP), les API de rendu graphiques sont Direct3D 11, Direct2D, Direct3D 10,1, Direct3D 10,0, Direct3D 9Ex, Direct3D 9c et les API Direct3D antérieures, ainsi que GDI et GDI+. WIC (Windows Imaging Component) et DirectWrite sont des technologies associées au traitement des images, et Direct2D effectue le rendu du texte. L’API d’accélération vidéo DirectX (DXVA), basée sur Direct3D 9c et Direct3D 9Ex, est utilisée pour le traitement vidéo.

À mesure que les API graphiques Windows évoluent vers la base Direct3D, Microsoft investit plus d’efforts pour garantir l’interopérabilité entre les API. Les API Direct3D récemment développées et les API de niveau supérieur basées sur les API Direct3D prennent également en charge les cas nécessaires pour assurer la compatibilité avec les anciennes API. Pour illustrer cela, les applications Direct2D peuvent utiliser Direct3D 10,1 en partageant un appareil Direct3D 10,1. En outre, les API Direct3D 11, Direct2D et Direct3D 10,1 peuvent tous tirer parti de DirectX Graphics infrastructure (DXGI) 1,1, qui permet des surfaces partagées synchronisées qui prennent entièrement en charge l’interopérabilité entre ces API. Les API DXGI 1,1 interagissent avec GDI et avec GDI+ par Association, en obtenant le contexte de périphérique GDI à partir d’une surface DXGI 1,1. Pour plus d’informations, consultez la documentation relative à l’interopérabilité DXGI et GDI disponible sur MSDN.

Le partage de surface non synchronisé est pris en charge par le runtime Direct3D 9Ex. Les applications vidéo DXVA peuvent utiliser l’application auxiliaire Direct3D 9Ex et DXGI Interoperability pour l’interopérabilité DXVA basée sur Direct3D 9Ex avec Direct3D 11 pour le nuanceur de calcul, ou peuvent interagir avec Direct2D pour les contrôles 2D ou le rendu de texte. WIC et DirectWrite interagissent également avec GDI, Direct2D et par Association, d’autres API Direct3D.

Direct3D 10,0, Direct3D 9c et les runtimes Direct3D plus anciens ne prennent pas en charge les surfaces partagées. Les copies de mémoire système seront toujours utilisées pour l’interopérabilité avec les API GDI ou DXGI.

Notez que les scénarios d’interopérabilité dans ce document font référence à plusieurs API graphiques qui sont rendues sur une surface de rendu partagée, plutôt que dans la même fenêtre d’application. La synchronisation pour des API distinctes ciblant des surfaces différentes qui sont ensuite réparties dans la même fenêtre n’entre pas dans le cadre de ce document.

## <a name="api-interoperability-overview"></a>Vue d’ensemble de l’interopérabilité des API

L’interopérabilité du partage de surface des API graphiques Windows peut être décrite en termes de scénarios API-API et de fonctionnalités d’interopérabilité correspondantes. À compter de Windows 7 et de Windows Vista SP2 avec 7IP, les nouvelles API et les runtimes associés incluent Direct2D et les technologies associées : Direct3D 11 et DXGI 1,1. Les performances GDI ont également été améliorées dans Windows 7. Direct3D 10,1 a été introduit dans Windows Vista SP1. Le diagramme suivant illustre la prise en charge de l’interopérabilité entre les API.

![diagramme de prise en charge de l’interopérabilité entre les API graphiques Windows](images/surface-sharing-interoperability.png)

Dans ce diagramme, les flèches indiquent les scénarios d’interopérabilité dans lesquels la même surface peut être accessible par les API connectées. Les flèches bleues indiquent les mécanismes d’interopérabilité introduits dans Windows Vista. Les flèches vertes indiquent la prise en charge de l’interopérabilité pour les nouvelles API ou les améliorations qui aident les API plus anciennes à interagir avec les API plus récentes. Par exemple, les flèches vertes représentent le partage d’appareil, la prise en charge de la surface partagée, la prise en charge de la synchronisation Direct3D 9Ex/DXGI et l’obtention d’un contexte de périphérique GDI à partir d’une surface compatible.

## <a name="interoperability-scenarios"></a>Scénarios d’interopérabilité

À compter de Windows 7 et Windows Vista 7IP, les offres standard des API graphiques Windows prennent en charge plusieurs API de rendu sur la même surface DXGI 1,1.

**Direct3D 11, Direct3D 10,1, Direct2D : interopérabilité les unes avec les autres**

Les API Direct3D 11, Direct3D 10,1 et Direct2D (et les API associées telles que DirectWrite et WIC) peuvent interagir entre elles à l’aide des surfaces partagées de partage d’appareil ou de partage Direct3D 10,1.

### <a name="direct3d-101-device-sharing-with-direct2d"></a>Partage d’appareils Direct3D 10,1 avec Direct2D

Le partage d’appareils entre Direct2D et Direct3D 10,1 permet à une application d’utiliser les deux API pour effectuer un rendu fluide et efficace sur la même surface DXGI 1,1, à l’aide du même objet appareil Direct3D sous-jacent. Direct2D offre la possibilité d’appeler des API Direct2D à l’aide d’un périphérique Direct3D 10,1 existant, en tirant parti du fait que Direct2D repose sur les runtimes Direct3D 10,1 et DXGI 1,1. Les extraits de code suivants montrent comment Direct2D obtient la cible de rendu de l’appareil Direct3D 10,1 à partir d’une surface DXGI 1,1 associée à l’appareil. La cible de rendu de l’appareil Direct3D 10,1 peut exécuter des appels de dessin Direct2D entre les API BeginDraw et EndDraw.


```C++
// Direct3D 10.1 Device and Swapchain creation
HRESULT hr = D3D10CreateDeviceandSwapChain1(
                pAdapter,
                DriverType,
                Software,
                D3D10_CREATE_DEVICE_BGRA_SUPPORT,
                featureLevel,
                D3D10_1_SDK_VERSION,
                pSwapChainDesc,
                &pSwapChain,
                &pDevice
                );

hr = pSwapChain->GetBuffer(
        0,
        __uuidof(IDXGISurface),
        (void **)&pDXGIBackBuffer
        ));

// Direct3D 10.1 API rendering calls
...

hr = D2D1CreateFactory(
        D2D1_FACTORY_TYPE_SINGLE_THREADED,
        &m_spD2DFactory
        ));

pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pDXGIBackBuffer,
        &renderTargetProperties,
        &pD2DBackBufferRenderTarget
        ));
...

pD2DBackBufferRenderTarget->BeginDraw();
//Direct2D API rendering calls
...

pD2DBackBufferRenderTarget->EndDraw();

pSwapChain->Present(0, 0);
```



**Remarques**

-   L’appareil Direct3D 10,1 associé doit prendre en charge le format BGRA. Cet appareil a été créé en appelant D3D10CreateDevice1 avec le paramètre D3D10 \_ Create \_ Device \_ BGRA \_ support. Le format BGRA est pris en charge à partir du niveau de fonctionnalité 9,1 de Direct3D 10.
-   L’application ne doit pas créer plusieurs ID2D1RenderTargets qui s’associent au même appareil Direct3D 10.1.
-   Pour des performances optimales, gardez à tout moment au moins une ressource, comme des textures ou des surfaces associées à l’appareil.

Le partage d’appareils est adapté à l’utilisation monothread et à thread unique d’un appareil de rendu partagé par les API de rendu Direct3D 10,1 et Direct2D. Les surfaces partagées synchronisées permettent l’utilisation multithread, in-process et out-of-process de plusieurs appareils de rendu utilisés par les API Direct3D 10,1, Direct2D et Direct3D 11.

Une autre méthode d’interopérabilité Direct3D 10,1 et Direct2D consiste à utiliser ID3D1RenderTarget :: CreateSharedBitmap, qui crée un objet ID2D1Bitmap à partir de IDXGISurface. Vous pouvez écrire une scène Direct3D 10.1 dans le bitmap et la restituer avec Direct2D. Pour plus d’informations, consultez la [méthode ID2D1RenderTarget :: CreateSharedBitmap](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap).

### <a name="direct2d-software-rasterization"></a>Pixellisation de logiciels Direct2D

Le partage d’appareils avec Direct3D 10,1 n’est pas pris en charge lors de l’utilisation du convertisseur de logiciel Direct2D, par exemple, en spécifiant l' \_ \_ utilisation de la cible de rendu d2d1 \_ \_ force \_ \_ le rendu logiciel dans l’utilisation de la cible de rendu d2d1 \_ lors de \_ \_ la création d’une cible de rendu Direct2D.

Direct2D peut utiliser le rastériseur logiciel WARP10 pour partager des appareils avec Direct3D 10 ou Direct3D 11, mais les performances diminuent considérablement.

### <a name="dxgi-11-synchronized-shared-surfaces"></a>DXGI 1,1 surfaces partagées synchronisées

Direct3D 11, Direct3D 10,1 et les API Direct2D utilisent tous DXGI 1,1, qui fournit les fonctionnalités permettant de synchroniser la lecture et l’écriture dans la même surface de mémoire vidéo (DXGISurface1) par deux ou plusieurs périphériques Direct3D. Les appareils de rendu utilisant des surfaces partagées synchronisées peuvent être des appareils Direct3D 10,1 ou Direct3D 11, chacun s’exécutant dans le même processus ou des processus interactifs.

Les applications peuvent utiliser des surfaces partagées synchronisées pour interagir entre n’importe quel appareil DXGI 1,1, tel que Direct3D 11 et Direct3D 10,1, ou entre Direct3D 11 et Direct2D, en obtenant l’appareil Direct3D 10,1 à partir de l’objet cible de rendu Direct2D.

Dans les API Direct3D 10,1 et versions ultérieures, pour utiliser DXGI 1,1, assurez-vous que le périphérique Direct3D est créé à l’aide d’un objet d’adaptateur DXGI 1,1, qui est énuméré à partir de l’objet de fabrique DXGI 1,1. Appelez CreateDXGIFactory1 pour créer l’objet IDXGIFactory1, et EnumAdapters1 pour énumérer l’objet IDXGIAdapter1. L’objet IDXGIAdapter1 doit être passé dans le cadre de l’appel D3D10CreateDevice ou D3D10CreateDeviceAndSwapChain. Pour plus d’informations sur les API DXGI 1,1, consultez le [Guide de programmation pour dxgi](https://msdn.microsoft.com/library/ee418147(VS.85).aspx).

### <a name="apis"></a>API

**D3D10 \_ ressources \_ \_ partagées divers \_ KEYEDMUTEX**  
Lors de la création de la ressource partagée synchronisée, définissez D3D10 \_ Resource \_ misc \_ Shared \_ KEYEDMUTEX dans l' \_ indicateur misc des ressources D3D10 \_ \_ .  


```C++
typedef enum D3D10_RESOURCE_MISC_FLAG {
    D3D10_RESOURCE_MISC_GENERATE_MIPS      = 0x1L,
    D3D10_RESOURCE_MISC_SHARED             = 0x2L,
    D3D10_RESOURCE_MISC_TEXTURECUBE        = 0x4L,
    D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX  = 0x10L,
    D3D10_RESOURCE_MISC_GDI_COMPATIBLE     = 0x20L,
}   D3D10_RESOURCE_MISC_FLAG;
```



**D3D10 \_ ressources \_ \_ partagées divers \_ KEYEDMUTEX**  
Permet à la ressource créée d’être synchronisée à l’aide des API IDXGIKeyedMutex :: AcquireSync et ReleaseSync. Les API de création de ressource Direct3D 10,1 suivantes qui prennent toutes \_ un \_ \_ paramètre d’indicateur de ressource D3D10 ont été étendues pour prendre en charge le nouvel indicateur.  

-   ID3D10Device1::CreateTexture1D
-   ID3D10Device1::CreateTexture2D
-   ID3D10Device1::CreateTexture3D
-   ID3D10Device1 :: CreateBuffer

  
Si l’une des fonctions répertoriées est appelée avec l' \_ indicateur de KEYEDMUTEX partagé divers de la ressource D3D10, \_ \_ \_ l’interface retournée peut être interrogée pour une interface IDXGIKeyedMutex, qui implémente les API AcquireSync et ReleaseSync pour synchroniser l’accès à la surface. L’appareil qui crée la surface et tout autre appareil ouvrant l’aire (à l’aide de OpenSharedResource) est requis pour appeler IDXGIKeyedMutex :: AcquireSync avant toute commande de rendu sur la surface, et IDXGIKeyedMutex :: ReleaseSync une fois le rendu terminé.  
Les appareils WARP et REF ne prennent pas en charge les ressources partagées. Si vous tentez de créer une ressource avec cet indicateur sur un appareil WARP ou REF, la méthode Create renverra un \_ code d’erreur E OUTOFMEMORY.  
**INTERFACE IDXGIKEYEDMUTEX**  
Une nouvelle interface dans DXGI 1,1, IDXGIKeyedMutex, représente un mutex à clé qui permet un accès exclusif à une ressource partagée qui est utilisée par plusieurs appareils. Pour obtenir une documentation de référence sur cette interface et ses deux méthodes, AcquireSync et ReleaseSync, consultez [IDXGIKeyedMutex](https://msdn.microsoft.com/library/ee421920(VS.85).aspx).  
</dl>

### <a name="sample-synchronized-surface-sharing-between-two-direct3d-101-devices"></a>Exemple : partage de surface synchronisé entre deux appareils Direct3D 10,1

L’exemple ci-dessous illustre le partage d’une surface entre deux périphériques Direct3D 10,1. La surface partagée synchronisée est créée par un appareil Direct3D 10.1.


```C++
// Create Sync Shared Surface using Direct3D10.1 Device 1.
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = width;
desc.Height = height;
desc.MipLevels = 1;
desc.ArraySize = 1;
// must match swapchain format in order to CopySubresourceRegion.
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
// creates 2D texture as a Synchronized Shared Surface.
desc.MiscFlags = D3D10_RESOURCE_MISC_SHARED_KEYEDMUTEX;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
ID3D10Texture2D* g_pShared = NULL;
g_pd3dDevice1->CreateTexture2D( &desc, NULL, &g_pShared );

// QI IDXGIResource interface to synchronized shared surface.
IDXGIResource* pDXGIResource = NULL;
g_pShared->QueryInterface(__uuidof(IDXGIResource), (LPVOID*) &pDXGIResource);

// obtain handle to IDXGIResource object.
pDXGIResource->GetSharedHandle(&g_hsharedHandle);
pDXGIResource->Release();
if ( !g_hsharedHandle )
    return E_FAIL;

// QI IDXGIKeyedMutex interface of synchronized shared surface's resource handle.
hr = g_pShared->QueryInterface( __uuidof(IDXGIKeyedMutex),
    (LPVOID*)&g_pDXGIKeyedMutex_dev1 );
If ( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev1 == NULL ) )
    return E_FAIL;
```



Le même appareil Direct3D 10.1 peut obtenir la surface partagée synchronisée pour le rendu en appelant AcquireSync, puis libérer la surface pour le rendu de l’autre appareil en appelant ReleaseSync. Lorsqu’il ne partage pas la surface partagée synchronisée avec un autre périphérique Direct3D, le créateur peut obtenir et libérer la surface partagée synchronisée (pour démarrer et terminer le rendu) en acquérant et en libérant à l’aide de la même valeur de clé.


```C++
// Obtain handle to Sync Shared Surface created by Direct3D10.1 Device 1.
hr = g_pd3dDevice2->OpenSharedResource( g_hsharedHandle,__uuidof(ID3D10Texture2D),
                                        (LPVOID*) &g_pdev2Shared);
if (FAILED (hr))
    return hr;
hr = g_pdev2Shared->QueryInterface( __uuidof(IDXGIKeyedMutex),
                                    (LPVOID*) &g_pDXGIKeyedMutex_dev2);
if( FAILED( hr ) || ( g_pDXGIKeyedMutex_dev2 == NULL ) )
    return E_FAIL;

// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2.
UINT acqKey = 1;
UINT relKey = 0;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev2->AcquireSync(acqKey, timeOut);
if ( result == WAIT_OBJECT_0 )
    // Rendering calls using Device 2.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev2->ReleaseSync(relKey));
if (result == WAIT_OBJECT_0)
    return S_OK;
```



Le deuxième appareil Direct3D 10.1 peut obtenir la surface partagée synchronisée pour le rendu en appelant AcquireSync, puis libérer la surface pour le rendu du premier appareil en appelant ReleaseSync. Notez que l’appareil 2 est en mesure d’acquérir la surface partagée synchronisée à l’aide de la même valeur de clé que celle spécifiée dans l’appel ReleaseSync par l’appareil 1.


```C++
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1.
UINT acqKey = 0;
UINT relKey = 1;
DWORD timeOut = 5;
DWORD result = g_pDXGIKeyedMutex_dev1->AcquireSync(acqKey, timeOut);
if (result == WAIT_OBJECT_0)
    // Rendering calls using Device 1.
else
    // Handle unable to acquire shared surface error.
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(relKey));
if ( result == WAIT_OBJECT_0 )
    return S_OK;
```



Les appareils supplémentaires qui partagent la même surface peuvent avoir l’acquisition et la libération de la surface à l’aide de clés supplémentaires, comme indiqué dans les appels suivants.


```C++
// Within Device 1's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 1
result = g_pDXGIKeyedMutex_dev1->AcquireSync(0, timeOut);
// Rendering calls using Device 1
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(1);
...
////////////////////////////////////////////////////////////////////////////
// Within Device 2's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 2
result = g_pDXGIKeyedMutex_dev2->AcquireSync(1, timeOut);
// Rendering calls using Device 2
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(2);

////////////////////////////////////////////////////////////////////////////
// Within Device 3's process/thread:
// Rendering onto Sync Shared Surface from D3D10.1 Device 1 using D3D10.1 Device 3
result = g_pDXGIKeyedMutex_dev1->AcquireSync(2, timeOut);
// Rendering calls using Device 3
...
result = g_pDXGIKeyedMutex_dev1->ReleaseSync(0);
...
```



Notez qu’une application réelle peut toujours être rendue sur une surface intermédiaire qui est ensuite copiée dans la surface partagée pour empêcher tout appareil en attente sur un autre appareil partageant l’aire.

### <a name="using-synchronized-shared-surfaces-with-direct2d-and-direct3d-11"></a>Utilisation de surfaces partagées synchronisées avec Direct2D et Direct3D 11

De même, pour le partage entre les API Direct3D 11 et Direct3D 10,1, une surface partagée synchronisée peut être créée à partir d’un périphérique d’API et partagée avec les autres périphériques d’API, in ou out of process.

Les applications qui utilisent Direct2D peuvent partager un appareil Direct3D 10,1 et utiliser une surface partagée synchronisée pour interagir avec Direct3D 11 ou d’autres périphériques Direct3D 10,1, qu’ils appartiennent au même processus ou à des processus différents. Toutefois, pour les applications à un seul thread, le partage d’appareils est la méthode d’interopérabilité la plus performante et la plus efficace entre Direct2D et Direct3D 10 ou Direct3D 11.

### <a name="software-rasterizer"></a>Rastériseur logiciel

Les surfaces partagées synchronisées ne sont pas prises en charge lorsque les applications utilisent les rastériseurs de logiciel Direct3D ou Direct2D, y compris le rastériseur de référence et la déformation, au lieu d’utiliser l’accélération matérielle graphique.

### <a name="interoperability-between-direct3d-9ex-and-dxgi-based-apis"></a>Interopérabilité entre les API Direct3D 9Ex et DXGI

Les API Direct3D 9Ex comprenaient la notion de partage de surface pour permettre à d’autres API de lire à partir de la surface partagée. Pour partager la lecture et l’écriture dans une surface partagée Direct3D 9Ex, vous devez ajouter une synchronisation manuelle à l’application elle-même.

### <a name="direct3d-9ex-shared-surfaces-plus-manual-synchronization-helper"></a>Applications partagées Direct3D 9Ex et application auxiliaire de synchronisation manuelle

La tâche la plus fondamentale dans Direct3D 9Ex et Direct3D 10 ou 11 Interoperability consiste à passer une seule surface du premier appareil (appareil A) au deuxième (appareil B) de telle sorte que lorsque l’appareil B acquiert un handle sur la surface, le rendu de l’appareil A est garanti comme étant terminé. Par conséquent, l’appareil B peut utiliser cette surface sans crainte. Cela est très similaire au problème classique des consommateurs de producteurs et cette discussion modélise le problème de cette façon. Le premier appareil qui utilise la surface, puis l’abandon est le producteur (appareil A), et l’appareil qui est initialement en attente est le consommateur (appareil B). Toutes les applications réelles sont plus sophistiquées que cela, et enchaînent plusieurs blocs de construction producteur-consommateur pour créer les fonctionnalités souhaitées.

Les blocs de construction producteur-consommateur sont implémentés dans l’application auxiliaire à l’aide d’une file d’attente de surfaces. Les surfaces sont mises en file d’attente par le producteur et déplacées en file d’attente par le consommateur. Le programme d’assistance introduit trois interfaces COM : ISurfaceQueue, ISurfaceProducer et ISurfaceConsumer.

### <a name="high-level-overview-of-helper"></a>High-Level vue d’ensemble de l’application auxiliaire

L’objet ISurfaceQueue est le bloc de construction pour l’utilisation des surfaces partagées. Il est créé avec un appareil Direct3D initialisé et une description pour créer un nombre fixe de surfaces partagées. L’objet de file d’attente gère la création de ressources et l’ouverture de code. Le nombre et le type de surfaces sont fixes ; une fois les surfaces créées, l’application ne peut pas les ajouter ou les supprimer.

Chaque instance de l’objet ISurfaceQueue fournit une sorte de rue unidirectionnelle qui peut être utilisée pour envoyer des surfaces de l’appareil producteur à l’appareil consommateur. Plusieurs rues à sens unique peuvent être utilisées pour activer des scénarios de partage de surface entre des appareils d’applications spécifiques.

**Création/durée de vie des objets**  
Il existe deux façons de créer l’objet de file d’attente : via CreateSurfaceQueue ou via la méthode Clone de ISurfaceQueue. Étant donné que les interfaces sont des objets COM, la gestion de la durée de vie COM standard s’applique.  
**Modèle producteur/consommateur**  
Emqueue () : le producteur appelle cette fonction pour indiquer qu’elle est effectuée avec la surface, qui peut désormais devenir disponible pour un autre appareil. Lors du retour de cette fonction, l’appareil producteur ne dispose plus de droits sur la surface et il n’est pas possible de continuer à l’utiliser.  
Dequeue () : l’appareil consommateur appelle cette fonction pour obtenir une surface partagée. L’API garantit que toutes les surfaces déplacées en file d’attente sont prêtes à être utilisées.  
**Métadonnées**  
L’API prend en charge l’Association de métadonnées aux surfaces partagées.  
Enqueue () a la possibilité de spécifier des métadonnées supplémentaires qui seront transmises à l’appareil consommateur. Les métadonnées doivent être inférieures à un maximum connu au moment de la création.  
Dequeue () peut éventuellement passer une mémoire tampon et un pointeur vers la taille de la mémoire tampon. La file d’attente remplit la mémoire tampon avec les métadonnées de l’appel de mise en file d’attente correspondant.  
**clonage**  
Chaque objet ISurfaceQueue résout une synchronisation unidirectionnelle. Nous partons du principe que la grande majorité des applications utilisant cette API utilisera un système fermé. Le système le plus simple et fermé avec deux appareils qui envoient des surfaces en arrière-plan requiert deux files d’attente. L’objet ISurfaceQueue possède une méthode Clone () pour permettre la création de plusieurs files d’attente qui font toutes partie du même pipeline plus grand.  
Clone crée un nouvel objet ISurfaceQueue à partir d’un objet existant et partage toutes les ressources ouvertes entre eux. L’objet obtenu a exactement les mêmes surfaces que la file d’attente source. Les files d’attente clonées peuvent avoir des tailles de métadonnées différentes les unes des autres.  
**Surfaces**  
Le ISurfaceQueue est responsable de la création et de la gestion de ses surfaces. La mise en file d’attente des surfaces arbitraires n’est pas valide. En outre, une surface ne doit avoir qu’un seul « propriétaire » actif. Elle doit se trouver dans une file d’attente spécifique ou être utilisée par un appareil spécifique. Il n’est pas possible de le faire sur plusieurs files d’attente ou pour que les appareils continuent à utiliser l’aire après qu’elle a été mise en file d’attente.  
</dl>

### <a name="api-details"></a>Détails de l’API

### <a name="isurfacequeue"></a>IsurfaceQueue

La file d’attente est chargée de créer et de gérer les ressources partagées. Il fournit également les fonctionnalités permettant de chaîner plusieurs files d’attente à l’aide du clone. La file d’attente a des méthodes qui ouvrent l’appareil de production et un appareil consommateur. Un seul d’entre eux peut être ouvert à tout moment.

La file d’attente expose les API suivantes :



|                             |                                                                                  |
|-----------------------------|----------------------------------------------------------------------------------|
| CreateSurfaceQueue          | Crée un objet ISurfaceQueue (la file d’attente « racine »).                              |
| ISurfaceQueue::OpenConsumer | Retourne une interface pour l’appareil consommateur à défiler.                        |
| ISurfaceQueue::OpenProducer | Retourne une interface pour l’appareil producteur à enqueuer.                        |
| ISurfaceQueue :: Clone        | Crée un objet ISurfaceQueue qui partage des surfaces avec l’objet de file d’attente racine. |



 

**CreateSurfaceQueue**  


```C++
typedef struct SURFACE_QUEUE_DESC {
  UINT            Width;
  UINT            Height;
  DXGI_FORMAT     Format;
  UINT            NumSurfaces;
  UINT            MetaDataSize;
  DWORD           Flags;
} SURFACE_QUEUE_DESC;
```



**Members** (Membres)  

**Largeur**, **hauteur**  des dimensions des surfaces partagées. Toutes les surfaces partagées doivent avoir les mêmes dimensions.  
**Format** Format des surfaces partagées. Toutes les surfaces partagées doivent avoir le même format. Les formats valides dépendent des appareils qui seront utilisés, car différentes paires d’appareils peuvent partager différents types de format.  
**NumSurfaces**  Nombre de surfaces qui font partie de la file d’attente. Il s’agit d’un nombre fixe.  
 **MetaDataSize**  Taille maximale de la mémoire tampon des métadonnées.  
**Indicateurs**  Indicateurs permettant de contrôler le comportement de la file d’attente. Consultez la section Notes.  



```C++
HRESULT CreateSurfaceQueue(
  [in]   SURFACE_QUEUE_DESC *pDesc,
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Paramètres**

 *pDesc* \[ dans \]  la description de la file d’attente de surface partagée à créer.  

 *pDevice* \[ dans \]  l’appareil qui doit être utilisé pour créer les surfaces partagées. Il s’agit d’un paramètre explicite en raison d’une fonctionnalité de Windows Vista. Pour les surfaces partagées entre Direct3D 9 et Direct3D 10, les surfaces doivent être créées avec Direct3D 9.  

 *ppQueue* \[ out au \]  retour, contient un pointeur vers l’objet ISurfaceQueue.  


**Valeurs de retour**

Si *pDevice* n’est pas en capacité de partager des ressources, cette fonction retourne l’appel de dxgi \_ Error \_ non valide \_ . Cette fonction crée les ressources. En cas d’échec, elle retourne une erreur. Si elle est réussie, elle retourne la valeur \_ OK.

**Remarques**

La création de l’objet de file d’attente crée également toutes les surfaces. Toutes les surfaces sont supposées être des cibles de rendu 2D et seront créées avec les indicateurs de la cible de rendu de liaison D3D10 et de la \_ \_ ressource de \_ \_ \_ nuanceur de liaison D3D10 \_ définis (ou les indicateurs équivalents pour les différents runtimes).

Le développeur peut spécifier un indicateur qui indique si la file d’attente est accessible par plusieurs threads. Si aucun indicateur n’est défini (**Flags** = = 0), la file d’attente est utilisée par plusieurs threads. Le développeur peut spécifier un accès à thread unique, ce qui désactive le code de synchronisation et améliore les performances dans ces cas. Chaque file d’attente clonée possède son propre indicateur. par conséquent, il est possible que des files d’attente différentes dans le système aient des contrôles de synchronisation différents.

 **Ouvrir un producteur**  


```C++
HRESULT OpenProducer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceProducer **ppProducer
);
```



**Paramètres**  

*pDevice* \[ dans\]  

Appareil producteur qui met en file d’attente des surfaces sur la file d’attente de surface. 

*ppProducer* \[ out \] retourne un objet à l’interface de producteur.  


**Valeurs de retour**

Si l’appareil n’est pas en capacité de partager des surfaces, retourne l’erreur DXGI de l' \_ \_ appel non valide \_ .

**Ouvrir un consommateur**  


```C++
HRESULT OpenConsumer(
  [in]   IUnknown *pDevice,
  [out]  IDXGIXSurfaceConsumer **ppConsumer
);
```



**Paramètres**  
 *pDevice* \[ dans\]  
 Appareil grand public qui défile les surfaces de la file d’attente de surface. 
 *ppConsumer* \[ out \]  retourne un objet à l’interface du consommateur.  


**Valeurs de retour**

Si l’appareil n’est pas en capacité de partager des surfaces, retourne l’erreur DXGI de l' \_ \_ appel non valide \_ .

**Remarques**

Cette fonction ouvre toutes les surfaces de la file d’attente pour le périphérique d’entrée et les met en cache. Les appels suivants à Dequeue sont simplement placés dans le cache et n’ont pas besoin de rouvrir les surfaces à chaque fois.



### <a name="cloning-an-idxgixsurfacequeue"></a>Clonage d’un IDXGIXSurfaceQueue




```C++
typedef struct SHARED_SURFACE_QUEUE_CLONE_DESC {
  UINT         MetaDataSize;
  DWORD        Flags;
} SHARED_SURFACE_QUEUE_CLONE_DESC;
```



Les **membres** **MetaDataSize** et **Flags** ont le même comportement que pour CreateSurfaceQueue.  



```C++
HRESULT Clone(
  [in]   SHARED_SURFACE_QUEUE_CLONE_DESC *pDesc,
  [out]  IDXGIXSurfaceQueue **ppQueue
);
```



**Paramètres**

*pDesc* \[ dans \] un struct qui fournit une description de l’objet clone à créer. Ce paramètre doit être initialisé.  
*ppQueue* \[ out \] retourne l’objet initialisé.  
</dl>

**Remarques**

Vous pouvez cloner à partir de n’importe quel objet de file d’attente existant, même s’il ne s’agit pas de la racine.  
</dl>

### <a name="idxgixsurfaceconsumer"></a>IDXGIXSurfaceConsumer

<dl>


```C++
HRESULT Dequeue(
  [in]      REFIID    id,
  [out]     void      **ppSurface,
  [in,out]  void      *pBuffer,
  [in,out]  UINT      *pBufferSize,
  [in]      DWORD     dwTimeout
);
```



**Paramètres**  
*ID* \[ dans\]  
REFIID d’une surface 2D de l’appareil consommateur.  

-   Pour un IDirect3DDevice9, REFIID doit être \_ \_ uuidof (IDirect3DTexture9).
-   Pour un ID3D10Device, REFIID doit être \_ \_ uuidof (ID3D10Texture2D).
-   Pour un ID3D11Device, REFIID doit être \_ \_ uuidof (ID3D11Texture2D).

*ppSurface* \[ out \] retourne un pointeur vers l’aire.  
*pbuffer* \[ dans, sortie \] d’un paramètre facultatif et, si la **valeur** n’est pas null, en cas de retour, contient les métadonnées qui ont été passées sur l’appel de mise en file d’attente correspondant.  
*pBufferSize* \[ dans, sortie \] de la taille de *pbuffer*, en octets. Retourne le nombre d’octets retournés dans *pbuffer*. Si l’appel de mise en file d’attente n’a pas fourni de métadonnées, *pbuffer* a la valeur 0.  
*dwTimeout* \[ dans \] spécifie une valeur de délai d’attente. Pour plus d’informations, consultez les notes.  
</dl>

**Valeurs de retour**

Cette fonction peut retourner \_ un délai d’attente si une valeur de délai d’attente est spécifiée et que la fonction ne retourne pas avant la valeur du délai d’attente. Consultez la section Notes. Si aucune surface n’est disponible, la fonction retourne avec *ppSurface* défini sur **null**, *pBufferSize* défini sur 0 et la valeur de retour est 0x80070120 (Win32 \_ à \_ HRESULT ( \_ délai d’attente)).  
</dl>

**Remarques**

Cette API peut se bloquer si la file d’attente est vide. Le paramètre *dwTimeout* fonctionne de la même façon que les API de synchronisation Windows, telles que WaitForSingleObject. Pour un comportement non bloquant, utilisez un délai d’expiration de 0.  
</dl>

### <a name="isurfaceproducer"></a>ISurfaceProducer

Cette interface fournit deux méthodes qui permettent à l’application d’empiler des surfaces. Une fois qu’une surface est mise en file d’attente, le pointeur de surface n’est plus valide et ne peut pas être utilisé en toute sécurité. La seule action que l’application doit effectuer avec le pointeur consiste à la libérer.



|                           |                                                                                                                                                       |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ISurfaceProducer :: emqueue | Met en file d’attente une surface vers l’objet de file d’attente. Une fois cet appel terminé, le producteur est réalisé avec la surface et la surface est prête pour un autre appareil. |
| ISurfaceProducer :: Flush   | Utilisé si les applications doivent avoir un comportement non bloquant. Pour plus de détails, consultez la section Notes.                                                                  |



 

**Enqueue (empiler)**  


```C++
HRESULT Enqueue(
  [in]  IUnknown *pSurface,
  [in]  void *pBuffer,
  [in]  UINT BufferSize,
  [in]  DWORD Flags
);
```



**Paramètres**  
*pSurface* \[ dans\]  
Surface du périphérique de production qui doit être mise en file d’attente. Cette surface doit être une surface déplacée de la file d’attente du même réseau de file d’attente. *pbuffer* \[ dans \] un paramètre facultatif, qui est utilisé pour passer des métadonnées. Il doit pointer vers les données qui seront transmises à l’appel de retrait de la file d’attente.  
*BufferSize* \[ dans \] la taille de *pbuffer*, en octets.  
*Indicateurs* \[ dans \] un paramètre facultatif qui contrôle le comportement de cette fonction. Le seul indicateur est l' \_ indicateur de file d’attente de surface n’est pas en attente \_ \_ \_ \_ . Consultez les notes relatives au vidage. Si aucun indicateur n’est passé (*Flags* = = 0), le comportement de blocage par défaut est utilisé.  
</dl>

**Valeurs de retour**

Cette fonction peut retourner \_ une erreur dxgi lors du \_ \_ \_ dessin quand un indicateur d’attente de la file d’attente de surface n' \_ \_ \_ \_ \_ est pas utilisé.  
</dl>

**Remarques**

-   Cette fonction place la surface sur la file d’attente. Si l’application ne spécifie pas l' \_ indicateur de file d’attente \_ de surface \_ n' \_ \_ attend pas, cette fonction bloque et effectue une synchronisation GPU-CPU pour s’assurer que tout le rendu sur la surface en file d’attente est terminé. Si cette fonction est réussie, une surface est disponible pour la défile d’attente. Si vous souhaitez un comportement non bloquant, utilisez l' \_ indicateur do not \_ Wait. Pour plus d’informations, consultez Flush ().
-   Conformément aux règles de décompte de références COM, la surface retournée par Dequeue est AddRef (), de sorte que l’application n’a pas besoin de le faire. Après l’appel de la mise en file d’attente, l’application doit libérer la surface, car elle ne l’utilise plus.

**Purge**  


```C++
HRESULT Flush(
  [in]  DWORD Flags,
  [out] UINT *nSurfaces
);
```



**Paramètres**  
*Flags* \[in\]  
Le seul indicateur est l' \_ indicateur de file d’attente de surface n’est pas en attente \_ \_ \_ \_ . Consultez la section Notes. *nSurfaces* \[ out \] retourne le nombre de surfaces toujours en attente et non vidées.  
</dl>

**Valeurs de retour**

Cette fonction peut retourner une \_ erreur \_ dxgi \_ quand \_ l' \_ indicateur d’attente de la file d’attente de surface n' \_ \_ \_ \_ est pas utilisé. Cette fonction retourne S \_ OK si des surfaces ont été vidées avec succès. Cette fonction retourne l' \_ erreur dxgi en \_ \_ \_ dessinant uniquement si aucune surface n’a été vidée. Ensemble, la valeur de retour et *nSurfaces* indiquent à l’application ce qui a été effectué et si un travail reste à faire.  
</dl>

**Remarques**

Le vidage est explicite uniquement si l’appel précédent à Enqueue a utilisé \_ l' \_ indicateur do not Wait ; sinon, il s’agit d’une absence d’opération. Si l’appel à Enqueue a utilisé l' \_ indicateur do not \_ Wait, la file d’attente est retournée immédiatement et la synchronisation GPU-CPU n’est pas garantie. La surface est toujours considérée comme étant mise en file d’attente, l’appareil producteur ne peut pas continuer à l’utiliser, mais elle n’est pas disponible pour la défile d’attente. Pour essayer de valider la surface de la file d’attente, Flush doit être appelé. Le vidage tente de valider toutes les surfaces actuellement mises en file d’attente. Si aucun indicateur n’est passé au vidage, il bloque et efface l’intégralité de la file d’attente, en prêtant toutes les surfaces qu’il contient pour la défile d’attente. Si l' \_ indicateur ne pas \_ attendre est utilisé, la file d’attente vérifie les surfaces pour voir si l’une d’elles est prête ; cette étape est non bloquante. Les surfaces qui ont terminé la synchronisation GPU-UC sont prêtes pour l’appareil grand public. Les surfaces toujours en attente ne seront pas affectées. La fonction retourne le nombre de surfaces qui doivent encore être vidées.

> [!Note]  
> Flush n’interrompt pas la sémantique de la file d’attente. L’API garantit que les surfaces mises en file d’attente seront validées avant que les surfaces soient mises en file d’attente par la suite, quel que soit le moment où la synchronisation GPU-CPU se produit.

 

  
</dl>

### <a name="direct3d-9ex-and-dxgi-interop-helper-how-to-use"></a>Application auxiliaire Direct3D 9Ex et DXGI Interop : comment utiliser

Nous pensons que la plupart des cas d’utilisation impliquent deux appareils partageant un certain nombre de surfaces. Étant donné qu’il s’agit également du scénario le plus simple, ce document explique en détail comment utiliser les API pour atteindre cet objectif, aborde une variation non bloquante et se termine par une brève section sur l’initialisation de trois appareils.

### <a name="two-devices"></a>Deux appareils

L’exemple d’application qui utilise cette application d’assistance peut utiliser Direct3D 9Ex et Direct3D 11 ensemble. L’application peut traiter le contenu avec les deux appareils et présenter le contenu à l’aide de Direct3D 9. Le traitement peut signifier le rendu du contenu, le décodage de la vidéo, l’exécution des nuanceurs de calcul, etc. Pour chaque trame, l’application traite tout d’abord avec Direct3D 11, puis traite avec Direct3D 9 et enfin présente avec Direct3D 9. En outre, le traitement avec Direct3D 11 produira des métadonnées que le Direct3D 9 doit utiliser. Cette section traite de l’utilisation de l’application d’assistance en trois parties qui correspondent à cette séquence : initialisation, boucle principale et nettoyage.

**D’initialisation**  
L’initialisation implique les étapes suivantes :  

1.  Initialisez les deux appareils.
2.  Créez la file d’attente racine : m \_ 11to9Queue.
3.  Cloner à partir de la file d’attente racine : m \_ 9to11Queue.
4.  Appelez OpenProducer/OpenConsumer sur les deux files d’attente.

Les noms de files d’attente utilisent les chiffres 9 et 11 pour indiquer l’API qui est le producteur et qui est le producteur de l’utilisateur : **m \_ à la file d’attente du ***consommateur*****. En conséquence, m \_ 11to9Queue indique une file d’attente pour laquelle l’appareil Direct3D 11 produit des surfaces consommées par l’appareil Direct3D 9. De même, m \_ 9to11Queue indique une file d’attente pour laquelle Direct3D 9 produit des surfaces consommées par Direct3D 11.  
La file d’attente racine est initialement remplie et toutes les files d’attente clonées sont initialement vides. Cela ne doit pas être un problème pour l’application, à l’exception du premier cycle des enfilements et des retraits de file d’attente et de la disponibilité des métadonnées. Si une file d’attente demande des métadonnées mais qu’aucune n’a été définie (soit parce qu’aucune n’a été initialement, soit la file d’attente n’a rien défini), Dequeue constate qu’aucune métadonnée n’a été reçue.  

1.  **Initialisez les deux appareils.**  
    ```C++
    m_pD3D9Device = InitializeD3D9ExDevice();
    m_pD3D11Device = InitializeD3D11Device();
    ```

    

2.  **Créez la file d’attente racine.**  
    Cette étape crée également les surfaces. Les restrictions de taille et de format sont identiques à la création d’une ressource partagée. La taille de la mémoire tampon des métadonnées est fixée au moment de la création, et dans ce cas, nous allons simplement passer un UINT.  
    La file d’attente doit être créée avec un nombre fixe de surfaces. Les performances varient en fonction du scénario. Le fait de disposer de plusieurs surfaces augmente le risque que les appareils soient occupés. Par exemple, s’il n’y a qu’une seule surface, il n’y aura aucune parallélisation entre les deux appareils. D’un autre côté, l’augmentation du nombre de surfaces augmente l’encombrement mémoire, ce qui peut dégrader les performances. Cet exemple utilise deux surfaces.  
    ```C++
    SURFACE_QUEUE_DESC Desc;
    Desc.Width        = 640;
    Desc.Height       = 480;
    Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
    Desc.NumSurfaces  = 2;
    Desc.MetaDataSize = sizeof(UINT);
    Desc.Flags        = 0;

    CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
    ```

    

3.  **Clonez la file d’attente racine.**  
    Chaque file d’attente clonée doit utiliser les mêmes surfaces, mais elle peut avoir des tailles de mémoire tampon de métadonnées différentes et des indicateurs différents. Dans ce cas, il n’y a pas de métadonnées de Direct3D 9 vers Direct3D 11.  
    ```C++
    SURFACE_QUEUE_CLONE_DESC Desc;
    Desc.MetaDataSize = 0;
    Desc.Flags        = 0;

    m_11to9Queue->Clone(&Desc, &m_9to11Queue);
    ```

    

4.  **Ouvrez les appareils producteur et grand public.**  
    L’application doit effectuer cette étape avant d’appeler Enqueue et Dequeue. L’ouverture d’un producteur et d’un consommateur retourne des interfaces qui contiennent les API d’empilement/retrait de la file d’attente.  
    ```C++
    // Open for m_p9to11Queue.
    m_p9to11Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
    m_p9to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

    // Open for m_p11to9Queue.
    m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
    m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
    ```

    

**Boucle principale**  
L’utilisation de la file d’attente est modélisée après le problème de producteur/consommateur classique. Pensez à cela d’un point de vue de chaque appareil. Chaque appareil doit effectuer les étapes suivantes : Dequeue pour obtenir une surface de sa file d’attente de consommation, traiter sur l’aire, puis mettre en file d’attente dans sa file d’attente de production. Pour l’appareil Direct3D 11, l’utilisation de Direct3D 9 est presque identique.  


```C++
// Direct3D 9 Device.
IDirect3DTexture9* pTexture9 = NULL;
REFIID             surfaceID9 = _uuidof(IDirect3DTexture9);
UINT               metaData;
UINT               metaDataSize;
while (!done)
{
    // Dequeue surface.
    m_pD3D9Consumer->Dequeue(surfaceID9, (void**)&pSurface9,
                             &metaData, &metaDataSize, INFINITE);

    // Process the surface.
    ProcessD3D9(pSurface9);

    // Present the surface using the meta data.
    PresentD3D9(pSurface9, metaData, metaDataSize);

    // Enqueue surface.
    m_pD3D9Producer->Enqueue(pSurface9, NULL, 0, 0);
}
```



**Nettoyage en trop**  
Cette étape est très simple. En plus des étapes normales de nettoyage des API Direct3D, l’application doit libérer les interfaces COM de retour.  


```C++
m_pD3D9Producer->Release();
m_pD3D9Consumer->Release();
m_pD3D11Producer->Release();
m_pD3D11Consumer->Release();
m_p9to11Queue->Release();
m_p11to9Queue->Release();
```



</dl>

### <a name="non-blocking-use"></a>Utilisation non bloquante

L’exemple précédent est logique pour un cas d’utilisation multithread dans lequel chaque appareil a son propre thread. L’exemple utilise les versions bloquantes des API : infini pour timeout et aucun indicateur pour Enqueue. Si vous souhaitez utiliser le programme d’assistance de façon non bloquante, vous ne devez apporter que quelques modifications. Cette section montre une utilisation non bloquante avec les deux appareils sur un thread.

**D’initialisation**  
L’initialisation est identique à l’exception des indicateurs. Étant donné que l’application est monothread, utilisez cet indicateur pour la création. Cela désactive une partie du code de synchronisation, ce qui peut potentiellement améliorer les performances.  


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
```




```C++
SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = SURFACE_QUEUE_FLAG_SINGLE_THREADED;

m_11to9Queue->Clone(&Desc, &m_9to11Queue);
```



L’ouverture des appareils producteur et grand public est identique à celle de l’exemple de blocage.  
**Utilisation de la file d’attente**  
Il existe de nombreuses façons d’utiliser la file d’attente de façon non bloquante, avec différentes caractéristiques de performances. L’exemple suivant est simple, mais a des performances médiocres en raison d’une rotation et d’une interrogation excessives. Malgré ces problèmes, l’exemple montre comment utiliser l’application auxiliaire. L’approche consiste à se positionner en permanence dans une boucle et à supprimer la file d’attente, le processus, l’empilement et le vidage. Si l’une des étapes échoue parce que la ressource n’est pas disponible, l’application essaie simplement de relancer la boucle suivante.  


```C++
// Direct3D 11 Device.
ID3D11Texture2D* pSurface11 = NULL;
REFIID           surfaceID11 = __uuidof(ID3D11Texture2D);
UINT             metaData;
while (!done)
{
    //
    // D3D11 Portion.
    //

    // Dequeue surface.
    hr = m_pD3D11Consumer->Dequeue(surfaceID11,
                                   (void**)&pSurface11,
                                   NULL, 0, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr))
    {
        // Process the surface and return some meta data.
        ProcessD3D11(pSurface11, &metaData);

        // Enqueue surface.
        m_pD3D11Producer->Enqueue(pSurface11, &metaData,
                                  sizeof(UINT),
                                  SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D11Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);

    //
    // Do the same with the Direct3D 9 Device.
    //

    // Dequeue surface.
    hr = m_pD3D9Consumer->Dequeue(surfaceID9,
                                  (void**)&pSurface9,
                                  &metaData,
                                  &metaDataSize, 0);
    // Only continue if we got a surface.
    if (SUCCEEDED(hr)))
    {
        // Process the surface.
        ProcessD3D9(pSurface9);

        // Present the surface using the meta data.
        PresentD3D9(pSurface9, metaData, metaDataSize);

        // Enqueue surface.
        m_pD3D9Producer->Enqueue(pSurface9, NULL, 0,
                                 SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
    }
    // Flush the queue to check if any surfaces completed.
    m_pD3D9Producer->Flush(NULL,SURFACE_QUEUE_FLAG_DO_NOT_WAIT);
}
```



Une solution plus complexe pourrait vérifier la valeur de retour de Enqueue et de Flush pour déterminer si le vidage est nécessaire.  
</dl>

### <a name="three-devices"></a>Trois appareils

L’extension des exemples précédents pour couvrir plusieurs appareils est simple. Le code suivant effectue l’initialisation. Une fois que les objets producteur/consommateur ont été créés, le code permettant de les utiliser est le même. Cet exemple a trois appareils et donc trois files d’attente. Les surfaces circulent de Direct3D 9 vers Direct3D 10 vers Direct3D 11.


```C++
SURFACE_QUEUE_DESC Desc;
Desc.Width        = 640;
Desc.Height       = 480;
Desc.Format       = DXGI_FORMAT_R16G16B16A16_FLOAT;
Desc.NumSurfaces  = 2;
Desc.MetaDataSize = sizeof(UINT);
Desc.Flags        = 0;

SURFACE_QUEUE_CLONE_DESC Desc;
Desc.MetaDataSize = 0;
Desc.Flags        = 0;

CreateSurfaceQueue(&Desc, m_pD3D9Device, &m_11to9Queue);
m_11to9Queue->Clone(&Desc, &m_9to10Queue);
m_11to9Queue->Clone(&Desc, &m_10to11Queue);
```



Comme mentionné précédemment, le clonage fonctionne de la même façon, quelle que soit la file d’attente clonée. Par exemple, le deuxième appel de clonage aurait pu être en dehors de l' \_ objet m 9to10Queue.


```C++
// Open for m_p9to10Queue.
m_p9to10Queue->OpenProducer(m_pD3D9Device, &m_pD3D9Producer);
m_p9to10Queue->OpenConsumer(m_pD3D10Device, &m_pD3D10Consumer);

// Open for m_p10to11Queue.
m_p10to11Queue->OpenProducer(m_pD3D10Device, &m_pD3D10Producer);
m_p10to11Queue->OpenConsumer(m_pD3D11Device, &m_pD3D11Consumer);

// Open for m_p11to9Queue.
m_p11to9Queue->OpenProducer(m_pD3D11Device, &m_pD3D11Producer);
m_p11to9Queue->OpenConsumer(m_pD3D9Device, &m_pD3D9Consumer);
```



## <a name="conclusion"></a>Conclusion

Vous pouvez créer des solutions qui utilisent l’interopérabilité pour utiliser la puissance de plusieurs API DirectX. L’interopérabilité de l’API Windows Graphics offre désormais un Common surface Management Runtime DXGI 1,1. Ce Runtime active la prise en charge de partage de surface synchronisé dans les API récemment développées, telles que Direct3D 11, Direct3D 10,1 et Direct2D. Les améliorations de l’interopérabilité entre les nouvelles API et les API existantes contribuent à la migration des applications et à la compatibilité descendante. Les API de consommateur Direct3D 9Ex et DXGI 1,1 peuvent interagir, comme le montre le mécanisme de synchronisation fourni via l’exemple de code d’assistance sur MSDN Code Gallery.

 

 