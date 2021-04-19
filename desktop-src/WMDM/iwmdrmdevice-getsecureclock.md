---
title: Méthode IWMDRMDevice GetSecureClock
description: La méthode GetSecureClock récupère l’horloge sécurisée, de sorte que les licences basées sur le temps peuvent être appliquées.
ms.assetid: 6de9b7ce-9c2a-44e5-9de7-40cfbaf4d92c
keywords:
- Méthode GetSecureClock Gestionnaire de périphériques Windows Media
- Méthode GetSecureClock Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSecureClock
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClock
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaa92c3bc2ee82facf2f2e1043e71467a0c55bd8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106538575"
---
# <a name="iwmdrmdevicegetsecureclock-method"></a><span data-ttu-id="9a277-106">IWMDRMDevice :: GetSecureClock, méthode</span><span class="sxs-lookup"><span data-stu-id="9a277-106">IWMDRMDevice::GetSecureClock method</span></span>

<span data-ttu-id="9a277-107">La méthode **GetSecureClock** récupère l’horloge sécurisée, de sorte que les licences basées sur le temps peuvent être appliquées.</span><span class="sxs-lookup"><span data-stu-id="9a277-107">The **GetSecureClock** method retrieves the secure clock, so time-based licenses can be enforced.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a277-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a277-108">Syntax</span></span>


```C++
HRESULT GetSecureClock(
  [out] BYTE  **ppbSecureClock,
  [out] DWORD *pcbSecureClock,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="9a277-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a277-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a277-110">*ppbSecureClock* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a277-110">*ppbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a277-111">Horloge sécurisée récupérée.</span><span class="sxs-lookup"><span data-stu-id="9a277-111">Retrieved secure clock.</span></span>

</dd> <dt>

<span data-ttu-id="9a277-112">*pcbSecureClock* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a277-112">*pcbSecureClock* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a277-113">Taille de l’horloge sécurisée, en octets.</span><span class="sxs-lookup"><span data-stu-id="9a277-113">Size of the secure clock, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9a277-114">*pdwFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9a277-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9a277-115">Indicateurs d’état de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9a277-115">Device status flags.</span></span> <span data-ttu-id="9a277-116">Cette valeur doit être l’un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="9a277-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="9a277-117">Indicateur</span><span class="sxs-lookup"><span data-stu-id="9a277-117">Flag</span></span>                     | <span data-ttu-id="9a277-118">Description</span><span class="sxs-lookup"><span data-stu-id="9a277-118">Description</span></span>                            |
|--------------------------|----------------------------------------|
| <span data-ttu-id="9a277-119">\_ISWMDRM d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="9a277-119">WMDRM\_DEVICE\_ISWMDRM</span></span>   | <span data-ttu-id="9a277-120">L’appareil prend en charge Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="9a277-120">The device supports Windows Media DRM.</span></span> |
| <span data-ttu-id="9a277-121">\_NEEDCLOCK d’appareil WMDRM \_</span><span class="sxs-lookup"><span data-stu-id="9a277-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span> | <span data-ttu-id="9a277-122">L’appareil a besoin d’une horloge.</span><span class="sxs-lookup"><span data-stu-id="9a277-122">The device needs clock.</span></span>                |
| <span data-ttu-id="9a277-123">\_appareil WMDRM \_ révoqué</span><span class="sxs-lookup"><span data-stu-id="9a277-123">WMDRM\_DEVICE\_REVOKED</span></span>   | <span data-ttu-id="9a277-124">L’appareil a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="9a277-124">The device has been revoked.</span></span>           |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a277-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9a277-125">Return value</span></span>

<span data-ttu-id="9a277-126">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9a277-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9a277-127">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9a277-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9a277-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9a277-128">Return code</span></span>                                                                          | <span data-ttu-id="9a277-129">Description</span><span class="sxs-lookup"><span data-stu-id="9a277-129">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9a277-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a277-130"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9a277-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="9a277-131">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a277-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9a277-132">Requirements</span></span>



| <span data-ttu-id="9a277-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9a277-133">Requirement</span></span> | <span data-ttu-id="9a277-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="9a277-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9a277-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="9a277-135">Header</span></span><br/>  | <dl> <span data-ttu-id="9a277-136"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a277-136"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a277-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9a277-137">Library</span></span><br/> | <dl> <span data-ttu-id="9a277-138"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a277-138"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a277-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a277-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a277-140">**GetSecureClockChallenge**</span><span class="sxs-lookup"><span data-stu-id="9a277-140">**GetSecureClockChallenge**</span></span>](iwmdrmdevice-getsecureclockchallenge.md)
</dt> <dt>

[<span data-ttu-id="9a277-141">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="9a277-141">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> <dt>

[<span data-ttu-id="9a277-142">**SetSecureClockResponse**</span><span class="sxs-lookup"><span data-stu-id="9a277-142">**SetSecureClockResponse**</span></span>](iwmdrmdevice-setsecureclockresponse.md)
</dt> </dl>

 

 





