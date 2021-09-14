---
description: 'Vous pouvez accéder directement à la mémoire de surface à l’aide de la méthode IDirect3DSurface9 :: LockRect.'
ms.assetid: ad669c22-6163-4fbb-bad0-160ced5bc558
title: Accès direct à la mémoire de surface (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ed9a65265671e6509172eccd9a1b66ea91507f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127124486"
---
# <a name="accessing-surface-memory-directly-direct3d-9"></a>Accès direct à la mémoire de surface (Direct3D 9)

Vous pouvez accéder directement à la mémoire de surface à l’aide de la méthode [**IDirect3DSurface9 :: LockRect**](/windows/desktop/api) . Quand vous appelez cette méthode, le paramètre pRect est un pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui décrit le rectangle sur la surface auquel accéder directement. Pour demander que la surface entière soit verrouillée, affectez à pRect la **valeur null**. En outre, vous pouvez spécifier un **Rect** qui couvre uniquement une partie de la surface. Si deux rectangles ne se chevauchent pas, deux threads ou processus peuvent verrouiller simultanément plusieurs rectangles dans une surface. Notez qu’un tampon d’arrière-plan à échantillonnage ne peut pas être verrouillé.

La méthode [**IDirect3DSurface9 :: LockRect**](/windows/desktop/api) remplit une structure [**\_ Rect D3DLOCKED**](d3dlocked-rect.md) avec toutes les informations pour accéder correctement à la mémoire de l’aire. La structure inclut des informations sur le pas à pas et a un pointeur vers les bits verrouillés. Lorsque vous avez terminé d’accéder à la mémoire d’exposition, appelez la méthode [**IDirect3DSurface9 :: UnlockRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dsurface9-unlockrect) pour la déverrouiller.

Si une surface est verrouillée, vous pouvez manipuler directement son contenu. La liste suivante décrit quelques conseils pour éviter les problèmes courants liés au rendu direct de la mémoire de surface.

-   Ne jamais supposer une tonalité d’affichage constante. Examinez toujours les informations de pas retournées par la méthode [**IDirect3DSurface9 :: LockRect**](/windows/desktop/api) . Ce pas à pas peut varier pour plusieurs raisons, notamment l’emplacement de la mémoire d’exposition, le type de carte d’affichage ou même la version du pilote Direct3D. Pour plus d’informations, consultez [largeur et tangage (Direct3D 9)](width-vs--pitch.md).
-   Veillez à copier les surfaces déverrouillées. Les méthodes de copie Direct3D échouent si elles sont appelées sur une surface verrouillée.
-   Limitez l’activité de votre application lorsqu’une surface est verrouillée.
-   Toujours copier les données alignées pour afficher la mémoire. Windows 98 utilise un gestionnaire d’erreurs de page, Vflatd. 386, pour implémenter une mémoire tampon d’image plate virtuelle pour les cartes d’affichage avec mémoire commutée. Le gestionnaire permet à ces appareils d’affichage de présenter une mémoire tampon de trame linéaire à Direct3D. La copie de données non alignées sur la mémoire d’affichage peut entraîner l’interruption des opérations par le système si la copie s’étend sur des banques de mémoire.
-   Une surface peut ne pas être verrouillée si elle appartient à une ressource affectée au \_ pool de mémoire D3DPOOL par défaut, sauf s’il s’agit d’une texture dynamique ou d’une surface créée à l’aide de [**IDirect3DDevice9 :: CreateOffscreenPlainSurface**](/windows/desktop/api). Les surfaces de mémoire tampon d’arrière-plan, accessibles à l’aide des méthodes [**IDirect3DDevice9 :: GetBackBuffer**](/windows/desktop/api) et [**IDirect3DSwapChain9 :: GetBackBuffer**](/windows/desktop/api) , peuvent être verrouillées uniquement si la chaîne de permutation a été créée avec le membre Flags des [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) pour inclure la mémoire tampon d’arrière-plan D3DPRESENTFLAG \_ verrouillable \_ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
