---
title: IWMDRMLicense CreateDecryptor, méthode (wmdrmsdk. h)
description: La méthode CreateDecryptor crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- Méthode CreateDecryptor format Windows Media
- Méthode CreateDecryptor format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode CreateDecryptor
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544416"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="02c95-106">IWMDRMLicense :: CreateDecryptor, méthode</span><span class="sxs-lookup"><span data-stu-id="02c95-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="02c95-107">La méthode **CreateDecryptor** crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.</span><span class="sxs-lookup"><span data-stu-id="02c95-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="02c95-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02c95-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="02c95-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02c95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02c95-110">*ppDecryptor* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="02c95-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02c95-111">Reçoit un pointeur vers l’interface [**IWMDRMDecrypt**](iwmdrmdecrypt.md) de l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="02c95-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02c95-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="02c95-112">Return value</span></span>

<span data-ttu-id="02c95-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="02c95-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="02c95-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="02c95-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="02c95-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="02c95-115">Return code</span></span>                                                                                                | <span data-ttu-id="02c95-116">Description</span><span class="sxs-lookup"><span data-stu-id="02c95-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="02c95-117"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="02c95-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="02c95-118">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="02c95-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="02c95-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02c95-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="02c95-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="02c95-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="02c95-121">Notes</span><span class="sxs-lookup"><span data-stu-id="02c95-121">Remarks</span></span>

<span data-ttu-id="02c95-122">Aucun.</span><span class="sxs-lookup"><span data-stu-id="02c95-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="02c95-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="02c95-123">Requirements</span></span>



| <span data-ttu-id="02c95-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="02c95-124">Requirement</span></span> | <span data-ttu-id="02c95-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="02c95-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="02c95-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="02c95-126">Header</span></span><br/> | <dl> <span data-ttu-id="02c95-127"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="02c95-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02c95-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="02c95-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02c95-129">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="02c95-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="02c95-130">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="02c95-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





