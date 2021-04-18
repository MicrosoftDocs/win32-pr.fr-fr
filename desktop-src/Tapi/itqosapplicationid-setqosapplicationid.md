---
description: La méthode SetQOSApplicationID définit l’identificateur de QOS pour l’application.
ms.assetid: e25cf749-6673-47eb-b843-4066f475b8f1
title: 'ITQOSApplicationID :: SetQOSApplicationID, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7893c8038fd7a47fc1978a20e5aba5cc8293d9a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543368"
---
# <a name="itqosapplicationidsetqosapplicationid-method"></a><span data-ttu-id="fb60f-103">ITQOSApplicationID :: SetQOSApplicationID, méthode</span><span class="sxs-lookup"><span data-stu-id="fb60f-103">ITQOSApplicationID::SetQOSApplicationID method</span></span>

<span data-ttu-id="fb60f-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="fb60f-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="fb60f-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="fb60f-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="fb60f-106">La méthode **SetQOSApplicationID** définit l’identificateur de QoS pour l’application.</span><span class="sxs-lookup"><span data-stu-id="fb60f-106">The **SetQOSApplicationID** method sets the QOS identifier for the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb60f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb60f-107">Syntax</span></span>


```C++
HRESULT SetQOSApplicationID(
  [in] BSTR pApplicationID,
  [in] BSTR pApplicationGUID,
  [in] BSTR pSubIDs
);
```



## <a name="parameters"></a><span data-ttu-id="fb60f-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb60f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb60f-109">*pApplicationID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb60f-109">*pApplicationID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60f-110">Identificateur unique du processus d’application.</span><span class="sxs-lookup"><span data-stu-id="fb60f-110">Unique identifier for the application process.</span></span>

</dd> <dt>

<span data-ttu-id="fb60f-111">*pApplicationGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb60f-111">*pApplicationGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60f-112">GUID de l’application.</span><span class="sxs-lookup"><span data-stu-id="fb60f-112">Application GUID.</span></span>

</dd> <dt>

<span data-ttu-id="fb60f-113">*pSubIDs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb60f-113">*pSubIDs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb60f-114">Sub-IDs associé à l’appel en cours.</span><span class="sxs-lookup"><span data-stu-id="fb60f-114">Sub-IDs associated with the current call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb60f-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb60f-115">Return value</span></span>

<span data-ttu-id="fb60f-116">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="fb60f-116">This method can return one of these values.</span></span>



| <span data-ttu-id="fb60f-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fb60f-117">Return code</span></span>                                                                                   | <span data-ttu-id="fb60f-118">Description</span><span class="sxs-lookup"><span data-stu-id="fb60f-118">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="fb60f-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fb60f-119"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="fb60f-120">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="fb60f-120">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="fb60f-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="fb60f-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="fb60f-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="fb60f-122">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="fb60f-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb60f-123">Requirements</span></span>



| <span data-ttu-id="fb60f-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb60f-124">Requirement</span></span> | <span data-ttu-id="fb60f-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb60f-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="fb60f-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="fb60f-126">TAPI version</span></span><br/> | <span data-ttu-id="fb60f-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="fb60f-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="fb60f-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="fb60f-128">Header</span></span><br/>       | <dl> <span data-ttu-id="fb60f-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb60f-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="fb60f-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="fb60f-130">Library</span></span><br/>      | <dl> <span data-ttu-id="fb60f-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb60f-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="fb60f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="fb60f-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="fb60f-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb60f-133"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb60f-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb60f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb60f-135">**ITQOSApplicationID**</span><span class="sxs-lookup"><span data-stu-id="fb60f-135">**ITQOSApplicationID**</span></span>](itqosapplicationid.md)
</dt> </dl>

 

 




