---
description: La gestion des ressources est le processus dans lequel les ressources sont promues du stockage de mémoire système vers le stockage accessible aux appareils et ignorées à partir du stockage accessible à l’appareil.
ms.assetid: 4aa55313-b86c-48e7-829a-a0917c2ebae7
title: Gestion des ressources (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b860f1c394de932f167de94a3552315b1b70396e9900fccc079ab09142c9e31c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117728462"
---
# <a name="managing-resources-direct3d-9"></a>Gestion des ressources (Direct3D 9)

La gestion des ressources est le processus dans lequel les ressources sont promues du stockage de mémoire système vers le stockage accessible aux appareils et ignorées à partir du stockage accessible à l’appareil. Le temps d’exécution de Direct3D a son propre algorithme de gestion basé sur une technique de priorité la moins récemment utilisée. Direct3D bascule vers une technique de priorité la plus récemment utilisée lorsqu’il détecte que plus de ressources que ne peut coexister dans la mémoire accessible par l’appareil sont utilisées dans une seule trame entre [**IDirect3DDevice9 :: BeginScene**](/windows/desktop/api) et [**IDirect3DDevice9 :: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) appels.

Utilisez l’indicateur [**D3DPOOL \_ par défaut**](./d3dpool.md) au moment de la création pour spécifier qu’une ressource est placée dans le pool de mémoires le plus approprié pour l’ensemble des utilisations demandées pour la ressource donnée. Il s’agit généralement de la mémoire vidéo, y compris la mémoire vidéo locale et la mémoire AGP (Accelerated Graphics Port). Les ressources dans le pool par défaut ne sont pas conservées par le biais de transitions entre les États perdus et opérationnels de l’appareil. Ces ressources doivent être libérées avant d’appeler Reset et doivent ensuite être recréées.

Utilisez l' [**indicateur \_ managé D3DPOOL**](./d3dpool.md) au moment de la création pour spécifier une ressource managée. Les ressources managées sont conservées par le biais de transitions entre les États perdus et opérationnels de l’appareil. Ces ressources existent à la fois dans la mémoire vidéo et la mémoire système. Une ressource managée est copiée dans la mémoire vidéo quand elle est nécessaire pendant le rendu. L’appareil peut être restauré à l’aide d’un appel à [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), et ces ressources continuent à fonctionner normalement sans être rechargées avec des données. Toutefois, si l’appareil doit être détruit et recréé, toutes les ressources doivent être recréées.

La gestion des ressources n’est pas recommandée pour les ressources qui changent avec une fréquence élevée. Par exemple, les tampons de vertex et d’index qui sont utilisés pour parcourir un graphique de scène chaque image qui rend uniquement la géométrie visible par l’utilisateur modifie chaque frame. Étant donné que les ressources managées sont sauvegardées par la mémoire système, les modifications constantes doivent être mises à jour dans la mémoire système, ce qui peut entraîner une sérieuse dégradation des performances. Pour ce scénario particulier, vous devez utiliser [**D3DPOOL \_ par défaut**](./d3dpool.md) avec [**D3DUSAGE \_ Dynamic**](d3dusage.md) .

Un autre exemple pour lequel la gestion des ressources n’est pas recommandée (et qui n’est pas explicitement autorisée par le Runtime) est la gestion d’une texture créée avec [**D3DUSAGE \_ RENDERTARGET**](d3dusage.md). Si la mémoire utilisée par les cibles de rendu était gérée par le runtime, son contenu doit constamment être copié dans la mémoire système pendant le rendu, ce qui entraîne des pénalités en matière de performances. Pour cette raison, les cibles de rendu doivent être créées dans le pool par défaut. Si l’accès au processeur des données contenues dans une cible de rendu est nécessaire, les données doivent être copiées dans une ressource créée dans [**D3DPOOL \_ SYSTEMMEM**](./d3dpool.md) à l’aide de [**IDirect3DDevice9 :: UpdateTexture**](/windows/desktop/api)ou [**IDirect3DDevice9 :: UpdateSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatesurface)

Pour plus d’informations sur l’état perdu d’un appareil, consultez [appareils perdus (Direct3D 9)](lost-devices.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
