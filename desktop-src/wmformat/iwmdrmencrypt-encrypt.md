---
title: IWMDRMEncrypt, méthode de chiffrement (wmdrmsdk. h)
description: La méthode Encrypt chiffre une mémoire tampon de données en place.
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- Méthode Encrypt Windows Media format
- Méthode Encrypt Windows Media format, interface IWMDRMEncrypt
- Interface IWMDRMEncrypt Windows Media format, méthode Encrypt
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528371"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="fa7d1-106">IWMDRMEncrypt :: Encrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="fa7d1-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="fa7d1-107">La méthode **Encrypt** chiffre une mémoire tampon de données en place.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="fa7d1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fa7d1-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="fa7d1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fa7d1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fa7d1-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="fa7d1-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7d1-111">Données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-111">Data to encrypt.</span></span> <span data-ttu-id="fa7d1-112">Si la méthode est réussie, les données sont chiffrées lors du retour.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="fa7d1-113">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa7d1-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7d1-114">Taille des données en octets.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="fa7d1-115">*pWMCryptoData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fa7d1-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fa7d1-116">Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) contenant des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="fa7d1-117">Affectez la valeur **null** pour utiliser les valeurs de chiffrement par défaut.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fa7d1-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fa7d1-118">Return value</span></span>

<span data-ttu-id="fa7d1-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fa7d1-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fa7d1-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="fa7d1-121">Return code</span></span>                                                                          | <span data-ttu-id="fa7d1-122">Description</span><span class="sxs-lookup"><span data-stu-id="fa7d1-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fa7d1-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fa7d1-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fa7d1-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa7d1-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="fa7d1-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fa7d1-125">Remarks</span></span>

<span data-ttu-id="fa7d1-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="fa7d1-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="fa7d1-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa7d1-127">Requirements</span></span>



| <span data-ttu-id="fa7d1-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa7d1-128">Requirement</span></span> | <span data-ttu-id="fa7d1-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa7d1-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fa7d1-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="fa7d1-130">Header</span></span><br/> | <dl> <span data-ttu-id="fa7d1-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="fa7d1-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fa7d1-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa7d1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa7d1-133">**Interface IWMDRMEncrypt**</span><span class="sxs-lookup"><span data-stu-id="fa7d1-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="fa7d1-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="fa7d1-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





