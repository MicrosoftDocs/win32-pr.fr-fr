---
title: IWMDRMLicense CreateEncryptor, méthode (wmdrmsdk. h)
description: La méthode CreateEncryptor crée un objet chiffreur à l’aide des paramètres de la licence actuelle.
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- Méthode CreateEncryptor format Windows Media
- Méthode CreateEncryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, CreateEncryptor, méthode
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528145"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="83efc-106">IWMDRMLicense :: CreateEncryptor, méthode</span><span class="sxs-lookup"><span data-stu-id="83efc-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="83efc-107">La méthode **CreateEncryptor** crée un objet chiffreur à l’aide des paramètres de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="83efc-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="83efc-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83efc-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="83efc-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83efc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83efc-110">*ppEncryptor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83efc-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83efc-111">Reçoit un pointeur vers l’interface [**IWMDRMEncrypt**](iwmdrmencrypt.md) de l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="83efc-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83efc-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83efc-112">Return value</span></span>

<span data-ttu-id="83efc-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="83efc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="83efc-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="83efc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="83efc-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="83efc-115">Return code</span></span>                                                                                                | <span data-ttu-id="83efc-116">Description</span><span class="sxs-lookup"><span data-stu-id="83efc-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="83efc-117"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="83efc-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="83efc-118">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="83efc-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="83efc-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="83efc-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="83efc-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="83efc-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="83efc-121">Notes</span><span class="sxs-lookup"><span data-stu-id="83efc-121">Remarks</span></span>

<span data-ttu-id="83efc-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="83efc-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="83efc-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83efc-123">Requirements</span></span>



| <span data-ttu-id="83efc-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83efc-124">Requirement</span></span> | <span data-ttu-id="83efc-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="83efc-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83efc-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="83efc-126">Header</span></span><br/> | <dl> <span data-ttu-id="83efc-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="83efc-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83efc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83efc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83efc-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="83efc-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="83efc-130">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="83efc-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





