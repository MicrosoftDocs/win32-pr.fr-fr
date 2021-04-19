---
description: Crée et ajoute un objet de référence de données en tant qu’objet enfant. Action déconseillée.
ms.assetid: 71a770a2-1502-4b93-b368-990c3318bd33
title: 'IDirectXFileData :: AddDataReference, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataReference
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 44834af51380c3b8bdbb4e9a4b24bf911ea6a07f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106545886"
---
# <a name="idirectxfiledataadddatareference-method"></a><span data-ttu-id="ede1f-104">IDirectXFileData :: AddDataReference, méthode</span><span class="sxs-lookup"><span data-stu-id="ede1f-104">IDirectXFileData::AddDataReference method</span></span>

<span data-ttu-id="ede1f-105">Crée et ajoute un objet de référence de données en tant qu’objet enfant.</span><span class="sxs-lookup"><span data-stu-id="ede1f-105">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="ede1f-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="ede1f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="ede1f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ede1f-107">Syntax</span></span>


```C++
HRESULT AddDataReference(
  [in]       LPCSTR szRef,
  [in] const GUID   *pguidRef
);
```



## <a name="parameters"></a><span data-ttu-id="ede1f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ede1f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede1f-109">*szRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ede1f-109">*szRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede1f-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ede1f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ede1f-111">Pointeur vers le nom de l’objet de données référencé.</span><span class="sxs-lookup"><span data-stu-id="ede1f-111">Pointer to the name of the referenced data object.</span></span> <span data-ttu-id="ede1f-112">Ce paramètre peut avoir la **valeur null** si pguidRef fournit une référence au GUID.</span><span class="sxs-lookup"><span data-stu-id="ede1f-112">This parameter can be **NULL** if pguidRef provides a reference to the GUID.</span></span>

</dd> <dt>

<span data-ttu-id="ede1f-113">*pguidRef* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ede1f-113">*pguidRef* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ede1f-114">Type : **const [**GUID**](guid.md) \***</span><span class="sxs-lookup"><span data-stu-id="ede1f-114">Type: **const [**GUID**](guid.md)\***</span></span>

<span data-ttu-id="ede1f-115">Pointeur vers le GUID représentant les données.</span><span class="sxs-lookup"><span data-stu-id="ede1f-115">Pointer to the GUID representing the data.</span></span> <span data-ttu-id="ede1f-116">Ce paramètre peut avoir la **valeur null** si szRef fournit une référence au nom.</span><span class="sxs-lookup"><span data-stu-id="ede1f-116">This parameter can be **NULL** if szRef provides a reference to the name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede1f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ede1f-117">Return value</span></span>

<span data-ttu-id="ede1f-118">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ede1f-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ede1f-119">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ede1f-119">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="ede1f-120">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="ede1f-120">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="ede1f-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ede1f-121">Remarks</span></span>

<span data-ttu-id="ede1f-122">Pour que cette méthode aboutisse, le paramètre szRef ou pguidRef doit être non **null**.</span><span class="sxs-lookup"><span data-stu-id="ede1f-122">For this method to succeed, either the szRef or pguidRef parameter must be non-**NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ede1f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ede1f-123">Requirements</span></span>



| <span data-ttu-id="ede1f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ede1f-124">Requirement</span></span> | <span data-ttu-id="ede1f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ede1f-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ede1f-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ede1f-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ede1f-127"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="ede1f-127"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="ede1f-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ede1f-128">Library</span></span><br/> | <dl> <span data-ttu-id="ede1f-129"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ede1f-129"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ede1f-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ede1f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ede1f-131">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="ede1f-131">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> </dl>

 

 
