---
description: Récupère un pointeur vers le nom d’un objet de fichier DirectX. Action déconseillée.
ms.assetid: feb3faa2-22b9-47ed-8a38-33092821d484
title: 'IDirectXFileObject :: GetName, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileObject.GetName
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 134a1ce61ed1dc0d98a4daf3ba80dd4b0976c372
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106529606"
---
# <a name="idirectxfileobjectgetname-method"></a><span data-ttu-id="7388c-104">IDirectXFileObject :: GetName, méthode</span><span class="sxs-lookup"><span data-stu-id="7388c-104">IDirectXFileObject::GetName method</span></span>

<span data-ttu-id="7388c-105">Récupère un pointeur vers le nom d’un objet de fichier DirectX.</span><span class="sxs-lookup"><span data-stu-id="7388c-105">Retrieves a pointer to a DirectX file object's name.</span></span> <span data-ttu-id="7388c-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="7388c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="7388c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7388c-107">Syntax</span></span>


```C++
HRESULT GetName(
  [out]     LPSTR   pstrNameBuf,
  [in, out] LPDWORD pdwBufLen
);
```



## <a name="parameters"></a><span data-ttu-id="7388c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7388c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7388c-109">*pstrNameBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7388c-109">*pstrNameBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7388c-110">Type : **[ **LPSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7388c-110">Type: **[**LPSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7388c-111">Pointeur vers la mémoire tampon dans laquelle le nom de l’objet fichier DirectX sera copié.</span><span class="sxs-lookup"><span data-stu-id="7388c-111">Pointer to the buffer in which the DirectX file object's name will be copied.</span></span> <span data-ttu-id="7388c-112">Affectez la valeur **null** si seule la longueur de la mémoire tampon est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="7388c-112">Set to **NULL** if only the buffer length is needed.</span></span>

</dd> <dt>

<span data-ttu-id="7388c-113">*pdwBufLen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7388c-113">*pdwBufLen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7388c-114">Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7388c-114">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7388c-115">Pointeur vers une valeur DWORD spécifiant la longueur de la mémoire tampon vers laquelle pointe pstrNameBuf.</span><span class="sxs-lookup"><span data-stu-id="7388c-115">Pointer to a DWORD specifying the length of the buffer pointed to by pstrNameBuf.</span></span> <span data-ttu-id="7388c-116">La valeur du paramètre pdwBufLen sera modifiée en fonction de la longueur de la mémoire tampon nécessaire pour contenir le nom de l’objet, même si pstrNameBuf est **null**.</span><span class="sxs-lookup"><span data-stu-id="7388c-116">The pdwBufLen parameter value will be modified to the buffer length needed to hold the object's name even if pstrNameBuf is **NULL**.</span></span> <span data-ttu-id="7388c-117">Dans les deux cas, la fonction retourne DXFILEERR \_ BADVALUE si la valeur d’origine de pdwBufLen n’est pas aussi grande que la longueur nécessaire pour contenir le nom de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7388c-117">In either case, the function will return DXFILEERR\_BADVALUE if the original value of pdwBufLen is not as large as or larger than the length needed to hold the object's name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7388c-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7388c-118">Return value</span></span>

<span data-ttu-id="7388c-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7388c-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7388c-120">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="7388c-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="7388c-121">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="7388c-121">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="requirements"></a><span data-ttu-id="7388c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7388c-122">Requirements</span></span>



| <span data-ttu-id="7388c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7388c-123">Requirement</span></span> | <span data-ttu-id="7388c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="7388c-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7388c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="7388c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="7388c-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="7388c-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="7388c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7388c-127">Library</span></span><br/> | <dl> <span data-ttu-id="7388c-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7388c-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7388c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7388c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7388c-130">IDirectXFileObject</span><span class="sxs-lookup"><span data-stu-id="7388c-130">IDirectXFileObject</span></span>](idirectxfileobject.md)
</dt> </dl>

 

 
