---
description: Obtient une liste des profils d’accélération vidéo DirectX (DXVA) pris en charge par le pilote d’affichage.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9 :: GetDXVAGuids, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521522"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="08a19-103">IDirect3DVideoDevice9 :: GetDXVAGuids, méthode</span><span class="sxs-lookup"><span data-stu-id="08a19-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="08a19-104">Obtient une liste des profils d’accélération vidéo DirectX (DXVA) pris en charge par le pilote d’affichage.</span><span class="sxs-lookup"><span data-stu-id="08a19-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="08a19-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08a19-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="08a19-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="08a19-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a19-107">*pNumGuids*</span><span class="sxs-lookup"><span data-stu-id="08a19-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="08a19-108">En entrée, spécifie le nombre d’éléments dans le tableau *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="08a19-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="08a19-109">Si *pGuids* a la valeur **null**, la valeur de `*pNumGuids` doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="08a19-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="08a19-110">En sortie, si *pGuids* a la **valeur null**, *pNumGuids* reçoit le nombre de profils DXVA en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="08a19-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="08a19-111">Sinon, *pNumGuids* reçoit le nombre réel de GUID copiés dans le tableau *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="08a19-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="08a19-112">*pGuids*</span><span class="sxs-lookup"><span data-stu-id="08a19-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="08a19-113">Adresse d’un tableau de GUID ou **null**.</span><span class="sxs-lookup"><span data-stu-id="08a19-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="08a19-114">Si la valeur n’est pas **null**, le tableau reçoit une liste de GUID qui spécifient des profils DXVA en mode restreint.</span><span class="sxs-lookup"><span data-stu-id="08a19-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="08a19-115">Ces GUID sont définis dans DXVA. h et sont documentés dans la [spécification dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="08a19-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08a19-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="08a19-116">Return value</span></span>

<span data-ttu-id="08a19-117">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="08a19-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="08a19-118">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="08a19-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a19-119">Notes</span><span class="sxs-lookup"><span data-stu-id="08a19-119">Remarks</span></span>

<span data-ttu-id="08a19-120">Appelez cette méthode deux fois.</span><span class="sxs-lookup"><span data-stu-id="08a19-120">Call this method twice.</span></span> <span data-ttu-id="08a19-121">Lors du premier appel, affectez à *pGuids* la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="08a19-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="08a19-122">Le paramètre *pNumGuids* reçoit le nombre de GUID du profil DXVA.</span><span class="sxs-lookup"><span data-stu-id="08a19-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="08a19-123">Allouez un tableau de GUID avec la taille requise et rappelez la méthode.</span><span class="sxs-lookup"><span data-stu-id="08a19-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="08a19-124">Cette fois-ci, définissez *pGuids* sur l’adresse du tableau.</span><span class="sxs-lookup"><span data-stu-id="08a19-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="08a19-125">La méthode remplit le tableau avec la liste des GUID de profil DXVA.</span><span class="sxs-lookup"><span data-stu-id="08a19-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a19-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="08a19-126">Requirements</span></span>



| <span data-ttu-id="08a19-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="08a19-127">Requirement</span></span> | <span data-ttu-id="08a19-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="08a19-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="08a19-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a19-129">Minimum supported client</span></span><br/> | <span data-ttu-id="08a19-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a19-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="08a19-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="08a19-131">Minimum supported server</span></span><br/> | <span data-ttu-id="08a19-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="08a19-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="08a19-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="08a19-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="08a19-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="08a19-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a19-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08a19-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a19-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="08a19-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
