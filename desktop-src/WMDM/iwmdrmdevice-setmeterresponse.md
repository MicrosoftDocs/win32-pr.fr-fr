---
title: Méthode IWMDRMDevice SetMeterResponse
description: La méthode SetMeterResponse définit la réponse de contrôle.
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- Méthode SetMeterResponse Gestionnaire de périphériques Windows Media
- Méthode SetMeterResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode SetMeterResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542333"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="80c3a-106">IWMDRMDevice :: SetMeterResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="80c3a-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="80c3a-107">La méthode **SetMeterResponse** définit la réponse de contrôle.</span><span class="sxs-lookup"><span data-stu-id="80c3a-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="80c3a-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80c3a-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="80c3a-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80c3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80c3a-110">*pbMeterResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80c3a-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c3a-111">Réponse de contrôle à définir.</span><span class="sxs-lookup"><span data-stu-id="80c3a-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="80c3a-112">*cbMeterResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80c3a-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80c3a-113">Taille de la réponse de contrôle, en octets.</span><span class="sxs-lookup"><span data-stu-id="80c3a-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="80c3a-114">*pdwFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80c3a-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80c3a-115">Indicateurs de réponse.</span><span class="sxs-lookup"><span data-stu-id="80c3a-115">Response flags.</span></span> <span data-ttu-id="80c3a-116">Cette valeur doit être l’un des indicateurs suivants.</span><span class="sxs-lookup"><span data-stu-id="80c3a-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="80c3a-117">Indicateur</span><span class="sxs-lookup"><span data-stu-id="80c3a-117">Flag</span></span>                            | <span data-ttu-id="80c3a-118">Description</span><span class="sxs-lookup"><span data-stu-id="80c3a-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="80c3a-119">\_réponse du compteur WMDRM \_ \_ All</span><span class="sxs-lookup"><span data-stu-id="80c3a-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="80c3a-120">Toutes les réponses de compteur.</span><span class="sxs-lookup"><span data-stu-id="80c3a-120">All meter responses.</span></span>     |
| <span data-ttu-id="80c3a-121">réponse de compteur de WMDRM \_ \_ \_ partielle</span><span class="sxs-lookup"><span data-stu-id="80c3a-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="80c3a-122">Réponses à des compteurs partiels.</span><span class="sxs-lookup"><span data-stu-id="80c3a-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80c3a-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80c3a-123">Return value</span></span>

<span data-ttu-id="80c3a-124">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="80c3a-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="80c3a-125">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="80c3a-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="80c3a-126">Code de retour</span><span class="sxs-lookup"><span data-stu-id="80c3a-126">Return code</span></span>                                                                          | <span data-ttu-id="80c3a-127">Description</span><span class="sxs-lookup"><span data-stu-id="80c3a-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="80c3a-128"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80c3a-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="80c3a-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="80c3a-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80c3a-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80c3a-130">Requirements</span></span>



| <span data-ttu-id="80c3a-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80c3a-131">Requirement</span></span> | <span data-ttu-id="80c3a-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="80c3a-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80c3a-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="80c3a-133">Header</span></span><br/>  | <dl> <span data-ttu-id="80c3a-134"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80c3a-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="80c3a-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80c3a-135">Library</span></span><br/> | <dl> <span data-ttu-id="80c3a-136"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80c3a-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80c3a-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80c3a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80c3a-138">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="80c3a-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





