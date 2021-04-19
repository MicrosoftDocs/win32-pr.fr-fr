---
description: Un bloc d’État peut être utilisé pour capturer tous les États des appareils (Voir l’état des blocs d’État enregistrer et restaurer (Direct3D 9)).
ms.assetid: e14077e4-1453-4aa3-b2de-4d3a829a819a
title: Enregistrement de tous les États d’appareil avec un StateBlock (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bfdb4f9b3a9c1e33c2e8e7f50765f1656bd59e1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516556"
---
# <a name="saving-all-device-states-with-a-stateblock-direct3d-9"></a><span data-ttu-id="77ac7-103">Enregistrement de tous les États d’appareil avec un StateBlock (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="77ac7-103">Saving All Device States with a StateBlock (Direct3D 9)</span></span>

<span data-ttu-id="77ac7-104">Un bloc d’État peut être utilisé pour capturer tous les États des appareils (Voir l' [État des blocs d’État enregistrer et restaurer (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="77ac7-104">A state block can be used to capture all device states (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span> <span data-ttu-id="77ac7-105">Les éléments d’état suivants sont inclus dans l’état de l’appareil :</span><span class="sxs-lookup"><span data-stu-id="77ac7-105">The following state elements are included in the device state:</span></span>

-   <span data-ttu-id="77ac7-106">État du vertex (voir [enregistrement des États des vertex avec un StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="77ac7-106">Vertex state (see [Saving Vertex States With a StateBlock (Direct3D 9)](saving-vertex-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="77ac7-107">État de pixel (voir [enregistrement de l’état de Pixel avec un StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span><span class="sxs-lookup"><span data-stu-id="77ac7-107">Pixel state (see [Saving Pixel State With a StateBlock (Direct3D 9)](saving-pixel-states-with-a-stateblock.md)).</span></span>
-   <span data-ttu-id="77ac7-108">Chaque texture assignée à un échantillonneur.</span><span class="sxs-lookup"><span data-stu-id="77ac7-108">Each texture assigned to a sampler.</span></span>
-   <span data-ttu-id="77ac7-109">Chaque texture de vertex.</span><span class="sxs-lookup"><span data-stu-id="77ac7-109">Each vertex texture.</span></span>
-   <span data-ttu-id="77ac7-110">Chaque texture de mappage de déplacement.</span><span class="sxs-lookup"><span data-stu-id="77ac7-110">Each displacement map texture.</span></span>
-   <span data-ttu-id="77ac7-111">Palette de texture actuelle.</span><span class="sxs-lookup"><span data-stu-id="77ac7-111">The current texture palette.</span></span>
-   <span data-ttu-id="77ac7-112">Pour chaque flux de vertex : un pointeur vers la mémoire tampon de vertex, chaque argument de [**IDirect3DDevice9 :: SetStreamSource**](/windows/desktop/api)et le séparateur (le cas échéant) à partir de [**IDirect3DDevice9 :: SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span><span class="sxs-lookup"><span data-stu-id="77ac7-112">For each vertex stream: a pointer to the vertex buffer, each argument from [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api), and the divider (if any) from [**IDirect3DDevice9::SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq).</span></span>
-   <span data-ttu-id="77ac7-113">Pointeur vers la mémoire tampon d’index.</span><span class="sxs-lookup"><span data-stu-id="77ac7-113">A pointer to the index buffer.</span></span>
-   <span data-ttu-id="77ac7-114">La fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="77ac7-114">The viewport.</span></span>
-   <span data-ttu-id="77ac7-115">Rectangle de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="77ac7-115">The scissors rectangle.</span></span>
-   <span data-ttu-id="77ac7-116">Matrices universelles, de vue et de projection.</span><span class="sxs-lookup"><span data-stu-id="77ac7-116">The world, view, and projection matrices.</span></span>
-   <span data-ttu-id="77ac7-117">Transformations de texture.</span><span class="sxs-lookup"><span data-stu-id="77ac7-117">The texture transforms.</span></span>
-   <span data-ttu-id="77ac7-118">Plans de découpage (le cas échéant).</span><span class="sxs-lookup"><span data-stu-id="77ac7-118">The clipping planes (if any).</span></span>
-   <span data-ttu-id="77ac7-119">La matière actuelle.</span><span class="sxs-lookup"><span data-stu-id="77ac7-119">The current material.</span></span>

<span data-ttu-id="77ac7-120">Pour capturer tous les États d’appareil avec un bloc d’État, spécifiez D3DSBT \_ All lors de l’appel de [**IDirect3DDevice9 :: CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span><span class="sxs-lookup"><span data-stu-id="77ac7-120">To capture all device states with a state block, specify D3DSBT\_ALL when calling [**IDirect3DDevice9::CreateStateBlock**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).</span></span>

## <a name="related-topics"></a><span data-ttu-id="77ac7-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="77ac7-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="77ac7-122">État de l’enregistrement et de la restauration des blocs d’État</span><span class="sxs-lookup"><span data-stu-id="77ac7-122">State Blocks Save and Restore State</span></span>](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
