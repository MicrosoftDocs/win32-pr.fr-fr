---
description: Définit les types d’appareils.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Énumération D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529603"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="da9c9-103">Énumération D3DDEVTYPE</span><span class="sxs-lookup"><span data-stu-id="da9c9-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="da9c9-104">Définit les types d’appareils.</span><span class="sxs-lookup"><span data-stu-id="da9c9-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="da9c9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="da9c9-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="da9c9-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="da9c9-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="da9c9-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_HAL D3DDEVTYPE**</span><span class="sxs-lookup"><span data-stu-id="da9c9-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="da9c9-108">Pixellisation matérielle.</span><span class="sxs-lookup"><span data-stu-id="da9c9-108">Hardware rasterization.</span></span> <span data-ttu-id="da9c9-109">L’ombrage est effectué avec des logiciels, du matériel ou des transformations et éclairages mixtes.</span><span class="sxs-lookup"><span data-stu-id="da9c9-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="da9c9-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE \_ NULLREF**</span><span class="sxs-lookup"><span data-stu-id="da9c9-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="da9c9-111">Initialisez Direct3D sur un ordinateur sur lequel aucune pixellisation matérielle ou de référence n’est disponible, et activez les ressources pour la création de contenu 3D.</span><span class="sxs-lookup"><span data-stu-id="da9c9-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="da9c9-112">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="da9c9-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da9c9-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ Ref**</span><span class="sxs-lookup"><span data-stu-id="da9c9-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="da9c9-114">Les fonctionnalités Direct3D sont implémentées dans le logiciel ; Toutefois, le rastériseur de référence utilise des instructions d’UC spéciales à chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="da9c9-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="da9c9-115">L’appareil de référence est installé par le SDK Windows 8,0 ou une version ultérieure et est conçu comme une aide au débogage uniquement pour le développement.</span><span class="sxs-lookup"><span data-stu-id="da9c9-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="da9c9-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="da9c9-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="da9c9-117">Un périphérique logiciel enfichable inscrit auprès de [**IDirect3D9 :: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span><span class="sxs-lookup"><span data-stu-id="da9c9-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="da9c9-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="da9c9-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="da9c9-119">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="da9c9-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="da9c9-120">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="da9c9-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="da9c9-121">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="da9c9-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da9c9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="da9c9-122">Remarks</span></span>

<span data-ttu-id="da9c9-123">Toutes les méthodes de l’interface [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) qui prennent un type d’appareil **D3DDEVTYPE** échouent si D3DDEVTYPE \_ NULLREF est spécifié.</span><span class="sxs-lookup"><span data-stu-id="da9c9-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="da9c9-124">Pour utiliser ces méthodes, remplacez D3DDEVTYPE \_ ref dans l’appel de méthode.</span><span class="sxs-lookup"><span data-stu-id="da9c9-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="da9c9-125">Un \_ appareil Ref D3DDEVTYPE doit être créé dans la \_ mémoire de travail D3DPOOL, sauf si des mémoires tampons de vertex et d’index sont requises.</span><span class="sxs-lookup"><span data-stu-id="da9c9-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="da9c9-126">Pour prendre en charge les mémoires tampons de vertex et d’index, créez l’appareil dans la \_ mémoire D3DPOOL SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="da9c9-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="da9c9-127">Si D3dref9.dll est installé, Direct3D utilise le rastériseur de référence pour créer un type d' \_ appareil Ref D3DDEVTYPE, même si D3DDEVTYPE \_ NULLREF est spécifié.</span><span class="sxs-lookup"><span data-stu-id="da9c9-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="da9c9-128">Si D3dref9.dll n’est pas disponible et que D3DDEVTYPE \_ NULLREF est spécifié, Direct3D ne rend ni ne présente la scène.</span><span class="sxs-lookup"><span data-stu-id="da9c9-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="da9c9-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da9c9-129">Requirements</span></span>



| <span data-ttu-id="da9c9-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da9c9-130">Requirement</span></span> | <span data-ttu-id="da9c9-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="da9c9-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da9c9-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="da9c9-132">Header</span></span><br/> | <dl> <span data-ttu-id="da9c9-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="da9c9-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da9c9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da9c9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da9c9-135">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="da9c9-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="da9c9-136">**IDirect3D9::CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="da9c9-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="da9c9-137">**IDirect3D9::CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="da9c9-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="da9c9-138">**IDirect3D9::CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="da9c9-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="da9c9-139">**IDirect3D9::CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="da9c9-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="da9c9-140">**IDirect3D9::GetDeviceCaps**</span><span class="sxs-lookup"><span data-stu-id="da9c9-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="da9c9-141">**\_Paramètres de création de D3DDEVICE \_**</span><span class="sxs-lookup"><span data-stu-id="da9c9-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
