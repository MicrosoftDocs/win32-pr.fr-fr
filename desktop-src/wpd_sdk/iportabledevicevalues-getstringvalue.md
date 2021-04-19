---
description: La méthode GetStringValue récupère une valeur de chaîne (type VT \_ LPWStr) spécifiée par une clé.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'IPortableDeviceValues :: GetStringValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537832"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="b7352-103">IPortableDeviceValues :: GetStringValue, méthode</span><span class="sxs-lookup"><span data-stu-id="b7352-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="b7352-104">La méthode **GetStringValue** récupère une valeur de chaîne (type VT \_ LPWStr) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="b7352-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7352-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7352-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b7352-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7352-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7352-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b7352-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7352-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b7352-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b7352-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b7352-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7352-110">Pointeur vers la valeur **LPWStr** récupérée.</span><span class="sxs-lookup"><span data-stu-id="b7352-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="b7352-111">L’appelant est chargé d’appeler **CoTaskMemFree** pour libérer de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="b7352-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7352-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b7352-112">Return value</span></span>

<span data-ttu-id="b7352-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b7352-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b7352-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b7352-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b7352-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b7352-115">Return code</span></span>                                                                                                            | <span data-ttu-id="b7352-116">Description</span><span class="sxs-lookup"><span data-stu-id="b7352-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="b7352-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b7352-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b7352-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7352-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="b7352-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b7352-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b7352-120">La propriété spécifiée par la *clé* n’est pas un type **LPWStr** .</span><span class="sxs-lookup"><span data-stu-id="b7352-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="b7352-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="b7352-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b7352-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b7352-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="b7352-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7352-123">Examples</span></span>

<span data-ttu-id="b7352-124">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des événements de service pris en charge](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="b7352-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7352-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7352-125">Requirements</span></span>



| <span data-ttu-id="b7352-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7352-126">Requirement</span></span> | <span data-ttu-id="b7352-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7352-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7352-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b7352-128">Header</span></span><br/>  | <dl> <span data-ttu-id="b7352-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7352-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b7352-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b7352-130">Library</span></span><br/> | <dl> <span data-ttu-id="b7352-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b7352-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7352-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7352-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7352-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b7352-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b7352-134">**IPortableDeviceValues :: GetAt**</span><span class="sxs-lookup"><span data-stu-id="b7352-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="b7352-135">**IPortableDeviceValues :: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="b7352-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="b7352-136">Récupération des événements de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7352-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="b7352-137">Récupération des formats de service pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7352-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="b7352-138">Récupération des méthodes de service prises en charge</span><span class="sxs-lookup"><span data-stu-id="b7352-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




