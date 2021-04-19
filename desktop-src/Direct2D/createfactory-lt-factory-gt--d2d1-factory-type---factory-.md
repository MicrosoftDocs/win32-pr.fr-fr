---
title: Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
description: Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D. | Fonction Factory D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) (D2d1. h)
ms.assetid: c1c25d51-15ea-4075-a896-bd6501bf68c1
keywords:
- Fonction de fabrique D2D1CreateFactory (D2D1_FACTORY_TYPE, Factory) Direct2D
topic_type:
- apiref
api_name:
- D2D1CreateFactory Factory (D2D1_FACTORY_TYPE,Factory ) Function
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c03400cec8c838ba561a7eb504674e074d7b3199
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106535785"
---
# <a name="d2d1createfactoryfactoryd2d1_factory_typefactory-function"></a><span data-ttu-id="c7105-105"><Factory>Fonction D2D1CreateFactory ( \_ \_ type de fabrique d2d1, Factory \* \* )</span><span class="sxs-lookup"><span data-stu-id="c7105-105">D2D1CreateFactory<Factory>(D2D1\_FACTORY\_TYPE,Factory\*\*) Function</span></span>

<span data-ttu-id="c7105-106">Crée un objet de fabrique qui peut être utilisé pour créer des ressources Direct2D.</span><span class="sxs-lookup"><span data-stu-id="c7105-106">Creates a factory object that can be used to create Direct2D resources.</span></span>

``` syntax
template<class Factory>
HRESULT D2D1CreateFactory(
    __in D2D1_FACTORY_TYPE factoryType,
    __out Factory **factory
);
```

## <a name="template-parameters"></a><span data-ttu-id="c7105-107">Paramètres de modèle</span><span class="sxs-lookup"><span data-stu-id="c7105-107">Template Parameters</span></span>



| <span data-ttu-id="c7105-108">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c7105-108">Parameter</span></span> | <span data-ttu-id="c7105-109">Description</span><span class="sxs-lookup"><span data-stu-id="c7105-109">Description</span></span>                                                 |
|-----------|-------------------------------------------------------------|
| <span data-ttu-id="c7105-110">*Fabrique*</span><span class="sxs-lookup"><span data-stu-id="c7105-110">*Factory*</span></span> | <span data-ttu-id="c7105-111">Type de [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) à créer.</span><span class="sxs-lookup"><span data-stu-id="c7105-111">The type of [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) to create.</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="c7105-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7105-112">Parameters</span></span>



| <span data-ttu-id="c7105-113">Paramètre</span><span class="sxs-lookup"><span data-stu-id="c7105-113">Parameter</span></span>     | <span data-ttu-id="c7105-114">Description</span><span class="sxs-lookup"><span data-stu-id="c7105-114">Description</span></span>                                                                     |
|---------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c7105-115">*factoryType*</span><span class="sxs-lookup"><span data-stu-id="c7105-115">*factoryType*</span></span> | <span data-ttu-id="c7105-116">Le modèle de thread de la fabrique et les ressources qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="c7105-116">The threading model of the factory and the resources it creates.</span></span>                |
| <span data-ttu-id="c7105-117">*usine*</span><span class="sxs-lookup"><span data-stu-id="c7105-117">*factory*</span></span>     | <span data-ttu-id="c7105-118">Lorsque cette méthode est retournée, contient l’adresse d’un pointeur vers la nouvelle fabrique.</span><span class="sxs-lookup"><span data-stu-id="c7105-118">When this method returns, contains the address of a pointer to the new factory.</span></span> |



 

## <a name="return-value"></a><span data-ttu-id="c7105-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c7105-119">Return Value</span></span>

<span data-ttu-id="c7105-120">Si la méthode est réussie, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c7105-120">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c7105-121">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c7105-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="examples"></a><span data-ttu-id="c7105-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="c7105-122">Examples</span></span>

<span data-ttu-id="c7105-123">L’exemple suivant crée une fabrique.</span><span class="sxs-lookup"><span data-stu-id="c7105-123">The following example creates a factory.</span></span>


```C++
HRESULT DemoApp::CreateDeviceIndependentResources()
{
    HRESULT hr = S_OK;

    // Create a Direct2D factory.
    hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &m_pDirect2dFactory);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="c7105-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7105-124">Requirements</span></span>



| <span data-ttu-id="c7105-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7105-125">Requirement</span></span> | <span data-ttu-id="c7105-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7105-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7105-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7105-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c7105-128">Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7105-128">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="c7105-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7105-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c7105-130">Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="c7105-130">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="c7105-131">Téléphone minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7105-131">Minimum supported phone</span></span><br/>  | <span data-ttu-id="c7105-132">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]</span><span class="sxs-lookup"><span data-stu-id="c7105-132">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/>                                                  |
| <span data-ttu-id="c7105-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="c7105-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7105-134"><dt>D2d1. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7105-134"><dt>D2d1.h</dt></span></span> </dl>                                                        |
| <span data-ttu-id="c7105-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c7105-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="c7105-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c7105-136"><dt>D2d1.lib</dt></span></span> </dl>                                                      |
| <span data-ttu-id="c7105-137">DLL</span><span class="sxs-lookup"><span data-stu-id="c7105-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7105-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7105-138"><dt>D2d1.dll</dt></span></span> </dl>                                                      |



 

