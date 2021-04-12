---
description: Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil d’accélération vidéo DirectX (DXVA) spécifié.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9 :: GetUncompressedDXVAFormats, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319006"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="5d7e4-103">IDirect3DVideoDevice9 :: GetUncompressedDXVAFormats, méthode</span><span class="sxs-lookup"><span data-stu-id="5d7e4-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="5d7e4-104">Obtient une liste de formats de pixel non compressés qui peuvent être rendus à l’aide d’un profil d’accélération vidéo DirectX (DXVA) spécifié.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="5d7e4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d7e4-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="5d7e4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d7e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d7e4-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="5d7e4-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7e4-108">Pointeur vers un GUID qui spécifie le profil DXVA.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="5d7e4-109">Pour obtenir la liste des profils pris en charge, appelez [**IDirect3DVideoDevice9 :: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="5d7e4-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="5d7e4-110">*pNumFormats*</span><span class="sxs-lookup"><span data-stu-id="5d7e4-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7e4-111">En entrée, spécifie le nombre d’éléments dans le tableau *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="5d7e4-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="5d7e4-112">Si *pFormats* a la valeur **null**, la valeur de `*pNumFormats` doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="5d7e4-113">En sortie, si *pFormats* a la **valeur null**, *pNumFormats* reçoit le nombre de formats de pixel pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="5d7e4-114">Sinon, *pNumFormats* reçoit le nombre réel de formats de pixel copiés dans le tableau *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="5d7e4-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="5d7e4-115">*pFormats*</span><span class="sxs-lookup"><span data-stu-id="5d7e4-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="5d7e4-116">Adresse d’un tableau de valeurs **D3DFORMAT** , ou **null**.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="5d7e4-117">Si la valeur n’est pas **null**, le tableau reçoit une liste de formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d7e4-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5d7e4-118">Return value</span></span>

<span data-ttu-id="5d7e4-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5d7e4-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5d7e4-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d7e4-121">Notes</span><span class="sxs-lookup"><span data-stu-id="5d7e4-121">Remarks</span></span>

<span data-ttu-id="5d7e4-122">Appelez cette méthode deux fois.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-122">Call this method twice.</span></span> <span data-ttu-id="5d7e4-123">Lors du premier appel, affectez à *pFormats* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="5d7e4-124">Le paramètre *pNumFormats* reçoit le nombre de formats.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="5d7e4-125">Allouez un tableau **D3DFORMAT** avec la taille requise, puis rappelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="5d7e4-126">Cette fois-ci, définissez *pFormats* sur l’adresse du tableau.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="5d7e4-127">La méthode remplit le tableau avec la liste des formats de pixel.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="5d7e4-128">Le pilote doit retourner les formats dans l’ordre de préférence décroissant, avec le format le plus préféré listé en premier.</span><span class="sxs-lookup"><span data-stu-id="5d7e4-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d7e4-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5d7e4-129">Requirements</span></span>



| <span data-ttu-id="5d7e4-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5d7e4-130">Requirement</span></span> | <span data-ttu-id="5d7e4-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="5d7e4-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="5d7e4-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d7e4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5d7e4-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d7e4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d7e4-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5d7e4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5d7e4-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5d7e4-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="5d7e4-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="5d7e4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d7e4-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d7e4-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d7e4-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5d7e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d7e4-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="5d7e4-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




