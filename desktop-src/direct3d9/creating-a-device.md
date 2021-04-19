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
# <a name="creating-a-device-direct3d-9"></a><span data-ttu-id="f536c-103">Création d’un appareil (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="f536c-103">Creating a Device (Direct3D 9)</span></span>

<span data-ttu-id="f536c-104">Pour créer un appareil Direct3D, commencez par créer un objet Direct3D (voir [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span><span class="sxs-lookup"><span data-stu-id="f536c-104">To create a Direct3D device, first create a Direct3D object (see [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9)).</span></span> <span data-ttu-id="f536c-105">Tous les appareils de rendu créés par un objet Direct3D partagent les mêmes ressources physiques.</span><span class="sxs-lookup"><span data-stu-id="f536c-105">All rendering devices created by a Direct3D object share the same physical resources.</span></span> <span data-ttu-id="f536c-106">Si vous créez plusieurs appareils de rendu à partir d’un seul objet Direct3D, des pénalités de performances extrêmes sont générées, car elles partagent le même matériel.</span><span class="sxs-lookup"><span data-stu-id="f536c-106">If you create multiple rendering devices from a single Direct3D object, extreme performance penalties will be incurred because they share the same hardware.</span></span>

<span data-ttu-id="f536c-107">Tout d’abord, initialisez les valeurs de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) utilisée pour créer le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f536c-107">First, initialize values for the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure that is used to create the Direct3D device.</span></span> <span data-ttu-id="f536c-108">L’exemple de code suivant spécifie une application avec fenêtres dans laquelle la mémoire tampon d’arrière-plan est copiée dans la mémoire tampon d’origine pendant une opération de synchronisation verticale uniquement.</span><span class="sxs-lookup"><span data-stu-id="f536c-108">The following code example specifies a windowed application where the back buffer is copied to the front buffer during a vertical sync operation only.</span></span>


```
LPDIRECT3DDEVICE9 pDevice = NULL;

D3DPRESENT_PARAMETERS d3dpp; 

ZeroMemory( &d3dpp, sizeof(d3dpp) );
d3dpp.Windowed   = TRUE;
d3dpp.SwapEffect = D3DSWAPEFFECT_COPY;
```



<span data-ttu-id="f536c-109">Ensuite, créez le périphérique Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f536c-109">Next, create the Direct3D device.</span></span> <span data-ttu-id="f536c-110">L’appel de [**IDirect3D9 :: CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) suivant spécifie l’adaptateur par défaut, un périphérique de couche d’abstraction matérielle (HAL) et le traitement du vertex logiciel.</span><span class="sxs-lookup"><span data-stu-id="f536c-110">The following [**IDirect3D9::CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call specifies the default adapter, a hardware abstraction layer (HAL) device, and software vertex processing.</span></span>


```
if( FAILED( g_pD3D->CreateDevice( D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                                    &d3dpp, &d3dDevice ) ) )
    return E_FAIL;
```



<span data-ttu-id="f536c-111">Notez qu’un appel pour créer, mettre à jour ou réinitialiser l’appareil doit se produire uniquement sur le même thread que la procédure de fenêtre de la fenêtre de focus.</span><span class="sxs-lookup"><span data-stu-id="f536c-111">Note that a call to create, release, or reset the device should happen only on the same thread as the window procedure of the focus window.</span></span>

<span data-ttu-id="f536c-112">Après avoir créé l’appareil, définissez son état.</span><span class="sxs-lookup"><span data-stu-id="f536c-112">After creating the device, set its state.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f536c-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f536c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f536c-114">Périphériques Direct3D</span><span class="sxs-lookup"><span data-stu-id="f536c-114">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
