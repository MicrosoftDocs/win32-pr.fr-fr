---
title: ID3DX11EffectPass IsValid, méthode (D3dx11effect. h)
description: Testez un passage pour voir s’il contient une syntaxe valide.
ms.assetid: 3c6ddcef-1303-4161-889c-c3ca271b6ad0
keywords:
- Méthode IsValid Direct3D 11
- Méthode IsValid Direct3D 11, interface ID3DX11EffectPass
- Interface ID3DX11EffectPass Direct3D 11, méthode IsValid
topic_type:
- apiref
api_name:
- ID3DX11EffectPass.IsValid
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50db900d3cea82197fb56ce3a57a5a548220ca1f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974539"
---
# <a name="id3dx11effectpassisvalid-method"></a><span data-ttu-id="24824-106">ID3DX11EffectPass :: IsValid, méthode</span><span class="sxs-lookup"><span data-stu-id="24824-106">ID3DX11EffectPass::IsValid method</span></span>

<span data-ttu-id="24824-107">Testez un passage pour voir s’il contient une syntaxe valide.</span><span class="sxs-lookup"><span data-stu-id="24824-107">Test a pass to see if it contains valid syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="24824-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24824-108">Syntax</span></span>


```C++
BOOL IsValid();
```



## <a name="parameters"></a><span data-ttu-id="24824-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24824-109">Parameters</span></span>

<span data-ttu-id="24824-110">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="24824-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24824-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="24824-111">Return value</span></span>

<span data-ttu-id="24824-112">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="24824-112">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="24824-113">**True** si la syntaxe du code est valide ; Sinon, **false**.</span><span class="sxs-lookup"><span data-stu-id="24824-113">**TRUE** if the code syntax is valid; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="24824-114">Notes</span><span class="sxs-lookup"><span data-stu-id="24824-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="24824-115">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="24824-115">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="24824-116">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="24824-116">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="24824-117">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="24824-117">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="24824-118">Spécifications</span><span class="sxs-lookup"><span data-stu-id="24824-118">Requirements</span></span>



| <span data-ttu-id="24824-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="24824-119">Requirement</span></span> | <span data-ttu-id="24824-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="24824-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24824-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="24824-121">Header</span></span><br/>  | <dl> <span data-ttu-id="24824-122"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="24824-122"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="24824-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="24824-123">Library</span></span><br/> | <dl> <span data-ttu-id="24824-124"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="24824-124"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24824-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="24824-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24824-126">ID3DX11EffectPass</span><span class="sxs-lookup"><span data-stu-id="24824-126">ID3DX11EffectPass</span></span>](id3dx11effectpass.md)
</dt> </dl>

 

