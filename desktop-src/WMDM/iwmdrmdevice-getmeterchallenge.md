---
title: Méthode IWMDRMDevice GetMeterChallenge
description: La méthode GetMeterChallenge récupère le défi de contrôle.
ms.assetid: 4c122886-46bd-4e63-8e7d-5e6132363662
keywords:
- Méthode GetMeterChallenge Gestionnaire de périphériques Windows Media
- Méthode GetMeterChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetMeterChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a916afa90d1db310041f9b92be94d3af9154df4b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532488"
---
# <a name="iwmdrmdevicegetmeterchallenge-method"></a><span data-ttu-id="b7aeb-106">IWMDRMDevice :: GetMeterChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="b7aeb-106">IWMDRMDevice::GetMeterChallenge method</span></span>

<span data-ttu-id="b7aeb-107">La méthode **GetMeterChallenge** récupère le défi de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-107">The **GetMeterChallenge** method retrieves the metering challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7aeb-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7aeb-108">Syntax</span></span>


```C++
HRESULT GetMeterChallenge(
  [in]  BSTR  bstrMeterCert,
  [out] BYTE  **ppbMeterChallenge,
  [out] DWORD *pcbMeterChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="b7aeb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7aeb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7aeb-110">*bstrMeterCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7aeb-110">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aeb-111">Certificat de contrôle que le propriétaire du contenu envoie à l’ordinateur hôte pour la collecte des données de contrôle associées sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="b7aeb-111">Metering certificate that the content owner sends to the host computer for collecting the associated metering data on the device</span></span>

</dd> <dt>

<span data-ttu-id="b7aeb-112">*ppbMeterChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7aeb-112">*ppbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aeb-113">Résultat du test de contrôle récupéré.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-113">Retrieved metering challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="b7aeb-114">*pcbMeterChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7aeb-114">*pcbMeterChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7aeb-115">Taille du test de contrôle, en octets.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-115">The size of the metering challenge, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7aeb-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7aeb-116">Return value</span></span>

<span data-ttu-id="b7aeb-117">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7aeb-118">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7aeb-119">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b7aeb-119">Return code</span></span>                                                                          | <span data-ttu-id="b7aeb-120">Description</span><span class="sxs-lookup"><span data-stu-id="b7aeb-120">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b7aeb-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7aeb-121"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b7aeb-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7aeb-122">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b7aeb-123">Notes</span><span class="sxs-lookup"><span data-stu-id="b7aeb-123">Remarks</span></span>

<span data-ttu-id="b7aeb-124">Les données de contrôle sont collectées et stockées dans le magasin de données DRM sur l’appareil pour le contenu avec contrôle activé.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-124">Metering data is collected and stored in the DRM data store on the device for content with metering enabled.</span></span> <span data-ttu-id="b7aeb-125">Les actions telles que la lecture seront enregistrées.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-125">Actions such as play will be recorded.</span></span> <span data-ttu-id="b7aeb-126">Lorsque cette fonction est appelée, l’appareil recueille les données de contrôle dans le magasin de données DRM sous la forme d’un document XML et l’envoie au hostcomputer.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-126">When this function is called, the device collects the metering data in the DRM data store in the form of an XML document and sends it to the hostcomputer.</span></span> <span data-ttu-id="b7aeb-127">Si les données sont trop nombreuses, elles sont envoyées en plusieurs phases.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-127">If there is too much data, it is sent in phases.</span></span>

<span data-ttu-id="b7aeb-128">Lorsque l’ordinateur hôte reçoit les données de contrôle, il envoie les données via Internet à l’URL spécifiée dans le certificat de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b7aeb-128">When the host computer receives the metering data, it sends the data over the Internet to the URL specified in the metering certificate.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7aeb-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7aeb-129">Requirements</span></span>



| <span data-ttu-id="b7aeb-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7aeb-130">Requirement</span></span> | <span data-ttu-id="b7aeb-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7aeb-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7aeb-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7aeb-132">Header</span></span><br/>  | <dl> <span data-ttu-id="b7aeb-133"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b7aeb-133"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="b7aeb-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7aeb-134">Library</span></span><br/> | <dl> <span data-ttu-id="b7aeb-135"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7aeb-135"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7aeb-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7aeb-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7aeb-137">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="b7aeb-137">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





