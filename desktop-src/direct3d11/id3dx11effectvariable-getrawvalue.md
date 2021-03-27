---
title: Méthode ID3DX11EffectVariable GetRawValue (D3dx11effect. h)
description: obtenir des données
ms.assetid: 1b2a319c-880c-4f5a-b4e9-17405351b7d9
keywords:
- Méthode GetRawValue Direct3D 11
- Méthode GetRawValue Direct3D 11, interface ID3DX11EffectVariable
- Interface ID3DX11EffectVariable Direct3D 11, méthode GetRawValue
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.GetRawValue
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be03051433e3ae4fd5891d1859529bb305b08bb0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982474"
---
# <a name="id3dx11effectvariablegetrawvalue-method"></a><span data-ttu-id="580a9-106">ID3DX11EffectVariable :: GetRawValue, méthode</span><span class="sxs-lookup"><span data-stu-id="580a9-106">ID3DX11EffectVariable::GetRawValue method</span></span>

<span data-ttu-id="580a9-107">obtenir des données</span><span class="sxs-lookup"><span data-stu-id="580a9-107">Get data.</span></span>

## <a name="syntax"></a><span data-ttu-id="580a9-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="580a9-108">Syntax</span></span>


```C++
HRESULT GetRawValue(
   void *pData,
   UINT Offset,
   UINT Count
);
```



## <a name="parameters"></a><span data-ttu-id="580a9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="580a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="580a9-110">*pData*</span><span class="sxs-lookup"><span data-stu-id="580a9-110">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="580a9-111">Type : **void \***</span><span class="sxs-lookup"><span data-stu-id="580a9-111">Type: **void\***</span></span>

<span data-ttu-id="580a9-112">Pointeur vers la variable.</span><span class="sxs-lookup"><span data-stu-id="580a9-112">A pointer to the variable.</span></span>

</dd> <dt>

<span data-ttu-id="580a9-113">*Offset*</span><span class="sxs-lookup"><span data-stu-id="580a9-113">*Offset*</span></span> 
</dt> <dd>

<span data-ttu-id="580a9-114">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="580a9-114">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="580a9-115">Décalage (en octets) entre le début du pointeur et les données.</span><span class="sxs-lookup"><span data-stu-id="580a9-115">The offset (in bytes) from the beginning of the pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="580a9-116">*Count*</span><span class="sxs-lookup"><span data-stu-id="580a9-116">*Count*</span></span> 
</dt> <dd>

<span data-ttu-id="580a9-117">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="580a9-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="580a9-118">Nombre d’octets à récupérer.</span><span class="sxs-lookup"><span data-stu-id="580a9-118">The number of bytes to get.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="580a9-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="580a9-119">Return value</span></span>

<span data-ttu-id="580a9-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="580a9-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="580a9-121">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="580a9-121">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="580a9-122">Notes</span><span class="sxs-lookup"><span data-stu-id="580a9-122">Remarks</span></span>

<span data-ttu-id="580a9-123">Cette méthode n’effectue aucune conversion ou vérification de type ; C’est pourquoi il s’agit d’un moyen très rapide d’accéder à des éléments de tableau.</span><span class="sxs-lookup"><span data-stu-id="580a9-123">This method does no conversion or type checking; it is therefore a very quick way to access array items.</span></span>

> [!Note]  
> <span data-ttu-id="580a9-124">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="580a9-124">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="580a9-125">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="580a9-125">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="580a9-126">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="580a9-126">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="580a9-127">Spécifications</span><span class="sxs-lookup"><span data-stu-id="580a9-127">Requirements</span></span>



| <span data-ttu-id="580a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="580a9-128">Requirement</span></span> | <span data-ttu-id="580a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="580a9-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="580a9-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="580a9-130">Header</span></span><br/>  | <dl> <span data-ttu-id="580a9-131"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="580a9-131"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="580a9-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="580a9-132">Library</span></span><br/> | <dl> <span data-ttu-id="580a9-133"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="580a9-133"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="580a9-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="580a9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="580a9-135">ID3DX11EffectVariable</span><span class="sxs-lookup"><span data-stu-id="580a9-135">ID3DX11EffectVariable</span></span>](id3dx11effectvariable.md)
</dt> </dl>

 

