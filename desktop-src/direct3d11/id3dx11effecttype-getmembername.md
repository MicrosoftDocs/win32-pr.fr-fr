---
title: Méthode ID3DX11EffectType GetMemberName (D3dx11effect. h)
description: Obtient le nom d’un membre.
ms.assetid: cd231741-09e1-4e69-9384-5cdfbf83fc8b
keywords:
- Méthode GetMemberName Direct3D 11
- Méthode GetMemberName Direct3D 11, interface ID3DX11EffectType
- Interface ID3DX11EffectType Direct3D 11, méthode GetMemberName
topic_type:
- apiref
api_name:
- ID3DX11EffectType.GetMemberName
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4aa9a24067d8ef19680ca58e41659da850659b2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323045"
---
# <a name="id3dx11effecttypegetmembername-method"></a><span data-ttu-id="30057-106">ID3DX11EffectType :: GetMemberName, méthode</span><span class="sxs-lookup"><span data-stu-id="30057-106">ID3DX11EffectType::GetMemberName method</span></span>

<span data-ttu-id="30057-107">Obtient le nom d’un membre.</span><span class="sxs-lookup"><span data-stu-id="30057-107">Get the name of a member.</span></span>

## <a name="syntax"></a><span data-ttu-id="30057-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="30057-108">Syntax</span></span>


```C++
LPCSTR GetMemberName(
   UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="30057-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="30057-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30057-110">*Index*</span><span class="sxs-lookup"><span data-stu-id="30057-110">*Index*</span></span> 
</dt> <dd>

<span data-ttu-id="30057-111">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30057-111">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30057-112">Index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="30057-112">A zero-based index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30057-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="30057-113">Return value</span></span>

<span data-ttu-id="30057-114">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="30057-114">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="30057-115">Nom du membre.</span><span class="sxs-lookup"><span data-stu-id="30057-115">The name of the member.</span></span>

## <a name="remarks"></a><span data-ttu-id="30057-116">Notes</span><span class="sxs-lookup"><span data-stu-id="30057-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="30057-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="30057-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="30057-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="30057-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="30057-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="30057-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="30057-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="30057-120">Requirements</span></span>



| <span data-ttu-id="30057-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="30057-121">Requirement</span></span> | <span data-ttu-id="30057-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="30057-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30057-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="30057-123">Header</span></span><br/>  | <dl> <span data-ttu-id="30057-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="30057-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="30057-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="30057-125">Library</span></span><br/> | <dl> <span data-ttu-id="30057-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="30057-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30057-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="30057-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30057-128">ID3DX11EffectType</span><span class="sxs-lookup"><span data-stu-id="30057-128">ID3DX11EffectType</span></span>](id3dx11effecttype.md)
</dt> </dl>

 

