---
description: Recherche un commentaire particulier dans un nuanceur. Le commentaire est identifié par un code à quatre caractères (FOURCC) dans le premier DWORD du commentaire.
ms.assetid: 86ab8330-fd48-4d14-835c-92399c6c8a38
title: D3DXFindShaderComment, fonction (D3DX9Shader. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFindShaderComment
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 394c72bcf7076075318cd664cf56bbb464d7e3cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523826"
---
# <a name="d3dxfindshadercomment-function"></a><span data-ttu-id="ea343-104">D3DXFindShaderComment fonction)</span><span class="sxs-lookup"><span data-stu-id="ea343-104">D3DXFindShaderComment function</span></span>

<span data-ttu-id="ea343-105">Recherche un commentaire particulier dans un nuanceur.</span><span class="sxs-lookup"><span data-stu-id="ea343-105">Searches through a shader for a particular comment.</span></span> <span data-ttu-id="ea343-106">Le commentaire est identifié par un code à quatre caractères (FOURCC) dans le premier DWORD du commentaire.</span><span class="sxs-lookup"><span data-stu-id="ea343-106">The comment is identified by a four-character code (FOURCC) in the first DWORD of the comment.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea343-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ea343-107">Syntax</span></span>


```C++
HRESULT D3DXFindShaderComment(
  _In_  const DWORD   *pFunction,
  _In_        DWORD   FourCC,
  _In_        LPCVOID *ppData,
  _Out_       UINT    *pSizeInBytes
);
```



## <a name="parameters"></a><span data-ttu-id="ea343-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ea343-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea343-109">*pFunction* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea343-109">*pFunction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea343-110">Type : **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ea343-110">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea343-111">Pointeur vers le flux de fonction de nuanceur DWORD.</span><span class="sxs-lookup"><span data-stu-id="ea343-111">Pointer to the shader function DWORD stream.</span></span>

</dd> <dt>

<span data-ttu-id="ea343-112">*FourCC* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea343-112">*FourCC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea343-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ea343-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ea343-114">Code FOURCC qui identifie le bloc de commentaires.</span><span class="sxs-lookup"><span data-stu-id="ea343-114">FOURCC code that identifies the comment block.</span></span> <span data-ttu-id="ea343-115">Consultez [formats FourCC](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="ea343-115">See [FourCC Formats](d3dformat.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea343-116">*ppData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ea343-116">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea343-117">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea343-117">Type: **[**LPCVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea343-118">Retourne un pointeur vers les données de commentaire (à l’exclusion du jeton de commentaire et du code FOURCC).</span><span class="sxs-lookup"><span data-stu-id="ea343-118">Returns a pointer to the comment data (not including the comment token and FOURCC code).</span></span> <span data-ttu-id="ea343-119">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="ea343-119">This value can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ea343-120">*pSizeInBytes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ea343-120">*pSizeInBytes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea343-121">Type : **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ea343-121">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ea343-122">Retourne la taille des données de commentaire en octets.</span><span class="sxs-lookup"><span data-stu-id="ea343-122">Returns the size of the comment data in bytes.</span></span> <span data-ttu-id="ea343-123">Cette valeur peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="ea343-123">This value can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea343-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ea343-124">Return value</span></span>

<span data-ttu-id="ea343-125">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ea343-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ea343-126">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea343-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ea343-127">Si le commentaire est introuvable et qu’aucune autre erreur ne s’est produite, S \_ false est retourné.</span><span class="sxs-lookup"><span data-stu-id="ea343-127">If the comment is not found, and no other error has occurred, S\_FALSE is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea343-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ea343-128">Requirements</span></span>



| <span data-ttu-id="ea343-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ea343-129">Requirement</span></span> | <span data-ttu-id="ea343-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="ea343-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea343-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="ea343-131">Header</span></span><br/>  | <dl> <span data-ttu-id="ea343-132"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea343-132"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="ea343-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ea343-133">Library</span></span><br/> | <dl> <span data-ttu-id="ea343-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea343-134"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ea343-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ea343-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea343-136">Fonctions de nuanceur</span><span class="sxs-lookup"><span data-stu-id="ea343-136">Shader Functions</span></span>](dx9-graphics-reference-d3dx-functions-shader.md)
</dt> </dl>

 

 
