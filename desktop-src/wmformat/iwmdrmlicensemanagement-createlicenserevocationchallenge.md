---
title: Méthode IWMDRMLicenseManagement CreateLicenseRevocationChallenge (wmdrmsdk. h)
description: La méthode CreateLicenseRevocationChallenge génère une demande de révocation de licence.
ms.assetid: 31fcf7a7-1af8-4474-abac-eddb1070975b
keywords:
- Méthode CreateLicenseRevocationChallenge format Windows Media
- Méthode CreateLicenseRevocationChallenge format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode CreateLicenseRevocationChallenge
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseRevocationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e7fd0acb41b9a2548e5be708611529bea92e131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528523"
---
# <a name="iwmdrmlicensemanagementcreatelicenserevocationchallenge-method"></a><span data-ttu-id="28009-106">IWMDRMLicenseManagement :: CreateLicenseRevocationChallenge, méthode</span><span class="sxs-lookup"><span data-stu-id="28009-106">IWMDRMLicenseManagement::CreateLicenseRevocationChallenge method</span></span>

<span data-ttu-id="28009-107">La méthode **CreateLicenseRevocationChallenge** génère une demande de révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="28009-107">The **CreateLicenseRevocationChallenge** method generates a license revocation challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="28009-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28009-108">Syntax</span></span>


```C++
HRESULT CreateLicenseRevocationChallenge(
  [in]  BYTE  *pbMachineID,
  [in]  DWORD cbMachineID,
  [in]  BYTE  *pbChallenge,
  [in]  DWORD cbChallenge,
  [out] BYTE  **ppbChallengeOutput,
  [out] DWORD *pcbChallengeOutput
);
```



## <a name="parameters"></a><span data-ttu-id="28009-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28009-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28009-110">*pbMachineID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28009-110">*pbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-111">Identificateur de l’ordinateur spécifié par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28009-111">User-specified machine identifier.</span></span> <span data-ttu-id="28009-112">Cette valeur est utilisée pour interroger une licence sur le serveur et doit être conforme au format utilisé par le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="28009-112">This value is used to query for a license on the server and must conform to whatever format the license server uses.</span></span>

</dd> <dt>

<span data-ttu-id="28009-113">*cbMachineID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28009-113">*cbMachineID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-114">Taille, en octets, de l’identificateur de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="28009-114">Size, in bytes, of the machine identifier.</span></span>

</dd> <dt>

<span data-ttu-id="28009-115">*pbChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28009-115">*pbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-116">Données de stimulation spécifiées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="28009-116">User-specified challenge data.</span></span> <span data-ttu-id="28009-117">Ces données, en plus de l’identificateur de l’ordinateur, sont utilisées pour interroger le serveur de licences afin d’identifier les licences à révoquer.</span><span class="sxs-lookup"><span data-stu-id="28009-117">This data, in addition to the machine identifier, is used to query the license server for licenses to be revoked.</span></span>

</dd> <dt>

<span data-ttu-id="28009-118">*cbChallenge* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="28009-118">*cbChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-119">Taille, en octets, des données de stimulation.</span><span class="sxs-lookup"><span data-stu-id="28009-119">Size, in bytes, of the challenge data.</span></span>

</dd> <dt>

<span data-ttu-id="28009-120">*ppbChallengeOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28009-120">*ppbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-121">Adresse d’un pointeur qui reçoit l’adresse de la sortie de la stimulation.</span><span class="sxs-lookup"><span data-stu-id="28009-121">Address of a pointer that receives the address of the challenge output.</span></span> <span data-ttu-id="28009-122">Cette mémoire tampon est celle qui est envoyée au service de révocation de licence.</span><span class="sxs-lookup"><span data-stu-id="28009-122">This buffer is the data that is sent to the license revocation service.</span></span> <span data-ttu-id="28009-123">Lorsque vous avez terminé ces données, vous devez libérer la mémoire en appelant **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="28009-123">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="28009-124">*pcbChallengeOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="28009-124">*pcbChallengeOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="28009-125">Adresse d’une variable qui reçoit la taille des données de sortie de la stimulation allouée, en octets.</span><span class="sxs-lookup"><span data-stu-id="28009-125">Address of a variable that receives the size of the allocated challenge output data, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28009-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="28009-126">Return value</span></span>

<span data-ttu-id="28009-127">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="28009-127">The method returns an **HRESULT**.</span></span> <span data-ttu-id="28009-128">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="28009-128">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="28009-129">Code de retour</span><span class="sxs-lookup"><span data-stu-id="28009-129">Return code</span></span>                                                                          | <span data-ttu-id="28009-130">Description</span><span class="sxs-lookup"><span data-stu-id="28009-130">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="28009-131"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="28009-131"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="28009-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="28009-132">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="28009-133">Notes</span><span class="sxs-lookup"><span data-stu-id="28009-133">Remarks</span></span>

<span data-ttu-id="28009-134">Aucun.</span><span class="sxs-lookup"><span data-stu-id="28009-134">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="28009-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="28009-135">Requirements</span></span>



| <span data-ttu-id="28009-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="28009-136">Requirement</span></span> | <span data-ttu-id="28009-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="28009-137">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="28009-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="28009-138">Header</span></span><br/> | <dl> <span data-ttu-id="28009-139"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="28009-139"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28009-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="28009-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28009-141">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="28009-141">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





