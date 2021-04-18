---
title: Méthode IWMDRMLicenseManagement ProcessLicenseDeletionMessage (wmdrmsdk. h)
description: La méthode ProcessLicenseDeletion supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.
ms.assetid: 478dd156-feb8-4eda-9d3a-35db3e65c227
keywords:
- Méthode ProcessLicenseDeletionMessage format Windows Media
- Méthode ProcessLicenseDeletionMessage format Windows Media, interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement Windows Media format, méthode ProcessLicenseDeletionMessage
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.ProcessLicenseDeletionMessage
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9338c1bc4ef78e658cc25ab95f5c50556af3ed09
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540435"
---
# <a name="iwmdrmlicensemanagementprocesslicensedeletionmessage-method"></a><span data-ttu-id="b4089-106">IWMDRMLicenseManagement ::P méthode rocessLicenseDeletionMessage</span><span class="sxs-lookup"><span data-stu-id="b4089-106">IWMDRMLicenseManagement::ProcessLicenseDeletionMessage method</span></span>

<span data-ttu-id="b4089-107">La méthode **ProcessLicenseDeletion** supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.</span><span class="sxs-lookup"><span data-stu-id="b4089-107">The **ProcessLicenseDeletion** method deletes a license that was imported for content originally protected with another content protection system.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4089-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b4089-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseDeletionMessage(
  [in] BSTR bstrDeletionMessage
);
```



## <a name="parameters"></a><span data-ttu-id="b4089-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b4089-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4089-110">*bstrDeletionMessage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b4089-110">*bstrDeletionMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b4089-111">Message identifiant la licence à supprimer.</span><span class="sxs-lookup"><span data-stu-id="b4089-111">Message identifying the license to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4089-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b4089-112">Return value</span></span>

<span data-ttu-id="b4089-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b4089-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b4089-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b4089-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b4089-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b4089-115">Return code</span></span>                                                                          | <span data-ttu-id="b4089-116">Description</span><span class="sxs-lookup"><span data-stu-id="b4089-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b4089-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b4089-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b4089-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b4089-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b4089-119">Notes</span><span class="sxs-lookup"><span data-stu-id="b4089-119">Remarks</span></span>

<span data-ttu-id="b4089-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="b4089-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4089-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4089-121">Requirements</span></span>



| <span data-ttu-id="b4089-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4089-122">Requirement</span></span> | <span data-ttu-id="b4089-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4089-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4089-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4089-124">Header</span></span><br/> | <dl> <span data-ttu-id="b4089-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b4089-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4089-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b4089-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4089-127">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="b4089-127">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





