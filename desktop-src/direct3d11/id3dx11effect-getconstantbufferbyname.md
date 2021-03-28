---
title: Méthode ID3DX11Effect GetConstantBufferByName (D3dx11effect. h)
description: Obtient une mémoire tampon constante par nom.
ms.assetid: 11757615-4068-430d-9ab0-f83f02af8e55
keywords:
- Méthode GetConstantBufferByName Direct3D 11
- Méthode GetConstantBufferByName Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetConstantBufferByName
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa01d20bfeebfa3f689a58aae5c5face8b879e3c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870173"
---
# <a name="id3dx11effectgetconstantbufferbyname-method"></a><span data-ttu-id="c36b1-106">ID3DX11Effect :: GetConstantBufferByName, méthode</span><span class="sxs-lookup"><span data-stu-id="c36b1-106">ID3DX11Effect::GetConstantBufferByName method</span></span>

<span data-ttu-id="c36b1-107">Obtient une mémoire tampon constante par nom.</span><span class="sxs-lookup"><span data-stu-id="c36b1-107">Get a constant buffer by name.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36b1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c36b1-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByName(
   LPCSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="c36b1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c36b1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36b1-110">*Nom*</span><span class="sxs-lookup"><span data-stu-id="c36b1-110">*Name*</span></span> 
</dt> <dd>

<span data-ttu-id="c36b1-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="c36b1-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="c36b1-112">Nom de la mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="c36b1-112">The constant-buffer name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36b1-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c36b1-113">Return value</span></span>

<span data-ttu-id="c36b1-114">Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="c36b1-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="c36b1-115">Pointeur vers la mémoire tampon constante indiquée par le nom.</span><span class="sxs-lookup"><span data-stu-id="c36b1-115">A pointer to the constant buffer indicated by the Name.</span></span> <span data-ttu-id="c36b1-116">Consultez [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="c36b1-116">See [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c36b1-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c36b1-117">Remarks</span></span>

<span data-ttu-id="c36b1-118">Un effet qui contient une variable qui sera lue/écrite par une application nécessite au moins une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="c36b1-118">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="c36b1-119">Pour des performances optimales, un effet doit organiser des variables en une ou plusieurs mémoires tampons constantes en fonction de leur fréquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c36b1-119">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="c36b1-120">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c36b1-120">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c36b1-121">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c36b1-121">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c36b1-122">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c36b1-122">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c36b1-123">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c36b1-123">Requirements</span></span>



| <span data-ttu-id="c36b1-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c36b1-124">Requirement</span></span> | <span data-ttu-id="c36b1-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c36b1-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36b1-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="c36b1-126">Header</span></span><br/>  | <dl> <span data-ttu-id="c36b1-127"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c36b1-127"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c36b1-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c36b1-128">Library</span></span><br/> | <dl> <span data-ttu-id="c36b1-129"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c36b1-129"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c36b1-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c36b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c36b1-131">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="c36b1-131">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

