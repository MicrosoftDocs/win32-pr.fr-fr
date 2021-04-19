---
title: WMDRMCreateProtectedProvider, fonction (wmdrmsdk. h)
description: La fonction WMDRMCreateProtectedProvider crée une fabrique de classes qui peut créer les autres objets des API étendues du client Windows Media DRM.
ms.assetid: 0882062f-48a2-43bc-8853-a8a3d6bc2f52
keywords:
- WMDRMCreateProtectedProvider fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCreateProtectedProvider
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f046de906c7753fa200de5075cf2064721940b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537368"
---
# <a name="wmdrmcreateprotectedprovider-function"></a><span data-ttu-id="0ae47-104">WMDRMCreateProtectedProvider fonction)</span><span class="sxs-lookup"><span data-stu-id="0ae47-104">WMDRMCreateProtectedProvider function</span></span>

<span data-ttu-id="0ae47-105">La fonction **WMDRMCreateProtectedProvider** crée une fabrique de classes qui peut créer les autres objets des API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="0ae47-105">The **WMDRMCreateProtectedProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="0ae47-106">Cette fonction requiert une bibliothèque de stubs de la part de Microsoft et crée des objets qui prennent en charge les fonctionnalités DRM protégées.</span><span class="sxs-lookup"><span data-stu-id="0ae47-106">This function requires a stub library from Microsoft and creates objects that support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ae47-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0ae47-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProtectedProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="0ae47-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0ae47-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ae47-109">*ppDRMProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0ae47-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ae47-110">Reçoit un pointeur vers l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="0ae47-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ae47-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0ae47-111">Return value</span></span>

<span data-ttu-id="0ae47-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="0ae47-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0ae47-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="0ae47-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0ae47-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="0ae47-114">Return code</span></span>                                                                          | <span data-ttu-id="0ae47-115">Description</span><span class="sxs-lookup"><span data-stu-id="0ae47-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0ae47-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0ae47-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0ae47-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="0ae47-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0ae47-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0ae47-118">Remarks</span></span>

<span data-ttu-id="0ae47-119">Aucun.</span><span class="sxs-lookup"><span data-stu-id="0ae47-119">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ae47-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0ae47-120">Requirements</span></span>



| <span data-ttu-id="0ae47-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0ae47-121">Requirement</span></span> | <span data-ttu-id="0ae47-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="0ae47-122">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0ae47-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="0ae47-123">Header</span></span><br/> | <dl> <span data-ttu-id="0ae47-124"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ae47-124"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ae47-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0ae47-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ae47-126">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="0ae47-126">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="0ae47-127">**WMDRMCreateProvider**</span><span class="sxs-lookup"><span data-stu-id="0ae47-127">**WMDRMCreateProvider**</span></span>](wmdrmcreateprovider.md)
</dt> </dl>

 

 





