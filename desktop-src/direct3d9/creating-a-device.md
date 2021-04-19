---
description: Pour créer un appareil Direct3D, commencez par créer un objet Direct3D (voir Direct3DCreate9).
ms.assetid: 06810f31-fa6c-416e-bd7b-65cfb3e6d7f2
title: Création d’un appareil (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9c033ed25262f0a3bcdee9db73509ddf5cb53b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516767"
---
# <a name="creating-a-device-direct3d-9"></a>Création d’un appareil (Direct3D 9)

Pour créer un appareil Direct3D, commencez par créer un objet Direct3D (voir [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)). Tous les appareils de rendu créés par un objet Direct3D partagent les mêmes ressources physiques. Si vous créez plusieurs appareils de rendu à partir d’un seul objet Direct3D, des pénalités de performances extrêmes sont générées, car elles partagent le même matériel.

Tout d’abord, initialisez les valeurs de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) utilisée pour créer le périphérique Direct3D. L’exemple de code suivant spécifie une application avec fenêtres dans laquelle la mémoire tampon d’arrière-plan est copiée dans la mémoire tampon d’origine pendant une opération de synchronisation verticale uniquement.


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



Ensuite, créez le périphérique Direct3D. L’appel de [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) suivant spécifie l’adaptateur par défaut, un périphérique de couche d’abstraction matérielle (HAL) et le traitement du vertex logiciel.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



Notez qu’un appel pour créer, mettre à jour ou réinitialiser l’appareil doit se produire uniquement sur le même thread que la procédure de fenêtre de la fenêtre de focus.

Après avoir créé l’appareil, définissez son état.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
