---
description: La méthode SetIPortableDeviceValuesValue ajoute une nouvelle valeur IPortableDeviceValues (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 3e51964e-6ee0-4885-94ca-cc8000b456b4
title: 'IPortableDeviceValues :: SetIPortableDeviceValuesValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 265a5d3633dfa8252ff7afd4042a41e476040d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539621"
---
# <a name="iportabledevicevaluessetiportabledevicevaluesvalue-method"></a><span data-ttu-id="f91a8-103">IPortableDeviceValues :: SetIPortableDeviceValuesValue, méthode</span><span class="sxs-lookup"><span data-stu-id="f91a8-103">IPortableDeviceValues::SetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="f91a8-104">La méthode **SetIPortableDeviceValuesValue** ajoute une nouvelle valeur **IPORTABLEDEVICEVALUES** (type VT \_ inconnu) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="f91a8-104">The **SetIPortableDeviceValuesValue** method adds a new **IPortableDeviceValues** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f91a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f91a8-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesValue(
  [in] REFPROPERTYKEY        key,
  [in] IPortableDeviceValues *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f91a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f91a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f91a8-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f91a8-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f91a8-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="f91a8-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f91a8-109">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f91a8-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f91a8-110">Pointeur vers une interface **IPortableDeviceValues** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="f91a8-110">Pointer to an **IPortableDeviceValues** interface that specifies the new value.</span></span> <span data-ttu-id="f91a8-111">Le kit de développement logiciel (SDK) copie une référence à l’interface envoyée et appelle **AddRef** dessus.</span><span class="sxs-lookup"><span data-stu-id="f91a8-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f91a8-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f91a8-112">Return value</span></span>

<span data-ttu-id="f91a8-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f91a8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f91a8-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="f91a8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f91a8-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f91a8-115">Return code</span></span>                                                                          | <span data-ttu-id="f91a8-116">Description</span><span class="sxs-lookup"><span data-stu-id="f91a8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f91a8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f91a8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f91a8-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="f91a8-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f91a8-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f91a8-119">Remarks</span></span>

<span data-ttu-id="f91a8-120">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="f91a8-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="f91a8-121">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="f91a8-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="f91a8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f91a8-122">Requirements</span></span>



| <span data-ttu-id="f91a8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f91a8-123">Requirement</span></span> | <span data-ttu-id="f91a8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f91a8-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f91a8-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f91a8-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f91a8-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f91a8-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f91a8-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f91a8-127">Library</span></span><br/> | <dl> <span data-ttu-id="f91a8-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f91a8-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f91a8-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f91a8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f91a8-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f91a8-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f91a8-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="f91a8-131">**IPortableDeviceValues::GetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-getiportabledevicevaluesvalue.md)
</dt> </dl>

 

 




