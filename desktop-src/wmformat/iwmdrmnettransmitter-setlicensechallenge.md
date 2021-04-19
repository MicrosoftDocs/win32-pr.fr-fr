---
title: Méthode IWMDRMNetTransmitter SetLicenseChallenge (wmdrmsdk. h)
description: La méthode SetLicenseChallenge traite un défi de licence envoyé par un récepteur Windows Media DRM pour les périphériques réseau.
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- Méthode SetLicenseChallenge format Windows Media
- Méthode SetLicenseChallenge format Windows Media, interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter Windows Media format, méthode SetLicenseChallenge
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540358"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="293bb-106">IWMDRMNetTransmitter :: SetLicenseChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="293bb-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="293bb-107">La méthode **SetLicenseChallenge** traite un défi de licence envoyé par un récepteur Windows Media DRM pour les périphériques réseau.</span><span class="sxs-lookup"><span data-stu-id="293bb-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="293bb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="293bb-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="293bb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="293bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="293bb-110">*pbLicenseChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="293bb-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293bb-111">Pointeur vers les données de demande de licence qui ont été envoyées par un récepteur.</span><span class="sxs-lookup"><span data-stu-id="293bb-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="293bb-112">*cbLicenseChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="293bb-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="293bb-113">Taille de la demande de licence en octets.</span><span class="sxs-lookup"><span data-stu-id="293bb-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="293bb-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="293bb-114">Return value</span></span>

<span data-ttu-id="293bb-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="293bb-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="293bb-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="293bb-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="293bb-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="293bb-117">Return code</span></span>                                                                          | <span data-ttu-id="293bb-118">Description</span><span class="sxs-lookup"><span data-stu-id="293bb-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="293bb-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="293bb-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="293bb-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="293bb-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="293bb-121">Notes</span><span class="sxs-lookup"><span data-stu-id="293bb-121">Remarks</span></span>

<span data-ttu-id="293bb-122">Si cette méthode est réussie, les appels suivants aux autres méthodes de **IWMDRMNetTransmitter** utiliseront les informations du Challenge traité.</span><span class="sxs-lookup"><span data-stu-id="293bb-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="293bb-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="293bb-123">Requirements</span></span>



| <span data-ttu-id="293bb-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="293bb-124">Requirement</span></span> | <span data-ttu-id="293bb-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="293bb-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="293bb-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="293bb-126">Header</span></span><br/> | <dl> <span data-ttu-id="293bb-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="293bb-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="293bb-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="293bb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="293bb-129">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="293bb-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





