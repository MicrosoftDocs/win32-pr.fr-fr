---
description: Définit la transformation de la vue universelle droitier pour un sprite. Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.
ms.assetid: 83654e9a-8991-49ec-ab28-cf9063126dbe
title: 'ID3DXSprite :: SetWorldViewRH, méthode (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.SetWorldViewRH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f7521f60f819829fc72ba907b57d4e4eb13682a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527118"
---
# <a name="id3dxspritesetworldviewrh-method"></a><span data-ttu-id="e1310-104">ID3DXSprite :: SetWorldViewRH, méthode</span><span class="sxs-lookup"><span data-stu-id="e1310-104">ID3DXSprite::SetWorldViewRH method</span></span>

<span data-ttu-id="e1310-105">Définit la transformation de la vue universelle droitier pour un sprite.</span><span class="sxs-lookup"><span data-stu-id="e1310-105">Sets the right-handed world-view transform for a sprite.</span></span> <span data-ttu-id="e1310-106">Un appel à cette méthode est requis avant d’effectuer un billboarding ou de trier des sprites.</span><span class="sxs-lookup"><span data-stu-id="e1310-106">A call to this method is required before billboarding or sorting sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1310-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1310-107">Syntax</span></span>


```C++
HRESULT SetWorldViewRH(
  [in] const D3DXMATRIX *pWorld,
  [in] const D3DXMATRIX *pView
);
```



## <a name="parameters"></a><span data-ttu-id="e1310-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1310-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1310-109">*pWorld* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1310-109">*pWorld* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1310-110">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1310-110">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1310-111">Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="e1310-111">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a world transform.</span></span> <span data-ttu-id="e1310-112">Si la **valeur est null**, la matrice d’identité est utilisée pour la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="e1310-112">If **NULL**, the identity matrix is used for the world transform.</span></span>

</dd> <dt>

<span data-ttu-id="e1310-113">*pview* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e1310-113">*pView* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1310-114">Type : **const [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="e1310-114">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="e1310-115">Pointeur vers un [**D3DXMATRIX**](d3dxmatrix.md) qui contient une transformation de vue.</span><span class="sxs-lookup"><span data-stu-id="e1310-115">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) that contains a view transform.</span></span> <span data-ttu-id="e1310-116">Si la **valeur est null**, la matrice d’identité est utilisée pour la transformation de vue.</span><span class="sxs-lookup"><span data-stu-id="e1310-116">If **NULL**, the identity matrix is used for the view transform.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1310-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1310-117">Return value</span></span>

<span data-ttu-id="e1310-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1310-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1310-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1310-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e1310-120">Si la méthode échoue, la valeur suivante est retournée. D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="e1310-120">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="e1310-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e1310-121">Remarks</span></span>

<span data-ttu-id="e1310-122">Un appel à cette méthode (ou à [**ID3DXSprite :: SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) est requis si le sprite est rendu avec la valeur de l’indicateur de [D3DXSprite du \_ \_ panneau](d3dxsprite.md), du D3DXSprite \_ \_ \_ \_ de profondeur de tri FRONTTOBACK ou \_ \_ de la profondeur de tri D3DXSprite BACKTOFRONT \_ \_ [**:: Begin**](id3dxsprite--begin.md).</span><span class="sxs-lookup"><span data-stu-id="e1310-122">A call to this method (or to [**ID3DXSprite::SetWorldViewLH**](id3dxsprite--setworldviewlh.md)) is required if the sprite will be rendered with the [D3DXSprite\_\_BILLBOARD](d3dxsprite.md), D3DXSprite\_\_SORT\_DEPTH\_FRONTTOBACK, or D3DXSprite\_\_SORT\_DEPTH\_BACKTOFRONT flag value in [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e1310-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1310-123">Requirements</span></span>



| <span data-ttu-id="e1310-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1310-124">Requirement</span></span> | <span data-ttu-id="e1310-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1310-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1310-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e1310-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e1310-127"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1310-127"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e1310-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e1310-128">Library</span></span><br/> | <dl> <span data-ttu-id="e1310-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1310-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e1310-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1310-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1310-131">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="e1310-131">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> </dl>

 

 




