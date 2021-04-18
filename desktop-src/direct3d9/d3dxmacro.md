---
description: Décrit les définitions de préprocesseur utilisées par un objet Effect.
ms.assetid: 43413b79-e331-4466-b288-bd4439c135a2
title: D3DXMACRO, structure (D3dx9shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMACRO
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 7fd6c52b94c3fb6f36c9b3a8e2b4b513fb8903f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106525904"
---
# <a name="d3dxmacro-structure"></a><span data-ttu-id="2493e-103">D3DXMACRO, structure</span><span class="sxs-lookup"><span data-stu-id="2493e-103">D3DXMACRO structure</span></span>

<span data-ttu-id="2493e-104">Décrit les définitions de préprocesseur utilisées par un objet Effect.</span><span class="sxs-lookup"><span data-stu-id="2493e-104">Describes preprocessor definitions used by an effect object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2493e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2493e-105">Syntax</span></span>


```C++
typedef struct D3DXMACRO {
  LPCSTR Name;
  LPCSTR Definition;
} D3DXMACRO, *LPD3DXMACRO;
```



## <a name="members"></a><span data-ttu-id="2493e-106">Membres</span><span class="sxs-lookup"><span data-stu-id="2493e-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="2493e-107">**Nom**</span><span class="sxs-lookup"><span data-stu-id="2493e-107">**Name**</span></span>
</dt> <dd>

<span data-ttu-id="2493e-108">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2493e-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2493e-109">Nom du préprocesseur.</span><span class="sxs-lookup"><span data-stu-id="2493e-109">Preprocessor name.</span></span>

</dd> <dt>

<span data-ttu-id="2493e-110">**Définition**</span><span class="sxs-lookup"><span data-stu-id="2493e-110">**Definition**</span></span>
</dt> <dd>

<span data-ttu-id="2493e-111">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2493e-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="2493e-112">Nom de la définition.</span><span class="sxs-lookup"><span data-stu-id="2493e-112">Definition name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2493e-113">Notes</span><span class="sxs-lookup"><span data-stu-id="2493e-113">Remarks</span></span>

<span data-ttu-id="2493e-114">Pour utiliser **D3DXMACRO** sur plusieurs lignes, préfixez chaque caractère de nouvelle ligne avec une barre oblique inverse (par exemple, une \# définition dans le langage C).</span><span class="sxs-lookup"><span data-stu-id="2493e-114">To use **D3DXMACRO** s in more than one line, prefix each new line character with a backslash (like a \#define in the C language).</span></span> <span data-ttu-id="2493e-115">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="2493e-115">For example:</span></span>


```
sample=
macro.Name = "DO_CODE_BLOCK";
macro.Definition =
    "/* here is a block of code */\\\n"
    "{ do something ... }\\\n";
```



<span data-ttu-id="2493e-116">Notez les 3 barres obliques inverses à la fin de la ligne.</span><span class="sxs-lookup"><span data-stu-id="2493e-116">Notice the 3 backslash characters at the end of the line.</span></span> <span data-ttu-id="2493e-117">Les deux premières sont requises pour générer un seul « \\ », suivi du caractère de saut de ligne « \\ n ».</span><span class="sxs-lookup"><span data-stu-id="2493e-117">The first two are required to output a single '\\', followed by the newline character "\\n".</span></span> <span data-ttu-id="2493e-118">Si vous le souhaitez, vous pouvez également mettre fin à vos lignes à l’aide de « \\ \\ \\ r \\ n ».</span><span class="sxs-lookup"><span data-stu-id="2493e-118">Optionally, you may also want to terminate your lines using "\\\\\\r\\n".</span></span>

## <a name="requirements"></a><span data-ttu-id="2493e-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2493e-119">Requirements</span></span>



| <span data-ttu-id="2493e-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2493e-120">Requirement</span></span> | <span data-ttu-id="2493e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2493e-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2493e-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="2493e-122">Header</span></span><br/> | <dl> <span data-ttu-id="2493e-123"><dt>D3dx9shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="2493e-123"><dt>D3dx9shader.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2493e-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2493e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2493e-125">Structures d’effet</span><span class="sxs-lookup"><span data-stu-id="2493e-125">Effect Structures</span></span>](dx9-graphics-reference-effects-structures.md)
</dt> <dt>

[<span data-ttu-id="2493e-126">**D3DXCreateEffectFromFile**</span><span class="sxs-lookup"><span data-stu-id="2493e-126">**D3DXCreateEffectFromFile**</span></span>](d3dxcreateeffectfromfile.md)
</dt> </dl>

 

 
