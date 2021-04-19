---
description: Identifie les données de ressource.
ms.assetid: f2ace2ad-228f-4f76-ab31-16e045e09331
title: Structure D3DXF_FILELOADRESOURCE (D3dx9xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXF_FILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- d3dx9xof.h
ms.openlocfilehash: ee5dc27b551382a5fa5d1c7f4833c94b205e5521
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531540"
---
# <a name="d3dxf_fileloadresource-structure"></a><span data-ttu-id="e807f-103">D3DXF \_ FILELOADRESOURCE, structure</span><span class="sxs-lookup"><span data-stu-id="e807f-103">D3DXF\_FILELOADRESOURCE structure</span></span>

<span data-ttu-id="e807f-104">Identifie les données de ressource.</span><span class="sxs-lookup"><span data-stu-id="e807f-104">Identifies resource data.</span></span>

## <a name="syntax"></a><span data-ttu-id="e807f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e807f-105">Syntax</span></span>


```C++
typedef struct D3DXF_FILELOADRESOURCE {
  HMODULE hModule;
  LPCSTR  lpName;
  LPCSTR  lpType;
} D3DXF_FILELOADRESOURCE, *LPD3DXF_FILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="e807f-106">Membres</span><span class="sxs-lookup"><span data-stu-id="e807f-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="e807f-107">**hModule**</span><span class="sxs-lookup"><span data-stu-id="e807f-107">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="e807f-108">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e807f-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e807f-109">Handle du module contenant la ressource à charger.</span><span class="sxs-lookup"><span data-stu-id="e807f-109">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="e807f-110">Si ce membre a la **valeur null**, la ressource doit être attachée au fichier exécutable qui l’utilisera.</span><span class="sxs-lookup"><span data-stu-id="e807f-110">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="e807f-111">**lpName**</span><span class="sxs-lookup"><span data-stu-id="e807f-111">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="e807f-112">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e807f-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e807f-113">Pointeur vers une chaîne spécifiant le nom de la ressource à charger.</span><span class="sxs-lookup"><span data-stu-id="e807f-113">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="e807f-114">Par exemple, si la ressource est un maillage, ce membre doit spécifier le nom du fichier de maillage.</span><span class="sxs-lookup"><span data-stu-id="e807f-114">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="e807f-115">**lpType**</span><span class="sxs-lookup"><span data-stu-id="e807f-115">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="e807f-116">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e807f-116">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e807f-117">Pointeur vers une chaîne qui spécifie le type défini par l’utilisateur qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="e807f-117">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e807f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e807f-118">Remarks</span></span>

<span data-ttu-id="e807f-119">Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](id3dxfile--createenumobject.md) et spécifie l’indicateur [D3DXF \_ FILELOAD \_ FROMRESOURCE](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="e807f-119">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](id3dxfile--createenumobject.md) method and specifies the [D3DXF\_FILELOAD\_FROMRESOURCE](d3dxf.md) flag.</span></span>

## <a name="requirements"></a><span data-ttu-id="e807f-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e807f-120">Requirements</span></span>



| <span data-ttu-id="e807f-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e807f-121">Requirement</span></span> | <span data-ttu-id="e807f-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="e807f-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e807f-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="e807f-123">Header</span></span><br/> | <dl> <span data-ttu-id="e807f-124"><dt>D3dx9xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e807f-124"><dt>D3dx9xof.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e807f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e807f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e807f-126">Structures de fichiers D3DX X</span><span class="sxs-lookup"><span data-stu-id="e807f-126">D3DX X File Structures</span></span>](dx9-graphics-reference-d3dx-x-file-structures.md)
</dt> </dl>

 

 
