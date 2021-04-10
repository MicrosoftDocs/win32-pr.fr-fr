---
description: Crée un périphérique de décodage DXVA (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9 :: CreateDXVADevice, méthode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114226"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a><span data-ttu-id="e6191-103">IDirect3DVideoDevice9 :: CreateDXVADevice, méthode</span><span class="sxs-lookup"><span data-stu-id="e6191-103">IDirect3DVideoDevice9::CreateDXVADevice method</span></span>

<span data-ttu-id="e6191-104">Crée un périphérique de décodage DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="e6191-104">Creates a DirectX Video Acceleration (DXVA) decoder device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6191-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6191-105">Syntax</span></span>


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a><span data-ttu-id="e6191-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6191-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6191-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="e6191-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="e6191-108">Pointeur vers un GUID qui spécifie le périphérique à créer.</span><span class="sxs-lookup"><span data-stu-id="e6191-108">Pointer to a GUID that specifies the device to create.</span></span>

</dd> <dt>

<span data-ttu-id="e6191-109">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="e6191-109">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="e6191-110">Pointeur vers une structure [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) qui spécifie le format de l’image non compressée.</span><span class="sxs-lookup"><span data-stu-id="e6191-110">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the format of the uncompressed image.</span></span>

</dd> <dt>

<span data-ttu-id="e6191-111">*pData*</span><span class="sxs-lookup"><span data-stu-id="e6191-111">*pData*</span></span> 
</dt> <dd>

<span data-ttu-id="e6191-112">Pointeur vers une structure **DXVA \_ ConnectMode** qui spécifie le mode DXVA et le profil restreint.</span><span class="sxs-lookup"><span data-stu-id="e6191-112">Pointer to a **DXVA\_ConnectMode** structure that specifies the DXVA mode and restricted profile.</span></span>

</dd> <dt>

<span data-ttu-id="e6191-113">*DataSize*</span><span class="sxs-lookup"><span data-stu-id="e6191-113">*DataSize*</span></span> 
</dt> <dd>

<span data-ttu-id="e6191-114">Taille de la structure **DXVA \_ ConnectMode** , en octets.</span><span class="sxs-lookup"><span data-stu-id="e6191-114">Size of the **DXVA\_ConnectMode** structure, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="e6191-115">*ppDXVADevice*</span><span class="sxs-lookup"><span data-stu-id="e6191-115">*ppDXVADevice*</span></span> 
</dt> <dd>

<span data-ttu-id="e6191-116">Reçoit un pointeur vers l’interface [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) .</span><span class="sxs-lookup"><span data-stu-id="e6191-116">Receives a pointer to the [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) interface.</span></span> <span data-ttu-id="e6191-117">L’appelant doit libérer l’interface.</span><span class="sxs-lookup"><span data-stu-id="e6191-117">The caller must release the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6191-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6191-118">Return value</span></span>

<span data-ttu-id="e6191-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e6191-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e6191-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e6191-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6191-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6191-121">Requirements</span></span>



| <span data-ttu-id="e6191-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6191-122">Requirement</span></span> | <span data-ttu-id="e6191-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6191-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e6191-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6191-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e6191-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6191-125">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e6191-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6191-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e6191-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6191-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e6191-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6191-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6191-129"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6191-129"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6191-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6191-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6191-131">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="e6191-131">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




