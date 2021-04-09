---
description: Active/désactive le mode de dessin des lignes de style OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'ID3DXLine :: SetGLLines, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870205"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="1147b-103">ID3DXLine :: SetGLLines, méthode</span><span class="sxs-lookup"><span data-stu-id="1147b-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="1147b-104">Active/désactive le mode de dessin des lignes de style OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1147b-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="1147b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1147b-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="1147b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1147b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1147b-107">*bGLLines* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1147b-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1147b-108">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1147b-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1147b-109">Active/désactive le dessin de style OpenGL.</span><span class="sxs-lookup"><span data-stu-id="1147b-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="1147b-110">**True** active les lignes de style OpenGL, tandis que **false** active les lignes de style Direct3D.</span><span class="sxs-lookup"><span data-stu-id="1147b-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1147b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1147b-111">Return value</span></span>

<span data-ttu-id="1147b-112">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1147b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1147b-113">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1147b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1147b-114">Si la méthode échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="1147b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="1147b-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1147b-115">Requirements</span></span>



| <span data-ttu-id="1147b-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1147b-116">Requirement</span></span> | <span data-ttu-id="1147b-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="1147b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1147b-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="1147b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="1147b-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="1147b-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="1147b-120">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1147b-120">Library</span></span><br/> | <dl> <span data-ttu-id="1147b-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1147b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1147b-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1147b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1147b-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="1147b-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
