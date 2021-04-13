---
description: Décrit les paramètres de création d’un appareil.
ms.assetid: 7db5ef2b-6894-4113-b726-8b238bb4fb2f
title: Structure D3DDEVICE_CREATION_PARAMETERS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVICE_CREATION_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 72b2f35f1666ec2095c6ea8f5d5588dc7fd62f2c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322766"
---
# <a name="d3ddevice_creation_parameters-structure"></a><span data-ttu-id="086c8-103">Structure des paramètres de \_ création de D3DDEVICE \_</span><span class="sxs-lookup"><span data-stu-id="086c8-103">D3DDEVICE\_CREATION\_PARAMETERS structure</span></span>

<span data-ttu-id="086c8-104">Décrit les paramètres de création d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="086c8-104">Describes the creation parameters for a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="086c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="086c8-105">Syntax</span></span>


```C++
typedef struct D3DDEVICE_CREATION_PARAMETERS {
  UINT       AdapterOrdinal;
  D3DDEVTYPE DeviceType;
  HWND       hFocusWindow;
  DWORD      BehaviorFlags;
} D3DDEVICE_CREATION_PARAMETERS, *LPD3DDEVICE_CREATION_PARAMETERS;
```



## <a name="members"></a><span data-ttu-id="086c8-106">Membres</span><span class="sxs-lookup"><span data-stu-id="086c8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="086c8-107">**AdapterOrdinal**</span><span class="sxs-lookup"><span data-stu-id="086c8-107">**AdapterOrdinal**</span></span>
</dt> <dd>

<span data-ttu-id="086c8-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="086c8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="086c8-109">Nombre ordinal qui désigne l’adaptateur d’affichage.</span><span class="sxs-lookup"><span data-stu-id="086c8-109">Ordinal number that denotes the display adapter.</span></span> <span data-ttu-id="086c8-110">\_La valeur par défaut de D3DADAPTER est toujours la carte d’affichage principale.</span><span class="sxs-lookup"><span data-stu-id="086c8-110">D3DADAPTER\_DEFAULT is always the primary display adapter.</span></span> <span data-ttu-id="086c8-111">Utilisez cet ordinal comme paramètre d’adaptateur pour l’une des méthodes [**IDirect3D9**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="086c8-111">Use this ordinal as the Adapter parameter for any of the [**IDirect3D9**](/windows/desktop/api) methods.</span></span> <span data-ttu-id="086c8-112">Notez que les différentes instances d’objets Direct3D 9,0 peuvent utiliser des ordinaux différents.</span><span class="sxs-lookup"><span data-stu-id="086c8-112">Note that different instances of Direct3D 9.0 objects can use different ordinals.</span></span> <span data-ttu-id="086c8-113">Les adaptateurs peuvent entrer ou sortir un système lorsque les utilisateurs ajoutent ou suppriment des analyses d’un système à plusieurs écrans ou lorsqu’ils échangent à chaud un ordinateur portable.</span><span class="sxs-lookup"><span data-stu-id="086c8-113">Adapters can enter or leave a system when users, for example, add or remove monitors from a multiple-monitor system or when they hot-swap a laptop.</span></span> <span data-ttu-id="086c8-114">Par conséquent, utilisez cet ordinal uniquement dans une instance Direct3D 9,0 connue comme valide, c’est-à-dire, soit le Direct3D 9,0 qui a créé cette interface [**IDirect3DDevice9**](/windows/desktop/api) , soit le Direct3D 9,0 retourné par [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), comme il a été appelé via cette interface **IDirect3DDevice9** .</span><span class="sxs-lookup"><span data-stu-id="086c8-114">Consequently, use this ordinal only in a Direct3D 9.0 instance known to be valid, that is, either the Direct3D 9.0 that created this [**IDirect3DDevice9**](/windows/desktop/api) interface or the Direct3D 9.0 returned from [**GetDirect3D**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdirect3d), as called through this **IDirect3DDevice9** interface.</span></span>

</dd> <dt>

<span data-ttu-id="086c8-115">**DeviceType**</span><span class="sxs-lookup"><span data-stu-id="086c8-115">**DeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="086c8-116">Type : **[ **D3DDEVTYPE**](./d3ddevtype.md)**</span><span class="sxs-lookup"><span data-stu-id="086c8-116">Type: **[**D3DDEVTYPE**](./d3ddevtype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="086c8-117">Membre du type énuméré [**D3DDEVTYPE**](./d3ddevtype.md) .</span><span class="sxs-lookup"><span data-stu-id="086c8-117">Member of the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type.</span></span> <span data-ttu-id="086c8-118">Indique la quantité de fonctionnalités émulées pour cet appareil.</span><span class="sxs-lookup"><span data-stu-id="086c8-118">Denotes the amount of emulated functionality for this device.</span></span> <span data-ttu-id="086c8-119">La valeur de ce paramètre reflète la valeur passée à l’appel [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) qui a créé cet appareil.</span><span class="sxs-lookup"><span data-stu-id="086c8-119">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="086c8-120">**hFocusWindow**</span><span class="sxs-lookup"><span data-stu-id="086c8-120">**hFocusWindow**</span></span>
</dt> <dd>

<span data-ttu-id="086c8-121">Type : **[ **HWND**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="086c8-121">Type: **[**HWND**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="086c8-122">Handle de fenêtre auquel le focus appartient pour cet appareil Direct3D.</span><span class="sxs-lookup"><span data-stu-id="086c8-122">Window handle to which focus belongs for this Direct3D device.</span></span> <span data-ttu-id="086c8-123">La valeur de ce paramètre reflète la valeur passée à l’appel [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) qui a créé cet appareil.</span><span class="sxs-lookup"><span data-stu-id="086c8-123">The value of this parameter mirrors the value passed to the [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) call that created this device.</span></span>

</dd> <dt>

<span data-ttu-id="086c8-124">**BehaviorFlags**</span><span class="sxs-lookup"><span data-stu-id="086c8-124">**BehaviorFlags**</span></span>
</dt> <dd>

<span data-ttu-id="086c8-125">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="086c8-125">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="086c8-126">Combinaison d’une ou de plusieurs constantes [D3DCREATE](d3dcreate.md) qui contrôlent le comportement global de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="086c8-126">A combination of one or more [D3DCREATE](d3dcreate.md) constants that control global behavior of the device.</span></span> <span data-ttu-id="086c8-127">Ces constantes reflètent les constantes transmises à [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) lorsque l’appareil a été créé.</span><span class="sxs-lookup"><span data-stu-id="086c8-127">These constants mirror the constants passed to [**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice) when the device was created.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="086c8-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="086c8-128">Requirements</span></span>



| <span data-ttu-id="086c8-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="086c8-129">Requirement</span></span> | <span data-ttu-id="086c8-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="086c8-130">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="086c8-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="086c8-131">Header</span></span><br/> | <dl> <span data-ttu-id="086c8-132"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="086c8-132"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="086c8-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="086c8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="086c8-134">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="086c8-134">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="086c8-135">**GetCreationParameters**</span><span class="sxs-lookup"><span data-stu-id="086c8-135">**GetCreationParameters**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getcreationparameters)
</dt> <dt>

[<span data-ttu-id="086c8-136">**CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="086c8-136">**CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> </dl>

 

 
