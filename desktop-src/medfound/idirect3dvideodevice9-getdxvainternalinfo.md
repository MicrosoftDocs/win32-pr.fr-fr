---
description: Recherche la quantité de mémoire de travail allouée par la couche d’abstraction matérielle (HAL) pour son usage privé.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9 :: GetDXVAInternalInfo, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521439"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="2bca2-103">IDirect3DVideoDevice9 :: GetDXVAInternalInfo, méthode</span><span class="sxs-lookup"><span data-stu-id="2bca2-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="2bca2-104">Recherche la quantité de mémoire de travail allouée par la couche d’abstraction matérielle (HAL) pour son usage privé.</span><span class="sxs-lookup"><span data-stu-id="2bca2-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="2bca2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2bca2-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="2bca2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2bca2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2bca2-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="2bca2-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="2bca2-108">Pointeur vers un GUID qui spécifie le profil DXVA.</span><span class="sxs-lookup"><span data-stu-id="2bca2-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="2bca2-109">Pour obtenir la liste des profils pris en charge, appelez [**IDirect3DVideoDevice9 :: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="2bca2-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="2bca2-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="2bca2-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="2bca2-111">Pointeur vers une structure [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) qui spécifie la taille et le format de pixel des données non compressées.</span><span class="sxs-lookup"><span data-stu-id="2bca2-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="2bca2-112">*pMemoryUsed*</span><span class="sxs-lookup"><span data-stu-id="2bca2-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="2bca2-113">Reçoit la quantité de mémoire de travail allouée par la couche HAL, en octets.</span><span class="sxs-lookup"><span data-stu-id="2bca2-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2bca2-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2bca2-114">Return value</span></span>

<span data-ttu-id="2bca2-115">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2bca2-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2bca2-116">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2bca2-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2bca2-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2bca2-117">Requirements</span></span>



| <span data-ttu-id="2bca2-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2bca2-118">Requirement</span></span> | <span data-ttu-id="2bca2-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="2bca2-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="2bca2-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bca2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2bca2-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bca2-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2bca2-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2bca2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2bca2-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2bca2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="2bca2-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="2bca2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="2bca2-125"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="2bca2-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2bca2-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2bca2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2bca2-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="2bca2-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




