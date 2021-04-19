---
description: Interroge l’État lecture/écriture d’une surface de décodage DXVA (DirectX Video Acceleration).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9 :: QueryStatus, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518982"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="b9e25-103">IDirect3DDXVADevice9 :: QueryStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="b9e25-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="b9e25-104">Interroge l’État lecture/écriture d’une surface de décodage DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="b9e25-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9e25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9e25-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b9e25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9e25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9e25-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="b9e25-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e25-108">Pointeur vers l’interface **IDirect3DSurface9** de la surface à interroger.</span><span class="sxs-lookup"><span data-stu-id="b9e25-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="b9e25-109">*Indicateurs*</span><span class="sxs-lookup"><span data-stu-id="b9e25-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="b9e25-110">Spécifie le type de requête à effectuer.</span><span class="sxs-lookup"><span data-stu-id="b9e25-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="b9e25-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9e25-111">Value</span></span>                                                                                                                             | <span data-ttu-id="b9e25-112">Signification</span><span class="sxs-lookup"><span data-stu-id="b9e25-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="b9e25-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e25-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="b9e25-114">Teste si la surface peut être utilisée en toute sécurité pour l’écriture.</span><span class="sxs-lookup"><span data-stu-id="b9e25-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="b9e25-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="b9e25-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="b9e25-116">Teste si la surface peut être utilisée en toute sécurité pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="b9e25-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9e25-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9e25-117">Return value</span></span>

<span data-ttu-id="b9e25-118">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9e25-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9e25-119">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9e25-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9e25-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9e25-120">Requirements</span></span>



| <span data-ttu-id="b9e25-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9e25-121">Requirement</span></span> | <span data-ttu-id="b9e25-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9e25-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b9e25-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9e25-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9e25-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9e25-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9e25-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b9e25-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9e25-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b9e25-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9e25-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9e25-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9e25-128"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9e25-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9e25-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9e25-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9e25-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="b9e25-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




