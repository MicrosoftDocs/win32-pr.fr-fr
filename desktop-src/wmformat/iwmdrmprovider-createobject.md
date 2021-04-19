---
title: IWMDRMProvider CreateObject, méthode (wmdrmsdk. h)
description: La méthode CreateObject récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.
ms.assetid: d408f7f3-9e49-4747-ac8f-d39db31d1240
keywords:
- Méthode CreateObject Windows Media format
- Méthode CreateObject Windows Media format, interface IWMDRMProvider
- Interface IWMDRMProvider Windows Media format, CreateObject, méthode
topic_type:
- apiref
api_name:
- IWMDRMProvider.CreateObject
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0422138391b0d6f5e38fbc81fd5141bd3d8535
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523506"
---
# <a name="iwmdrmprovidercreateobject-method"></a><span data-ttu-id="26ff1-106">IWMDRMProvider :: CreateObject, méthode</span><span class="sxs-lookup"><span data-stu-id="26ff1-106">IWMDRMProvider::CreateObject method</span></span>

<span data-ttu-id="26ff1-107">La méthode **CreateObject** récupère un pointeur vers une interface spécifiée, en créant l’objet d’implémentation, si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="26ff1-107">The **CreateObject** method retrieves a pointer to a specified interface, creating the implementing object if needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ff1-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="26ff1-108">Syntax</span></span>


```C++
HRESULT CreateObject(
  [in]  REFIID riid,
  [out] void   **ppvObject
);
```



## <a name="parameters"></a><span data-ttu-id="26ff1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="26ff1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26ff1-110">*riid* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="26ff1-110">*riid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26ff1-111">Identificateur de l’interface à créer.</span><span class="sxs-lookup"><span data-stu-id="26ff1-111">Identifier of the interface to be created.</span></span> <span data-ttu-id="26ff1-112">Définissez l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="26ff1-112">Set to one of the following values.</span></span>

-   <span data-ttu-id="26ff1-113">IID \_ IWMDRMLicenseManagement</span><span class="sxs-lookup"><span data-stu-id="26ff1-113">IID\_IWMDRMLicenseManagement</span></span>
-   <span data-ttu-id="26ff1-114">IID \_ IWMDRMLicenseQuery</span><span class="sxs-lookup"><span data-stu-id="26ff1-114">IID\_IWMDRMLicenseQuery</span></span>
-   <span data-ttu-id="26ff1-115">IID \_ IWMDRMNetReceiver</span><span class="sxs-lookup"><span data-stu-id="26ff1-115">IID\_IWMDRMNetReceiver</span></span>
-   <span data-ttu-id="26ff1-116">IID \_ IWMDRMNetTransmitter</span><span class="sxs-lookup"><span data-stu-id="26ff1-116">IID\_IWMDRMNetTransmitter</span></span>
-   <span data-ttu-id="26ff1-117">IID \_ IWMDRMSecurity</span><span class="sxs-lookup"><span data-stu-id="26ff1-117">IID\_IWMDRMSecurity</span></span>

</dd> <dt>

<span data-ttu-id="26ff1-118">*ppvObject* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="26ff1-118">*ppvObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="26ff1-119">Adresse d’un pointeur qui reçoit l’adresse de l’interface demandée.</span><span class="sxs-lookup"><span data-stu-id="26ff1-119">Address of a pointer that receives the address of the requested interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26ff1-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="26ff1-120">Return value</span></span>

<span data-ttu-id="26ff1-121">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="26ff1-121">The method returns an **HRESULT**.</span></span> <span data-ttu-id="26ff1-122">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="26ff1-122">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="26ff1-123">Code de retour</span><span class="sxs-lookup"><span data-stu-id="26ff1-123">Return code</span></span>                                                                          | <span data-ttu-id="26ff1-124">Description</span><span class="sxs-lookup"><span data-stu-id="26ff1-124">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="26ff1-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="26ff1-125"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="26ff1-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="26ff1-126">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="26ff1-127">Notes</span><span class="sxs-lookup"><span data-stu-id="26ff1-127">Remarks</span></span>

<span data-ttu-id="26ff1-128">Aucun.</span><span class="sxs-lookup"><span data-stu-id="26ff1-128">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ff1-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="26ff1-129">Requirements</span></span>



| <span data-ttu-id="26ff1-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="26ff1-130">Requirement</span></span> | <span data-ttu-id="26ff1-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="26ff1-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="26ff1-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="26ff1-132">Header</span></span><br/>  | <dl> <span data-ttu-id="26ff1-133"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="26ff1-133"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="26ff1-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="26ff1-134">Library</span></span><br/> | <dl> <span data-ttu-id="26ff1-135"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="26ff1-135"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ff1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="26ff1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ff1-137">**Interface IWMDRMProvider**</span><span class="sxs-lookup"><span data-stu-id="26ff1-137">**IWMDRMProvider Interface**</span></span>](iwmdrmprovider.md)
</dt> <dt>

[<span data-ttu-id="26ff1-138">**Interface IWMDRMLicenseManagement**</span><span class="sxs-lookup"><span data-stu-id="26ff1-138">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="26ff1-139">**Interface IWMDRMLicenseQuery**</span><span class="sxs-lookup"><span data-stu-id="26ff1-139">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="26ff1-140">**Interface IWMDRMNetReceiver**</span><span class="sxs-lookup"><span data-stu-id="26ff1-140">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="26ff1-141">**Interface IWMDRMNetTransmitter**</span><span class="sxs-lookup"><span data-stu-id="26ff1-141">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> <dt>

[<span data-ttu-id="26ff1-142">**Interface IWMDRMSecurity**</span><span class="sxs-lookup"><span data-stu-id="26ff1-142">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





