---
title: WMDRMCreateProvider, fonction (wmdrmsdk. h)
description: La fonction WMDRMCreateProvider crée une fabrique de classes qui peut créer les autres objets des API étendues du client Windows Media DRM.
ms.assetid: 25ec2fbf-136a-4f40-b2d3-f35b42178c60
keywords:
- WMDRMCreateProvider fonction Windows Media format
topic_type:
- apiref
api_name:
- WMDRMCreateProvider
api_location:
- Wmdrmsdk.dll
- Ext-MS-Win-mm-wmdrmsdk-l1-1-0.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cdf7a102d969ce916f8a5692d994c183305409a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528654"
---
# <a name="wmdrmcreateprovider-function"></a><span data-ttu-id="b9bb6-104">WMDRMCreateProvider fonction)</span><span class="sxs-lookup"><span data-stu-id="b9bb6-104">WMDRMCreateProvider function</span></span>

<span data-ttu-id="b9bb6-105">La fonction **WMDRMCreateProvider** crée une fabrique de classes qui peut créer les autres objets des API étendues du client Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b9bb6-105">The **WMDRMCreateProvider** function creates a class factory that can create the other objects of the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="b9bb6-106">Cette fonction ne nécessite pas de bibliothèque de stubs de la part de Microsoft et crée des objets qui ne prennent pas en charge les fonctionnalités DRM protégées.</span><span class="sxs-lookup"><span data-stu-id="b9bb6-106">This function does not require a stub library from Microsoft and creates objects that do not support the protected DRM features.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9bb6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b9bb6-107">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE WMDRMCreateProvider(
  _Out_ IWMDRMProvider **ppDRMProvider
);
```



## <a name="parameters"></a><span data-ttu-id="b9bb6-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b9bb6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9bb6-109">*ppDRMProvider* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b9bb6-109">*ppDRMProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9bb6-110">Reçoit un pointeur vers l’interface [**IWMDRMProvider**](iwmdrmprovider.md) de l’objet nouvellement créé.</span><span class="sxs-lookup"><span data-stu-id="b9bb6-110">Receives a pointer to the [**IWMDRMProvider**](iwmdrmprovider.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9bb6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b9bb6-111">Return value</span></span>

<span data-ttu-id="b9bb6-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b9bb6-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b9bb6-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b9bb6-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b9bb6-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b9bb6-114">Return code</span></span>                                                                          | <span data-ttu-id="b9bb6-115">Description</span><span class="sxs-lookup"><span data-stu-id="b9bb6-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b9bb6-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b9bb6-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b9bb6-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9bb6-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b9bb6-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b9bb6-118">Requirements</span></span>



| <span data-ttu-id="b9bb6-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b9bb6-119">Requirement</span></span> | <span data-ttu-id="b9bb6-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="b9bb6-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9bb6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="b9bb6-121">Header</span></span><br/>  | <dl> <span data-ttu-id="b9bb6-122"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9bb6-122"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9bb6-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b9bb6-123">Library</span></span><br/> | <dl> <span data-ttu-id="b9bb6-124"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9bb6-124"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |
| <span data-ttu-id="b9bb6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b9bb6-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b9bb6-126"><dt>Wmdrmsdk.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9bb6-126"><dt>Wmdrmsdk.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9bb6-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9bb6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9bb6-128">**Fonctions**</span><span class="sxs-lookup"><span data-stu-id="b9bb6-128">**Functions**</span></span>](drm-functions.md)
</dt> <dt>

[<span data-ttu-id="b9bb6-129">**WMDRMCreateProtectedProvider**</span><span class="sxs-lookup"><span data-stu-id="b9bb6-129">**WMDRMCreateProtectedProvider**</span></span>](wmdrmcreateprotectedprovider.md)
</dt> </dl>

 

 





