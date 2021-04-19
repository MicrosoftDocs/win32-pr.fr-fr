---
title: Méthode IWMDRMDevice SetLicenseResponse
description: La méthode SetLicenseResponse définit la réponse de la licence.
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- Méthode SetLicenseResponse Gestionnaire de périphériques Windows Media
- Méthode SetLicenseResponse Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode SetLicenseResponse
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528719"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="39661-106">IWMDRMDevice :: SetLicenseResponse, méthode</span><span class="sxs-lookup"><span data-stu-id="39661-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="39661-107">La méthode **SetLicenseResponse** définit la réponse de la licence.</span><span class="sxs-lookup"><span data-stu-id="39661-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="39661-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39661-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="39661-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39661-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39661-110">*pbResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39661-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39661-111">Spécifie la réponse à définir.</span><span class="sxs-lookup"><span data-stu-id="39661-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="39661-112">*cbResponse* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39661-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39661-113">Taille de la réponse, en octets.</span><span class="sxs-lookup"><span data-stu-id="39661-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39661-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39661-114">Return value</span></span>

<span data-ttu-id="39661-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="39661-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="39661-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="39661-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="39661-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="39661-117">Return code</span></span>                                                                          | <span data-ttu-id="39661-118">Description</span><span class="sxs-lookup"><span data-stu-id="39661-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="39661-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="39661-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="39661-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="39661-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39661-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39661-121">Requirements</span></span>



| <span data-ttu-id="39661-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39661-122">Requirement</span></span> | <span data-ttu-id="39661-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="39661-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39661-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="39661-124">Header</span></span><br/>  | <dl> <span data-ttu-id="39661-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="39661-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="39661-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39661-126">Library</span></span><br/> | <dl> <span data-ttu-id="39661-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39661-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39661-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39661-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39661-129">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="39661-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





