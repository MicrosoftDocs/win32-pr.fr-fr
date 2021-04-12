---
description: Les applications Direct3D peuvent obtenir de nombreux effets spéciaux en appliquant différentes textures à une primitive au cours de plusieurs passes de rendu.
ms.assetid: 884cc928-305e-46b9-acbf-ca58dfbc05e6
title: Fusion de texture multipasse (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0a042088694f686003a6dc259cf1d914db2b59
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109150"
---
# <a name="multipass-texture-blending-direct3d-9"></a><span data-ttu-id="98a0f-103">Fusion de texture multipasse (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="98a0f-103">Multipass Texture Blending (Direct3D 9)</span></span>

<span data-ttu-id="98a0f-104">Les applications Direct3D peuvent obtenir de nombreux effets spéciaux en appliquant différentes textures à une primitive au cours de plusieurs passes de rendu.</span><span class="sxs-lookup"><span data-stu-id="98a0f-104">Direct3D applications can achieve numerous special effects by applying various textures to a primitive over the course of multiple rendering passes.</span></span> <span data-ttu-id="98a0f-105">Le terme courant pour cela est la fusion de texture multipasse.</span><span class="sxs-lookup"><span data-stu-id="98a0f-105">The common term for this is multipass texture blending.</span></span> <span data-ttu-id="98a0f-106">Une utilisation classique de la fusion de texture multipasse consiste à émuler les effets des modèles d’éclairage et d’ombrage complexes en appliquant plusieurs couleurs à partir de différentes textures.</span><span class="sxs-lookup"><span data-stu-id="98a0f-106">A typical use for multipass texture blending is to emulate the effects of complex lighting and shading models by applying multiple colors from several different textures.</span></span> <span data-ttu-id="98a0f-107">Une telle application est appelée « mappage clair ».</span><span class="sxs-lookup"><span data-stu-id="98a0f-107">One such application is called light mapping.</span></span> <span data-ttu-id="98a0f-108">Pour plus d’informations, consultez [mappage de lumière avec des textures (Direct3D 9)](light-mapping-with-textures.md).</span><span class="sxs-lookup"><span data-stu-id="98a0f-108">For more information, see [Light Mapping with Textures (Direct3D 9)](light-mapping-with-textures.md).</span></span>

> [!Note]  
> <span data-ttu-id="98a0f-109">Certains appareils peuvent appliquer plusieurs textures à des primitives en une seule passe.</span><span class="sxs-lookup"><span data-stu-id="98a0f-109">Some devices are capable of applying multiple textures to primitives in a single pass.</span></span> <span data-ttu-id="98a0f-110">Pour plus d’informations, consultez [fusion de textures (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="98a0f-110">For details, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span>

 

<span data-ttu-id="98a0f-111">Si le matériel de l’utilisateur ne prend pas en charge la fusion de plusieurs textures, votre application peut utiliser la fusion de texture multipasse pour obtenir les mêmes effets visuels.</span><span class="sxs-lookup"><span data-stu-id="98a0f-111">If the user's hardware does not support multiple texture blending, your application can use multipass texture blending to achieve the same visual effects.</span></span> <span data-ttu-id="98a0f-112">Toutefois, l’application ne peut pas supporter les fréquences d’images possibles lors de l’utilisation de plusieurs fusions de texture.</span><span class="sxs-lookup"><span data-stu-id="98a0f-112">However, the application cannot sustain the frame rates that are possible when using multiple texture blending.</span></span>

<span data-ttu-id="98a0f-113">Pour effectuer une fusion de texture multipasse dans une application C/C++.</span><span class="sxs-lookup"><span data-stu-id="98a0f-113">To perform multipass texture blending in a C/C++ application.</span></span>

1.  <span data-ttu-id="98a0f-114">Définissez une texture dans l’étape de texture 0 en appelant la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) .</span><span class="sxs-lookup"><span data-stu-id="98a0f-114">Set a texture in texture stage 0 by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span>
2.  <span data-ttu-id="98a0f-115">Sélectionnez la couleur souhaitée et les arguments et opérations de fusion alpha à l’aide de la méthode [**IDirect3DDevice9 :: SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .</span><span class="sxs-lookup"><span data-stu-id="98a0f-115">Select the desired color and alpha blending arguments and operations with the [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) method.</span></span> <span data-ttu-id="98a0f-116">Les paramètres par défaut conviennent parfaitement pour la fusion de texture multipasse.</span><span class="sxs-lookup"><span data-stu-id="98a0f-116">The default settings are well-suited for multipass texture blending.</span></span>
3.  <span data-ttu-id="98a0f-117">Affichez les objets appropriés dans la scène.</span><span class="sxs-lookup"><span data-stu-id="98a0f-117">Render the appropriate objects in the scene.</span></span>
4.  <span data-ttu-id="98a0f-118">Définit la texture suivante dans l’étape de texture 0.</span><span class="sxs-lookup"><span data-stu-id="98a0f-118">Set the next texture in texture stage 0.</span></span>
5.  <span data-ttu-id="98a0f-119">Définissez les \_ États de rendu D3DRS SRCBLEND et D3DRS \_ DESTBLEND pour ajuster les facteurs de fusion source et de destination en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="98a0f-119">Set the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states to adjust the source and destination blending factors as needed.</span></span> <span data-ttu-id="98a0f-120">Le système fusionne les nouvelles textures avec les pixels existants dans la surface de cible de rendu en fonction de ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="98a0f-120">The system blends the new textures with the existing pixels in the render-target surface according to these parameters.</span></span>
6.  <span data-ttu-id="98a0f-121">Répétez les étapes 3, 4 et 5 avec autant de textures que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="98a0f-121">Repeat Steps 3, 4, and 5 with as many textures as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98a0f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="98a0f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98a0f-123">Fusion de texture</span><span class="sxs-lookup"><span data-stu-id="98a0f-123">Texture Blending</span></span>](texture-blending.md)
</dt> </dl>

 

 
