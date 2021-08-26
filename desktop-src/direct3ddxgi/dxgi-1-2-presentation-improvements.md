---
title: Retourner le modèle, les rectangles modifiés, les zones défilantes
description: DXGI 1,2 prend en charge une nouvelle chaîne de permutation-modèle, des rectangles modifiés et des zones défilantes. Nous expliquons les avantages de l’utilisation de la nouvelle chaîne de permutation-modèle et de l’optimisation de la présentation en spécifiant des rectangles incorrects et des zones défilantes.
ms.assetid: 22236FBD-E881-49B5-8AE9-96FB526DFEF8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12f191af4a94b1379e2539b8d544163467fe4dc49141f244e8dcc1f13a3e36af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984212"
---
# <a name="flip-model-dirty-rectangles-scrolled-areas"></a>Retourner le modèle, les rectangles modifiés, les zones défilantes

DXGI 1,2 prend en charge une nouvelle chaîne de permutation-modèle, des rectangles modifiés et des zones défilantes. Nous expliquons les avantages de l’utilisation de la nouvelle chaîne de permutation-modèle et de l’optimisation de la présentation en spécifiant des rectangles incorrects et des zones défilantes.

## <a name="dxgi-flip-model-presentation"></a>Présentation DXGI Flip-Model

DXGI 1,2 ajoute la prise en charge du modèle de retournement pour les API Direct3D 10 et versions ultérieures. dans Windows 7, Direct3D 9ex first a adopté la [présentation flip-model](../direct3darticles/direct3d-9ex-improvements.md) pour éviter de copier inutilement la mémoire tampon de chaîne d’échange. En utilisant Flip Model, les mémoires tampons d’arrière-plan sont retournées entre le runtime et Gestionnaire de fenêtrage (DWM), de sorte que le DWM compose toujours directement à partir de la mémoire tampon d’arrière-plan au lieu de copier le contenu de la mémoire tampon d’arrière-plan.

Les API DXGI 1,2 incluent une interface révisée de la chaîne d’échange DXGI, [**IDXGISwapChain1**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgiswapchain1). Vous pouvez utiliser plusieurs méthodes d’interface [**IDXGIFactory2**](/windows/desktop/api/DXGI1_2/nn-dxgi1_2-idxgifactory2) pour créer l’objet **IDXGISwapChain1** approprié à utiliser avec un handle [**HWND**](../winprog/windows-data-types.md) , un objet [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow?view=winrt-19041) , [DirectComposition](../directcomp/directcomposition-portal.md)ou le [**Windows. L'. Framework XAML**](/uwp/api/Windows.UI.Xaml?view=winrt-19041) .

Vous sélectionnez le modèle de retournement de présentation en spécifiant l' [**effet d’échange dxgi retourner la valeur d’énumération \_ \_ \_ \_ séquentielle**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect) dans le membre **SwapEffect** de la structure de la [**chaîne de \_ permutation dxgi \_ \_ DESC1**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) et en définissant le membre **BufferCount** de la **\_ chaîne de permutation \_ \_** dxgi DESC1 sur un minimum de 2. Pour plus d’informations sur l’utilisation de DXGI Flip Model, consultez [dxgi Flip Model](dxgi-flip-model.md). En raison de la présentation fluide et des autres nouvelles fonctionnalités de retournement du modèle de présentation, nous vous recommandons d’utiliser l’outil retourner le modèle de présentation pour toutes les nouvelles applications que vous écrivez avec Direct3D 10 et les API ultérieures.

## <a name="using-dirty-rectangles-and-the-scroll-rectangle-in-swap-chain-presentation"></a>Utilisation de rectangles modifiés et du rectangle de défilement dans la présentation de la chaîne de permutation

En utilisant des rectangles incorrects et le rectangle de défilement dans la présentation de la chaîne de permutation, vous économisez l’utilisation de la bande passante de mémoire et l’utilisation associée de la puissance système, car la quantité de données de pixels dont le système d’exploitation a besoin pour dessiner le cadre suivant est réduite si le système d’exploitation n’a pas besoin de dessiner l’ensemble Pour les applications qui sont souvent affichées via Connexion Bureau à distance et d’autres technologies d’accès à distance, les économies sont particulièrement perceptibles dans la qualité d’affichage, car ces technologies utilisent des rectangles incorrects et des métadonnées de défilement.

Vous pouvez utiliser Scroll uniquement avec les chaînes de permutation DXGI qui s’exécutent dans le modèle de présentation Flip. Vous pouvez utiliser des rectangles modifiés avec les chaînes de permutation DXGI qui s’exécutent à la fois dans le modèle Flip et dans le modèle BitBlt (défini avec [**dxgi \_ swap \_ Effect \_ Sequential**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)).

Dans ce scénario et cette illustration, nous présentons les fonctionnalités d’utilisation des rectangles incorrects et de défilement. Ici, une application défilante contient du texte et anime une vidéo. L’application utilise des rectangles modifiés pour mettre à jour simplement la vidéo d’animation et la nouvelle ligne de la fenêtre, au lieu de mettre à jour la fenêtre entière. Le rectangle de défilement permet au système d’exploitation de copier et de traduire le contenu précédemment rendu sur le nouveau Frame et de restituer uniquement la nouvelle ligne sur le nouveau Frame.

L’application effectue une présentation en appelant la méthode [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) . Dans cet appel, l’application passe un pointeur vers une structure de [**\_ \_ paramètres dxgi présente**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters) qui comprend des rectangles incorrects et le nombre de rectangles modifiés, ou le rectangle de défilement et le décalage de défilement associé, ou les deux rectangles de modification et le rectangle de défilement. Notre application passe 2 rectangles incorrects et le rectangle de défilement. Le rectangle de défilement est la zone du frame précédent que le système d’exploitation doit copier dans le frame actuel avant de restituer le frame actuel. L’application spécifie la vidéo animée et la nouvelle ligne en tant que rectangles modifiés, et le système d’exploitation les affiche sur le frame actuel.

![illustration du chevauchement des rectangles de défilement et de modification](images/dxgipresentparam.png)

``` syntax
DirtyRectsCount = 2
pDirtyRects[ 0 ] = { 10, 30, 40, 50 } // Video
pDirtyRects[ 1 ] = { 0, 70, 50, 80 } // New line
*pScrollRect = { 0, 0, 50, 70 }
*pScrollOffset = { 0, -10 }
```

Le rectangle en pointillés affiche le rectangle de défilement dans le frame actuel. Le rectangle de défilement est spécifié par le membre **pScrollRect** des [**\_ \_ paramètres dxgi present**](/windows/desktop/api/DXGI1_2/ns-dxgi1_2-dxgi_present_parameters). La flèche affiche le décalage de défilement. Le décalage de défilement est spécifié par le membre **pScrollOffset** des **\_ \_ paramètres dxgi present**. Les rectangles pleins affichent les rectangles modifiés que l’application a mis à jour avec le nouveau contenu. Les rectangles remplis sont spécifiés par les membres **DirtyRectsCount** et **PDirtyRects** des **\_ \_ paramètres dxgi présents**.

### <a name="sample-2-buffer-flip-model-swap-chain-with-dirty-rectangles-and-scroll-rectangle"></a>Exemple 2 : chaîne de permutation du modèle de mise en mémoire tampon avec rectangles modifiés et rectangle de défilement

L’illustration et la séquence suivantes montrent un exemple d’opération de présentation de DXGI Flip-Model qui utilise des rectangles modifiés et un rectangle de défilement. Dans cet exemple, nous utilisons le nombre minimal de mémoires tampons pour la présentation de retournement de modèle, qui est un nombre de tampons de deux, une mémoire tampon d’arrière-plan qui contient le contenu d’affichage de l’application et une mémoire tampon d’arrière-plan qui contient le frame actuel que l’application souhaite restituer.

1.  Comme indiqué dans le tampon d’avant au début du frame, l’application avec défilement affiche initialement un frame avec du texte et anime la vidéo.
2.  Pour afficher le frame suivant, l’application effectue le rendu sur la mémoire tampon d’arrière-plan des rectangles incorrects qui mettent à jour la vidéo d’animation et la nouvelle ligne pour la fenêtre.
3.  Lorsque l’application appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1), elle spécifie les rectangles modifiés et le rectangle de défilement et le décalage. Le runtime copie ensuite le rectangle de défilement du frame précédent moins les rectangles modifiés mis à jour dans la mémoire tampon d’arrière-plan actuelle.
4.  Le runtime échange enfin les mémoires tampons d’arrière-plan et d’arrière-plan.

![exemple de chaîne de permutation de modèle avec rectangles défilant et incorrects](images/2-buffer-flip-model-swap-chain.png)

### <a name="tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames"></a>Suivi des rectangles de modification et des rectangles de défilement sur plusieurs frames

Lorsque vous utilisez des rectangles modifiés dans votre application, vous devez effectuer le suivi des rectangles modifiés pour prendre en charge le rendu incrémentiel. Quand votre application appelle [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) avec des rectangles incorrects, vous devez vous assurer que chaque pixel dans les rectangles incorrects est à jour. Si vous ne rerendez pas complètement la totalité de la zone du rectangle modifié ou si vous ne savez pas quelles sont les zones modifiées, vous devez copier les données de la mémoire tampon d’arrière-plan entièrement cohérente précédente dans la mémoire tampon d’arrière-plan actuelle et obsolète avant de commencer le rendu.

Le runtime copie uniquement les différences entre les zones mises à jour du frame précédent et les zones mises à jour du frame actuel sur la mémoire tampon d’arrière-plan actuelle. Si ces zones se croisent, le runtime copie uniquement la différence entre elles. Comme vous pouvez le voir dans le diagramme et la séquence suivants, vous devez copier l’intersection entre le rectangle de modification de l’image 1 et le rectangle de modification de l’image 2 dans le rectangle de modification de l’image 2.

1.  Présente le rectangle sale dans le frame 1.
2.  Copiez l’intersection entre le rectangle modifié du frame 1 et le rectangle modifié du frame 2 dans le rectangle de modification du frame 2.
3.  Présente le rectangle sale dans le frame 2.

![suivi des rectangles de défilement et de modification sur plusieurs frames](images/track-dirty-rects-scroll-rects.png)

Pour généraliser, pour une chaîne de permutation avec N mémoires tampons, la zone que le runtime copie à partir du dernier frame jusqu’au frame actuel sur le présent du frame actuel est :

![équation pour calculer la zone copiée par le Runtime](images/runtime-copy-equation.png)

où buffer indique l’index de mémoire tampon dans une chaîne de permutation, en commençant par l’index de la mémoire tampon actuel à zéro.

Vous pouvez effectuer le suivi de toute intersection entre le frame précédent et les rectangles non intègres du frame actuel en conservant une copie des rectangles incorrects du frame précédent ou en rerendant les rectangles incorrects du nouveau Frame avec le contenu approprié à partir de l’image précédente.

De même, dans les cas où la chaîne de permutation contient plus de 2 mémoires tampons d’arrière-plan, vous devez vous assurer que les zones qui se chevauchent entre les rectangles de modification de la mémoire tampon active et les rectangles incorrects de tous les frames précédents sont copiées ou ré-restituées.

### <a name="tracking-a-single-intersection-between-2-dirty-rectangles"></a>Suivi d’une seule intersection entre 2 rectangles incorrects

Dans le cas le plus simple, lorsque vous mettez à jour un rectangle de modification unique par trame, les rectangles modifiés entre deux frames peuvent se croiser. Pour déterminer si le rectangle de modification du frame précédent et le rectangle de modification du frame actuel se chevauchent, vous devez vérifier si le rectangle modifié du frame précédent croise le rectangle modifié du frame actuel. Vous pouvez appeler la fonction GDI [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) pour déterminer si deux structures [**Rect**](/previous-versions//dd162897(v=vs.85)) qui représentent les deux rectangles incorrects se croisent.

Dans cet extrait de code, un appel à [**IntersectRect**](/windows/win32/api/winuser/nf-winuser-intersectrect) retourne l’intersection de deux rectangles incorrects dans un autre [**Rect**](/previous-versions//dd162897(v=vs.85)) appelé dirtyRectCopy. Une fois que l’extrait de code a déterminé que les deux rectangles incorrects se croisent, il appelle la méthode [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) pour copier la région d’intersection dans le frame actuel.

```
RECT dirtyRectPrev, dirtyRectCurrent, dirtyRectCopy;
 
if (IntersectRect( &dirtyRectCopy, &dirtyRectPrev, &dirtyRectCurrent ))
{
       D3D11_BOX intersectBox;
       intersectBox.left    = dirtyRectCopy.left;
       intersectBox.top     = dirtyRectCopy.top;
       intersectBox.front   = 0;
       intersectBox.right   = dirtyRectCopy.right;
       intersectBox.bottom  = dirtyRectCopy.bottom;
       intersectBox.back    = 1;
 
       d3dContext->CopySubresourceRegion1(pBackbuffer,
                                    0,
                                    0,
                                    0,
                                    0,
                                    pPrevBackbuffer,
                                    0,
                                    &intersectBox,
                                    0
                                    );
}

// Render additional content to the current pBackbuffer and call Present1.
```

Si vous utilisez cet extrait de code dans votre application, l’application est alors prête à appeler [**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1) pour mettre à jour le frame actuel avec le rectangle de modification actuel.

### <a name="tracking-intersections-between-n-dirty-rectangles"></a>Suivi des intersections entre N rectangles incorrects

Si vous spécifiez plusieurs rectangles incorrects, qui peuvent inclure un rectangle impropre pour la ligne de défilement récemment révélée, par trame, vous devez vérifier et suivre les chevauchements qui peuvent se produire entre tous les rectangles de modification de l’image précédente et tous les rectangles incorrects du frame actuel. Pour calculer les intersections entre les rectangles modifiés du frame précédent et les rectangles modifiés du frame actuel, vous pouvez regrouper les rectangles incorrects dans des régions.

Dans cet extrait de code, nous appelons la fonction GDI [**SetRectRgn**](/windows/win32/api/wingdi/nf-wingdi-setrectrgn) pour convertir chaque rectangle sale en une région rectangulaire, puis nous appelons la fonction GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) pour combiner toutes les régions rectangulaires incorrectes dans un groupe.

```
HRGN hDirtyRgnPrev, hDirtyRgnCurrent, hRectRgn; // Handles to regions 
// Save all the dirty rectangles from the previous frame.
 
RECT dirtyRect[N]; // N is the number of dirty rectangles in current frame, which includes newly scrolled area.
 
int iReturn;
SetRectRgn(hDirtyRgnCurrent, 
       dirtyRect[0].left, 
       dirtyRect[0].top, 
       dirtyRect[0].right, 
       dirtyRect[0].bottom 
       );

for (int i = 1; i<N; i++)
{
   SetRectRgn(hRectRgn, 
          dirtyRect[0].left, 
          dirtyRect[0].top, 
          dirtyRect[0].right, 
          dirtyRect[0].bottom 
          );

   iReturn = CombineRgn(hDirtyRgnCurrent,
                        hDirtyRgnCurrent,
                        hRectRgn,
                        RGN_OR
                        );
   // Handle the error that CombineRgn returns for iReturn.
}
```

Vous pouvez maintenant utiliser la fonction GDI [**CombineRgn**](/windows/win32/api/wingdi/nf-wingdi-combinergn) pour déterminer l’intersection entre la région modifiée du frame précédent et la région modifiée du frame actuel. Une fois que vous avez obtenu la région d’intersection, appelez la fonction GDI [**GetRegionData**](/windows/win32/api/wingdi/nf-wingdi-getregiondata) pour obtenir chaque rectangle de la région d’intersection, puis appelez la méthode [**ID3D11DeviceContext1 :: CopySubresourceRegion1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) pour copier chaque rectangle d’intersection dans la mémoire tampon d’arrière-plan actuelle. L’extrait de code suivant montre comment utiliser ces fonctions GDI et Direct3D.

```
HRGN hIntersectRgn;
bool bRegionsIntersect;
iReturn = CombineRgn(hIntersectRgn, hDirtyRgnCurrent, hDirtyRgnPrev, RGN_AND);
if (iReturn == ERROR)
{
       // Handle error.
}
else if(iReturn == NULLREGION)
{
       bRegionsIntersect = false;
}
else
{
       bRegionsIntersect = true;
}
 
if (bRegionsIntersect)
{
       int rgnDataSize = GetRegionData(hIntersectRgn, 0, NULL);
       if (rgnDataSize)
       {
              char pMem[] = new char[size];
              RGNDATA* pRgnData = reinterpret_cast<RGNDATA*>(pMem);
              iReturn = GetRegionData(hIntersectRgn, rgnDataSize, pRgnData);
              // Handle iReturn failure.
 
              for (int rectcount = 0; rectcount < pRgnData->rdh.nCount; ++r)
              {
                     const RECT* pIntersectRect = reinterpret_cast<RECT*>(pRgnData->Buffer) +                                            
                                                  rectcount;                
                     D3D11_BOX intersectBox;
                     intersectBox.left    = pIntersectRect->left;
                     intersectBox.top     = pIntersectRect->top;
                     intersectBox.front   = 0;
                     intersectBox.right   = pIntersectRect->right;
                     intersectBox.bottom  = pIntersectRect->bottom;
                     intersectBox.back    = 1;
 
                     d3dContext->CopySubresourceRegion1(pBackbuffer,
                                                      0,
                                                      0,
                                                      0,
                                                      0,
                                                      pPrevBackbuffer,
                                                      0,
                                                      &intersectBox,
                                                      0
                                                      );
              }

              delete [] pMem;
       }
}
```

### <a name="bitblt-model-swap-chain-with-dirty-rectangles"></a>Chaîne d’échange de modèle BitBlt avec rectangles modifiés

Vous pouvez utiliser des rectangles modifiés avec les chaînes de permutation DXGI qui s’exécutent dans le modèle BitBlt (défini avec l' [**\_ effet d’échange dxgi \_ \_ séquentiel**](/windows/desktop/api/DXGI/ne-dxgi-dxgi_swap_effect)). Les chaînes d’échange de modèle BitBlt qui utilisent plusieurs mémoires tampons doivent également suivre les rectangles de modification qui se chevauchent entre les frames de la même façon que celle décrite dans [suivi des rectangles incorrects et des rectangles de défilement sur plusieurs frames](#tracking-dirty-rectangles-and-scroll-rectangles-across-multiple-frames) pour les chaînes de permutation du modèle. Les chaînes d’échange de modèle BitBlt avec une seule mémoire tampon n’ont pas besoin de suivre les rectangles de modification qui se chevauchent, car la mémoire tampon entière est redessinée à chaque trame.

## <a name="related-topics"></a>Rubriques connexes

[Améliorations de DXGI 1,2](dxgi-1-2-improvements.md)
