---
description: Identifie les données de ressource. Action déconseillée.
ms.assetid: acb379c7-ac80-412f-8891-d5917b3f8da4
title: DXFILELOADRESOURCE, structure (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXFILELOADRESOURCE
api_type:
- HeaderDef
api_location:
- DXFile.h
ms.openlocfilehash: 233fe6acb13a6ae654a714028a316d7d6f6871ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106541255"
---
# <a name="dxfileloadresource-structure"></a><span data-ttu-id="33d37-104">DXFILELOADRESOURCE, structure</span><span class="sxs-lookup"><span data-stu-id="33d37-104">DXFILELOADRESOURCE structure</span></span>

<span data-ttu-id="33d37-105">Identifie les données de ressource.</span><span class="sxs-lookup"><span data-stu-id="33d37-105">Identifies resource data.</span></span> <span data-ttu-id="33d37-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="33d37-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="33d37-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33d37-107">Syntax</span></span>


```C++
typedef struct DXFILELOADRESOURCE {
  HMODULE hModule;
  LPCTSTR lpName;
  LPCTSTR lpType;
} DXFILELOADRESOURCE, *LPDXFILELOADRESOURCE;
```



## <a name="members"></a><span data-ttu-id="33d37-108">Membres</span><span class="sxs-lookup"><span data-stu-id="33d37-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="33d37-109">**hModule**</span><span class="sxs-lookup"><span data-stu-id="33d37-109">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="33d37-110">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33d37-110">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33d37-111">Handle du module contenant la ressource à charger.</span><span class="sxs-lookup"><span data-stu-id="33d37-111">Handle of the module containing the resource to be loaded.</span></span> <span data-ttu-id="33d37-112">Si ce membre a la **valeur null**, la ressource doit être attachée au fichier exécutable qui l’utilisera.</span><span class="sxs-lookup"><span data-stu-id="33d37-112">If this member is **NULL**, the resource must be attached to the executable file that will use it.</span></span>

</dd> <dt>

<span data-ttu-id="33d37-113">**lpName**</span><span class="sxs-lookup"><span data-stu-id="33d37-113">**lpName**</span></span>
</dt> <dd>

<span data-ttu-id="33d37-114">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33d37-114">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33d37-115">Pointeur vers une chaîne spécifiant le nom de la ressource à charger.</span><span class="sxs-lookup"><span data-stu-id="33d37-115">Pointer to a string specifying the name of the resource to be loaded.</span></span> <span data-ttu-id="33d37-116">Par exemple, si la ressource est un maillage, ce membre doit spécifier le nom du fichier de maillage.</span><span class="sxs-lookup"><span data-stu-id="33d37-116">For example, if the resource is a mesh, this member should specify the name of the mesh file.</span></span>

</dd> <dt>

<span data-ttu-id="33d37-117">**lpType**</span><span class="sxs-lookup"><span data-stu-id="33d37-117">**lpType**</span></span>
</dt> <dd>

<span data-ttu-id="33d37-118">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="33d37-118">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="33d37-119">Pointeur vers une chaîne qui spécifie le type défini par l’utilisateur qui identifie la ressource.</span><span class="sxs-lookup"><span data-stu-id="33d37-119">Pointer to a string specifying the user-defined type identifying the resource.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33d37-120">Notes</span><span class="sxs-lookup"><span data-stu-id="33d37-120">Remarks</span></span>

<span data-ttu-id="33d37-121">Cette structure identifie une ressource à charger lorsqu’une application utilise la méthode [**CreateEnumObject**](idirectxfile--createenumobject.md) et spécifie DXFILELOAD \_ FROMRESOURCE.</span><span class="sxs-lookup"><span data-stu-id="33d37-121">This structure identifies a resource to be loaded when an application uses the [**CreateEnumObject**](idirectxfile--createenumobject.md) method and specifies DXFILELOAD\_FROMRESOURCE.</span></span>

## <a name="requirements"></a><span data-ttu-id="33d37-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="33d37-122">Requirements</span></span>



| <span data-ttu-id="33d37-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="33d37-123">Requirement</span></span> | <span data-ttu-id="33d37-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="33d37-124">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="33d37-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="33d37-125">Header</span></span><br/> | <dl> <span data-ttu-id="33d37-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="33d37-126"><dt>DXFile.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33d37-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="33d37-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33d37-128">Structures de fichiers X</span><span class="sxs-lookup"><span data-stu-id="33d37-128">X File Structures</span></span>](dx9-graphics-reference-x-file-structures.md)
</dt> <dt>

[<span data-ttu-id="33d37-129">**CreateEnumObject**</span><span class="sxs-lookup"><span data-stu-id="33d37-129">**CreateEnumObject**</span></span>](idirectxfile--createenumobject.md)
</dt> <dt>

[<span data-ttu-id="33d37-130">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="33d37-130">DXFILE Constants</span></span>](dxfile.md)
</dt> </dl>

 

 
