---
title: Interface ID3DX11EffectConstantBuffer (D3dx11effect. h)
description: Une interface de mémoire tampon constante accède aux mémoires tampons constantes ou aux mémoires tampons de texture.
ms.assetid: 2106cb51-dc0a-4ab6-adb6-2deb06922af1
keywords:
- Interface ID3DX11EffectConstantBuffer Direct3D 11
- Interface ID3DX11EffectConstantBuffer Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11EffectConstantBuffer
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfea2e8e67af30075990d6643b10bb86cf3021ae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323078"
---
# <a name="id3dx11effectconstantbuffer-interface"></a><span data-ttu-id="a3f8f-105">Interface ID3DX11EffectConstantBuffer</span><span class="sxs-lookup"><span data-stu-id="a3f8f-105">ID3DX11EffectConstantBuffer interface</span></span>

<span data-ttu-id="a3f8f-106">Une interface de mémoire tampon constante accède aux mémoires tampons constantes ou aux mémoires tampons de texture.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-106">A constant-buffer interface accesses constant buffers or texture buffers.</span></span>

## <a name="members"></a><span data-ttu-id="a3f8f-107">Membres</span><span class="sxs-lookup"><span data-stu-id="a3f8f-107">Members</span></span>

<span data-ttu-id="a3f8f-108">L’interface **ID3DX11EffectConstantBuffer** hérite de [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="a3f8f-108">The **ID3DX11EffectConstantBuffer** interface inherits from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span> <span data-ttu-id="a3f8f-109">**ID3DX11EffectConstantBuffer** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="a3f8f-109">**ID3DX11EffectConstantBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="a3f8f-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3f8f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a3f8f-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="a3f8f-111">Methods</span></span>

<span data-ttu-id="a3f8f-112">L’interface **ID3DX11EffectConstantBuffer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-112">The **ID3DX11EffectConstantBuffer** interface has these methods.</span></span>



| <span data-ttu-id="a3f8f-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="a3f8f-113">Method</span></span>                                                                             | <span data-ttu-id="a3f8f-114">Description</span><span class="sxs-lookup"><span data-stu-id="a3f8f-114">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------|:-----------------------------------------------------|
| [<span data-ttu-id="a3f8f-115">**GetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-115">**GetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-getconstantbuffer.md)         | <span data-ttu-id="a3f8f-116">Obtient une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-116">Get a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="a3f8f-117">**GetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-117">**GetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-gettexturebuffer.md)           | <span data-ttu-id="a3f8f-118">Obtenir une mémoire tampon de texture.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-118">Get a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="a3f8f-119">**SetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-119">**SetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-setconstantbuffer.md)         | <span data-ttu-id="a3f8f-120">Définissez une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-120">Set a constant-buffer.</span></span><br/>                    |
| [<span data-ttu-id="a3f8f-121">**SetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-121">**SetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-settexturebuffer.md)           | <span data-ttu-id="a3f8f-122">Définissez une texture-buffer.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-122">Set a texture-buffer.</span></span><br/>                     |
| [<span data-ttu-id="a3f8f-123">**UndoSetConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-123">**UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md) | <span data-ttu-id="a3f8f-124">Restaure une mémoire tampon constante définie précédemment.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-124">Reverts a previously set constant buffer.</span></span><br/> |
| [<span data-ttu-id="a3f8f-125">**UndoSetTextureBuffer**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-125">**UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)   | <span data-ttu-id="a3f8f-126">Restaure une mémoire tampon de texture précédemment définie.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-126">Reverts a previously set texture buffer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="a3f8f-127">Notes</span><span class="sxs-lookup"><span data-stu-id="a3f8f-127">Remarks</span></span>

<span data-ttu-id="a3f8f-128">Utilisez des mémoires tampons constantes pour stocker de nombreuses constantes d’effet ; regroupement de constantes dans des tampons en fonction de leur fréquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-128">Use constant buffers to store many effect constants; grouping constants into buffers based on their frequency of update.</span></span> <span data-ttu-id="a3f8f-129">Cela vous permet de réduire le nombre de modifications d’État et d’effectuer le moins d’appels d’API pour modifier l’État.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-129">This allows you to minimize the number of state changes as well as make the fewest API calls to change state.</span></span> <span data-ttu-id="a3f8f-130">Ces deux facteurs conduisent à de meilleures performances.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-130">Both of these factors lead to better performance.</span></span>

> [!Note]  
> <span data-ttu-id="a3f8f-131">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-131">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="a3f8f-132">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="a3f8f-132">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="a3f8f-133">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="a3f8f-133">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a3f8f-134">Spécifications</span><span class="sxs-lookup"><span data-stu-id="a3f8f-134">Requirements</span></span>



| <span data-ttu-id="a3f8f-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a3f8f-135">Requirement</span></span> | <span data-ttu-id="a3f8f-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="a3f8f-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3f8f-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="a3f8f-137">Header</span></span><br/>  | <dl> <span data-ttu-id="a3f8f-138"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3f8f-138"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="a3f8f-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a3f8f-139">Library</span></span><br/> | <dl> <span data-ttu-id="a3f8f-140"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="a3f8f-140"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3f8f-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a3f8f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3f8f-142">**ID3DX11EffectVariable**</span><span class="sxs-lookup"><span data-stu-id="a3f8f-142">**ID3DX11EffectVariable**</span></span>](id3dx11effectvariable.md)
</dt> <dt>

[<span data-ttu-id="a3f8f-143">Effets 11 interfaces</span><span class="sxs-lookup"><span data-stu-id="a3f8f-143">Effects 11 Interfaces</span></span>](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[<span data-ttu-id="a3f8f-144">Interfaces D3DX</span><span class="sxs-lookup"><span data-stu-id="a3f8f-144">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





