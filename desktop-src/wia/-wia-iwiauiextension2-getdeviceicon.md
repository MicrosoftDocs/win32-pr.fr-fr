---
description: Obtient une icône d’appareil personnalisé.
ms.assetid: ea768dd1-22fe-4a0f-8851-b152e28d65fb
title: 'IWiaUIExtension2 :: GetDeviceIcon, méthode (Wiadevd. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.GetDeviceIcon
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d071332a1947c4eb6398235d6941a6843a4fa54c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526445"
---
# <a name="iwiauiextension2getdeviceicon-method"></a><span data-ttu-id="f8735-103">IWiaUIExtension2 :: GetDeviceIcon, méthode</span><span class="sxs-lookup"><span data-stu-id="f8735-103">IWiaUIExtension2::GetDeviceIcon method</span></span>

<span data-ttu-id="f8735-104">Obtient une icône d’appareil personnalisé.</span><span class="sxs-lookup"><span data-stu-id="f8735-104">Gets a custom device icon.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8735-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f8735-105">Syntax</span></span>


```C++
HRESULT GetDeviceIcon(
  [in]  BSTR  bstrDeviceId,
  [out] HICON *phIcon,
  [in]  ULONG nSize
);
```



## <a name="parameters"></a><span data-ttu-id="f8735-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f8735-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8735-107">*bstrDeviceId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8735-107">*bstrDeviceId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8735-108">Type : **BSTR**</span><span class="sxs-lookup"><span data-stu-id="f8735-108">Type: **BSTR**</span></span>

<span data-ttu-id="f8735-109">Spécifie l’ID d’appareil de l’appareil WIA pour lequel l’icône doit être obtenue.</span><span class="sxs-lookup"><span data-stu-id="f8735-109">Specifies the device ID of the WIA device for which the icon is to be obtained.</span></span>

</dd> <dt>

<span data-ttu-id="f8735-110">*phIcon* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="f8735-110">*phIcon* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f8735-111">Type : \**HICON \** _</span><span class="sxs-lookup"><span data-stu-id="f8735-111">Type: \**HICON\** _</span></span>

<span data-ttu-id="f8735-112">Pointe vers un emplacement de mémoire qui reçoit un handle pour l’icône de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="f8735-112">Points to a memory location that will receive a handle for the icon for the device.</span></span>

</dd> <dt>

<span data-ttu-id="f8735-113">_nSize \* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f8735-113">_nSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8735-114">Type : **ULong**</span><span class="sxs-lookup"><span data-stu-id="f8735-114">Type: **ULONG**</span></span>

<span data-ttu-id="f8735-115">Spécifie la taille d’icône souhaitée, en pixels.</span><span class="sxs-lookup"><span data-stu-id="f8735-115">Specifies the desired icon size, in pixels.</span></span> <span data-ttu-id="f8735-116">L’icône est supposée être carrée et nSize spécifie à la fois la largeur et la hauteur de l’icône demandée.</span><span class="sxs-lookup"><span data-stu-id="f8735-116">The icon is assumed to be square, and nSize specifies both the width and height of the requested icon.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8735-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f8735-117">Return value</span></span>

<span data-ttu-id="f8735-118">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="f8735-118">Type: **HRESULT**</span></span>

<span data-ttu-id="f8735-119">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f8735-119">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="f8735-120">Si la méthode échoue, elle retourne un code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="f8735-120">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="f8735-121">Le tableau suivant présente certains des codes d’état de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="f8735-121">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="f8735-122">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="f8735-122">Error code</span></span>    | <span data-ttu-id="f8735-123">Description</span><span class="sxs-lookup"><span data-stu-id="f8735-123">Description</span></span>                                                                                                  |
|---------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8735-124">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f8735-124">E\_INVALIDARG</span></span> | <span data-ttu-id="f8735-125">Le paramètre bstrDeviceId ou phIcon a la **valeur null**, ou bstrDeviceId ne pointe pas vers une chaîne d’ID d’appareil WIA valide</span><span class="sxs-lookup"><span data-stu-id="f8735-125">Parameter bstrDeviceId or phIcon is **NULL**, or bstrDeviceId does not point to a valid WIA device ID string</span></span> |
| <span data-ttu-id="f8735-126">E \_ échec</span><span class="sxs-lookup"><span data-stu-id="f8735-126">E\_FAIL</span></span>       | <span data-ttu-id="f8735-127">Aucune ressource icône n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f8735-127">No icon resource is available.</span></span>                                                                               |
| <span data-ttu-id="f8735-128">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="f8735-128">E\_NOTIMPL</span></span>    | <span data-ttu-id="f8735-129">Aucune icône de la taille demandée n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="f8735-129">No icon of the size requested is available.</span></span>                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="f8735-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f8735-130">Requirements</span></span>



| <span data-ttu-id="f8735-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f8735-131">Requirement</span></span> | <span data-ttu-id="f8735-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="f8735-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f8735-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8735-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f8735-134">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8735-134">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f8735-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f8735-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f8735-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f8735-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="f8735-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="f8735-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8735-138"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8735-138"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




