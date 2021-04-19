---
title: Méthode IWMDRMDevice GetSecureClockChallenge
description: La méthode GetSecureClockChallenge récupère le résultat du Challenge d’horloge sécurisé.
ms.assetid: cbef160c-91a3-47d1-9d7a-e649ce2c77ff
keywords:
- Méthode GetSecureClockChallenge Gestionnaire de périphériques Windows Media
- Méthode GetSecureClockChallenge Gestionnaire de périphériques Windows Media, interface IWMDRMDevice
- Interface IWMDRMDevice Windows Media Gestionnaire de périphériques, méthode GetSecureClockChallenge
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetSecureClockChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7e57165f75a23d13d847e028deb69de383e2855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537315"
---
# <a name="iwmdrmdevicegetsecureclockchallenge-method"></a><span data-ttu-id="e6864-106">IWMDRMDevice :: GetSecureClockChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="e6864-106">IWMDRMDevice::GetSecureClockChallenge method</span></span>

<span data-ttu-id="e6864-107">La méthode **GetSecureClockChallenge** récupère le résultat du Challenge d’horloge sécurisé.</span><span class="sxs-lookup"><span data-stu-id="e6864-107">The **GetSecureClockChallenge** method retrieves the secure clock challenge result.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6864-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6864-108">Syntax</span></span>


```C++
HRESULT GetSecureClockChallenge(
  [out] BYTE  **ppbChallenge,
  [out] DWORD *pcbChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="e6864-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6864-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6864-110">*ppbChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6864-110">*ppbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6864-111">Résultat de la stimulation récupéré.</span><span class="sxs-lookup"><span data-stu-id="e6864-111">Retrieved challenge result.</span></span>

</dd> <dt>

<span data-ttu-id="e6864-112">*pcbChallenge* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6864-112">*pcbChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6864-113">Taille du résultat de la vérification, en octets.</span><span class="sxs-lookup"><span data-stu-id="e6864-113">Size of the challenge result, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6864-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6864-114">Return value</span></span>

<span data-ttu-id="e6864-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e6864-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e6864-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e6864-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e6864-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e6864-117">Return code</span></span>                                                                          | <span data-ttu-id="e6864-118">Description</span><span class="sxs-lookup"><span data-stu-id="e6864-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e6864-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e6864-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e6864-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6864-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e6864-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6864-121">Requirements</span></span>



| <span data-ttu-id="e6864-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6864-122">Requirement</span></span> | <span data-ttu-id="e6864-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6864-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6864-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="e6864-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e6864-125"><dt>WMDDRMSP. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e6864-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="e6864-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e6864-126">Library</span></span><br/> | <dl> <span data-ttu-id="e6864-127"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6864-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6864-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6864-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6864-129">**GetSecureClock**</span><span class="sxs-lookup"><span data-stu-id="e6864-129">**GetSecureClock**</span></span>](iwmdrmdevice-getsecureclock.md)
</dt> <dt>

[<span data-ttu-id="e6864-130">**Interface IWMDRMDevice**</span><span class="sxs-lookup"><span data-stu-id="e6864-130">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





