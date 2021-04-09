---
description: Notez qu’au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API D3DDisassemble. Cette fonction, qui Désassemble un effet compilé dans une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, est dépréciée.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: D3DX10DisassembleEffect, fonction (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953922"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="6996a-104">D3DX10DisassembleEffect fonction)</span><span class="sxs-lookup"><span data-stu-id="6996a-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="6996a-105">Au lieu d’utiliser cette fonction héritée, nous vous recommandons d’utiliser l’API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="6996a-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="6996a-106">Cette fonction, qui Désassemble un effet compilé dans une chaîne de texte qui contient des instructions d’assembly et des affectations de registres, est dépréciée.</span><span class="sxs-lookup"><span data-stu-id="6996a-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="6996a-107">Utilisez plutôt [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="6996a-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="6996a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6996a-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="6996a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6996a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6996a-110">*pEffect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6996a-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6996a-111">Type : **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="6996a-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="6996a-112">Pointeur vers l’interface d’effet (voir [**interface ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="6996a-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="6996a-113">*EnableColorCode* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6996a-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6996a-114">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6996a-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6996a-115">Incluez des balises HTML dans la sortie pour coder en couleur le résultat.</span><span class="sxs-lookup"><span data-stu-id="6996a-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="6996a-116">*ppDisassembly* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6996a-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6996a-117">Type : **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="6996a-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="6996a-118">Adresse d’une mémoire tampon (voir [**interface ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) qui contient l’effet désassemblé.</span><span class="sxs-lookup"><span data-stu-id="6996a-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6996a-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6996a-119">Return value</span></span>

<span data-ttu-id="6996a-120">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6996a-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6996a-121">Retourne l’un des [codes de retour Direct3D 10](d3d10-graphics-reference-returnvalues.md)suivants.</span><span class="sxs-lookup"><span data-stu-id="6996a-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6996a-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6996a-122">Requirements</span></span>



| <span data-ttu-id="6996a-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6996a-123">Requirement</span></span> | <span data-ttu-id="6996a-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="6996a-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6996a-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="6996a-125">Header</span></span><br/> | <dl> <span data-ttu-id="6996a-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="6996a-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6996a-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6996a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6996a-128">Fonctions usage général</span><span class="sxs-lookup"><span data-stu-id="6996a-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
