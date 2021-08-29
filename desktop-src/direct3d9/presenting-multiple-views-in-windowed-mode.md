---
description: En plus de la chaîne de permutation qui est détenue et manipulée via l’interface IDirect3DDevice9, une application peut créer des chaînes de permutation supplémentaires afin de présenter plusieurs vues à partir du même appareil.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Présentation de plusieurs vues en mode fenêtre (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f43dbbbb300b8ec095593dc3eae1426487fd354a578460f03eb1025ee1a5568b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095589"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Présentation de plusieurs vues en mode fenêtre (Direct3D 9)

En plus de la chaîne de permutation qui est détenue et manipulée via l’interface [**IDirect3DDevice9**](/windows/desktop/api) , une application peut créer des chaînes de permutation supplémentaires afin de présenter plusieurs vues à partir du même appareil. L’application crée généralement une chaîne de permutation par vue à l’aide de la méthode [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) et associe chaque chaîne de permutation à une fenêtre particulière. L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis les présente individuellement.

Une seule chaîne de permutation à la fois peut être en plein écran sur chaque carte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 
