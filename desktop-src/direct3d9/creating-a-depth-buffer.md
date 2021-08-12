---
description: Une mémoire tampon de profondeur est une propriété de l’appareil. Pour créer un tampon de profondeur géré par Direct3D, définissez les membres appropriés de la structure de \_ paramètres D3DPRESENT comme indiqué dans l’exemple de code suivant.
ms.assetid: 2b442cf7-2146-4dea-809a-ebb8bcfbec08
title: Création d’un tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d2f79e6ad32aa2c10b92d0233f85d86744d0a2c562b1991c89990d61bad506c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527921"
---
# <a name="creating-a-depth-buffer-direct3d-9"></a>Création d’un tampon de profondeur (Direct3D 9)

Une mémoire tampon de profondeur est une propriété de l’appareil. Pour créer un tampon de profondeur géré par Direct3D, définissez les membres appropriés de la structure [**de \_ paramètres D3DPRESENT**](d3dpresent-parameters.md) comme indiqué dans l’exemple de code suivant.


```
D3DPRESENT_PARAMETERS d3dpp; 
ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed               = TRUE;
d3dpp.SwapEffect             = D3DSWAPEFFECT_COPY;
d3dpp.EnableAutoDepthStencil = TRUE;
d3dpp.AutoDepthStencilFormat = D3DFMT_D16;
```



En affectant la **valeur true** au membre EnableAutoDepthStencil, vous indiquez à Direct3D de gérer les mémoires tampons de profondeur pour l’application. Notez que AutoDepthStencilFormat doit être défini sur un format de mémoire tampon de profondeur valide. L' \_ indicateur D3DFMT D16 spécifie une mémoire tampon de profondeur de 16 bits, si celle-ci est disponible.

L’appel suivant à la méthode [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) crée un appareil qui crée ensuite une mémoire tampon de profondeur.


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                &d3dpp, &d3dDevice ) ) )
return E_FAIL;
```



La mémoire tampon de profondeur est définie automatiquement en tant que cible de rendu de l’appareil. Lorsque l’appareil est réinitialisé, le tampon de profondeur est automatiquement détruit et recréé dans la nouvelle taille.

Pour créer une surface de mémoire tampon de profondeur, utilisez la méthode [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Pour définir une nouvelle surface de mémoire tampon de profondeur pour l’appareil, utilisez la méthode [**IDirect3DDevice9 :: SetDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setdepthstencilsurface) .

Pour utiliser la mémoire tampon de profondeur dans votre application, vous devez activer la mémoire tampon de profondeur. Pour plus d’informations, consultez Activation de la [mise en mémoire tampon de profondeur (Direct3D 9)](enabling-depth-buffering.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
