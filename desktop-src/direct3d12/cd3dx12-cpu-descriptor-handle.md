---
title: Structure CD3DX12_CPU_DESCRIPTOR_HANDLE (D3dx12. h)
description: Structure d’assistance pour permettre l’initialisation simple d’une structure de \_ \_ handle de descripteur de processeur D3D12 \_ .
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- Structure CD3DX12_CPU_DESCRIPTOR_HANDLE
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d1045202c531aa200745fc89ed067628a175486
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545266"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a><span data-ttu-id="8aea6-104">\_Structure de \_ handle de descripteur de processeur CD3DX12 \_</span><span class="sxs-lookup"><span data-stu-id="8aea6-104">CD3DX12\_CPU\_DESCRIPTOR\_HANDLE structure</span></span>

<span data-ttu-id="8aea6-105">Structure d’assistance pour permettre l’initialisation simple d’une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="8aea6-105">A helper structure to enable easy initialization of a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aea6-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8aea6-106">Syntax</span></span>


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a><span data-ttu-id="8aea6-107">Membres</span><span class="sxs-lookup"><span data-stu-id="8aea6-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="8aea6-108">**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ()**</span><span class="sxs-lookup"><span data-stu-id="8aea6-108">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE()**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-109">Crée une nouvelle instance non initialisée d’un \_ \_ handle de descripteur de processeur CD3DX12 \_ .</span><span class="sxs-lookup"><span data-stu-id="8aea6-109">Creates a new, uninitialized, instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-110">**\_ \_ handle de descripteur de processeur CD3DX12 explicite \_ ( \_ handle de descripteur d’uc const D3D12 \_ \_ &o)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-110">**explicit CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &o)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-111">Crée une nouvelle instance d’un \_ handle de \_ descripteur de processeur CD3DX12 \_ , initialisée avec le contenu d’une autre structure de [**\_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) .</span><span class="sxs-lookup"><span data-stu-id="8aea6-111">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with the contents of another [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-112">**\_ \_ Handle de descripteur de processeur CD3DX12 \_ (CD3DX12 \_ par défaut)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-112">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(CD3DX12\_DEFAULT)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-113">Crée une nouvelle instance d’un \_ handle de \_ descripteur de processeur CD3DX12 \_ , initialisée avec les paramètres par défaut (pointeur défini sur zéro).</span><span class="sxs-lookup"><span data-stu-id="8aea6-113">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initialized with default parameters (pointer set to zero).</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-114">**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ handle de descripteur de processeur const D3D12 \_ \_ &autre, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-114">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-115">Crée une nouvelle instance d’un \_ handle de \_ descripteur d’UC CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-115">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="8aea6-116">\_Handle de \_ descripteur de processeur D3D12 \_ &autre</span><span class="sxs-lookup"><span data-stu-id="8aea6-116">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="8aea6-117">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-117">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-118">**\_ \_ Handle de descripteur de processeur CD3DX12 \_ ( \_ handle de descripteur de processeur const D3D12 \_ \_ &autre, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-118">**CD3DX12\_CPU\_DESCRIPTOR\_HANDLE(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-119">Crée une nouvelle instance d’un \_ handle de \_ descripteur d’UC CD3DX12 \_ , en initialisant les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-119">Creates a new instance of a CD3DX12\_CPU\_DESCRIPTOR\_HANDLE, initializing the following parameters:</span></span>

<span data-ttu-id="8aea6-120">\_Handle de \_ descripteur de processeur D3D12 \_ &autre</span><span class="sxs-lookup"><span data-stu-id="8aea6-120">D3D12\_CPU\_DESCRIPTOR\_HANDLE &other</span></span>

<span data-ttu-id="8aea6-121">INT offsetInDescriptors : nombre de descripteurs par incrément.</span><span class="sxs-lookup"><span data-stu-id="8aea6-121">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="8aea6-122">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-122">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-123">**Offset (INT offsetInDescriptors, UINT descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-123">**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-124">Définit le décalage en fonction du nombre spécifié de descripteurs et de la quantité d’incrémentation pour chaque descripteur.</span><span class="sxs-lookup"><span data-stu-id="8aea6-124">Sets the offset based on the specified number of descriptors and how much to increment for each descriptor.</span></span> <span data-ttu-id="8aea6-125">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-125">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-126">INT offsetInDescriptors : nombre de descripteurs par incrément.</span><span class="sxs-lookup"><span data-stu-id="8aea6-126">INT offsetInDescriptors: The number of descriptors by which to increment.</span></span>

<span data-ttu-id="8aea6-127">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-127">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-128">**Offset (INT offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-128">**Offset(INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-129">Définit le décalage en fonction du nombre d’incréments spécifié.</span><span class="sxs-lookup"><span data-stu-id="8aea6-129">Sets the offset based on the specified number of increments.</span></span> <span data-ttu-id="8aea6-130">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-130">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-131">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-131">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-132">**opérateur = = ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_& autre) const**</span><span class="sxs-lookup"><span data-stu-id="8aea6-132">**operator==( \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-133">Teste l’égalité entre le handle de descripteur de processeur CD3DX12 actuel et le handle de descripteur de processeur D3D12 ou le handle de descripteur \_ \_ \_ de processeur \_ CD3DX12 spécifié \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8aea6-133">Tests for equality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-134">**opérateur ! = ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_& autre) const**</span><span class="sxs-lookup"><span data-stu-id="8aea6-134">**operator!=(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE& other) const**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-135">Vérifie l’inégalité entre le handle du descripteur d’UC CD3DX12 actuel et le handle de descripteur d’UC D3D12 ou le handle de descripteur \_ \_ \_ \_ \_ \_ de processeur CD3DX12 spécifié \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8aea6-135">Tests for inequality between the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE and the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-136">**opérateur = (const D3D12 \_ \_ handle de descripteur d’UC \_ &autre)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-136">**operator=(const D3D12\_CPU\_DESCRIPTOR\_HANDLE &other)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-137">Définit le \_ \_ handle de descripteur de processeur CD3DX12 actuel \_ sur les mêmes valeurs que le handle de \_ \_ descripteur de processeur D3D12 \_ ou le \_ \_ \_ handle de descripteur de processeur CD3DX12 spécifié.</span><span class="sxs-lookup"><span data-stu-id="8aea6-137">Sets the current CD3DX12\_CPU\_DESCRIPTOR\_HANDLE to the same values as the specified D3D12\_CPU\_DESCRIPTOR\_HANDLE or CD3DX12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-138">**Inline InitOffsetted ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-138">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-139">Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec le nombre spécifié d’éléments.</span><span class="sxs-lookup"><span data-stu-id="8aea6-139">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with the specified number of items.</span></span> <span data-ttu-id="8aea6-140">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-140">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-141">\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.</span><span class="sxs-lookup"><span data-stu-id="8aea6-141">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="8aea6-142">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-142">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-143">**Inline InitOffsetted ( \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-143">**inline InitOffsetted(\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-144">Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="8aea6-144">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="8aea6-145">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-145">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-146">\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.</span><span class="sxs-lookup"><span data-stu-id="8aea6-146">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="8aea6-147">INT offsetInDescriptors : nombre de descripteurs par lequel décaler.</span><span class="sxs-lookup"><span data-stu-id="8aea6-147">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="8aea6-148">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-148">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-149">**handle \_ \_ \_ \_ de de&scripteur InitOffsetted (out D3D12 descripteur de descripteur inline \_ ) statique, dans le handle \_ de \_ \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetScaledByIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-149">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetScaledByIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-150">Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="8aea6-150">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="8aea6-151">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-151">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-152">\_\_DeD3D12 \_ \_ de&scripteur de descripteur de processeur out handle \_ : génère le \_ handle de descripteur d’UC D3D12 résultant \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8aea6-152">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="8aea6-153">\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.</span><span class="sxs-lookup"><span data-stu-id="8aea6-153">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="8aea6-154">INT offsetScaledByIncrementSize : nombre d’incréments de décalage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-154">INT offsetScaledByIncrementSize: The number of increments by which to offset.</span></span>

</dd> <dt>

<span data-ttu-id="8aea6-155">**static Inline InitOffsetted ( \_ handle \_ \_ \_ de descripteur de processeur out D3D12 \_ &handle, \_ dans le \_ handle de \_ descripteur d’UC const D3D12 \_ \_ &base, int offsetInDescriptors, uint descriptorIncrementSize)**</span><span class="sxs-lookup"><span data-stu-id="8aea6-155">**static inline InitOffsetted(\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle, \_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**</span></span>
</dt> <dd>

<span data-ttu-id="8aea6-156">Initialise une structure [**de \_ \_ \_ handle de descripteur de processeur D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) avec un offset, à l’aide du nombre spécifié de descripteurs de la taille donnée.</span><span class="sxs-lookup"><span data-stu-id="8aea6-156">Initializes a [**D3D12\_CPU\_DESCRIPTOR\_HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) structure with an offset, using the specified number of descriptors of the given size.</span></span> <span data-ttu-id="8aea6-157">Utilise les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="8aea6-157">Uses the following parameters:</span></span>

<span data-ttu-id="8aea6-158">\_\_DeD3D12 \_ \_ de&scripteur de descripteur de processeur out handle \_ : génère le \_ handle de descripteur d’UC D3D12 résultant \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="8aea6-158">\_Out\_ D3D12\_CPU\_DESCRIPTOR\_HANDLE &handle: Outputs the resulting D3D12\_CPU\_DESCRIPTOR\_HANDLE.</span></span>

<span data-ttu-id="8aea6-159">\_Dans \_ \_ le handle de descripteur d’UC const D3D12 \_ \_ &base : adresse de base à partir de laquelle le décalage est pris.</span><span class="sxs-lookup"><span data-stu-id="8aea6-159">\_In\_ const D3D12\_CPU\_DESCRIPTOR\_HANDLE &base: The base address from which to offset.</span></span>

<span data-ttu-id="8aea6-160">INT offsetInDescriptors : nombre de descripteurs par lequel décaler.</span><span class="sxs-lookup"><span data-stu-id="8aea6-160">INT offsetInDescriptors: The number of descriptors by which to offset.</span></span>

<span data-ttu-id="8aea6-161">UINT descriptorIncrementSize : quantité par laquelle incrémenter pour chaque descripteur, y compris le remplissage.</span><span class="sxs-lookup"><span data-stu-id="8aea6-161">UINT descriptorIncrementSize: The amount by which to increment for each descriptor, including padding.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="8aea6-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8aea6-162">Requirements</span></span>



| <span data-ttu-id="8aea6-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8aea6-163">Requirement</span></span> | <span data-ttu-id="8aea6-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="8aea6-164">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8aea6-165">En-tête</span><span class="sxs-lookup"><span data-stu-id="8aea6-165">Header</span></span><br/> | <dl> <span data-ttu-id="8aea6-166"><dt>D3dx12. h</dt></span><span class="sxs-lookup"><span data-stu-id="8aea6-166"><dt>D3dx12.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aea6-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8aea6-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aea6-168">Structures d’assistance pour D3D12</span><span class="sxs-lookup"><span data-stu-id="8aea6-168">Helper Structures for D3D12</span></span>](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





