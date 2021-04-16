---
description: Récupère la taille des données binaires. Action déconseillée.
ms.assetid: 99a74043-ce87-4545-961f-dade54e77735
title: 'IDirectXFileBinary :: deDXFile, méthode (. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.GetSize
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 664e2bf026df6d9e4b5bc07067ce1ce7fe7669db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531005"
---
# <a name="idirectxfilebinarygetsize-method"></a><span data-ttu-id="d026c-104">IDirectXFileBinary :: deméthode, méthode</span><span class="sxs-lookup"><span data-stu-id="d026c-104">IDirectXFileBinary::GetSize method</span></span>

<span data-ttu-id="d026c-105">Récupère la taille des données binaires.</span><span class="sxs-lookup"><span data-stu-id="d026c-105">Retrieves the size of the binary data.</span></span> <span data-ttu-id="d026c-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="d026c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="d026c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d026c-107">Syntax</span></span>


```C++
HRESULT GetSize(
  [out] DWORD *pcbSize
);
```



## <a name="parameters"></a><span data-ttu-id="d026c-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d026c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d026c-109">*PCB* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d026c-109">*pcbSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d026c-110">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d026c-110">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d026c-111">Pointeur vers la taille retournée des données binaires, en octets.</span><span class="sxs-lookup"><span data-stu-id="d026c-111">Pointer to the returned size of the binary data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d026c-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d026c-112">Return value</span></span>

<span data-ttu-id="d026c-113">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d026c-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d026c-114">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d026c-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="d026c-115">Si la méthode échoue, la valeur de retour peut être DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="d026c-115">If the method fails, the return value can be DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d026c-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d026c-116">Requirements</span></span>



| <span data-ttu-id="d026c-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d026c-117">Requirement</span></span> | <span data-ttu-id="d026c-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="d026c-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d026c-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="d026c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="d026c-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="d026c-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="d026c-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d026c-121">Library</span></span><br/> | <dl> <span data-ttu-id="d026c-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d026c-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d026c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d026c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d026c-124">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="d026c-124">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
