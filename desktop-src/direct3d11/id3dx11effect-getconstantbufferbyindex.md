---
title: Méthode ID3DX11Effect GetConstantBufferByIndex (D3dx11effect. h)
description: Obtient une mémoire tampon constante par index.
ms.assetid: 146b146b-89ff-4d56-9ac7-e67a92a30e26
keywords:
- Méthode GetConstantBufferByIndex Direct3D 11
- Méthode GetConstantBufferByIndex Direct3D 11, interface ID3DX11Effect
- Interface ID3DX11Effect Direct3D 11, méthode GetConstantBufferByIndex
topic_type:
- apiref
api_name:
- ID3DX11Effect.GetConstantBufferByIndex
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfbc44b2d9ceea1bcfbf854a8d3c6998d03e3eec
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974659"
---
# <a name="id3dx11effectgetconstantbufferbyindex-method"></a><span data-ttu-id="b04ee-106">ID3DX11Effect :: GetConstantBufferByIndex, méthode</span><span class="sxs-lookup"><span data-stu-id="b04ee-106">ID3DX11Effect::GetConstantBufferByIndex method</span></span>

<span data-ttu-id="b04ee-107">Obtient une mémoire tampon constante par index.</span><span class="sxs-lookup"><span data-stu-id="b04ee-107">Get a constant buffer by index.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04ee-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b04ee-108">Syntax</span></span>


```C++
ID3DX11EffectConstantBuffer* GetConstantBufferByIndex(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="b04ee-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b04ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b04ee-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="b04ee-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="b04ee-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="b04ee-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="b04ee-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="b04ee-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b04ee-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b04ee-113">Return value</span></span>

<span data-ttu-id="b04ee-114">Type : **[ **ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b04ee-114">Type: **[**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md)\***</span></span>

<span data-ttu-id="b04ee-115">Pointeur vers un [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="b04ee-115">A pointer to a [**ID3DX11EffectConstantBuffer**](id3dx11effectconstantbuffer.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b04ee-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b04ee-116">Remarks</span></span>

<span data-ttu-id="b04ee-117">Un effet qui contient une variable qui sera lue/écrite par une application nécessite au moins une mémoire tampon constante.</span><span class="sxs-lookup"><span data-stu-id="b04ee-117">An effect that contains a variable that will be read/written by an application requires at least one constant buffer.</span></span> <span data-ttu-id="b04ee-118">Pour des performances optimales, un effet doit organiser des variables en une ou plusieurs mémoires tampons constantes en fonction de leur fréquence de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="b04ee-118">For best performance, an effect should organize variables into one or more constant buffers based on their frequency of update.</span></span>

> [!Note]  
> <span data-ttu-id="b04ee-119">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="b04ee-119">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="b04ee-120">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="b04ee-120">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="b04ee-121">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="b04ee-121">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b04ee-122">Spécifications</span><span class="sxs-lookup"><span data-stu-id="b04ee-122">Requirements</span></span>



| <span data-ttu-id="b04ee-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b04ee-123">Requirement</span></span> | <span data-ttu-id="b04ee-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b04ee-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04ee-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b04ee-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b04ee-126"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="b04ee-126"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="b04ee-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b04ee-127">Library</span></span><br/> | <dl> <span data-ttu-id="b04ee-128"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="b04ee-128"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b04ee-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b04ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04ee-130">ID3DX11Effect</span><span class="sxs-lookup"><span data-stu-id="b04ee-130">ID3DX11Effect</span></span>](id3dx11effect.md)
</dt> </dl>

 

