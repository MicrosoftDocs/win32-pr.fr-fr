---
description: Accède aux données du fichier. x.
ms.assetid: 0e92914b-47b3-4a88-87ba-ce3c14282dbb
title: 'ID3DXFileData :: Lock, méthode (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.Lock
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 27ef18fcb12b00f0b778ee15d582610ffe52fe54
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106532188"
---
# <a name="id3dxfiledatalock-method"></a><span data-ttu-id="fc60e-103">ID3DXFileData :: Lock, méthode</span><span class="sxs-lookup"><span data-stu-id="fc60e-103">ID3DXFileData::Lock method</span></span>

<span data-ttu-id="fc60e-104">Accède aux données du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="fc60e-104">Accesses the .x file data.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc60e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fc60e-105">Syntax</span></span>


```C++
HRESULT Lock(
  [in]       SIZE_T *pSize,
  [in] const VOID   **ppData
);
```



## <a name="parameters"></a><span data-ttu-id="fc60e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fc60e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc60e-107">*psize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc60e-107">*pSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc60e-108">Type : **[ **taille \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="fc60e-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="fc60e-109">Pointeur vers la taille des données du fichier. x.</span><span class="sxs-lookup"><span data-stu-id="fc60e-109">Pointer to the size of the .x file data.</span></span>

</dd> <dt>

<span data-ttu-id="fc60e-110">*ppData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fc60e-110">*ppData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc60e-111">Type : **const void \* \***</span><span class="sxs-lookup"><span data-stu-id="fc60e-111">Type: **const VOID\*\***</span></span>

<span data-ttu-id="fc60e-112">Adresse d’un pointeur pour recevoir le pointeur d’interface de l’objet de données de fichier [**ID3DXFileData**](id3dxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="fc60e-112">Address of a pointer to receive the [**ID3DXFileData**](id3dxfiledata.md) file data object's interface pointer.</span></span> <span data-ttu-id="fc60e-113">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="fc60e-113">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc60e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fc60e-114">Return value</span></span>

<span data-ttu-id="fc60e-115">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fc60e-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fc60e-116">Si la méthode est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fc60e-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fc60e-117">Si la méthode échoue, la valeur suivante est retournée : D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="fc60e-117">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc60e-118">Notes</span><span class="sxs-lookup"><span data-stu-id="fc60e-118">Remarks</span></span>

<span data-ttu-id="fc60e-119">Le pointeur *ppData* est uniquement valide pendant un **ID3DXFileData :: Lock** ... Séquence [**ID3DXFileData :: Unlock**](id3dxfiledata--unlock.md) .</span><span class="sxs-lookup"><span data-stu-id="fc60e-119">The *ppData* pointer is only valid during a **ID3DXFileData::Lock** ... [**ID3DXFileData::Unlock**](id3dxfiledata--unlock.md) sequence.</span></span> <span data-ttu-id="fc60e-120">Vous pouvez effectuer plusieurs appels de verrouillage.</span><span class="sxs-lookup"><span data-stu-id="fc60e-120">You can make multiple lock calls.</span></span> <span data-ttu-id="fc60e-121">Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.</span><span class="sxs-lookup"><span data-stu-id="fc60e-121">However, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="fc60e-122">Étant donné qu’il n’est pas garanti que les données de fichier soient correctement alignées avec les limites d’octets, vous devez accéder à *ppData* avec des pointeurs non alignés.</span><span class="sxs-lookup"><span data-stu-id="fc60e-122">Because file data is not guaranteed to be aligned properly with byte boundaries, you should access *ppData* with UNALIGNED pointers.</span></span>

<span data-ttu-id="fc60e-123">Il n’est pas garanti que les valeurs de paramètre retournées soient valides en raison d’une éventuelle altération de fichier ; par conséquent, votre code doit vérifier les valeurs de paramètre retournées.</span><span class="sxs-lookup"><span data-stu-id="fc60e-123">Returned parameter values are not guaranteed to be valid due to possible file corruption; therefore, your code should verify the returned parameter values.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc60e-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fc60e-124">Requirements</span></span>



| <span data-ttu-id="fc60e-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fc60e-125">Requirement</span></span> | <span data-ttu-id="fc60e-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="fc60e-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc60e-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="fc60e-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fc60e-128"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="fc60e-128"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fc60e-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fc60e-129">Library</span></span><br/> | <dl> <span data-ttu-id="fc60e-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fc60e-130"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fc60e-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fc60e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc60e-132">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="fc60e-132">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
