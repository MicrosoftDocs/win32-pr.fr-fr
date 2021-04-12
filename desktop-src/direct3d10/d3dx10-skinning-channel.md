---
description: Membre de la déclaration de vertex sur laquelle effectuer l’apparence de logiciel. Utilisé avec l’API ID3DX10SkinInfo ::D oSoftwareSkinning.
ms.assetid: 67c817cd-ce78-4e8b-bdc3-7c4d6670dee1
title: Structure D3DX10_SKINNING_CHANNEL (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_SKINNING_CHANNEL
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: 79f5807dc2539d770d3caa41bddf7aa4960ce682
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211822"
---
# <a name="d3dx10_skinning_channel-structure"></a><span data-ttu-id="56865-104">Structure de canal d' \_ apparence d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="56865-104">D3DX10\_SKINNING\_CHANNEL structure</span></span>

<span data-ttu-id="56865-105">Membre de la déclaration de vertex sur laquelle effectuer l’apparence de logiciel.</span><span class="sxs-lookup"><span data-stu-id="56865-105">The member of the vertex decl to do the software skinning on.</span></span> <span data-ttu-id="56865-106">Utilisé avec l’API [**ID3DX10SkinInfo ::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="56865-106">This is used with the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span>

## <a name="syntax"></a><span data-ttu-id="56865-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="56865-107">Syntax</span></span>


```C++
typedef struct D3DX10_SKINNING_CHANNEL {
  UINT SrcOffset;
  UINT DestOffset;
  BOOL IsNormal;
} D3DX10_SKINNING_CHANNEL, *LPD3DX10_SKINNING_CHANNEL;
```



## <a name="members"></a><span data-ttu-id="56865-108">Membres</span><span class="sxs-lookup"><span data-stu-id="56865-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="56865-109">**SrcOffset**</span><span class="sxs-lookup"><span data-stu-id="56865-109">**SrcOffset**</span></span>
</dt> <dd>

<span data-ttu-id="56865-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56865-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56865-111">Offset à partir du début de chaque vertex source.</span><span class="sxs-lookup"><span data-stu-id="56865-111">Offset from the beginning of each source vertex.</span></span>

</dd> <dt>

<span data-ttu-id="56865-112">**DestOffset**</span><span class="sxs-lookup"><span data-stu-id="56865-112">**DestOffset**</span></span>
</dt> <dd>

<span data-ttu-id="56865-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56865-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56865-114">Offset à partir du début de chaque vertex de destination.</span><span class="sxs-lookup"><span data-stu-id="56865-114">Offset from the beginning of each destination vertex.</span></span>

</dd> <dt>

<span data-ttu-id="56865-115">**IsNormal**</span><span class="sxs-lookup"><span data-stu-id="56865-115">**IsNormal**</span></span>
</dt> <dd>

<span data-ttu-id="56865-116">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="56865-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="56865-117">Détermine le tableau de matrices à utiliser dans l’API [**ID3DX10SkinInfo ::D osoftwareskinning**](id3dx10skininfo-dosoftwareskinning.md) .</span><span class="sxs-lookup"><span data-stu-id="56865-117">Determines which array of matrices to use in the [**ID3DX10SkinInfo::DoSoftwareSkinning**](id3dx10skininfo-dosoftwareskinning.md) API.</span></span> <span data-ttu-id="56865-118">Si la valeur est true, *pInverseTransposeBoneMatrices* est utilisé ; sinon, *pBoneMatrices* est utilisé.</span><span class="sxs-lookup"><span data-stu-id="56865-118">If this is true, the *pInverseTransposeBoneMatrices* will be used, otherwise *pBoneMatrices* will be used.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="56865-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="56865-119">Requirements</span></span>



| <span data-ttu-id="56865-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="56865-120">Requirement</span></span> | <span data-ttu-id="56865-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="56865-121">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="56865-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="56865-122">Header</span></span><br/> | <dl> <span data-ttu-id="56865-123"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="56865-123"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56865-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="56865-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56865-125">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="56865-125">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
