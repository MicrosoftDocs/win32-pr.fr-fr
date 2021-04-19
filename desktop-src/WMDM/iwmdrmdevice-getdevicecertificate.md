---
title: Méthode IWMDRMDevice GetDeviceCertificate
description: La méthode GetDeviceCertificate récupère le certificat de l’appareil.
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- Méthode GetDeviceCertificate Gestionnaire de périphériques Windows Media
- Méthode GetDeviceCertificate Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetDeviceCertificate
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523013"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="9d074-106">IWMDRMDevice :: GetDeviceCertificate, méthode</span><span class="sxs-lookup"><span data-stu-id="9d074-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="9d074-107">La méthode **GetDeviceCertificate** récupère le certificat de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="9d074-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d074-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d074-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="9d074-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d074-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d074-110">*pbstrDevCert* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9d074-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9d074-111">Pointeur vers un **BSTR** contenant le certificat d’appareil récupéré.</span><span class="sxs-lookup"><span data-stu-id="9d074-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d074-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9d074-112">Return value</span></span>

<span data-ttu-id="9d074-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9d074-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9d074-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9d074-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9d074-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9d074-115">Return code</span></span>                                                                          | <span data-ttu-id="9d074-116">Description</span><span class="sxs-lookup"><span data-stu-id="9d074-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9d074-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9d074-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9d074-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9d074-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9d074-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d074-119">Requirements</span></span>



| <span data-ttu-id="9d074-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d074-120">Requirement</span></span> | <span data-ttu-id="9d074-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d074-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d074-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d074-122">Header</span></span><br/>  | <dl> <span data-ttu-id="9d074-123"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9d074-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="9d074-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9d074-124">Library</span></span><br/> | <dl> <span data-ttu-id="9d074-125"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d074-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d074-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d074-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d074-127">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="9d074-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





