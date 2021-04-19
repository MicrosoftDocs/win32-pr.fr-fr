---
title: IWMSecureBuffer, méthode de chiffrement (wmdrmsdk. h)
description: La méthode Encrypt chiffre un pointeur de données.
ms.assetid: da391dcb-3ef8-4c09-bca6-507f67a24ee6
keywords:
- Méthode Encrypt Windows Media format
- Méthode Encrypt Windows Media format, interface IWMSecureBuffer
- Interface IWMSecureBuffer Windows Media format, méthode Encrypt
topic_type:
- apiref
api_name:
- IWMSecureBuffer.Encrypt
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7758903de5f4a68cddffee982ad457d03ae6094
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543975"
---
# <a name="iwmsecurebufferencrypt-method"></a><span data-ttu-id="efe65-106">IWMSecureBuffer :: Encrypt, méthode</span><span class="sxs-lookup"><span data-stu-id="efe65-106">IWMSecureBuffer::Encrypt method</span></span>

<span data-ttu-id="efe65-107">La méthode **Encrypt** chiffre un pointeur de données.</span><span class="sxs-lookup"><span data-stu-id="efe65-107">The **Encrypt** method encrypts a data pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="efe65-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efe65-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in] IWMSecureChannel *pSecureChannel
);
```



## <a name="parameters"></a><span data-ttu-id="efe65-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efe65-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efe65-110">*pSecureChannel* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="efe65-110">*pSecureChannel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efe65-111">Pointeur vers une interface de canal sécurisé contenant le pointeur de données à chiffrer.</span><span class="sxs-lookup"><span data-stu-id="efe65-111">Pointer to a secure channel interface containing the data pointer to encrypt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efe65-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="efe65-112">Return value</span></span>

<span data-ttu-id="efe65-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="efe65-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="efe65-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efe65-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="efe65-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="efe65-115">Return code</span></span>                                                                          | <span data-ttu-id="efe65-116">Description</span><span class="sxs-lookup"><span data-stu-id="efe65-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="efe65-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efe65-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="efe65-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="efe65-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efe65-119">Notes</span><span class="sxs-lookup"><span data-stu-id="efe65-119">Remarks</span></span>

<span data-ttu-id="efe65-120">Utilisez cette méthode pour chiffrer les pointeurs de données afin qu’ils puissent être envoyés à travers les limites des DLL.</span><span class="sxs-lookup"><span data-stu-id="efe65-120">Use this method to encrypt data pointers so they can be sent across DLL boundaries.</span></span>

## <a name="requirements"></a><span data-ttu-id="efe65-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efe65-121">Requirements</span></span>



| <span data-ttu-id="efe65-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efe65-122">Requirement</span></span> | <span data-ttu-id="efe65-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="efe65-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="efe65-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="efe65-124">Header</span></span><br/>  | <dl> <span data-ttu-id="efe65-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="efe65-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="efe65-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="efe65-126">Library</span></span><br/> | <dl> <span data-ttu-id="efe65-127"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efe65-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efe65-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efe65-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe65-129">**Déchiffrer**</span><span class="sxs-lookup"><span data-stu-id="efe65-129">**Decrypt**</span></span>](iwmsecurebuffer-decrypt.md)
</dt> <dt>

[<span data-ttu-id="efe65-130">**Interface IWMSecureBuffer**</span><span class="sxs-lookup"><span data-stu-id="efe65-130">**IWMSecureBuffer Interface**</span></span>](iwmsecurebuffer.md)
</dt> </dl>

 

 





