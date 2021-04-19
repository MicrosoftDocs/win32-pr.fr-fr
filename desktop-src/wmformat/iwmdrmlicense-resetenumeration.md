---
title: Méthode IWMDRMLicense ResetEnumeration (wmdrmsdk. h)
description: La méthode ResetEnumeration réinitialise la liste de licences à son état d’origine. La licence active devient la première licence de la liste.
ms.assetid: cb5a31a8-ee25-44d6-81ca-746c379cb99e
keywords:
- Méthode ResetEnumeration format Windows Media
- Méthode ResetEnumeration format Windows Media, interface IWMDRMLicense
- Interface IWMDRMLicense Windows Media format, méthode ResetEnumeration
topic_type:
- apiref
api_name:
- IWMDRMLicense.ResetEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510c05b4c974051d9902ed2d30d9cdf99956af
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528704"
---
# <a name="iwmdrmlicenseresetenumeration-method"></a><span data-ttu-id="bb942-107">IWMDRMLicense :: ResetEnumeration, méthode</span><span class="sxs-lookup"><span data-stu-id="bb942-107">IWMDRMLicense::ResetEnumeration method</span></span>

<span data-ttu-id="bb942-108">La méthode **ResetEnumeration** réinitialise la liste de licences à son état d’origine.</span><span class="sxs-lookup"><span data-stu-id="bb942-108">The **ResetEnumeration** method resets the license list to its original state.</span></span> <span data-ttu-id="bb942-109">La licence active devient la première licence de la liste.</span><span class="sxs-lookup"><span data-stu-id="bb942-109">The active license becomes the first license in the list.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb942-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bb942-110">Syntax</span></span>


```C++
HRESULT ResetEnumeration();
```



## <a name="parameters"></a><span data-ttu-id="bb942-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bb942-111">Parameters</span></span>

<span data-ttu-id="bb942-112">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="bb942-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb942-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bb942-113">Return value</span></span>

<span data-ttu-id="bb942-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bb942-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bb942-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bb942-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bb942-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="bb942-116">Return code</span></span>                                                                                                | <span data-ttu-id="bb942-117">Description</span><span class="sxs-lookup"><span data-stu-id="bb942-117">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="bb942-118"><dt>**le \_ RIV de la messagerie DRM E est \_ \_ \_ trop \_ petit**</dt></span><span class="sxs-lookup"><span data-stu-id="bb942-118"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="bb942-119">Une liste de révocation de contenu mise à jour est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="bb942-119">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="bb942-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bb942-120"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="bb942-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="bb942-121">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="bb942-122">Notes</span><span class="sxs-lookup"><span data-stu-id="bb942-122">Remarks</span></span>

<span data-ttu-id="bb942-123">Aucun.</span><span class="sxs-lookup"><span data-stu-id="bb942-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb942-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb942-124">Requirements</span></span>



| <span data-ttu-id="bb942-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb942-125">Requirement</span></span> | <span data-ttu-id="bb942-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb942-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb942-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb942-127">Header</span></span><br/>  | <dl> <span data-ttu-id="bb942-128"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb942-128"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb942-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb942-129">Library</span></span><br/> | <dl> <span data-ttu-id="bb942-130"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb942-130"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb942-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb942-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb942-132">**Interface IWMDRMLicense**</span><span class="sxs-lookup"><span data-stu-id="bb942-132">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





