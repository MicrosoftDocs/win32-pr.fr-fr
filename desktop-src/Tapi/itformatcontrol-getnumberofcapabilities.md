---
description: La méthode GetNumberOfCapabilities récupère le nombre de fonctionnalités associées au format actuel.
ms.assetid: 26e51c0d-c1cb-410f-ab19-eb884afa8431
title: 'ITFormatControl :: GetNumberOfCapabilities, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e29153f5ee9ce8c5e12b93a1d219905c40f80418
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533350"
---
# <a name="itformatcontrolgetnumberofcapabilities-method"></a><span data-ttu-id="7b4ae-103">ITFormatControl :: GetNumberOfCapabilities, méthode</span><span class="sxs-lookup"><span data-stu-id="7b4ae-103">ITFormatControl::GetNumberOfCapabilities method</span></span>

<span data-ttu-id="7b4ae-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="7b4ae-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="7b4ae-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="7b4ae-106">La méthode **GetNumberOfCapabilities** récupère le nombre de fonctionnalités associées au format actuel.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-106">The **GetNumberOfCapabilities** method retrieves the number of capabilities associated with the current format.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b4ae-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7b4ae-107">Syntax</span></span>


```C++
HRESULT GetNumberOfCapabilities(
  [out] DWORD *pdwCount
);
```



## <a name="parameters"></a><span data-ttu-id="7b4ae-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7b4ae-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7b4ae-109">*pdwCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7b4ae-109">*pdwCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7b4ae-110">Nombre de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-110">Count of the capabilities.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7b4ae-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7b4ae-111">Return value</span></span>

<span data-ttu-id="7b4ae-112">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-112">This method can return one of these values.</span></span>



| <span data-ttu-id="7b4ae-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="7b4ae-113">Return code</span></span>                                                                                   | <span data-ttu-id="7b4ae-114">Description</span><span class="sxs-lookup"><span data-stu-id="7b4ae-114">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="7b4ae-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4ae-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7b4ae-116">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-116">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7b4ae-117"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="7b4ae-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7b4ae-118">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="7b4ae-118">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7b4ae-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b4ae-119">Requirements</span></span>



| <span data-ttu-id="7b4ae-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b4ae-120">Requirement</span></span> | <span data-ttu-id="7b4ae-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b4ae-121">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7b4ae-122">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="7b4ae-122">TAPI version</span></span><br/> | <span data-ttu-id="7b4ae-123">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="7b4ae-123">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="7b4ae-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="7b4ae-124">Header</span></span><br/>       | <dl> <span data-ttu-id="7b4ae-125"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b4ae-125"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7b4ae-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="7b4ae-126">Library</span></span><br/>      | <dl> <span data-ttu-id="7b4ae-127"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7b4ae-127"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="7b4ae-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7b4ae-128">DLL</span></span><br/>          | <dl> <span data-ttu-id="7b4ae-129"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b4ae-129"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b4ae-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7b4ae-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b4ae-131">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="7b4ae-131">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




