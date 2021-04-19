---
description: Récupère le nom de cet objet de données de fichier.
ms.assetid: 182529cb-144c-4ed8-94bf-6688598e9ea7
title: 'ID3DXFileData :: GetName, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e27fc3e95280f29a33d4ececffc7c229563462a0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522370"
---
# <a name="id3dxfiledatagetname-method"></a><span data-ttu-id="ad059-103">ID3DXFileData :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="ad059-103">ID3DXFileData::GetName method</span></span>

<span data-ttu-id="ad059-104">Récupère le nom de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="ad059-104">Retrieves the name of this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad059-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad059-105">Syntax</span></span>


```C++
HRESULT GetName(
  [in]      LPSTR  szName,
  [in, out] SIZE_T *puiSize
);
```



## <a name="parameters"></a><span data-ttu-id="ad059-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad059-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad059-107">*szName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ad059-107">*szName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad059-108">Type : **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ad059-108">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ad059-109">Adresse d’un pointeur devant recevoir le nom de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="ad059-109">Address of a pointer to receive the name of this file data object.</span></span> <span data-ttu-id="ad059-110">Si ce paramètre a la **valeur null**, puiSize retourne la taille de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="ad059-110">If this parameter is **NULL**, then puiSize will return the size of the string.</span></span> <span data-ttu-id="ad059-111">Si szName pointe vers une mémoire valide, le nom de cet objet de données de fichier sera copié dans szName jusqu’au nombre de caractères spécifié par puiSize.</span><span class="sxs-lookup"><span data-stu-id="ad059-111">If szName points to valid memory, the name of this file data object will be copied into szName up to the number of characters given by puiSize.</span></span>

</dd> <dt>

<span data-ttu-id="ad059-112">*puiSize* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad059-112">*puiSize* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad059-113">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ad059-113">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ad059-114">Pointeur vers la taille de la chaîne qui représente le nom de cet objet de données de fichier.</span><span class="sxs-lookup"><span data-stu-id="ad059-114">Pointer to the size of the string that represents the name of this file data object.</span></span> <span data-ttu-id="ad059-115">Ce paramètre peut avoir la **valeur null** si szName fournit une référence au nom.</span><span class="sxs-lookup"><span data-stu-id="ad059-115">This parameter can be **NULL** if szName provides a reference to the name.</span></span> <span data-ttu-id="ad059-116">Ce paramètre retourne la taille de la chaîne si szName a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ad059-116">This parameter will return the size of the string if szName is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad059-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ad059-117">Return value</span></span>

<span data-ttu-id="ad059-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ad059-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ad059-119">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad059-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ad059-120">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="ad059-120">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad059-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ad059-121">Remarks</span></span>

<span data-ttu-id="ad059-122">Pour que cette méthode aboutisse, szName ou *puiSize* doit être non **null**.</span><span class="sxs-lookup"><span data-stu-id="ad059-122">For this method to succeed, either szName or *puiSize* must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad059-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ad059-123">Requirements</span></span>



| <span data-ttu-id="ad059-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ad059-124">Requirement</span></span> | <span data-ttu-id="ad059-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ad059-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad059-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ad059-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ad059-127"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad059-127"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="ad059-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ad059-128">Library</span></span><br/> | <dl> <span data-ttu-id="ad059-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad059-129"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ad059-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad059-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad059-131">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="ad059-131">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
