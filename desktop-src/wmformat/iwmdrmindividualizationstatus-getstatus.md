---
title: IWMDRMIndividualizationStatus GetStatus, méthode (wmdrmsdk. h)
description: La méthode GetStatus récupère des informations détaillées sur la progression de l’individualisation.
ms.assetid: 8985f3cc-006d-4fd5-b218-d3af3473b8e3
keywords:
- Méthode GetStatus Windows Media format
- Méthode GetStatus Windows Media format, interface IWMDRMIndividualizationStatus
- Interface IWMDRMIndividualizationStatus Windows Media format, GetStatus, méthode
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus.GetStatus
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f144f188de46d17702dd22aa12e2245156b59a21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523631"
---
# <a name="iwmdrmindividualizationstatusgetstatus-method"></a><span data-ttu-id="46d6b-106">IWMDRMIndividualizationStatus :: GetStatus, méthode</span><span class="sxs-lookup"><span data-stu-id="46d6b-106">IWMDRMIndividualizationStatus::GetStatus method</span></span>

<span data-ttu-id="46d6b-107">La méthode **GetStatus** récupère des informations détaillées sur la progression de l’individualisation.</span><span class="sxs-lookup"><span data-stu-id="46d6b-107">The **GetStatus** method retrieves detailed information about individualization progress.</span></span>

## <a name="syntax"></a><span data-ttu-id="46d6b-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46d6b-108">Syntax</span></span>


```C++
HRESULT GetStatus(
  [out] WM_INDIVIDUALIZE_STATUS *pStatus
);
```



## <a name="parameters"></a><span data-ttu-id="46d6b-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46d6b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d6b-110">*pStatus* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="46d6b-110">*pStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="46d6b-111">Reçoit une structure d’état de l' [**\_ \_ individualisation WM**](drmwm-individualize-status.md) contenant des informations détaillées sur l’état de la tentative d’individualisation.</span><span class="sxs-lookup"><span data-stu-id="46d6b-111">Receives a [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure containing detailed information about the status of the individualization attempt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d6b-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46d6b-112">Return value</span></span>

<span data-ttu-id="46d6b-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="46d6b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="46d6b-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="46d6b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="46d6b-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="46d6b-115">Return code</span></span>                                                                          | <span data-ttu-id="46d6b-116">Description</span><span class="sxs-lookup"><span data-stu-id="46d6b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="46d6b-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46d6b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="46d6b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="46d6b-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="46d6b-119">Notes</span><span class="sxs-lookup"><span data-stu-id="46d6b-119">Remarks</span></span>

<span data-ttu-id="46d6b-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="46d6b-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d6b-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46d6b-121">Requirements</span></span>



| <span data-ttu-id="46d6b-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46d6b-122">Requirement</span></span> | <span data-ttu-id="46d6b-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="46d6b-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d6b-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="46d6b-124">Header</span></span><br/> | <dl> <span data-ttu-id="46d6b-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="46d6b-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46d6b-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="46d6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46d6b-127">**Interface IWMDRMIndividualizationStatus**</span><span class="sxs-lookup"><span data-stu-id="46d6b-127">**IWMDRMIndividualizationStatus Interface**</span></span>](iwmdrmindividualizationstatus.md)
</dt> </dl>

 

 





