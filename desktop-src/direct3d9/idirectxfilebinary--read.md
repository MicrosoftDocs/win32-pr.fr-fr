---
description: Lit les données binaires. Action déconseillée.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'IDirectXFileBinary :: Read, méthode (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043152"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="09e45-104">IDirectXFileBinary :: Read, méthode</span><span class="sxs-lookup"><span data-stu-id="09e45-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="09e45-105">Lit les données binaires.</span><span class="sxs-lookup"><span data-stu-id="09e45-105">Reads the binary data.</span></span> <span data-ttu-id="09e45-106">Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="09e45-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="09e45-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09e45-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="09e45-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="09e45-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09e45-109">*pvData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="09e45-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e45-110">Type : **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09e45-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09e45-111">Pointeur vers la mémoire tampon qui reçoit les données qui ont été lues.</span><span class="sxs-lookup"><span data-stu-id="09e45-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="09e45-112">*cbSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="09e45-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09e45-113">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09e45-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09e45-114">Taille de la mémoire tampon vers laquelle pointe pvData, en octets.</span><span class="sxs-lookup"><span data-stu-id="09e45-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="09e45-115">*pcbRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="09e45-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="09e45-116">Type : **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="09e45-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="09e45-117">Pointeur vers le nombre d’octets réellement lus.</span><span class="sxs-lookup"><span data-stu-id="09e45-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09e45-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="09e45-118">Return value</span></span>

<span data-ttu-id="09e45-119">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="09e45-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="09e45-120">Si la méthode est réussie, la valeur de retour est DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="09e45-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="09e45-121">Si la méthode échoue, la valeur de retour peut être l’une des valeurs suivantes : DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.</span><span class="sxs-lookup"><span data-stu-id="09e45-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="09e45-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09e45-122">Requirements</span></span>



| <span data-ttu-id="09e45-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09e45-123">Requirement</span></span> | <span data-ttu-id="09e45-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="09e45-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09e45-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="09e45-125">Header</span></span><br/>  | <dl> <span data-ttu-id="09e45-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="09e45-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="09e45-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="09e45-127">Library</span></span><br/> | <dl> <span data-ttu-id="09e45-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09e45-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09e45-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="09e45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e45-130">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="09e45-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
