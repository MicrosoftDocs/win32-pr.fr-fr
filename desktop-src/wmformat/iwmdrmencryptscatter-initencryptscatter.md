---
title: Méthode IWMDRMEncryptScatter InitEncryptScatter (wmdrmsdk. h)
description: La méthode InitEncryptScatter Initialise l’interface IWMDRMEncryptScatter à utiliser.
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- Méthode InitEncryptScatter format Windows Media
- Méthode InitEncryptScatter format Windows Media, interface IWMDRMEncryptScatter
- Interface IWMDRMEncryptScatter Windows Media format, méthode InitEncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106524033"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="f7eb4-106">IWMDRMEncryptScatter :: InitEncryptScatter, méthode</span><span class="sxs-lookup"><span data-stu-id="f7eb4-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="f7eb4-107">La méthode **InitEncryptScatter** Initialise l’interface **IWMDRMEncryptScatter** à utiliser.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7eb4-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f7eb4-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="f7eb4-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f7eb4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7eb4-110">*cStreams* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7eb4-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7eb4-111">Nombre d’éléments dans le tableau *rgInfos* .</span><span class="sxs-lookup"><span data-stu-id="f7eb4-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="f7eb4-112">Il s’agit également du nombre de flux inclus dans les données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="f7eb4-113">*rgInfos* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f7eb4-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7eb4-114">Tableau d’une ou de plusieurs structures d' [**\_ informations de \_ diffusion \_ de chiffrement WMDRM**](wmdrm-encrypt-scatter-info.md) .</span><span class="sxs-lookup"><span data-stu-id="f7eb4-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="f7eb4-115">Chaque élément contient des informations de chiffrement pour un flux.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="f7eb4-116">Le nombre d’éléments de ce tableau doit être égal à la valeur de *cStreams*.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7eb4-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f7eb4-117">Return value</span></span>

<span data-ttu-id="f7eb4-118">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f7eb4-119">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f7eb4-120">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f7eb4-120">Return code</span></span>                                                                          | <span data-ttu-id="f7eb4-121">Description</span><span class="sxs-lookup"><span data-stu-id="f7eb4-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f7eb4-122"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f7eb4-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f7eb4-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f7eb4-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f7eb4-124">Notes</span><span class="sxs-lookup"><span data-stu-id="f7eb4-124">Remarks</span></span>

<span data-ttu-id="f7eb4-125">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f7eb4-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7eb4-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f7eb4-126">Requirements</span></span>



| <span data-ttu-id="f7eb4-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f7eb4-127">Requirement</span></span> | <span data-ttu-id="f7eb4-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7eb4-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f7eb4-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f7eb4-129">Header</span></span><br/> | <dl> <span data-ttu-id="f7eb4-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7eb4-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7eb4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7eb4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7eb4-132">**EncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="f7eb4-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="f7eb4-133">**Interface IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="f7eb4-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





