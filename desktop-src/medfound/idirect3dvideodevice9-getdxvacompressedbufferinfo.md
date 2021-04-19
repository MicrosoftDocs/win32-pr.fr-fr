---
description: Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529709"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="ef922-103">IDirect3DVideoDevice9 :: GetDXVACompressedBufferInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="ef922-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="ef922-104">Obtient des informations sur les mémoires tampons compressées nécessaires au décodage accéléré par le matériel.</span><span class="sxs-lookup"><span data-stu-id="ef922-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef922-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ef922-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ef922-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ef922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef922-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="ef922-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="ef922-108">Pointeur vers un GUID qui spécifie le profil DXVA.</span><span class="sxs-lookup"><span data-stu-id="ef922-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="ef922-109">Pour obtenir la liste des profils pris en charge, appelez [**IDirect3DVideoDevice9 :: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="ef922-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="ef922-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="ef922-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="ef922-111">Pointeur vers une structure [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) qui spécifie la taille et le format de pixel des données non compressées.</span><span class="sxs-lookup"><span data-stu-id="ef922-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="ef922-112">*pNumBuffers*</span><span class="sxs-lookup"><span data-stu-id="ef922-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="ef922-113">En entrée, spécifie le nombre d’éléments dans le tableau *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="ef922-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="ef922-114">Si *pBufferInfo* a la valeur **null**, la valeur de `*pNumBuffers` doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ef922-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="ef922-115">En sortie, si *pBufferInfo* a la **valeur null**, *pNumBuffers* reçoit la taille du tableau à allouer.</span><span class="sxs-lookup"><span data-stu-id="ef922-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="ef922-116">Sinon, *pNumBuffers* reçoit le nombre réel d’éléments qui sont copiés dans le tableau *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="ef922-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="ef922-117">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="ef922-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="ef922-118">Adresse d’un tableau de structures [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ef922-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="ef922-119">Si la valeur n’est pas **null**, la méthode copie une liste de structures **DXVACompBufferInfo** dans ce tableau.</span><span class="sxs-lookup"><span data-stu-id="ef922-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="ef922-120">Chaque structure correspond à un type de tampon de données compressé utilisé par l’accélérateur vidéo.</span><span class="sxs-lookup"><span data-stu-id="ef922-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="ef922-121">Affectez à tous les éléments du tableau la valeur zéro avant d’appeler cette méthode.</span><span class="sxs-lookup"><span data-stu-id="ef922-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="ef922-122">Chaque index de tableau correspond à l’un des types de surface DXVA définis dans DXVA. h.</span><span class="sxs-lookup"><span data-stu-id="ef922-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="ef922-123">L’accélérateur vidéo renvoie une liste des entrées de tableau de **\_ \_ \_ \_ mémoires tampons de type nombre** jusqu’à DXVA.</span><span class="sxs-lookup"><span data-stu-id="ef922-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="ef922-124">Pour plus d’informations, reportez-vous à la [spécification DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), section 3,4, « liste des descriptions de tampon ».</span><span class="sxs-lookup"><span data-stu-id="ef922-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="ef922-125">Si un type de mémoire tampon spécifique n’est pas utilisé par le profil DXVA, l’entrée à cet index contient des zéros pour toutes les valeurs.</span><span class="sxs-lookup"><span data-stu-id="ef922-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef922-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ef922-126">Return value</span></span>

<span data-ttu-id="ef922-127">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ef922-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef922-128">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ef922-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef922-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ef922-129">Requirements</span></span>



| <span data-ttu-id="ef922-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ef922-130">Requirement</span></span> | <span data-ttu-id="ef922-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="ef922-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ef922-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef922-132">Minimum supported client</span></span><br/> | <span data-ttu-id="ef922-133">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef922-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ef922-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef922-134">Minimum supported server</span></span><br/> | <span data-ttu-id="ef922-135">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ef922-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="ef922-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="ef922-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="ef922-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef922-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef922-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef922-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef922-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="ef922-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
