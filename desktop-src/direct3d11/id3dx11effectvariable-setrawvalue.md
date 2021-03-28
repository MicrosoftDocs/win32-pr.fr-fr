---
title: Méthode ID3DX11EffectVariable SetRawValue (D3dx11effect. h)
description: Définir des données.
ms.assetid: c5d53aa6-6cd8-4a93-9851-2a93bc6a728a
keywords:
- Méthode SetRawValue Direct3D 11
- Méthode SetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode SetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.SetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b5186e55b8b1d3472cb25ea6fa067988d4fb1f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211692"
---
# <a name="id3dx11effectvariablesetrawvalue-method"></a><span data-ttu-id="cac42-106">ID3DX11EffectVariable :: SetRawValue, méthode</span><span class="sxs-lookup"><span data-stu-id="cac42-106">ID3DX11EffectVariable::SetRawValue method</span></span>

<span data-ttu-id="cac42-107">Définir des données.</span><span class="sxs-lookup"><span data-stu-id="cac42-107">Set data.</span></span>

## <a name="syntax"></a><span data-ttu-id="cac42-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cac42-108">Syntax</span></span>


```C++
HRESULT SetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="cac42-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cac42-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac42-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="cac42-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="cac42-111">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="cac42-111">Type: **void\***</span></span>

<span data-ttu-id="cac42-112">Pointeur vers la variable.</span><span class="sxs-lookup"><span data-stu-id="cac42-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="cac42-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="cac42-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="cac42-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cac42-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cac42-115">Décalage (en octets) entre le début du pointeur et les données.</span><span class="sxs-lookup"><span data-stu-id="cac42-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="cac42-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="cac42-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="cac42-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="cac42-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="cac42-118">Nombre d’octets à définir.</span><span class="sxs-lookup"><span data-stu-id="cac42-118">The number of bytes to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac42-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cac42-119">Return value</span></span>

<span data-ttu-id="cac42-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cac42-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cac42-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="cac42-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cac42-122">Notes</span><span class="sxs-lookup"><span data-stu-id="cac42-122">Remarks</span></span>

<span data-ttu-id="cac42-123">Cette méthode n’effectue aucune conversion ou vérification de type ; C’est pourquoi il s’agit d’un moyen très rapide d’accéder à des éléments de tableau.</span><span class="sxs-lookup"><span data-stu-id="cac42-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="cac42-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="cac42-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="cac42-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="cac42-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="cac42-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="cac42-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="cac42-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="cac42-127">Requirements</span></span>



| <span data-ttu-id="cac42-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cac42-128">Requirement</span></span> | <span data-ttu-id="cac42-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="cac42-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cac42-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="cac42-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cac42-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="cac42-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="cac42-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cac42-132">Library</span></span><br/> | <dl> <span data-ttu-id="cac42-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="cac42-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cac42-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cac42-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac42-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="cac42-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

