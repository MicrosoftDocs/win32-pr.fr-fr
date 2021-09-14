---
description: 'En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode IDirect3DDevice9 :: CreateAdditionalSwapChain pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.'
ms.assetid: f0d01dfb-d1de-4d16-8c64-4ae56d7fed06
title: Plusieurs vues en mode fenêtre (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed750472d1816c0365298630cfb426982743b11a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918228"
---
# <a name="multiple-views-in-windowed-mode-direct3d-9"></a>Plusieurs vues en mode fenêtre (Direct3D 9)

En plus de la chaîne de permutation qui est détenue et manipulée par l’intermédiaire de l’objet Direct3DDevice, une application peut utiliser la méthode [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) pour créer des chaînes de permutation supplémentaires pour présenter plusieurs vues à partir du même appareil.

En règle générale, l’application crée une chaîne de permutation par vue et associe chaque chaîne de permutation à une vue particulière. L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis utilise la méthode [**IDirect3DDevice9 ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) replaced pour les présenter individuellement. Notez qu’une seule chaîne de permutation à la fois peut être en plein écran sur chaque carte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation d’une scène](presenting-a-scene.md)
</dt> </dl>

 

 
