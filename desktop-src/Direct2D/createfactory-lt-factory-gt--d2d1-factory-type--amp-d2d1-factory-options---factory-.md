---
title: Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
description: Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. | Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) (D2d1. h)
ms.assetid: 618d7fbc-3801-4507-8774-4e1f4f36af44
keywords:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE, D2D1_FACTORY_OPTIONS, Factory) fonction Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,D2D1_FACTORY_OPTIONS ,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b25e6588ef79b234402742d473982910255f4230
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106522332"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typed2d1_factory_optionsfactory-function"></a><span data-ttu-id="e27e3-105">D2D1CreateFactory <Factory> ( \_ type de fabrique d2d1 \_ , \_ OPTIONS de fabrique d2d1 \_&, Factory \* \* ) (fonction)</span><span class="sxs-lookup"><span data-stu-id="e27e3-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,D2D1\_FACTORY\_OPTIONS&,Factory\*\*) Function</span></span>

<span data-ttu-id="e27e3-106">Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="e27e3-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __in CONST D2D1_FACTORY_OPTIONS &factoryOptions,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="e27e3-107">Paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="e27e3-107">Template Parameters</span></span>



| <span data-ttu-id="e27e3-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e27e3-108">Parameter</span></span> | <span data-ttu-id="e27e3-109">Description</span><span class="sxs-lookup"><span data-stu-id="e27e3-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="e27e3-110">*Fabrique*</span><span class="sxs-lookup"><span data-stu-id="e27e3-110">*Factory*</span></span> | <span data-ttu-id="e27e3-111">Type de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) à créer.</span><span class="sxs-lookup"><span data-stu-id="e27e3-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="e27e3-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e27e3-112">Parameters</span></span>



| <span data-ttu-id="e27e3-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="e27e3-113">Parameter</span></span>        | <span data-ttu-id="e27e3-114">Description</span><span class="sxs-lookup"><span data-stu-id="e27e3-114">Description</span></span>                                                                     |
|------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="e27e3-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="e27e3-115">*factoryType*</span></span>    | <span data-ttu-id="e27e3-116">Le modèle de thread de la fabrique et les ressources qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="e27e3-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="e27e3-117">*factoryOptions*</span><span class="sxs-lookup"><span data-stu-id="e27e3-117">*factoryOptions*</span></span> | <span data-ttu-id="e27e3-118">Niveau de détail fourni à la couche de débogage.</span><span class="sxs-lookup"><span data-stu-id="e27e3-118">The level of detail provided to the debugging layer.</span></span>                            |
| <span data-ttu-id="e27e3-119">*usine*</span><span class="sxs-lookup"><span data-stu-id="e27e3-119">*factory*</span></span>        | <span data-ttu-id="e27e3-120">Lorsque cette méthode est retournée, contient l’adresse d’un pointeur vers la nouvelle fabrique.</span><span class="sxs-lookup"><span data-stu-id="e27e3-120">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="e27e3-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e27e3-121">Return Value</span></span>

<span data-ttu-id="e27e3-122">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e27e3-122">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e27e3-123">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e27e3-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27e3-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e27e3-124">Requirements</span></span>



| <span data-ttu-id="e27e3-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e27e3-125">Requirement</span></span> | <span data-ttu-id="e27e3-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e27e3-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e27e3-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e27e3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e27e3-128">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e27e3-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="e27e3-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e27e3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e27e3-130">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="e27e3-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="e27e3-131">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e27e3-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="e27e3-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="e27e3-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="e27e3-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="e27e3-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="e27e3-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="e27e3-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="e27e3-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e27e3-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="e27e3-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e27e3-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="e27e3-137">DLL</span><span class="sxs-lookup"><span data-stu-id="e27e3-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e27e3-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e27e3-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

