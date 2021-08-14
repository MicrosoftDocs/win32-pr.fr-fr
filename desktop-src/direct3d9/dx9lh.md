---
description: cette documentation fait spécifiquement référence aux extensions Windows Vista pour DirectX graphics.
ms.assetid: 3cc0b08c-e126-4f1b-b5d1-0d6c1ebeb0c5
title: résumé des fonctionnalités (Direct3D 9 pour Windows Vista)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242af80fa4d6f00c1e55d4852884f9fbbf8de287c6792b3b4aaaad196a6cd113
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523076"
---
# <a name="feature-summary-direct3d-9-for-windows-vista"></a>résumé des fonctionnalités (Direct3D 9 pour Windows Vista)

cette documentation fait spécifiquement référence aux extensions Windows Vista pour DirectX graphics. pour développer la puissance de DirectX pour Windows Vista, vous devez installer le kit de développement logiciel (sdk) Windows vista, ainsi que le kit de développement logiciel (sdk) directx. les Applications qui utilisent DirectX pour Windows Vista doivent utiliser un matériel qui utilise le pilote WDDM (Windows modèle de pilote de périphérique) au lieu de XPDM (modèle de pilote XP). les pilotes qui n’implémentent pas le WDDM ne peuvent pas instancier des interfaces graphiques Windows Vista DirectX.

découvrez les nouvelles fonctionnalités graphiques DirectX de Windows Vista dans l’une des sections suivantes :

-   [Changements de comportement des appareils](#device-behavior-changes)
-   [Désactivation du traitement des vertex logiciels multithread](#disabling-multithreaded-software-vertex-processing)
-   [Surfaces d’un bit](#one-bit-surfaces)
-   [Lecture des mémoires tampons de profondeur/stencil](#reading-depthstencil-buffers)
-   [Partager des ressources](#sharing-resources)
-   [Conversion sRVB avant la fusion](#srgb-conversion-before-blending)
-   [Améliorations apportées à StretchRect](#stretchrect-improvements)
-   [Création de texture dans la mémoire système](#texture-creation-in-system-memory)

## <a name="device-behavior-changes"></a>Changements de comportement des appareils

Les appareils ne sont à présent perdus que dans deux cas. Lorsque le matériel est réinitialisé parce qu’il est bloqué et lorsque le pilote de périphérique est arrêté. Lorsque le matériel se bloque, l’appareil peut être réinitialisé en appelant [**ResetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-resetex). Si le matériel se bloque, la mémoire de texture est perdue.

Après l’arrêt d’un pilote, l’objet IDirect9Ex doit être recréé pour reprendre le rendu.

Lorsque la zone de présentation est masquée par une autre fenêtre en mode fenêtre, ou lorsqu’une application en plein écran est réduite, [**PresentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) retourne S \_ D3DPRESENTATIONOCCLUDED. Les applications plein écran peuvent reprendre le rendu lorsqu’elles reçoivent un message de rappel [**WM \_ ACTIVATEAPP**](../winmsg/wm-activateapp.md) .

Dans les versions précédentes de DirectX, quand une application rencontrait une modification de mode, la seule façon de récupérer était de réinitialiser l’appareil et de recréer toutes les ressources de mémoire vidéo et les chaînes de permutation. désormais, avec DirectX pour Windows Vista, l’appel de Reset après une modification de mode n’entraîne pas la perte des surfaces de la mémoire de texture, des textures et des informations d’état, et ces ressources n’ont pas besoin d’être recréées.

## <a name="disabling-multithreaded-software-vertex-processing"></a>Désactivation du traitement des vertex logiciels multithread

Un nouveau bit de majuscules (D3DCREATE \_ désactiver \_ PSGP \_ Threading) a été ajouté pour désactiver le multithreading pour le traitement des vertex logiciels (swvp). Utilisez cette macro pour générer un indicateur de comportement pour IDirect3D9 :: CreateDevice.


```
#define D3DCREATE_DISABLE_PSGP_THREADING
```



## <a name="one-bit-surfaces"></a>Surfaces d’un bit

Il existe un nouveau type de format de surface binaire qui peut s’avérer particulièrement utile pour le traitement des glyphes de texte. Le nouveau format est appelé D3DFMT \_ a1. Une surface à un bit est conçue pour être utilisée comme une texture par pixel ou pour la sortie de la cible de rendu générée par ComposeRects ou ColorFill. Il n’y a pas d’épaisseur distincte pour la largeur et la hauteur de la surface ; une implémentation doit prendre en charge une surface de taille unique qui est de 2 000 texels x 8 Ko.

Une surface à un bit a un bit par Texel. par conséquent, une unité signifie que tous les composants (r, g, b, a) d’un pixel sont 1, et zéro signifie que tous les composants sont égaux à 0. Vous pouvez utiliser des surfaces d’un bit avec les API suivantes : ColorFill, UpdateSurface et UpdateTexture.

Quand une surface à un bit est lue, le runtime peut effectuer l’un des exemples de point ou le filtrage de convolution. Le filtre de convolution est réglable (voir [**SetConvolutionMonoKernel**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-setconvolutionmonokernel)).

Il existe des restrictions pour les surfaces d’un bit :

-   MIP-mapping n’est pas pris en charge
-   les données sRVB ne peuvent pas être lues ou écrites sur une surface à un bit.
-   Une surface à un bit ne peut pas être utilisée comme texture de vertex ou pour l’échantillonnage multiple.

## <a name="reading-depthstencil-buffers"></a>Lecture des mémoires tampons de profondeur/stencil

Utilisez IDirect3DDevice9 :: UpdateSurface pour lire ou écrire des données de profondeur/stencil à partir des surfaces obtenues à partir de IDirect3DDevice9 :: CreateDepthStencilSurface ou IDirect3DDevice9 :: GetDepthStencilSurface.

Tout d’abord, créez une surface verrouillable, profondeur uniquement ou stencil uniquement à l’aide de IDirect3DDevice9 :: CreateOffscreenPlainSurface. Utilisez l'un des éléments suivants :

-   D3DFMT \_ D16 \_ verrouillable
-   D3DFMT \_ D32F \_ verrouillable
-   D3DFMT \_ d32 \_ verrouillable
-   D3DFMT \_ S8 \_ verrouillable

Ensuite, transférez les données entre la mémoire tampon du stencil/profondeur et la surface de gabarit ou de la profondeur du stencil qui vient d’être créée. Le transfert est effectué à l’aide de IDirect3DDevice9 :: UpdateSurface.

UpdateSurface échoue quand les deux surfaces sont de format verrouillable ou non verrouillables.

Le transfert de données inexistantes génère une erreur (par exemple, le transfert d’une surface de profondeur non verrouillable uniquement vers une \_ surface D3DFMT S8 \_ verrouillable).

Le reste des restrictions pour IDirect3DDevice9 :: UpdateSurface s’applique toujours.

## <a name="sharing-resources"></a>Partager des ressources

Les ressources Direct3D peuvent désormais être partagées entre des appareils ou des processus. Cela s’applique à toutes les ressources Direct3D, y compris les textures, les mémoires tampons de vertex, les mémoires tampons d’index ou les surfaces (telles que les cibles de rendu, les mémoires tampons de stencil de profondeur ou les surfaces ordinaires hors écran). Pour être partagé, vous devez désigner une ressource pour le partage au moment de la création et localiser la ressource dans le pool par défaut (D3DPOOL \_ par défaut). Une fois qu’une ressource est créée pour le partage, elle peut être partagée entre plusieurs appareils au sein d’un processus ou partagée par plusieurs processus.

Pour activer les ressources partagées, les API de création de ressources ont un paramètre de handle supplémentaire. Il s’agit d’un HANDLE qui pointe vers la ressource partagée. Dans les révisions précédentes de DirectX, cet argument fait partie de la signature de l’API, mais il a été inutilisé et doit avoir la valeur **null**. à partir de Windows Vista, utilisez pSharedHandle de l’une des manières suivantes :

-   Définissez le pointeur (pSharedHandle) sur la **valeur null** pour ne pas partager une ressource. c’est comme le comportement de DirectX avant Windows Vista.
-   Pour créer une ressource partagée, appelez une API de création de ressource (voir ci-dessous) avec un handle non initialisé (le pointeur lui-même n’est pas **null** (pSharedHandle ! = **null**), mais le pointeur pointe vers une valeur **null** ( \* pSharedHandle = = **null**)). L’API génère une ressource partagée et retourne un handle valide.
-   Pour ouvrir et accéder à une ressource partagée créée précédemment à l’aide d’un handle de ressource partagée non NULL, définissez pSharedHandle sur l’adresse de ce handle. Une fois que vous avez ouvert la ressource partagée précédemment créée de cette manière, vous pouvez utiliser l’interface retournée dans l’API Direct3D 9 ou Direct3D 9Ex comme si l’interface était une ressource typique de ce type.

Les API de création de ressources incluent- [**CreateTexture**](/windows/desktop/api), [**CreateVolumeTexture**](/windows/desktop/api), [**CreateCubeTexture**](/windows/desktop/api), [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget), [**CreateVertexBuffer**](/windows/desktop/api), [**CreateIndexBuffer**](/windows/desktop/api), [**CreateDepthStencilSurface**](/windows/desktop/api), [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateDepthStencilSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createdepthstencilsurfaceex), [**CreateOffscreenPlainSurfaceEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createoffscreenplainsurfaceex)et [**CreateRenderTargetEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-createrendertargetex).

Certaines restrictions s’appliquent à l’utilisation des ressources partagées. Ce sont, entre autres, les suivantes :

-   L’API que vous utilisez pour ouvrir une ressource partagée doit correspondre à l’API que vous avez utilisée pour créer la ressource partagée. Par exemple, si vous avez utilisé [**CreateTexture**](/windows/desktop/api) pour créer une ressource partagée, vous devez utiliser **CreateTexture** pour ouvrir cette ressource partagée ; Si vous avez utilisé [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget) pour créer une ressource partagée, vous devez utiliser **CreateRenderTarget** pour ouvrir cette ressource partagée, et ainsi de suite.
-   Lorsque vous ouvrez une ressource partagée, vous devez spécifier D3DPOOL \_ par défaut.
-   Les ressources verrouillables (par exemple, les textures avec D3DUSAGE \_ Dynamic, les mémoires tampons de vertex et les mémoires tampons d’index) peuvent présenter des performances médiocres lorsqu’elles sont partagées. Les rendertargets verrouillables ne peuvent pas être partagés sur un matériel.
-   Les références à une ressource partagée inter-processus doivent avoir les mêmes dimensions que la ressource d’origine. Lors du passage d’un handle à travers le processus, incluez les informations de dimension afin que la référence puisse être créée de façon identique.
-   Les surfaces interprocessus partagées ne fournissent aucun mécanisme de synchronisation. Les modifications de lecture/écriture sur une surface partagée peuvent ne pas refléter la vue d’un processus de référencement de la surface quand cela est attendu. Pour assurer la synchronisation, utilisez des requêtes d’événements ou verrouillez la texture.
-   Seul le processus qui crée initialement une ressource partagée peut le verrouiller (tout processus qui ouvre une référence à cette ressource partagée ne peut pas le verrouiller).
-   Si une ressource partagée est verrouillée, les autres processus ne sont pas validés pour savoir si la ressource est disponible.

## <a name="srgb-conversion-before-blending"></a>Conversion sRVB avant la fusion

Vous pouvez maintenant vérifier si l’appareil peut convertir les données du pipeline en sRVB avant la fusion de la mémoire tampon de trame. Cela implique que l’appareil convertit les valeurs de cible de rendu de sRVB. Pour voir si la conversion est prise en charge par le matériel, vérifiez cette limite :


```
D3DPMISCCAPS_POSTBLENDSRGBCONVERT
```



Cette limite identifie le matériel qui prend en charge la conversion en sRVB avant la fusion. Cette fonctionnalité est importante pour le rendu de haute qualité à partir des mémoires tampons de trame FP16 dans le gestionnaire de fenêtrage (DWM, Desktop Window Manager).

## <a name="stretchrect-improvements"></a>Améliorations apportées à StretchRect

Dans les versions précédentes de DirectX, StretchRect présente de nombreuses restrictions pour gérer différents pilotes (consultez IDirect3DDevice9 :: StretchRect). Windows Vista est basé sur le modèle WDDM (Windows Device Driver Model). Ce nouveau modèle de pilote est bien plus robuste et permet aux pilotes de gérer des cas particuliers dans le matériel.

En général, la seule restriction restante est que la cible de rendu doit avoir été créée avec l’utilisation de la cible de rendu (D3DUSAGE \_ RENDERTARGET). Cette restriction est levée si vous effectuez une copie simple (où la source et la destination ont le même format, la même taille et il n’y a aucun sous-rectangle).

## <a name="texture-creation-in-system-memory"></a>Création de texture dans la mémoire système

Les applications qui ont besoin d’une plus grande souplesse sur l’utilisation, l’allocation et la suppression de la mémoire système peuvent maintenant créer des textures à partir d’un pointeur de mémoire système. Par exemple, une application peut créer une texture Direct3D à partir d’un pointeur bitmap de mémoire système GDI.

Vous devez effectuer deux opérations pour créer une telle texture :

-   Allouez suffisamment de mémoire système pour contenir la surface de texture. Le nombre minimal d’octets est de largeur x hauteur x octets par pixel.
-   Transmettez l’adresse d’un pointeur vers votre surface mémoire système pour le \* paramètre handle à IDirect3DDevice9 :: CreateTexture.

Voici le prototype de fonction pour IDirect3DDevice9 :: CreateTexture :


```
STDMETHOD(CreateTexture)(THIS_ UINT Width, UINT Height, UINT Levels, 
    DWORD Usage, D3DFORMAT Format, D3DPOOL Pool, IDirect3DTexture9** ppTexture, 
    HANDLE* pSharedHandle)
```



Une texture de mémoire système a les restrictions suivantes :

-   L’espacement de la texture doit être égal à la largeur de la texture multiplié par le nombre d’octets par pixel.
-   Lorsque vous utilisez des formats compressés (formats DXT), l’application est chargée d’allouer la taille correcte.
-   Seules les textures avec un niveau mipmap unique sont prises en charge.
-   La valeur passée à CreateTexture pour l’argument de pool doit être D3DPOOL \_ SYSTEMMEM.
-   Cette API encapsule la mémoire fournie dans une texture. Ne libérez pas cette mémoire tant que vous ne l’avez pas fait.

 

 
