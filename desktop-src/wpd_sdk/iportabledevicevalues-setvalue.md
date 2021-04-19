---
description: La méthode SetValue ajoute une nouvelle valeur PROPVARIANT ou remplace celle qui existe déjà.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'IPortableDeviceValues :: SetValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542306"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="78012-103">IPortableDeviceValues :: SetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="78012-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="78012-104">La méthode **SetValue** ajoute une nouvelle valeur **PROPVARIANT** ou remplace celle qui existe déjà.</span><span class="sxs-lookup"><span data-stu-id="78012-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="78012-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78012-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="78012-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="78012-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78012-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78012-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78012-108">**REFPROPERTYKEY** qui spécifie l’élément à créer ou à remplacer.</span><span class="sxs-lookup"><span data-stu-id="78012-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="78012-109">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="78012-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78012-110">**PROPVARIANT** qui spécifie la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="78012-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="78012-111">Le kit de développement logiciel (SDK) copie la valeur, de sorte que l’appelant peut libérer la variable locale en appelant **PropVariantClear** après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="78012-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78012-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="78012-112">Return value</span></span>

<span data-ttu-id="78012-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="78012-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="78012-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="78012-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="78012-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="78012-115">Return code</span></span>                                                                          | <span data-ttu-id="78012-116">Description</span><span class="sxs-lookup"><span data-stu-id="78012-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="78012-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="78012-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="78012-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="78012-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="78012-119">Notes</span><span class="sxs-lookup"><span data-stu-id="78012-119">Remarks</span></span>

<span data-ttu-id="78012-120">Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la définition  d’une mémoire tampon de taille zéro ou nulle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="78012-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="78012-121">Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="78012-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="78012-122">Cette méthode peut être utilisée pour récupérer une valeur de n’importe quel type de la collection.</span><span class="sxs-lookup"><span data-stu-id="78012-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="78012-123">Toutefois, si vous connaissez le type de valeur à l’avance, utilisez l’une des méthodes **Set...** spécialisées de cette interface pour éviter la surcharge liée à l’utilisation directe des valeurs PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="78012-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="78012-124">Si une valeur existante a la même clé que celle spécifiée par le paramètre de *clé* , elle remplace la valeur existante sans avertissement.</span><span class="sxs-lookup"><span data-stu-id="78012-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="78012-125">La mémoire clé existante est libérée de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="78012-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="78012-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="78012-126">Requirements</span></span>



| <span data-ttu-id="78012-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="78012-127">Requirement</span></span> | <span data-ttu-id="78012-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="78012-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78012-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="78012-129">Header</span></span><br/>  | <dl> <span data-ttu-id="78012-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="78012-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="78012-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="78012-131">Library</span></span><br/> | <dl> <span data-ttu-id="78012-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="78012-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78012-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="78012-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78012-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="78012-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="78012-135">**IPortableDeviceValues :: GetValue**</span><span class="sxs-lookup"><span data-stu-id="78012-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="78012-136">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="78012-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




