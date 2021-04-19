---
title: Méthode de déchiffrement IWMSecureBuffer (wmdrmsdk. h)
description: La méthode Decrypt déchiffre un pointeur de données qui a été chiffré en appelant la méthode Encrypt.
ms.assetid: 15cedb56-686a-4a3c-81a5-b1797cfe0838
keywords:
- Méthode de déchiffrement Windows Media format
- Méthode Decrypt Windows Media format, interface IWMSecureBuffer
- Interface IWMSecureBuffer Windows Media format, méthode Decrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Decrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6f48ae389090840e085c90b0bc5444e7cd6784e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106534917"
---
# <a name="iwmsecurebufferdecrypt-method"></a><span data-ttu-id="beb4d-106">IWMSecureBuffer ::D méthode ecrypt</span><span class="sxs-lookup"><span data-stu-id="beb4d-106">IWMSecureBuffer::Decrypt method</span></span>

<span data-ttu-id="beb4d-107">La méthode **Decrypt** déchiffre un pointeur de données qui a été chiffré en appelant la méthode [**Encrypt**](iwmsecurebuffer-encrypt.md) .</span><span class="sxs-lookup"><span data-stu-id="beb4d-107">The **Decrypt** method decrypts a data pointer that was encrypted by calling the [**Encrypt**](iwmsecurebuffer-encrypt.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="beb4d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="beb4d-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="beb4d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="beb4d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="beb4d-110">*pSecureChannel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="beb4d-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="beb4d-111">Pointeur vers une interface de canal sécurisé contenant le pointeur de données chiffrées.</span><span class="sxs-lookup"><span data-stu-id="beb4d-111">Pointer to a secure channel interface containing the encrypted data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="beb4d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="beb4d-112">Return value</span></span>

<span data-ttu-id="beb4d-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="beb4d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="beb4d-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="beb4d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="beb4d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="beb4d-115">Return code</span></span>                                                                          | <span data-ttu-id="beb4d-116">Description</span><span class="sxs-lookup"><span data-stu-id="beb4d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="beb4d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="beb4d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="beb4d-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="beb4d-119">Notes</span><span class="sxs-lookup"><span data-stu-id="beb4d-119">Remarks</span></span>

<span data-ttu-id="beb4d-120">Aucun.</span><span class="sxs-lookup"><span data-stu-id="beb4d-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="beb4d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="beb4d-121">Requirements</span></span>



| <span data-ttu-id="beb4d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="beb4d-122">Requirement</span></span> | <span data-ttu-id="beb4d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="beb4d-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="beb4d-124">Header</span></span><br/>  | <dl> <span data-ttu-id="beb4d-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="beb4d-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="beb4d-126">Library</span></span><br/> | <dl> <span data-ttu-id="beb4d-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="beb4d-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb4d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="beb4d-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4d-129">**Encrypt (Chiffrer)**</span><span class="sxs-lookup"><span data-stu-id="beb4d-129">**Encrypt**</span></span>](iwmsecurebuffer-encrypt.md)
</dt> <dt>

[<span data-ttu-id="beb4d-130">**Interface IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="beb4d-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





