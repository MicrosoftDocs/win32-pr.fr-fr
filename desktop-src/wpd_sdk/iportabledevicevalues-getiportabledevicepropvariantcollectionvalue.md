---
description: La méthode GetIPortableDevicePropVariantCollectionValue récupère une valeur IPortableDevicePropVariantCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'IPortableDeviceValues :: GetIPortableDevicePropVariantCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537873"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="a738d-103">IPortableDeviceValues :: GetIPortableDevicePropVariantCollectionValue, méthode</span><span class="sxs-lookup"><span data-stu-id="a738d-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="a738d-104">La méthode **GetIPortableDevicePropVariantCollectionValue** récupère une valeur **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="a738d-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a738d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a738d-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="a738d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a738d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a738d-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a738d-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a738d-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a738d-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a738d-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a738d-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a738d-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) récupérée.</span><span class="sxs-lookup"><span data-stu-id="a738d-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="a738d-111">L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="a738d-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a738d-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a738d-112">Return value</span></span>

<span data-ttu-id="a738d-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a738d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a738d-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a738d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a738d-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a738d-115">Return code</span></span>                                                                                                            | <span data-ttu-id="a738d-116">Description</span><span class="sxs-lookup"><span data-stu-id="a738d-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a738d-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a738d-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a738d-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a738d-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="a738d-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a738d-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="a738d-120">La propriété spécifiée par *Key* n’est pas une interface **IPortableDevicePropVariantCollection** .</span><span class="sxs-lookup"><span data-stu-id="a738d-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="a738d-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="a738d-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a738d-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="a738d-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="a738d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a738d-123">Requirements</span></span>



| <span data-ttu-id="a738d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a738d-124">Requirement</span></span> | <span data-ttu-id="a738d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="a738d-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a738d-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="a738d-126">Header</span></span><br/>  | <dl> <span data-ttu-id="a738d-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a738d-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a738d-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a738d-128">Library</span></span><br/> | <dl> <span data-ttu-id="a738d-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a738d-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a738d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a738d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a738d-131">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a738d-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a738d-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="a738d-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




