---
description: La méthode SetIPortableDeviceValuesCollectionValue ajoute une nouvelle valeur IPortableDeviceValuesCollection (type VT \_ inconnu) ou remplace celle qui existe déjà.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'IPortableDeviceValues :: SetIPortableDeviceValuesCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3f0c545a4daceed75971b0e659f85d72eca6d98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535938"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="e7698-103">IPortableDeviceValues :: SetIPortableDeviceValuesCollectionValue, méthode</span><span class="sxs-lookup"><span data-stu-id="e7698-103">IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="e7698-104">La méthode **SetIPortableDeviceValuesCollectionValue** ajoute une nouvelle valeur **IPORTABLEDEVICEVALUESCOLLECTION** (type VT \_ inconnu) ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="e7698-104">The **SetIPortableDeviceValuesCollectionValue** method adds a new **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7698-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7698-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e7698-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7698-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7698-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7698-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7698-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="e7698-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="e7698-109">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7698-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7698-110">Pointeur vers une interface **IPortableDeviceValuesCollection** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="e7698-110">Pointer to an **IPortableDeviceValuesCollection** interface that specifies the new value.</span></span> <span data-ttu-id="e7698-111">Le kit de développement logiciel (SDK) copie une référence à l’interface envoyée et appelle **AddRef** dessus.</span><span class="sxs-lookup"><span data-stu-id="e7698-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7698-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7698-112">Return value</span></span>

<span data-ttu-id="e7698-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7698-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7698-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="e7698-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7698-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="e7698-115">Return code</span></span>                                                                          | <span data-ttu-id="e7698-116">Description</span><span class="sxs-lookup"><span data-stu-id="e7698-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7698-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7698-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7698-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e7698-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7698-119">Notes</span><span class="sxs-lookup"><span data-stu-id="e7698-119">Remarks</span></span>

<span data-ttu-id="e7698-120">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="e7698-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="e7698-121">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="e7698-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7698-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7698-122">Requirements</span></span>



| <span data-ttu-id="e7698-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7698-123">Requirement</span></span> | <span data-ttu-id="e7698-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7698-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7698-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7698-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e7698-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7698-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7698-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7698-127">Library</span></span><br/> | <dl> <span data-ttu-id="e7698-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7698-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7698-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7698-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7698-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e7698-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e7698-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="e7698-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




