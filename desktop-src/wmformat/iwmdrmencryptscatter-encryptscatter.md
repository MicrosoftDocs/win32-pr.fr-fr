---
title: Méthode IWMDRMEncryptScatter EncryptScatter (wmdrmsdk. h)
description: La méthode EncryptScatter déchiffre et chiffre les données.
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- Méthode EncryptScatter format Windows Media
- Méthode EncryptScatter format Windows Media, interface IWMDRMEncryptScatter
- Interface IWMDRMEncryptScatter Windows Media format, méthode EncryptScatter
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542428"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="89e54-106">IWMDRMEncryptScatter :: EncryptScatter, méthode</span><span class="sxs-lookup"><span data-stu-id="89e54-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="89e54-107">La méthode **EncryptScatter** déchiffre et chiffre les données.</span><span class="sxs-lookup"><span data-stu-id="89e54-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="89e54-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89e54-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="89e54-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89e54-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89e54-110">*cBlocks* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89e54-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89e54-111">Nombre d’éléments dans le tableau *rgBlocks* .</span><span class="sxs-lookup"><span data-stu-id="89e54-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="89e54-112">*rgBlocks* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89e54-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89e54-113">Tableau d’une ou de plusieurs structures de [**\_ blocs de \_ diffusion \_ de chiffrement WMDRM**](wmdrm-encrypt-scatter-block.md) .</span><span class="sxs-lookup"><span data-stu-id="89e54-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="89e54-114">Chaque élément décrit un bloc de données à déchiffrer et à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="89e54-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="89e54-115">*pWMCryptoData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89e54-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89e54-116">Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) qui contient des paramètres de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="89e54-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="89e54-117">Affectez la valeur **null** pour utiliser les paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="89e54-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="89e54-118">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="89e54-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89e54-119">Taille de la mémoire tampon de données de sortie passée en tant que *pbOutput*.</span><span class="sxs-lookup"><span data-stu-id="89e54-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="89e54-120">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="89e54-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="89e54-121">Mémoire tampon de sortie.</span><span class="sxs-lookup"><span data-stu-id="89e54-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89e54-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="89e54-122">Return value</span></span>

<span data-ttu-id="89e54-123">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="89e54-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="89e54-124">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="89e54-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="89e54-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="89e54-125">Return code</span></span>                                                                          | <span data-ttu-id="89e54-126">Description</span><span class="sxs-lookup"><span data-stu-id="89e54-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="89e54-127"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="89e54-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="89e54-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="89e54-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="89e54-129">Notes</span><span class="sxs-lookup"><span data-stu-id="89e54-129">Remarks</span></span>

<span data-ttu-id="89e54-130">Aucun.</span><span class="sxs-lookup"><span data-stu-id="89e54-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="89e54-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="89e54-131">Requirements</span></span>



| <span data-ttu-id="89e54-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="89e54-132">Requirement</span></span> | <span data-ttu-id="89e54-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="89e54-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="89e54-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="89e54-134">Header</span></span><br/> | <dl> <span data-ttu-id="89e54-135"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="89e54-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89e54-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="89e54-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89e54-137">**InitEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="89e54-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="89e54-138">**Interface IWMDRMEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="89e54-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





