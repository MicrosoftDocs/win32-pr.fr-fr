---
title: Méthode ID3DX11Effect GetGroupByName (D3dx11effect. h)
description: Obtient un groupe d’effets par nom.
ms.assetid: 14b4b484-848a-409c-9a99-207ab25b7566
keywords:
- Méthode GetGroupByName Direct3D 11
- Méthode GetGroupByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetGroupByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetGroupByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1c2132dedb34fe71db30bf82b1c6d336f110a8f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996117"
---
# <a name="id3dx11effectgetgroupbyname-method"></a><span data-ttu-id="64547-106">ID3DX11Effect :: GetGroupByName, méthode</span><span class="sxs-lookup"><span data-stu-id="64547-106">ID3DX11Effect::GetGroupByName method</span></span>

<span data-ttu-id="64547-107">Obtient un groupe d’effets par nom.</span><span class="sxs-lookup"><span data-stu-id="64547-107">Gets an effect group by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="64547-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="64547-108">Syntax</span></span>


```C++
ID3DX11EffectGroup* GetGroupByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="64547-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="64547-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64547-110">*Nom*</span><span class="sxs-lookup"><span data-stu-id="64547-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="64547-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="64547-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="64547-112">Nom du groupe d’effets.</span><span class="sxs-lookup"><span data-stu-id="64547-112">Name of the effect group.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64547-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="64547-113">Return value</span></span>

<span data-ttu-id="64547-114">Type : **[ **ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span><span class="sxs-lookup"><span data-stu-id="64547-114">Type: **[**ID3DX11EffectGroup**](id3dx11effectgroup.md)\***</span></span>

<span data-ttu-id="64547-115">Pointeur vers une interface [**ID3DX11EffectGroup**](id3dx11effectgroup.md) .</span><span class="sxs-lookup"><span data-stu-id="64547-115">A pointer to an [**ID3DX11EffectGroup**](id3dx11effectgroup.md) interface.</span></span>

## <a name="remarks"></a><span data-ttu-id="64547-116">Notes</span><span class="sxs-lookup"><span data-stu-id="64547-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="64547-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="64547-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="64547-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="64547-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="64547-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="64547-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="64547-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="64547-120">Requirements</span></span>



| <span data-ttu-id="64547-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="64547-121">Requirement</span></span> | <span data-ttu-id="64547-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="64547-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64547-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="64547-123">Header</span></span><br/>  | <dl> <span data-ttu-id="64547-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="64547-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="64547-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="64547-125">Library</span></span><br/> | <dl> <span data-ttu-id="64547-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="64547-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64547-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="64547-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64547-128">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="64547-128">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

