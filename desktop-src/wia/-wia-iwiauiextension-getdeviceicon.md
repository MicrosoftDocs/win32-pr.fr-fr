---
description: Obtient une icône d’appareil personnalisé.
ms.assetid: 27763f39-80d8-4862-b045-e49c6e824c28
title: 'IWiaUIExtension :: GetDeviceIcon, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 36b61a25de1acb9b84ce68dc897514e0d4612a1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113291"
---
# <a name="iwiauiextensiongetdeviceicon-method"></a><span data-ttu-id="c82c8-103">IWiaUIExtension :: GetDeviceIcon, méthode</span><span class="sxs-lookup"><span data-stu-id="c82c8-103">IWiaUIExtension::GetDeviceIcon method</span></span>

<span data-ttu-id="c82c8-104">Obtient une icône d’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c82c8-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="c82c8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c82c8-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="c82c8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c82c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c82c8-107">*bstrDeviceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c82c8-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c82c8-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="c82c8-108">Type: **BSTR**</span></span>

<span data-ttu-id="c82c8-109">Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.</span><span class="sxs-lookup"><span data-stu-id="c82c8-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="c82c8-110">*phIcon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c82c8-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c82c8-111">Type : \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="c82c8-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="c82c8-112">Pointe vers un emplacement de mémoire qui reçoit un handle pour l’icône de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c82c8-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="c82c8-113">_nSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c82c8-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c82c8-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="c82c8-114">Type: **ULONG**</span></span>

<span data-ttu-id="c82c8-115">Spécifie la taille d’icône souhaitée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="c82c8-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="c82c8-116">L’icône est supposée être carrée et nSize spécifie à la fois la largeur et la hauteur de l’icône demandée.</span><span class="sxs-lookup"><span data-stu-id="c82c8-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c82c8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c82c8-117">Return value</span></span>

<span data-ttu-id="c82c8-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c82c8-118">Type: **HRESULT**</span></span>

<span data-ttu-id="c82c8-119">Si cette méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c82c8-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c82c8-120">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c82c8-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c82c8-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c82c8-121">Requirements</span></span>



| <span data-ttu-id="c82c8-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c82c8-122">Requirement</span></span> | <span data-ttu-id="c82c8-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="c82c8-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c82c8-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c82c8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="c82c8-125">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c82c8-125">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c82c8-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c82c8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="c82c8-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c82c8-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="c82c8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c82c8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="c82c8-129"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="c82c8-129"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




