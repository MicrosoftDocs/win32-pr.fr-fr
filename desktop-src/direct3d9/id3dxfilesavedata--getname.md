---
description: Récupère le nom de ce nœud de données de fichier ID3DXFileSaveData.
ms.assetid: ea697d23-42e7-4661-b605-3654f6a31055
title: 'ID3DXFileSaveData :: GetName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 00fa8c60f423343d3d4c594d31141a2f192802d3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043132"
---
# <a name="id3dxfilesavedatagetname-method"></a><span data-ttu-id="e8536-103">ID3DXFileSaveData :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="e8536-103">ID3DXFileSaveData::GetName method</span></span>

<span data-ttu-id="e8536-104">Récupère le nom de ce nœud de données de fichier [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="e8536-104">Retrieves the name of this [**ID3DXFileSaveData**](id3dxfilesavedata.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8536-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e8536-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="e8536-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e8536-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8536-107">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e8536-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8536-108">Type : **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e8536-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e8536-109">Adresse d’un pointeur devant recevoir le nom de ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="e8536-109">Address of a pointer to receive the name of this file data node.</span></span> <span data-ttu-id="e8536-110">Si ce paramètre a la **valeur null**, *puiSize* retourne la taille de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="e8536-110">If this parameter is **NULL**, then *puiSize* will return the size of the string.</span></span> <span data-ttu-id="e8536-111">Si szName pointe vers une mémoire valide, le nom de ce nœud de données de fichier sera copié dans szName jusqu’au nombre de caractères spécifié par *puiSize* .</span><span class="sxs-lookup"><span data-stu-id="e8536-111">If szName points to valid memory, the name of this file data node will be copied into szName up to the number of characters given by *puiSize* .</span></span>

</dd> <dt>

<span data-ttu-id="e8536-112">*puiSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e8536-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e8536-113">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="e8536-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e8536-114">Pointeur vers la taille de la chaîne qui représente le nom de ce nœud de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="e8536-114">Pointer to the size of the string that represents the name of this file data node.</span></span> <span data-ttu-id="e8536-115">Ce paramètre peut avoir la **valeur null** si szName fournit une référence au nom.</span><span class="sxs-lookup"><span data-stu-id="e8536-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="e8536-116">Ce paramètre retourne la taille de la chaîne si szName a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e8536-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8536-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e8536-117">Return value</span></span>

<span data-ttu-id="e8536-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e8536-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e8536-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e8536-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e8536-120">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="e8536-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8536-121">Notes</span><span class="sxs-lookup"><span data-stu-id="e8536-121">Remarks</span></span>

<span data-ttu-id="e8536-122">Pour que cette méthode aboutisse, *szName* ou *puiSize* doit être non **null**.</span><span class="sxs-lookup"><span data-stu-id="e8536-122">For this method to succeed, either *szName* or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8536-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e8536-123">Requirements</span></span>



| <span data-ttu-id="e8536-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e8536-124">Requirement</span></span> | <span data-ttu-id="e8536-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="e8536-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e8536-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="e8536-126">Header</span></span><br/>  | <dl> <span data-ttu-id="e8536-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8536-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e8536-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e8536-128">Library</span></span><br/> | <dl> <span data-ttu-id="e8536-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e8536-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e8536-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e8536-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8536-131">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="e8536-131">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 
