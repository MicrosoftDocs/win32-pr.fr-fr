---
description: Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires. Action déconseillée.
ms.assetid: 57c42ace-4313-40d8-9992-eaf12edf3a30
title: 'IDirectXFileBinary :: GetMimeType, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetMimeType
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 965006dc6fbad1176307341a19fd1f186e670104
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953836"
---
# <a name="idirectxfilebinarygetmimetype-method"></a><span data-ttu-id="5a13f-104">IDirectXFileBinary :: GetMimeType, méthode</span><span class="sxs-lookup"><span data-stu-id="5a13f-104">IDirectXFileBinary::GetMimeType method</span></span>

<span data-ttu-id="5a13f-105">Récupère le type MIME (Multipurpose Internet Mail Extensions) pour les données binaires.</span><span class="sxs-lookup"><span data-stu-id="5a13f-105">Retrieves the Multipurpose Internet Mail Extensions (MIME) type for the binary data.</span></span> <span data-ttu-id="5a13f-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="5a13f-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a13f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5a13f-107">Syntax</span></span>


```C++
HRESULT GetMimeType(
  [out] LPCSTR *pszMimeType
);
```



## <a name="parameters"></a><span data-ttu-id="5a13f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5a13f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a13f-109">*pszMimeType* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5a13f-109">*pszMimeType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a13f-110">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="5a13f-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5a13f-111">Adresse d’un pointeur pour recevoir la chaîne de type MIME.</span><span class="sxs-lookup"><span data-stu-id="5a13f-111">Address of a pointer to receive the MIME type string.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a13f-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5a13f-112">Return value</span></span>

<span data-ttu-id="5a13f-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5a13f-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5a13f-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5a13f-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="5a13f-115">Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="5a13f-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a13f-116">Notes</span><span class="sxs-lookup"><span data-stu-id="5a13f-116">Remarks</span></span>

<span data-ttu-id="5a13f-117">Quand aucun type MIME n’est spécifié dans un fichier DirectX pour un objet binaire, la fonction affecte à pszMimeType la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5a13f-117">When there is no MIME type specified in a DirectX file for a binary object, the function will set pszMimeType to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a13f-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5a13f-118">Requirements</span></span>



| <span data-ttu-id="5a13f-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5a13f-119">Requirement</span></span> | <span data-ttu-id="5a13f-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="5a13f-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5a13f-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="5a13f-121">Header</span></span><br/>  | <dl> <span data-ttu-id="5a13f-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a13f-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a13f-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5a13f-123">Library</span></span><br/> | <dl> <span data-ttu-id="5a13f-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a13f-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a13f-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5a13f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a13f-126">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="5a13f-126">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
