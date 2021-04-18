---
title: Méthode de déchiffrement IWMDRMDecrypt (wmdrmsdk. h)
description: La méthode Decrypt déchiffre une mémoire tampon de données sur place.
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- Méthode de déchiffrement Windows Media format
- Méthode Decrypt Windows Media format, interface IWMDRMDecrypt
- Interface IWMDRMDecrypt Windows Media format, méthode Decrypt
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532900"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="dfa10-106">IWMDRMDecrypt ::D méthode ecrypt</span><span class="sxs-lookup"><span data-stu-id="dfa10-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="dfa10-107">La méthode **Decrypt** déchiffre une mémoire tampon de données sur place.</span><span class="sxs-lookup"><span data-stu-id="dfa10-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="dfa10-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfa10-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="dfa10-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfa10-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfa10-110">*pbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="dfa10-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa10-111">Données à déchiffrer.</span><span class="sxs-lookup"><span data-stu-id="dfa10-111">Data to be decrypted.</span></span> <span data-ttu-id="dfa10-112">Si la méthode est réussie, ces données sont déchiffrées lors du retour.</span><span class="sxs-lookup"><span data-stu-id="dfa10-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="dfa10-113">*cbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfa10-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa10-114">Taille des données en octets.</span><span class="sxs-lookup"><span data-stu-id="dfa10-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="dfa10-115">*pWMCryptoData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfa10-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfa10-116">Pointeur vers une structure [**WMDRMCryptoData**](wmdrmcryptodata.md) contenant des paramètres supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="dfa10-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="dfa10-117">Peut avoir la **valeur null** si le contenu a été chiffré à l’aide des paramètres par défaut.</span><span class="sxs-lookup"><span data-stu-id="dfa10-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfa10-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfa10-118">Return value</span></span>

<span data-ttu-id="dfa10-119">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="dfa10-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dfa10-120">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dfa10-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dfa10-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="dfa10-121">Return code</span></span>                                                                          | <span data-ttu-id="dfa10-122">Description</span><span class="sxs-lookup"><span data-stu-id="dfa10-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dfa10-123"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dfa10-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dfa10-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfa10-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dfa10-125">Notes</span><span class="sxs-lookup"><span data-stu-id="dfa10-125">Remarks</span></span>

<span data-ttu-id="dfa10-126">Aucun.</span><span class="sxs-lookup"><span data-stu-id="dfa10-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfa10-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfa10-127">Requirements</span></span>



| <span data-ttu-id="dfa10-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfa10-128">Requirement</span></span> | <span data-ttu-id="dfa10-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfa10-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="dfa10-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfa10-130">Header</span></span><br/> | <dl> <span data-ttu-id="dfa10-131"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfa10-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfa10-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfa10-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfa10-133">**Interface IWMDRMDecrypt**</span><span class="sxs-lookup"><span data-stu-id="dfa10-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="dfa10-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="dfa10-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





