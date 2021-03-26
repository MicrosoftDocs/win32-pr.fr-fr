---
title: ID3DX11EffectStringVariable GetString, méthode (D3dx11effect. h)
description: Obtient la chaîne.
ms.assetid: ce96ae18-d316-41ba-9b2a-eac084b86098
keywords:
- Méthode GetString Direct3D 11
- GetString, méthode Direct3D 11, interface ID3DX11EffectStringVariable
- Interface ID3DX11EffectStringVariable Direct3D 11, méthode GetString
topic_type:
- apiref
api_name:
- ID3DX11EffectStringVariable.GetString
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15d15666bd70bf00395b7052b7820981dd8d0dcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104974471"
---
# <a name="id3dx11effectstringvariablegetstring-method"></a><span data-ttu-id="c43a2-106">ID3DX11EffectStringVariable :: GetString, méthode</span><span class="sxs-lookup"><span data-stu-id="c43a2-106">ID3DX11EffectStringVariable::GetString method</span></span>

<span data-ttu-id="c43a2-107">Obtient la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c43a2-107">Get the string.</span></span>

## <a name="syntax"></a><span data-ttu-id="c43a2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c43a2-108">Syntax</span></span>


```C++
HRESULT GetString(
   LPCSTR *ppString
);
```



## <a name="parameters"></a><span data-ttu-id="c43a2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c43a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c43a2-110">*ppString*</span><span class="sxs-lookup"><span data-stu-id="c43a2-110">*ppString*</span></span> 
</dt> <dd>

<span data-ttu-id="c43a2-111">Type : **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="c43a2-111">Type: **[**LPCSTR**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="c43a2-112">Pointeur vers la chaîne.</span><span class="sxs-lookup"><span data-stu-id="c43a2-112">A pointer to the string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c43a2-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c43a2-113">Return value</span></span>

<span data-ttu-id="c43a2-114">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c43a2-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c43a2-115">Retourne l’un des [codes de retour Direct3D 11](d3d11-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="c43a2-115">Returns one of the following [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c43a2-116">Notes</span><span class="sxs-lookup"><span data-stu-id="c43a2-116">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c43a2-117">Le kit de développement logiciel (SDK) DirectX ne fournit aucun binaire compilé pour les effets.</span><span class="sxs-lookup"><span data-stu-id="c43a2-117">The DirectX SDK does not supply any compiled binaries for effects.</span></span> <span data-ttu-id="c43a2-118">Vous devez utiliser la source Effects 11 pour créer votre application Effects-type.</span><span class="sxs-lookup"><span data-stu-id="c43a2-118">You must use Effects 11 source to build your effects-type application.</span></span> <span data-ttu-id="c43a2-119">Pour plus d’informations sur l’utilisation de la source Effects 11, consultez [différences entre les effets 10 et 11](d3d11-graphics-programming-guide-effects-differences.md).</span><span class="sxs-lookup"><span data-stu-id="c43a2-119">For more information about using Effects 11 source, see [Differences Between Effects 10 and Effects 11](d3d11-graphics-programming-guide-effects-differences.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c43a2-120">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c43a2-120">Requirements</span></span>



| <span data-ttu-id="c43a2-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c43a2-121">Requirement</span></span> | <span data-ttu-id="c43a2-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c43a2-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c43a2-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c43a2-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c43a2-124"><dt>D3dx11effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="c43a2-124"><dt>D3dx11effect.h</dt></span></span> </dl>                                                    |
| <span data-ttu-id="c43a2-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c43a2-125">Library</span></span><br/> | <dl> <span data-ttu-id="c43a2-126"><dt>N/A (une bibliothèque Effects 11 est disponible en ligne en tant que source partagée.)</dt></span><span class="sxs-lookup"><span data-stu-id="c43a2-126"><dt>N/A (An Effects 11 library is available online as shared source.)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c43a2-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c43a2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c43a2-128">ID3DX11EffectStringVariable</span><span class="sxs-lookup"><span data-stu-id="c43a2-128">ID3DX11EffectStringVariable</span></span>](id3dx11effectstringvariable.md)
</dt> </dl>

 

