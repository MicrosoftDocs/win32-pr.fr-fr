---
description: 'En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode IDirect3DDevice9 :: CreateAdditionalSwapChain pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Plusieurs vues en mode fenêtre (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e2784a4f2bd855293e427aa9297d2e5725a74a3f5bce52b4b53cdf3d9081062
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069019"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Plusieurs vues en mode fenêtre (Direct3D 9)

En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.

En règle générale, l’application crée une chaîne de permutation par vue et associe chaque chaîne de permutation à une vue particulière. L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis utilise la méthode [**IDirect3DDevice9 ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) replaced pour les présenter individuellement. Notez qu’une seule chaîne de permutation à la fois peut être en plein écran sur chaque carte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation d’une scène](presenting-a-scene.md)
</dt> </dl>

 

 
