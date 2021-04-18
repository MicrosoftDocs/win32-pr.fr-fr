---
description: Obtient un logo de bitmap personnalisé pour l’appareil.
ms.assetid: 56b3c7c9-64f4-4853-9eb7-d876d02a851f
title: 'IWiaUIExtension :: GetDeviceBitmapLogo, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceBitmapLogo
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 51db237c93a2167eb3c4bdae648f9d79da13319a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512984"
---
# <a name="iwiauiextensiongetdevicebitmaplogo-method"></a><span data-ttu-id="ee800-103">IWiaUIExtension :: GetDeviceBitmapLogo, méthode</span><span class="sxs-lookup"><span data-stu-id="ee800-103">IWiaUIExtension::GetDeviceBitmapLogo method</span></span>

<span data-ttu-id="ee800-104">Obtient un logo de bitmap personnalisé pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee800-104">Gets a custom bitmap logo for the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee800-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee800-105">Syntax</span></span>


```C++
HRESULT GetDeviceBitmapLogo(
  [in]  BSTR    bstrDeviceId,
  [out] HBITMAP *phBitmap,
  [in]  ULONG   nMaxWidth,
  [in]  ULONG   nMaxHeight
);
```



## <a name="parameters"></a><span data-ttu-id="ee800-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee800-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee800-107">*bstrDeviceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee800-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee800-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="ee800-108">Type: **BSTR**</span></span>

<span data-ttu-id="ee800-109">Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.</span><span class="sxs-lookup"><span data-stu-id="ee800-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="ee800-110">*phBitmap* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ee800-110">*phBitmap* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee800-111">Type : \**HBITMAP \** _</span><span class="sxs-lookup"><span data-stu-id="ee800-111">Type: \**HBITMAP\** _</span></span>

<span data-ttu-id="ee800-112">Pointe vers un emplacement de mémoire qui recevra un handle pour le logo bitmap de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="ee800-112">Points to a memory location that will receive a handle for the bitmap logo for the device.</span></span>

</dd> <dt>

<span data-ttu-id="ee800-113">_nMaxWidth \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee800-113">_nMaxWidth\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee800-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ee800-114">Type: **ULONG**</span></span>

<span data-ttu-id="ee800-115">Spécifie la largeur souhaitée de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="ee800-115">Specifies the desired width of the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="ee800-116">*nMaxHeight* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ee800-116">*nMaxHeight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee800-117">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="ee800-117">Type: **ULONG**</span></span>

<span data-ttu-id="ee800-118">Spécifie la hauteur souhaitée de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="ee800-118">Specifies the desired height of the bitmap.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee800-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ee800-119">Return value</span></span>

<span data-ttu-id="ee800-120">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ee800-120">Type: **HRESULT**</span></span>

<span data-ttu-id="ee800-121">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="ee800-121">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ee800-122">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ee800-122">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee800-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ee800-123">Requirements</span></span>



| <span data-ttu-id="ee800-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ee800-124">Requirement</span></span> | <span data-ttu-id="ee800-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="ee800-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ee800-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee800-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ee800-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee800-127">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ee800-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ee800-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ee800-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ee800-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ee800-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="ee800-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ee800-131"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee800-131"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




