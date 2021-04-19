---
description: La méthode GetIPortableDeviceKeyCollectionValue récupère une valeur IPortableDeviceKeyCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535990"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="82be5-103">IPortableDeviceValues :: GetIPortableDeviceKeyCollectionValue, méthode</span><span class="sxs-lookup"><span data-stu-id="82be5-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="82be5-104">La méthode **GetIPortableDeviceKeyCollectionValue** récupère une valeur **IPORTABLEDEVICEKEYCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="82be5-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="82be5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82be5-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="82be5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="82be5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82be5-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="82be5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="82be5-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="82be5-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="82be5-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="82be5-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="82be5-110">Pointeur vers le pointeur d’interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) récupéré.</span><span class="sxs-lookup"><span data-stu-id="82be5-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="82be5-111">L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="82be5-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82be5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="82be5-112">Return value</span></span>

<span data-ttu-id="82be5-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="82be5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="82be5-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="82be5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="82be5-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="82be5-115">Return code</span></span>                                                                                                            | <span data-ttu-id="82be5-116">Description</span><span class="sxs-lookup"><span data-stu-id="82be5-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="82be5-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="82be5-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="82be5-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="82be5-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="82be5-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="82be5-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="82be5-120">La propriété spécifiée par *Key* n’est pas une interface **IPortableDeviceKeyCollection** .</span><span class="sxs-lookup"><span data-stu-id="82be5-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="82be5-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="82be5-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="82be5-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="82be5-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="82be5-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="82be5-123">Examples</span></span>

<span data-ttu-id="82be5-124">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="82be5-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="82be5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="82be5-125">Requirements</span></span>



| <span data-ttu-id="82be5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="82be5-126">Requirement</span></span> | <span data-ttu-id="82be5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="82be5-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="82be5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="82be5-128">Header</span></span><br/>  | <dl> <span data-ttu-id="82be5-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="82be5-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="82be5-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="82be5-130">Library</span></span><br/> | <dl> <span data-ttu-id="82be5-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="82be5-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82be5-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="82be5-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82be5-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="82be5-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="82be5-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="82be5-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="82be5-135">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="82be5-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="82be5-136">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="82be5-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




