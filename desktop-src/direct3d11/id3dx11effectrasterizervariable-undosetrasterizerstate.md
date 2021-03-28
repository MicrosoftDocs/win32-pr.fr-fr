---
title: Méthode ID3DX11EffectRasterizerVariable UndoSetRasterizerState (D3dx11effect. h)
description: Restaure un état de rastériseur précédemment défini.
ms.assetid: 2801479c-cb70-4950-9888-73e271b669aa
keywords:
- Méthode UndoSetRasterizerState Direct3D 11
- Méthode UndoSetRasterizerState Direct3D 11, interface ID3DX11EffectRasterizerVariable
- Interface ID3DX11EffectRasterizerVariable Direct3D 11, méthode UndoSetRasterizerState
topic_type:
- apiref
api_name:
- ID3DX11EffectRasterizerVariable.UndoSetRasterizerState
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed05aa7380a1fb08bbd12d36328d33fa64fb7500
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211963"
---
# <a name="id3dx11effectrasterizervariableundosetrasterizerstate-method"></a><span data-ttu-id="ddb28-106">ID3DX11EffectRasterizerVariable :: UndoSetRasterizerState, méthode</span><span class="sxs-lookup"><span data-stu-id="ddb28-106">ID3DX11EffectRasterizerVariable::UndoSetRasterizerState method</span></span>

<span data-ttu-id="ddb28-107">Restaure un état de rastériseur précédemment défini.</span><span class="sxs-lookup"><span data-stu-id="ddb28-107">Reverts a previously set rasterizer state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddb28-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ddb28-108">Syntax</span></span>


```C++
HRESULT UndoSetRasterizerState(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="ddb28-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ddb28-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddb28-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="ddb28-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="ddb28-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ddb28-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ddb28-112">Index dans un tableau d’interfaces de rastérisation.</span><span class="sxs-lookup"><span data-stu-id="ddb28-112">Index into an array of rasterizer interfaces.</span></span> <span data-ttu-id="ddb28-113">S’il n’existe qu’une seule interface rastériseur, utilisez 0.</span><span class="sxs-lookup"><span data-stu-id="ddb28-113">If there is only one rasterizer interface, use 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddb28-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ddb28-114">Return value</span></span>

<span data-ttu-id="ddb28-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ddb28-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ddb28-116">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="ddb28-116">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ddb28-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ddb28-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ddb28-118">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="ddb28-118">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="ddb28-119">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="ddb28-119">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="ddb28-120">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="ddb28-120">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ddb28-121">Spécifications</span><span class="sxs-lookup"><span data-stu-id="ddb28-121">Requirements</span></span>



| <span data-ttu-id="ddb28-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ddb28-122">Requirement</span></span> | <span data-ttu-id="ddb28-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ddb28-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddb28-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="ddb28-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ddb28-125"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddb28-125"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="ddb28-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ddb28-126">Library</span></span><br/> | <dl> <span data-ttu-id="ddb28-127"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="ddb28-127"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddb28-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ddb28-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddb28-129">ID3DX11EffectRasterizerVariable</span><span class="sxs-lookup"><span data-stu-id="ddb28-129">ID3DX11EffectRasterizerVariable</span></span>](id3dx11effectrasterizervariable.md)
</dt> </dl>

 

