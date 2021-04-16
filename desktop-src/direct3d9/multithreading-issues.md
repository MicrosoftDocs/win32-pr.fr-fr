---
description: Les applications Direct3D en plein écran fournissent un handle de fenêtre à l’exécution de Direct3D.
ms.assetid: 66a9e14f-46c8-45e8-ae0e-4d8cf5106acc
title: Problèmes liés aux multithreads (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8d163698e6cc1b4855668d255ed46fd28700d1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392424"
---
# <a name="multithreading-issues-direct3d-9"></a>Problèmes liés aux multithreads (Direct3D 9)

Les applications Direct3D en plein écran fournissent un handle de fenêtre à l’exécution de Direct3D. La fenêtre est accrochée au moment de l’exécution. Cela signifie que tous les messages transmis à la procédure de message de fenêtre de l’application ont d’abord été examinés par la procédure de gestion des messages de l’exécution Direct3D.

Les modifications du mode d’affichage sont affectées par les routines de prise en charge intégrées au système d’exploitation sous-jacent. En cas de modification du mode, le système diffuse plusieurs messages à toutes les applications. Dans les applications Direct3D, les messages sont reçus sur le thread de procédure de fenêtre, qui n’est pas nécessairement le même thread que celui qui a appelé [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ou [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) (ou la version finale de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9), ce qui peut provoquer un changement de mode d’affichage). La durée d’exécution de Direct3D gère plusieurs sections critiques en interne. Étant donné qu’au moins l’une de ces sections critiques est conservée sur le commutateur de mode provoqué par **IDirect3DDevice9 :: Reset** ou **IDirect3D9 :: CreateDevice**, ces sections critiques sont conservées quand l’application reçoit les messages de fenêtre liés au mode de modification de mode.

Cette conception a des implications pour les applications multithread. En particulier, une application doit veiller à séparer fortement ses threads de gestion de message de fenêtre de ses threads Direct3D. Une application qui provoque une modification du mode sur un thread, mais effectue des appels Direct3D sur un thread différent dans sa procédure de fenêtre est menacée d’interblocage.

Pour ces raisons, Direct3D est conçu de sorte que les méthodes [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset), [**IDirect3D9 :: CreateDevice**](/windows/desktop/api), [**IDirect3DDevice9 :: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)ou la version finale de [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) ne puissent être appelées qu’à partir du même thread que celui qui gère les messages de fenêtre.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 
