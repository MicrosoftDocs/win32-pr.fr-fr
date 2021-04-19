---
description: Décrit comment utiliser les superpositions de matériel dans Direct3D 9.
ms.assetid: fa9d5bf5-4c0f-471a-b639-d329b0cd89a4
title: Prise en charge de la superposition matérielle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcae33cdf55de59bdcd074829d52b4c1c43ea5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521440"
---
# <a name="hardware-overlay-support"></a>Prise en charge de la superposition matérielle

Une superposition matérielle est une zone dédiée de la mémoire vidéo qui peut être superposée sur la surface principale. Aucune copie n’est effectuée lorsque la superposition est affichée. L’opération de superposition est effectuée dans le matériel, sans modification des données dans la surface principale.

L’utilisation de superpositions de matériel pour la lecture vidéo était courante dans les versions antérieures de Windows, car les superpositions sont efficaces pour le contenu vidéo avec une fréquence d’images élevée. À compter de Windows 7, Direct3D 9 prend en charge les superpositions matérielles. Cette prise en charge est principalement destinée à la lecture vidéo et diffère à certains égards des API DirectDraw précédentes :

-   La superposition ne peut pas être réduite, mise en miroir ou désentrelacée.
-   Les clés de couleur source et la fusion alpha ne sont pas prises en charge.
-   Les superpositions peuvent être étirées si le matériel de superposition le prend en charge. Dans le cas contraire, l’étirement n’est pas pris en charge. En pratique, tous les pilotes graphiques ne prennent pas en charge l’étirement.
-   Chaque périphérique prend en charge au plus une superposition.
-   La superposition est effectuée à l’aide d’une clé de couleur de destination, mais le runtime Direct3D sélectionne automatiquement la couleur et dessine le rectangle de destination. Direct3D effectue automatiquement le suivi de la position de la fenêtre et met à jour la position de superposition chaque fois que le **PresentEx** est appelé.

### <a name="creating-a-hardware-overlay-surface"></a>Création d’une surface de superposition matérielle

Pour interroger la prise en charge de la superposition, appelez **IDirect3D9 :: GetDeviceCaps**. Si le pilote prend en charge la superposition matérielle, l’indicateur de **\_ superposition D3DCAPS** est défini dans **D3DCAPS9. Membre Caps** .

Pour déterminer si un format de superposition spécifique est pris en charge pour un mode d’affichage donné, appelez [**IDirect3D9ExOverlayExtension :: CheckDeviceOverlayType**](/windows/desktop/api/d3d9/nf-d3d9-idirect3d9exoverlayextension-checkdeviceoverlaytype).

Pour créer la superposition, appelez **IDirect3D9Ex :: CreateDeviceEx** et spécifiez l’effet d’échange de **\_ superposition D3DSWAPEFFECT** . La mémoire tampon d’arrière-plan peut utiliser un format non RVB si le matériel le prend en charge.

Les surfaces de superposition présentent les limitations suivantes :

-   L’application ne peut pas créer plus d’une chaîne de permutation de superposition.
-   La superposition doit être utilisée en mode fenêtre. Elle ne peut pas être utilisée en mode plein écran.
-   L’effet d’échange de superposition doit être utilisé avec l’interface **IDirect3DDevice9Ex** . Elle n’est pas prise en charge pour **IDirect3DDevice9**.
-   L’échantillonnage multiple ne peut pas être utilisé.
-   Les indicateurs **D3DPRESENT \_ DONOTFLIP** et **D3DPRESENT \_ FLIPRESTART** ne sont pas pris en charge.
-   Les statistiques de présentation ne sont pas disponibles pour la surface de recouvrement.

Si le matériel ne prend pas en charge l’étirement, il est recommandé de créer une chaîne de permutation aussi grande que le mode d’affichage, afin que la fenêtre puisse être redimensionnée sur n’importe quelle dimension. La recréation de la chaîne de permutation n’est pas une méthode optimale pour gérer le redimensionnement de la fenêtre, car cela peut provoquer de graves artefacts de rendu. En outre, en raison de la façon dont le GPU gère la mémoire de superposition, la recréation de la chaîne de permutation peut entraîner une application à manquer de mémoire vidéo.

### <a name="new-d3dpresent_parameters-flags"></a>Nouveaux \_ indicateurs de paramètres D3DPRESENT

Les indicateurs **de \_ paramètres D3DPRESENT** suivants sont définis pour créer des superpositions.



| Indicateur                                      | Description                                                                                                                                                                        |
|-------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENTFLAG \_ superposition \_ LIMITEDRGB**   | La plage RVB est comprise entre 16 et 235. La valeur par défaut est comprise entre 0 et 255. <br/> Nécessite la fonctionnalité **D3DOVERLAYCAPS \_ LIMITEDRANGERGB** .<br/>                                                 |
| **\_Superposition \_ D3DPRESENTFLAG \_ BT709 YCbCr** | Les couleurs YUV utilisent la définition BT. 709. La valeur par défaut est BT. 601. <br/> Nécessite la fonctionnalité **D3DOVERLAYCAPS \_ YCbCr \_ BT709** .<br/>                                      |
| **\_Superposition \_ D3DPRESENTFLAG \_ xvYCC YCbCr** | Sortie des données à l’aide d’une extension YCbCr étendue (xvYCC).<br/> Requiert la fonctionnalité **D3DOVERLAYCAPS \_ YCbCr \_ BT601 \_ xvYCC** ou **D3DOVERLAYCAPS \_ YCbCr \_ BT709 \_ xvYCC** .<br/> |



 

### <a name="using-hardware-overlays"></a>Utilisation des superpositions matérielles

Pour afficher la surface de recouvrement, l’application appelle **IDirect3DDevice9Ex ::P resentex**. Le runtime Direct3D dessine automatiquement la clé de couleur de destination.

Les indicateurs **PresentEx** suivants sont définis pour les superpositions.



| Indicateur                              | Description                                                                                                                                                                                                                                                                           |
|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **D3DPRESENT \_ UPDATECOLORKEY**    | Définir cet indicateur si la Gestionnaire de fenêtrage (DWM) est désactivée. Avec cet indicateur, Direct3D redessine la clé de couleur.<br/> Si DWM est activé, cet indicateur n’est pas requis, car Direct3D dessine la clé de couleur une seule fois sur la surface que DWM utilise pour la redirection.<br/> |
| **D3DPRESENT \_ HIDEOVERLAY**       | Masque la superposition.                                                                                                                                                                                                                                                                    |
| **D3DPRESENT \_ UPDATEOVERLAYONLY** | Met à jour la superposition sans modifier le contenu.<br/> Cet indicateur est utile si la fenêtre se déplace alors que la vidéo est en pause.<br/>                                                                                                                                           |



 

Une application doit être préparée à gérer les cas suivants :

-   Si une autre application utilise la superposition, **PresentEx** retourne **D3DERR \_ NOTAVAILABLE**.
-   Si la fenêtre est déplacée vers un autre moniteur, l’application doit recréer la chaîne de permutation. Sinon, si l’application appelle **PresentEx** pour afficher la superposition sur une autre analyse, **PresentEx** retourne **D3DERR \_ INVALIDDEVICE**.
-   Si le mode d’affichage change, Direct3D tente de restaurer la superposition. Si le nouveau mode ne prend pas en charge la superposition, **PresentEx** retourne **D3DERR \_ UNSUPPORTEDOVERLAY**.

### <a name="example-code"></a>Exemple de code

L’exemple suivant montre comment créer une surface de recouvrement.


```C++
const UINT VIDEO_WIDTH = 256;
const UINT VIDEO_HEIGHT = 256;

HRESULT CreateHWOverlay(
    HWND hwnd, 
    IDirect3D9Ex *pD3D, 
    IDirect3DDevice9Ex **ppDevice
    )
{
    *ppDevice = NULL;

    D3DCAPS9                caps;
    ZeroMemory(&caps, sizeof(caps));

    HRESULT hr = pD3D->GetDeviceCaps(
        D3DADAPTER_DEFAULT,
        D3DDEVTYPE_HAL,
        &caps
        );

    if (FAILED(hr))
    {
        return hr;
    }

    // Check if overlay is supported.
    if (!(caps.Caps & D3DCAPS_OVERLAY))
    {
        return D3DERR_UNSUPPORTEDOVERLAY;
    }

    D3DOVERLAYCAPS          overlayCaps = { 0 };

    IDirect3DDevice9Ex           *pDevice = NULL;
    IDirect3D9ExOverlayExtension *pOverlay = NULL;

    // Check specific overlay capabilities.
    hr = pD3D->QueryInterface(IID_PPV_ARGS(&pOverlay));

    if (SUCCEEDED(hr))
    {
        hr = pOverlay->CheckDeviceOverlayType(
            D3DADAPTER_DEFAULT,
            D3DDEVTYPE_HAL,
            VIDEO_WIDTH,
            VIDEO_HEIGHT,
            D3DFMT_X8R8G8B8,
            NULL,
            D3DDISPLAYROTATION_IDENTITY,
            &overlayCaps
            );
    }

    // Create the overlay.
    if (SUCCEEDED(hr))
    {

        DWORD flags =   D3DCREATE_FPU_PRESERVE | 
                        D3DCREATE_MULTITHREADED | 
                        D3DCREATE_SOFTWARE_VERTEXPROCESSING;

        
        D3DPRESENT_PARAMETERS   pp = { 0 };

        pp.BackBufferWidth = overlayCaps.MaxOverlayDisplayWidth;
        pp.BackBufferHeight = overlayCaps.MaxOverlayDisplayHeight;
        pp.BackBufferFormat = D3DFMT_X8R8G8B8;
        pp.SwapEffect = D3DSWAPEFFECT_OVERLAY;
        pp.hDeviceWindow = hwnd;
        pp.Windowed = TRUE;
        pp.Flags = D3DPRESENTFLAG_VIDEO;
        pp.FullScreen_RefreshRateInHz = D3DPRESENT_RATE_DEFAULT;
        pp.PresentationInterval       = D3DPRESENT_INTERVAL_ONE;

        hr = pD3D->CreateDeviceEx(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL,
            NULL, flags, &pp, NULL, &pDevice);
    }

    if (SUCCEEDED(hr))
    {
        (*ppDevice) = pDevice;
        (*ppDevice)->AddRef();
    }

    SafeRelease(&pD3D);
    SafeRelease(&pDevice);
    SafeRelease(&pOverlay);
    return hr;
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[API vidéo Direct3D](direct3d-video-apis.md)
</dt> </dl>

 

 




