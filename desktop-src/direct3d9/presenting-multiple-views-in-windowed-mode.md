---
description: En plus de la chaîne de permutation qui est détenue et manipulée via l’interface IDirect3DDevice9, une application peut créer des chaînes de permutation supplémentaires afin de présenter plusieurs vues à partir du même appareil.
ms.assetid: 4fc09b9c-7adb-4f5d-80e0-2d39bc10420e
title: Présentation de plusieurs vues en mode fenêtre (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 039b02c487e06c7464dc8163c719371dc2b23706
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522767"
---
# <a name="presenting-multiple-views-in-windowed-mode-direct3d-9"></a>Présentation de plusieurs vues en mode fenêtre (Direct3D 9)

En plus de la chaîne de permutation qui est détenue et manipulée via l’interface [**IDirect3DDevice9**](/windows/desktop/api) , une application peut créer des chaînes de permutation supplémentaires afin de présenter plusieurs vues à partir du même appareil. L’application crée généralement une chaîne de permutation par vue à l’aide de la méthode [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) et associe chaque chaîne de permutation à une fenêtre particulière. L’application restitue des images dans les mémoires tampons d’arrière-plan de chaque chaîne de permutation, puis les présente individuellement.

Une seule chaîne de permutation à la fois peut être en plein écran sur chaque carte.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 
