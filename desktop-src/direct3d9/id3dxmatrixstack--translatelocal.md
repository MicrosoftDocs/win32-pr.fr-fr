---
description: Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.
ms.assetid: d4752a6c-2114-4016-a69f-dcc561d2c76b
title: 'ID3DXMATRIXStack :: TranslateLocal, méthode (D3dx9math. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMATRIXStack.TranslateLocal
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 784e623ae47dfece9b395d423437fb6ce661b223
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211842"
---
# <a name="id3dxmatrixstacktranslatelocal-method-d3dx9mathh"></a><span data-ttu-id="145f7-103">ID3DXMATRIXStack :: TranslateLocal, méthode (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="145f7-103">ID3DXMATRIXStack::TranslateLocal method (D3dx9math.h)</span></span>

<span data-ttu-id="145f7-104">Détermine le produit de la matrice de traduction calculée, déterminé par les facteurs donnés (x, y et z) et la matrice actuelle.</span><span class="sxs-lookup"><span data-stu-id="145f7-104">Determines the product of the computed translation matrix determined by the given factors (x, y, and z) and the current matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="145f7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="145f7-105">Syntax</span></span>


```C++
HRESULT TranslateLocal(
  [in] FLOAT x,
  [in] FLOAT y,
  [in] FLOAT z
);
```



## <a name="parameters"></a><span data-ttu-id="145f7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="145f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="145f7-107">*x* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="145f7-107">*x* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145f7-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145f7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145f7-109">Facteur de translation sur l’axe x.</span><span class="sxs-lookup"><span data-stu-id="145f7-109">The translation factor in the x-direction.</span></span>

</dd> <dt>

<span data-ttu-id="145f7-110">*y* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="145f7-110">*y* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145f7-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145f7-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145f7-112">Facteur de translation sur l’axe y.</span><span class="sxs-lookup"><span data-stu-id="145f7-112">The translation factor in the y-direction.</span></span>

</dd> <dt>

<span data-ttu-id="145f7-113">*z* \[\]</span><span class="sxs-lookup"><span data-stu-id="145f7-113">*z* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="145f7-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="145f7-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="145f7-115">Facteur de translation dans l’axe z.</span><span class="sxs-lookup"><span data-stu-id="145f7-115">The translation factor in the z-direction.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="145f7-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="145f7-116">Return value</span></span>

<span data-ttu-id="145f7-117">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="145f7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="145f7-118">Si la méthode est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="145f7-118">If the method succeeds, the return value is D3D\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="145f7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="145f7-119">Remarks</span></span>

<span data-ttu-id="145f7-120">Cette méthode multiplie la matrice actuelle par la matrice de traduction calculée (la transformation concerne l’origine locale de l’objet).</span><span class="sxs-lookup"><span data-stu-id="145f7-120">This method left-multiplies the current matrix with the computed translation matrix (transformation is about the local origin of the object).</span></span>


```
    
D3DXMATRIX tmp;
D3DXMatrixTranslation( &tmp, x, y, z );
m_stack[m_currentPos] = tmp * m_stack[m_currentPos];
```



## <a name="requirements"></a><span data-ttu-id="145f7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="145f7-121">Requirements</span></span>



| <span data-ttu-id="145f7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="145f7-122">Requirement</span></span> | <span data-ttu-id="145f7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="145f7-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="145f7-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="145f7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="145f7-125"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="145f7-125"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="145f7-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="145f7-126">Library</span></span><br/> | <dl> <span data-ttu-id="145f7-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="145f7-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="145f7-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="145f7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145f7-129">ID3DXMATRIXStack</span><span class="sxs-lookup"><span data-stu-id="145f7-129">ID3DXMATRIXStack</span></span>](id3dxmatrixstack.md)
</dt> <dt>

[<span data-ttu-id="145f7-130">**ID3DXMATRIXStack :: translate**</span><span class="sxs-lookup"><span data-stu-id="145f7-130">**ID3DXMATRIXStack::Translate**</span></span>](id3dxmatrixstack--translate.md)
</dt> </dl>

 

 
