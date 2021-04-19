---
description: Les fonctionnalités suivantes ont été modifiées dans Microsoft Direct3D 9. Si vous utilisez ces fonctionnalités, consultez les modifications répertoriées ci-dessous pour vous aider à migrer votre application vers Direct3D 9.
ms.assetid: 6f5b2cc1-5415-4af8-a964-051a5af42680
title: Conversion en Direct3D 9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becdb878ad462bfc0157fb15b3c9c1ef2ba158dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515573"
---
# <a name="converting-to-direct3d-9"></a>Conversion en Direct3D 9

Les fonctionnalités suivantes ont été modifiées dans Microsoft Direct3D 9. Si vous utilisez ces fonctionnalités, consultez les modifications répertoriées ci-dessous pour vous aider à migrer votre application vers Direct3D 9.

-   [Modifications de BaseVertexIndex](#basevertexindex-changes)
-   [Modifications de CreateImageSurface](#createimagesurface-changes)
-   [D3DENUM \_ aucune \_ \_ modification du niveau WHQL](/windows)
-   [Créer des modifications de ressources](#create-resource-changes)
-   [Modifications de EnumAdapterModes](#enumadaptermodes-changes)
-   [\_Modifications apportées à SetStreamSource](#getsetstreamsource-changes)
-   [Modifications de la qualité d’échantillonnage multiple](#multisampling-quality-changes)
-   [Modifications de ResourceManagerDiscardBytes](#resourcemanagerdiscardbytes-changes)
-   [Modifications de SetSoftwareVertexProcessing](#setsoftwarevertexprocessing-changes)
-   [Modifications de l’échantillonneur de texture](#texture-sampler-changes)
-   [Modifications de déclaration de vertex](#vertex-declaration-changes)
-   [Intervalles \_ et \_ modifications SwapEffects \_](#intervals-and-swapeffects-changes)

## <a name="basevertexindex-changes"></a>Modifications de BaseVertexIndex

Dans DirectX 8. x, IDirect3DDevice8 :: SetIndices nécessitait un pointeur vers la mémoire tampon d’index et un BaseVertexIndex pour la position de départ dans la mémoire tampon de vertex. Une application qui effectue un traitement par lot de différents objets dans la mémoire tampon de vertex devait basculer le tampon d’index (ou appeler IDirect3DDevice8 :: SetIndices) avant d’appeler IDirect3DDevice8 ::D rawIndexedPrimitive.

Dans Direct3D 9, la position de départ dans la mémoire tampon de vertex, *BaseVertexIndex*, a été déplacée vers IDirect3DDevice9 ::D rawindexedprimitive et son type de données est passé d’un DWORD à un entier.


```
HRESULT IDirect3DDevice9::DrawIndexedPrimitive( 
    D3DPRIMITIVETYPE PrimType, 
    INT BaseVertexIndex, 
    UINT minIndex, 
    UINT NumVertices, 
    UINT startIndex, 
    UINT primCount); 

HRESULT SetIndices(IDirect3DIndexBuffer9* pIndexData); 
```



## <a name="createimagesurface-changes"></a>Modifications de CreateImageSurface

IDirect3DDevice8 :: CreateImageSurface a été renommé [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface). Un paramètre supplémentaire qui prend un type D3DPOOL a été ajouté. D3DPOOL \_ Scratch retourne une surface qui a des caractéristiques identiques à une surface créée par IDirect3DDevice8 :: CreateImageSurface. D3DPOOL \_ par défaut est le pool approprié à utiliser avec [**StretchRect**](/windows/desktop/api) et [**ColorFill**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-colorfill).

## <a name="d3denum_no_whql_level-changes"></a>D3DENUM \_ aucune \_ \_ modification du niveau WHQL

Les applications doivent maintenant demander explicitement Microsoft Windows Hardware Quality Labs (WHQL), car la réponse est relativement longue (quelques secondes). D3DENUM \_ aucun \_ niveau WHQL n' \_ a été supprimé et le \_ niveau D3DENUM WHQL \_ a été ajouté.

## <a name="create-resource-changes"></a>Créer des modifications de ressources

Un descripteur a été ajouté à plusieurs méthodes et doit avoir la valeur **null**. Les méthodes affectées sont les suivantes :

-   [**CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
-   [**CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
-   [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
-   [**CreateVertexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
-   [**CreateIndexBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
-   [**CreateRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createrendertarget)
-   [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)
-   [**CreateOffscreenPlainSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createoffscreenplainsurface)

## <a name="enumadaptermodes-changes"></a>Modifications de EnumAdapterModes

Le [**EnumAdapterModes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) prend maintenant un D3DFORMAT.


```
HRESULT IDirect3D9::EnumAdapterModes( 
       UINT Adapter, 
       D3DFORMAT Format, 
       UINT Mode, 
       D3DDISPLAYMODE *pMode); 
```



Le format prend en charge un ensemble étendu de modes d’affichage. Pour protéger les applications des formats d’énumération qui n’ont pas été inventés lors de la livraison de l’application, l’application doit indiquer à Direct3D le format des modes d’affichage à énumérer. Le tableau résultant de modes d’affichage diffère uniquement par la largeur, la hauteur et la fréquence d’actualisation.

L’application spécifie un format de pixel et l’énumération est limitée aux modes d’affichage qui correspondent exactement au format. La liste suivante répertorie les formats autorisés :

-   D3DFMT \_ A1R5G5B5
-   D3DFMT \_ A2B10G10R10
-   D3DFMT \_ A8R8G8B8
-   D3DFMT \_ R5G6B5
-   D3DFMT \_ X1R5G5B5
-   D3DFMT \_ X8R8G8B8

L’énumération est équivalente pour les versions alpha et non alpha du même format. Le format retourné sera toujours rempli avec le même format que celui fourni par l’application.

Cette méthode traite 565 et 555 comme équivalents, et retourne la version correcte au format. La différence entre en jeu uniquement lorsque l’application verrouille la mémoire tampon d’arrière-plan, et qu’il existe un indicateur explicite que l’application doit définir afin d’y parvenir.

## <a name="getsetstreamsource-changes"></a>Modifications apportées à SetStreamSource

Un paramètre a été ajouté aux méthodes [**GetStreamSource**](/windows/desktop/api) et [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) . Le décalage est le nombre d’octets entre le début du flux et le début des données de vertex. Elle est mesurée en octets. Cela permet au pipeline de prendre en charge les décalages de flux. Pour déterminer si l’appareil prend en charge les décalages de flux, consultez D3DDEVCAPS2 \_ STREAMOFFSET.


```
HRESULT GetStreamSource(
    UINT StreamNumber,
    IDirect3DVertexBuffer9 **ppStreamData,
    UINT *pOffsetInBytes,
    UINT *pStride);
```



## <a name="multisampling-quality-changes"></a>Modifications de la qualité d’échantillonnage multiple

Auparavant, il existait uniquement l' \_ énumération de type D3DMULTISAMPLE. Direct3D 9 conserve cette énumération et ajoute l’idée d’un niveau de qualité pour chaque élément de l’énumération. Le niveau de qualité indique un compromis entre la qualité visuelle et les performances en indiquant le nombre d’échantillons masquables (au sens de D3DRS \_ MULTISAMPLEMASK).

Une application doit choisir le nombre d’exemples masquables requis, puis consulter pQualityLevels. Si la valeur est différente de zéro, cette valeur indique le nombre de niveaux de qualité que l’application peut passer aux différentes fonctions de création par le biais de MultiSampleQuality. Étant donné que les pilotes exposent tous les schémas d’échantillonnage multiple comme des niveaux de qualité à D3DMULTISAMPLE \_ non masquables, vous pouvez énumérer tous les schémas d’échantillonnage multiple disponibles à l’aide de ce type si votre application n’a pas besoin de masquer des exemples.

Le \_ bit D3DPRASTERCAPS STRETCHBLTMULTISAMPLE Cap a été retiré. Ce bit est utilisé pour signifier que la méthode d’échantillonnage multiple ne prenait pas en charge les masques d’écriture et n’a pas pu être activée/désactivée entre [**BeginScene**](/windows/desktop/api) et [**EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene). Ces méthodes non masquées sont désormais exposées via D3DMULTISAMPLE non \_ MASKABLE.


```
HRESULT CheckDeviceMultiSampleType( 
       UINT Adapter, 
       D3DDEVTYPE DeviceType, 
       D3DFORMAT SurfaceFormat, 
       BOOL Windowed, 
       D3DMULTISAMPLE_TYPE MultiSampleType, 
       DWORD * pQualityLevels); 
```



Il existe une valeur maximale différente pour chaque nombre d’échantillons masquables. Par exemple, les \_ exemples D3DMULTISAMPLE 4 \_ peuvent avoir trois niveaux de qualité, tandis que les \_ exemples D3DMULTISAMPLE 2 ne peuvent en \_ avoir qu’un seul. Il y a au plus huit niveaux de qualité pour chaque nombre d’échantillons pouvant être masqués (le pilote n’est pas autorisé à exprimer davantage). La qualité est comprise entre zéro et ( \* pQualityLevels-1).

## <a name="resourcemanagerdiscardbytes-changes"></a>Modifications de ResourceManagerDiscardBytes

ResourceManagerDiscardBytes a été remplacé par IDirect3DDevice9 :: EvictManagedResources. Il peut supprimer toutes les ressources, à la fois Direct3D et les ressources du pilote.

Le gestionnaire de ressources est désormais consulté lorsqu’une ressource (qu’elle soit gérée ou non) ne peut pas être créée car la mémoire vidéo est insuffisante. Le responsable sera automatiquement invité à libérer suffisamment de ressources pour que la création aboutisse. Dans DirectX 8,0, il ne s’agissait pas d’un processus automatisé.

## <a name="setsoftwarevertexprocessing-changes"></a>Modifications de SetSoftwareVertexProcessing

Une application peut créer un appareil en mode mixte pour utiliser le traitement des vertex logiciels et matériels.

Pour basculer entre les deux modes de traitement de vertex dans DirectX 8. x, appelez IDirect3DDevice8 :: SetRenderState. Il a été remplacé par [**SetSoftwareVertexProcessing**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsoftwarevertexprocessing) pour faciliter les problèmes causés par les blocs d’État. Cette nouvelle méthode n’est pas enregistrée par les blocs d’État.

## <a name="texture-sampler-changes"></a>Modifications de l’échantillonneur de texture

Direct3D 9 prend en charge jusqu’à seize surfaces de texture en une seule passe à l’aide du modèle de nuanceur de pixels 2 \_ 0 ; Toutefois, le nombre de coordonnées de texture reste limité à huit. L’état de l’étape de texture est associé aux surfaces, aux jeux de coordonnées, au traitement des vertex et au traitement des pixels. Pour gérer ces différences au moment de la compilation, [**SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) a été divisé en deux méthodes :

-   IDirect3DDevice9 :: SetTextureStageState sera toujours utilisé pour l’état de coordonnée de texture, comme les modes de retour à la ligne et la génération de coordonnées de texture.
-   [**SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) a été ajouté et sera désormais utilisé pour le filtrage, la juxtaposition, le serrage, le MIPLOD, etc. Cela fonctionnera pour seize échantillonneurs au maximum.

### <a name="settexturestagestate-changes"></a>Modifications de SetTextureStageState

IDirect3DDevice9 :: SetTextureStageState définit maintenant les États suivants :

-   Correction de l’état du traitement des vertex de fonction. Cet État contrôle la manipulation des coordonnées de texture D3DTSS \_ TEXTURETRANSFORMFLAGS et D3DTSS \_ TEXCOORDINDEX. Jusqu’à huit de chaque peuvent être définis (car huit coordonnées de texture sont toujours prises en charge). D3DTSS \_ TEXCOORDINDEX est un état de traitement de vertex de fonction fixe. Si un nuanceur de sommet programmable est utilisé, cet État est ignoré.
-   Correction de l’état du nuanceur de pixels de fonction (TextureStageState hérité).

    -   D3DTSS \_ ALPHAARG0
    -   D3DTSS \_ ALPHAARG1
    -   D3DTSS \_ ALPHAARG2
    -   D3DTSS \_ ALPHAOP
    -   D3DTSS \_ BUMPENVLOFFSET
    -   D3DTSS \_ BUMPENVLSCALE
    -   D3DTSS \_ BUMPENVMAT00
    -   D3DTSS \_ BUMPENVMAT01
    -   D3DTSS \_ BUMPENVMAT10
    -   D3DTSS \_ BUMPENVMAT11
    -   D3DTSS \_ COLORARG0
    -   D3DTSS \_ COLORARG1
    -   D3DTSS \_ COLORARG2
    -   D3DTSS \_ COLOROP
    -   D3DTSS \_ RESULTARG

    Le nombre d’États de nuanceur de pixels de fonction fixes qui peuvent être définis est inférieur ou égal au nombre représenté par MaxTextureBlendStages.

Le nombre d’échantillonneurs de texture disponibles pour l’application est déterminé par la version du nuanceur de pixels, comme indiqué dans le tableau suivant.



| Nom                    | Number                                                         |
|-------------------------|----------------------------------------------------------------|
| PS \_ 1 \_ 1 à PS \_ 1 \_ 3    | 4 échantillonneurs de texture                                             |
| PS \_ 1 \_ 4                | 6 échantillonneurs de texture                                             |
| PS \_ 2 \_ 0                | 16 échantillonneurs de texture                                            |
| pipeline de fonction fixe | Échantillonneurs de texture MaxTextureBlendStages/MaxSimultaneousTextures |



 

Les appareils qui prennent en charge le mappage de déplacement dans Direct3D 9 prennent en charge un échantillonneur supplémentaire (D3DDMAPSAMPLER), qui échantillonne les mappages de déplacement dans l’unité du paveur.

### <a name="setsamplerstate-changes"></a>Modifications de SetSamplerState

IDirect3DDevice9 :: SetSamplerState définit l’état de l’échantillonneur (y compris celui utilisé dans l’unité du paveur pour échantillonner les mappages de déplacement). Ils ont été renommés avec un \_ préfixe D3DSAMP pour permettre la détection des erreurs au moment de la compilation lors du Portage à partir de DirectX 8. x. Les États sont les suivants :

-   \_Adresse D3DSAMP
-   D3DSAMP \_ ADDRESSV
-   D3DSAMP \_ ADDRESSW
-   D3DSAMP \_ BORDERCOLOR
-   D3DSAMP \_ MAGFILTER
-   D3DSAMP \_ MAXANISOTROPY
-   D3DSAMP \_ MAXMIPLEVEL
-   D3DSAMP \_ MINFILTER
-   D3DSAMP \_ MIPFILTER
-   D3DSAMP \_ MIPMAPLODBIAS

## <a name="vertex-declaration-changes"></a>Modifications de déclaration de vertex

Les déclarations de vertex sont maintenant dissociées de la création du nuanceur de sommets. Les déclarations de vertex utilisent désormais une interface COM (Component Object Model).

Pour DirectX 8. x, les déclarations de vertex sont liées aux nuanceurs de vertex.

-   Pour le pipeline de fonction fixe, appelez [**SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) avec le code de format de vertex flexible de la mémoire tampon de vertex.
-   Pour les nuanceurs vertex, appelez IDirect3DDevice9 :: SetVertexShader avec un handle vers un nuanceur de sommets créé précédemment. Le nuanceur comprend une déclaration de vertex.

Pour Direct3D 9, les déclarations de vertex sont dissociées des nuanceurs de vertex et peuvent être utilisées avec le pipeline de fonction fixe ou avec les nuanceurs.

-   Pour le pipeline de fonction fixe, il n’est pas nécessaire d’appeler IDirect3DDevice9 :: SetVertexShader. Toutefois, si vous souhaitez basculer vers le pipeline de fonctions fixe et que vous avez précédemment utilisé un nuanceur de sommets, appelez IDirect3DDevice9 :: SetVertexShader (**null**). Une fois cette opération effectuée, vous devrez toujours appeler [**SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf) pour déclarer le code de la Commission.
-   Quand vous utilisez des nuanceurs vertex, appelez IDirect3DDevice9 :: SetVertexShader avec l’objet vertex shader. En outre, appelez IDirect3DDevice9 :: SetFVF pour configurer une déclaration de vertex. Cela utilise les informations implicites dans le prix de la Commission. [**SetVertexDeclaration**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexdeclaration) peut être appelé à la place de IDirect3DDevice9 :: SetFVF, car il prend en charge les déclarations de vertex qui ne peuvent pas être exprimées avec une Commission de la Commission.

## <a name="intervals-and-swapeffects-changes"></a>Intervalles et modifications SwapEffects

Plusieurs modifications ont été apportées pour permettre à l’utilisateur de mieux contrôler la fréquence d’actualisation du moniteur, le taux de présentation et le tampon avant et le dessin de la mémoire tampon d’arrière-plan. Les voici :

-   Suppression d’un effet d’échange, D3DSWAPEFFECT \_ Copy \_ Vsync et d’un taux de présentation, D3DPRESENT \_ rate \_ Unlimited.
-   Les paramètres D3DPRESENT ont été renommés \_ . PresentationInterval plein écran \_ à PresentationIntervals.
-   Ajout de l' \_ intervalle D3DPRESENT \_ immédiat, ce qui signifie que la présentation n’est pas synchronisée avec la synchronisation verticale. Comme dans DirectX 8. x, la \_ valeur par défaut de l’intervalle D3DPRESENT \_ est définie comme égale à zéro et est équivalente à D3DPRESENT \_ Interval \_ . \_ \_ La valeur par défaut de l’intervalle D3DPRESENT est pratique pour initialiser les \_ paramètres D3DPRESENT à zéro.

Pour obtenir une explication détaillée des modes et des intervalles pris en charge, consultez D3DPRESENT.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Graphiques Direct3D 9](dx9-graphics.md)
</dt> </dl>

 

 
