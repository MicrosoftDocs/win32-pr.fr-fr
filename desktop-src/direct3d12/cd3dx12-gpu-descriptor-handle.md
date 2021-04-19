---
title: Structure CD3DX12_GPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Structure d’assistance pour faciliter l’initialisation d’une \_ structure de handle de \_ descripteur GPU D3D12 \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- Structure CD3DX12_GPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106537241"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a><span data-ttu-id="e2b0d-104">\_Structure du \_ handle du descripteur GPU CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="e2b0d-104">CD3DX12\_GPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="e2b0d-105">Structure d’assistance pour faciliter l’initialisation d’une structure de [**\_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-105">A helper structure to enable easy initialization of a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2b0d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2b0d-106">Syntax</span></span>


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="e2b0d-107">Membres</span><span class="sxs-lookup"><span data-stu-id="e2b0d-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="e2b0d-108">**\_ \_ Handle de descripteur GPU CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-108">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-109">Crée une nouvelle instance non initialisée d’un \_ \_ handle de descripteur GPU CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-109">Creates a new, uninitialized, instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-110">**\_ \_ handle de descripteur GPU CD3DX12 explicite \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-110">**explicit CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-111">Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-111">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-112">**\_Handle du \_ descripteur GPU CD3DX12 \_ (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-112">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-113">Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , initialisée avec les paramètres par défaut (définit le pointeur sur zéro).</span><span class="sxs-lookup"><span data-stu-id="e2b0d-113">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (sets the pointer to zero).</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-114">**\_ \_ Handle de descripteur GPU CD3DX12 \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &autre, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-114">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-115">Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-115">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="e2b0d-116">\_Handle du \_ descripteur GPU D3D12 \_ &autre</span><span class="sxs-lookup"><span data-stu-id="e2b0d-116">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="e2b0d-117">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-118">**\_ \_ Handle de descripteur GPU CD3DX12 \_ ( \_ handle de descripteur gpu const D3D12 \_ \_ &autre, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-118">**CD3DX12\_GPU\_DESCRIPTOR\_HANDLE(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-119">Crée une nouvelle instance d’un \_ handle de \_ descripteur GPU CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-119">Creates a new instance of a CD3DX12\_GPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="e2b0d-120">\_Handle du \_ descripteur GPU D3D12 \_ &autre</span><span class="sxs-lookup"><span data-stu-id="e2b0d-120">D3D12\_GPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="e2b0d-121">INT offsetInDescriptors : nombre de descripteurs par incrément.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="e2b0d-122">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-124">Définit le décalage en fonction du nombre spécifié de descripteurs et de la quantité d’incrémentation pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="e2b0d-125">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-125">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-126">INT offsetInDescriptors : nombre de descripteurs par incrément.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="e2b0d-127">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-129">Définit le décalage en fonction du nombre d’incréments spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="e2b0d-130">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-130">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-131">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-132">**opérateur inline = = ( \_ dans le \_ handle de \_ descripteur de GPU const D3D12 \_ \_& autre) const**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-132">**inline operator==( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-133">Teste l’égalité entre le \_ handle du descripteur GPU CD3DX12 actuel et le handle du descripteur GPU D3D12 ou le handle du descripteur GPU \_ \_ \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-133">Tests for equality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-134">**opérateur inline ! = ( \_ dans le \_ handle de \_ descripteur GPU const D3D12 \_ \_& autre) const**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-134">**inline operator!=( \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-135">Vérifie l’inégalité entre le handle du \_ descripteur GPU CD3DX12 actuel et le handle du descripteur GPU D3D12 ou le handle du descripteur GPU \_ \_ \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-135">Tests for inequality between the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-136">**Operator = (D3D12 \_ \_ &handle du descripteur GPU const \_ )**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-136">**operator=(const D3D12\_GPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-137">Définit le handle du \_ \_ descripteur GPU CD3DX12 actuel \_ sur les mêmes valeurs que le handle du descripteur GPU D3D12 \_ ou le \_ \_ \_ \_ \_ handle du descripteur GPU CD3DX12 spécifié.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-137">Sets the current CD3DX12\_GPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_GPU\_DESCRIPTOR\_HANDLE or CD3DX12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-138">**Inline InitOffsetted ( \_ dans le \_ handle du \_ descripteur GPU const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-138">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-139">Initialise une structure [**de \_ \_ \_ handle de descripteur GPU D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) avec le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-139">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="e2b0d-140">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-140">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-141">\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-141">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="e2b0d-142">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-143">**Inline InitOffsetted ( \_ dans le \_ handle du \_ descripteur GPU const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-143">**inline InitOffsetted(\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-144">Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-144">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="e2b0d-145">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-145">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-146">\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-146">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="e2b0d-147">INT offsetInDescriptors : nombre de descripteurs par lequel décaler.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="e2b0d-148">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-149">**handle \_ \_ \_ de descripteur InitOffsetted (out D3D12 \_ descripteur &de descripteur, handle \_ de de&scripteur \_ de \_ \_ \_ \_ graphique**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-149">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-150">Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-150">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="e2b0d-151">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-151">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-152">\_\_D3D12 handle \_ \_ du descripteur GPU \_ de sortie de la gestion des & : génère le \_ handle du \_ descripteur GPU D3D12 résultant \_ .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-152">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="e2b0d-153">\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-153">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="e2b0d-154">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="e2b0d-155">**static Inline InitOffsetted ( \_ \_ \_ \_ descripteur de descripteur GPU out D3D12 \_ &handle, \_ dans le \_ handle de \_ descripteur GPU const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-155">**static inline InitOffsetted(\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="e2b0d-156">Initialise une structure [**de \_ \_ \_ handle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) de descripteur GPU D3D12 avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-156">Initializes a [**D3D12\_GPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="e2b0d-157">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="e2b0d-157">Uses the following parameters:</span></span>

<span data-ttu-id="e2b0d-158">\_\_D3D12 handle \_ \_ du descripteur GPU \_ de sortie de la gestion des & : génère le \_ handle du \_ descripteur GPU D3D12 résultant \_ .</span><span class="sxs-lookup"><span data-stu-id="e2b0d-158">\_Out\_ D3D12\_GPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_GPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="e2b0d-159">\_Dans \_ \_ \_ le handle de descripteur GPU const D3D12 \_ &base : adresse de base à partir de laquelle l’offset doit être décalé.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-159">\_In\_ const D3D12\_GPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="e2b0d-160">INT offsetInDescriptors : nombre de descripteurs par lequel décaler.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="e2b0d-161">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="e2b0d-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e2b0d-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2b0d-162">Requirements</span></span>



| <span data-ttu-id="e2b0d-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2b0d-163">Requirement</span></span> | <span data-ttu-id="e2b0d-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2b0d-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e2b0d-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="e2b0d-165">Header</span></span><br/> | <dl> <span data-ttu-id="e2b0d-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="e2b0d-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2b0d-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e2b0d-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2b0d-168">**\_Handle du \_ descripteur GPU D3D12 \_**</span><span class="sxs-lookup"><span data-stu-id="e2b0d-168">**D3D12\_GPU\_DESCRIPTOR\_HANDLE**</span></span>](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[<span data-ttu-id="e2b0d-169">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="e2b0d-169">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





