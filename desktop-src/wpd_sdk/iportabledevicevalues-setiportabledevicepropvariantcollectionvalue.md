---
description: La méthode SetIPortableDevicePropVariantCollectionValue ajoute une nouvelle valeur IPortableDevicePropVariantCollection (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: 'IPortableDeviceValues :: SetIPortableDevicePropVariantCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f39ad6745dbf30df87e87be7fba358b4d9ad2c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526040"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="c79b4-103">IPortableDeviceValues :: SetIPortableDevicePropVariantCollectionValue, méthode</span><span class="sxs-lookup"><span data-stu-id="c79b4-103">IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="c79b4-104">La méthode **SetIPortableDevicePropVariantCollectionValue** ajoute une nouvelle valeur **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (type VT \_ inconnu) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c79b4-104">The **SetIPortableDevicePropVariantCollectionValue** method adds a new **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="c79b4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c79b4-105">Syntax</span></span>


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="c79b4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c79b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c79b4-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c79b4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79b4-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="c79b4-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="c79b4-109">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c79b4-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c79b4-110">Pointeur vers une interface **IPortableDevicePropVariantCollection** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="c79b4-110">Pointer to an **IPortableDevicePropVariantCollection** interface that specifies the new value.</span></span> <span data-ttu-id="c79b4-111">Le kit de développement logiciel (SDK) copie une référence à l’interface envoyée et appelle **AddRef** dessus.</span><span class="sxs-lookup"><span data-stu-id="c79b4-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c79b4-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c79b4-112">Return value</span></span>

<span data-ttu-id="c79b4-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c79b4-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c79b4-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c79b4-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c79b4-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c79b4-115">Return code</span></span>                                                                          | <span data-ttu-id="c79b4-116">Description</span><span class="sxs-lookup"><span data-stu-id="c79b4-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c79b4-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c79b4-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c79b4-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="c79b4-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c79b4-119">Notes</span><span class="sxs-lookup"><span data-stu-id="c79b4-119">Remarks</span></span>

<span data-ttu-id="c79b4-120">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="c79b4-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="c79b4-121">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="c79b4-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="c79b4-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c79b4-122">Requirements</span></span>



| <span data-ttu-id="c79b4-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c79b4-123">Requirement</span></span> | <span data-ttu-id="c79b4-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="c79b4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c79b4-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="c79b4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="c79b4-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c79b4-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c79b4-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c79b4-127">Library</span></span><br/> | <dl> <span data-ttu-id="c79b4-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c79b4-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c79b4-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c79b4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c79b4-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="c79b4-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="c79b4-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="c79b4-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




