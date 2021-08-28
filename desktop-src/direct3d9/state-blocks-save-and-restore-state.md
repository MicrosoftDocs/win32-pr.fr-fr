---
description: Un bloc d’État est un groupe d’États de périphérique.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: État de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 104010f2ea057870b70e9887e5b325f1de68c463
ms.sourcegitcommit: 8d7ce0c4827f8a4fd501cc6487f1a8360e944577
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/24/2021
ms.locfileid: "122767653"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a>État de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)

Un bloc d’État est un groupe d’États de périphérique. L’état de l’appareil est constitué de l’état de rendu, de l’état du vertex, de l’état du pixel ou de tous les éléments ci-dessus. Un bloc d’état contient un instantané de l’état actuel d’un appareil, ou vous pouvez créer un bloc d’État qui enregistre chaque modification d’État apportée par votre application.

## <a name="capture-a-block-of-state"></a>Capturer un bloc d’État

Choisissez le type d’État que vous souhaitez capturer, puis créez un bloc d’État comme suit :


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



[**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock) crée un bloc d’État et capture automatiquement l’état de l’appareil. L’état de l’appareil est spécifié par le type de bloc d’État dans le premier argument. Cet État peut être l’un des suivants : tout l’état de l’appareil (voir [enregistrement de tous les États des appareils avec un StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), tout l’état des pixels (voir enregistrement de [l’état des pixels avec un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) ou tous les États des vertex (voir [enregistrement des États des vertex avec un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).

Le système d’effet utilise un bloc d’État pour enregistrer l’État. Après l’appel de [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) , un bloc d’État est créé et l’État est capturé. Quand [**ID3DXEffect :: end**](id3dxeffect--end.md) est appelé, l’état du bloc d’État est réappliqué à l’appareil.

## <a name="capture-individual-states"></a>Capturer des États individuels

Pour enregistrer une séquence d’état personnalisée, encapsulez l’état que vous souhaitez enregistrer dans une paire [**IDirect3DDevice9 :: BeginStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-beginstateblock) et [**IDirect3DDevice9 :: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) . BeginStateBlock indique à l’appareil actuel de configurer un bloc d’État et de l’ajouter à chaque modification d’État qui se produit jusqu’à l’appel de EndStateBlock. Voici un exemple :


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



Cela permet d’enregistrer un nombre quelconque de modifications d’état d’une séquence dans un stateblock personnalisé. Plus tard, lorsque vous souhaitez utiliser le stateblock pour réinitialiser l’état de l’appareil, appelez [**IDirect3DStateBlock9 :: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply). Cela remplacera uniquement l’état de l’appareil qui a été capturé dans le bloc d’État. Tout autre État d’appareil qui n’a pas été capturé avec le stateblock personnalisé n’est pas modifié. Là encore, étant donné que l’objet stateblock est une interface, vous devez le libérer une fois que vous avez fini de l’utiliser.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États (Direct3D 9)](states.md)
</dt> </dl>

 

 
