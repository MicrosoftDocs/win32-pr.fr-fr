---
description: Un bloc d’État est un groupe d’États de périphérique.
ms.assetid: 6b1917a8-8685-40c3-983d-6bd2fed95642
title: État de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c8f19d6409e0dc9c40f1d4c7711440a0dc09fe2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103949958"
---
# <a name="state-blocks-save-and-restore-state-direct3d-9"></a><span data-ttu-id="08cc9-103">État de l’enregistrement et de la restauration des blocs d’État (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08cc9-103">State Blocks Save and Restore State (Direct3D 9)</span></span>

<span data-ttu-id="08cc9-104">Un bloc d’État est un groupe d’États de périphérique.</span><span class="sxs-lookup"><span data-stu-id="08cc9-104">A state block is a group of device states.</span></span> <span data-ttu-id="08cc9-105">L’état de l’appareil est constitué de l’état de rendu, de l’état du vertex, de l’état du pixel ou de tous les éléments ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="08cc9-105">Device state is made up of render state, vertex state, pixel state, or all of the above.</span></span> <span data-ttu-id="08cc9-106">Un bloc d’état contient un instantané de l’état actuel d’un appareil, ou vous pouvez créer un bloc d’État qui enregistre chaque modification d’État apportée par votre application.</span><span class="sxs-lookup"><span data-stu-id="08cc9-106">A state block contains a snapshot of a device's current state, or you can create a state block that records each state change that your application makes.</span></span>

## <a name="capture-a-block-of-state"></a><span data-ttu-id="08cc9-107">Capturer un bloc d’État</span><span class="sxs-lookup"><span data-stu-id="08cc9-107">Capture a Block of State</span></span>

<span data-ttu-id="08cc9-108">Choisissez le type d’État que vous souhaitez capturer, puis créez un bloc d’État comme suit :</span><span class="sxs-lookup"><span data-stu-id="08cc9-108">Choose the type of state that you want to capture, and create a state block like this:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->CreateStateBlock( D3DSBT_ALL, &pStateBlock );
```



<span data-ttu-id="08cc9-109">[**IDirect3DDevice9 :: CreateStateBlock**](/windows/desktop/api) crée un bloc d’État et capture automatiquement l’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="08cc9-109">[**IDirect3DDevice9::CreateStateBlock**](/windows/desktop/api) creates a state block, and automatically captures the device state.</span></span> <span data-ttu-id="08cc9-110">L’état de l’appareil est spécifié par le type de bloc d’État dans le premier argument.</span><span class="sxs-lookup"><span data-stu-id="08cc9-110">The device state is specified by the state block type in the first argument.</span></span> <span data-ttu-id="08cc9-111">Cet État peut être l’un des suivants : tout l’état de l’appareil (voir [enregistrement de tous les États des appareils avec un StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), tout l’état des pixels (voir enregistrement de [l’état des pixels avec un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)) ou tous les États des vertex (voir [enregistrement des États des vertex avec un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="08cc9-111">This state can be one of the following: all device state (see [Saving All Device States with a StateBlock (Direct3D 9)](saving-all-device-states-with-a-stateblock.md)), all pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)), or all vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>

<span data-ttu-id="08cc9-112">Le système d’effet utilise un bloc d’État pour enregistrer l’État.</span><span class="sxs-lookup"><span data-stu-id="08cc9-112">The effect system uses a state block to save state.</span></span> <span data-ttu-id="08cc9-113">Après l’appel de [**ID3DXEffect :: Begin**](id3dxeffect--begin.md) , un bloc d’État est créé et l’État est capturé.</span><span class="sxs-lookup"><span data-stu-id="08cc9-113">After [**ID3DXEffect::Begin**](id3dxeffect--begin.md) is called, a state block is created and state is captured.</span></span> <span data-ttu-id="08cc9-114">Quand [**ID3DXEffect :: end**](id3dxeffect--end.md) est appelé, l’état du bloc d’État est réappliqué à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="08cc9-114">When [**ID3DXEffect::End**](id3dxeffect--end.md) is called, the state block state is reapplied to the device.</span></span>

## <a name="capture-individual-states"></a><span data-ttu-id="08cc9-115">Capturer des États individuels</span><span class="sxs-lookup"><span data-stu-id="08cc9-115">Capture Individual States</span></span>

<span data-ttu-id="08cc9-116">Pour enregistrer une séquence d’état personnalisée, encapsulez l’état que vous souhaitez enregistrer dans une paire [**IDirect3DDevice9 :: BeginStateBlock**](/windows/desktop/api) et [**IDirect3DDevice9 :: EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) .</span><span class="sxs-lookup"><span data-stu-id="08cc9-116">To save a custom state sequence, wrap the state that you want to save in a [**IDirect3DDevice9::BeginStateBlock**](/windows/desktop/api) and [**IDirect3DDevice9::EndStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endstateblock) pair.</span></span> <span data-ttu-id="08cc9-117">BeginStateBlock indique à l’appareil actuel de configurer un bloc d’État et de l’ajouter à chaque modification d’État qui se produit jusqu’à l’appel de EndStateBlock.</span><span class="sxs-lookup"><span data-stu-id="08cc9-117">BeginStateBlock tells the current device to set up a state block and add to it every state change that occurs until EndStateBlock is called.</span></span> <span data-ttu-id="08cc9-118">Voici un exemple :</span><span class="sxs-lookup"><span data-stu-id="08cc9-118">Here's an example:</span></span>


```
IDirect3DStateBlock9* pStateBlock = NULL;
pd3dDevice->BeginStateBlock();
pd3dDevice->SetRenderState ( D3DRS_ZENABLE, true );
pd3dDevice->EndStateBlock( &pStateBlock );
```



<span data-ttu-id="08cc9-119">Cela permet d’enregistrer un nombre quelconque de modifications d’état d’une séquence dans un stateblock personnalisé.</span><span class="sxs-lookup"><span data-stu-id="08cc9-119">This will save any number of state changes in any sequence to a custom stateblock.</span></span> <span data-ttu-id="08cc9-120">Plus tard, lorsque vous souhaitez utiliser le stateblock pour réinitialiser l’état de l’appareil, appelez [**IDirect3DStateBlock9 :: apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span><span class="sxs-lookup"><span data-stu-id="08cc9-120">Later, when you want to use the stateblock to reset the device state, call [**IDirect3DStateBlock9::Apply**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dstateblock9-apply).</span></span> <span data-ttu-id="08cc9-121">Cela remplacera uniquement l’état de l’appareil qui a été capturé dans le bloc d’État.</span><span class="sxs-lookup"><span data-stu-id="08cc9-121">This will overwrite only the device state that has been captured in the state block.</span></span> <span data-ttu-id="08cc9-122">Tout autre État d’appareil qui n’a pas été capturé avec le stateblock personnalisé n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="08cc9-122">Any other device state that was not captured with the custom stateblock will not be changed.</span></span> <span data-ttu-id="08cc9-123">Là encore, étant donné que l’objet stateblock est une interface, vous devez le libérer une fois que vous avez fini de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="08cc9-123">Once again, since the stateblock object is an interface, you will need to release it when you are done with it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08cc9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08cc9-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08cc9-125">États (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="08cc9-125">States (Direct3D 9)</span></span>](states.md)
</dt> </dl>

 

 
