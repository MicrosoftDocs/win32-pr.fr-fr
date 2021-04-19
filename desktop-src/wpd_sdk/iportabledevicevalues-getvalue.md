---
description: La méthode GetValue récupère une valeur PROPVARIANT spécifiée par une clé.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'IPortableDeviceValues :: GetValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525390"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="a31fd-103">IPortableDeviceValues :: GetValue, méthode</span><span class="sxs-lookup"><span data-stu-id="a31fd-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="a31fd-104">La méthode **GetValue** récupère une valeur **PROPVARIANT** spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="a31fd-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="a31fd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a31fd-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="a31fd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a31fd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a31fd-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a31fd-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fd-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="a31fd-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="a31fd-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a31fd-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a31fd-110">Pointeur vers la valeur **PROPVARIANT** récupérée.</span><span class="sxs-lookup"><span data-stu-id="a31fd-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="a31fd-111">L’appelant doit libérer la mémoire en appelant **PropVariantClear** lorsqu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="a31fd-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a31fd-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a31fd-112">Return value</span></span>

<span data-ttu-id="a31fd-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a31fd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a31fd-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a31fd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a31fd-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="a31fd-115">Return code</span></span>                                                                                                            | <span data-ttu-id="a31fd-116">Description</span><span class="sxs-lookup"><span data-stu-id="a31fd-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="a31fd-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a31fd-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="a31fd-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="a31fd-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a31fd-119"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="a31fd-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="a31fd-120">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="a31fd-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a31fd-121">Notes</span><span class="sxs-lookup"><span data-stu-id="a31fd-121">Remarks</span></span>

<span data-ttu-id="a31fd-122">Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la récupération d'  une mémoire tampon de taille nulle ou nulle n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a31fd-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="a31fd-123">Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="a31fd-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="a31fd-124">Cette méthode peut être utilisée pour récupérer une valeur de n’importe quel type de la collection.</span><span class="sxs-lookup"><span data-stu-id="a31fd-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="a31fd-125">Toutefois, si vous connaissez le type de valeur à l’avance, utilisez l’une des méthodes de récupération spécialisées de cette interface pour éviter la surcharge de travail avec les valeurs PROPVARIANT directement.</span><span class="sxs-lookup"><span data-stu-id="a31fd-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="a31fd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a31fd-126">Requirements</span></span>



| <span data-ttu-id="a31fd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a31fd-127">Requirement</span></span> | <span data-ttu-id="a31fd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="a31fd-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a31fd-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="a31fd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="a31fd-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a31fd-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a31fd-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a31fd-131">Library</span></span><br/> | <dl> <span data-ttu-id="a31fd-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a31fd-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a31fd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a31fd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a31fd-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a31fd-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a31fd-135">**IPortableDeviceValues::RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="a31fd-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="a31fd-136">**IPortableDeviceValues :: SetValue**</span><span class="sxs-lookup"><span data-stu-id="a31fd-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




