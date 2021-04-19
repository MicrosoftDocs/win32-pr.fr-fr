---
description: La méthode GetIPortableDeviceValuesCollectionValue récupère une valeur IPortableDeviceValuesCollection (type VT \_ inconnu) spécifiée par une clé.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'IPortableDeviceValues :: GetIPortableDeviceValuesCollectionValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525436"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="48d48-103">IPortableDeviceValues :: GetIPortableDeviceValuesCollectionValue, méthode</span><span class="sxs-lookup"><span data-stu-id="48d48-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="48d48-104">La méthode **GetIPortableDeviceValuesCollectionValue** récupère une valeur **IPORTABLEDEVICEVALUESCOLLECTION** (type VT \_ inconnu) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="48d48-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="48d48-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48d48-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="48d48-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48d48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48d48-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48d48-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48d48-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="48d48-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="48d48-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="48d48-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48d48-110">Adresse d’une variable qui reçoit un pointeur vers l’interface [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) récupérée.</span><span class="sxs-lookup"><span data-stu-id="48d48-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="48d48-111">L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="48d48-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48d48-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48d48-112">Return value</span></span>

<span data-ttu-id="48d48-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="48d48-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="48d48-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="48d48-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="48d48-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="48d48-115">Return code</span></span>                                                                                                            | <span data-ttu-id="48d48-116">Description</span><span class="sxs-lookup"><span data-stu-id="48d48-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="48d48-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="48d48-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="48d48-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="48d48-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="48d48-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="48d48-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="48d48-120">La propriété spécifiée par *Key* n’est pas une interface **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="48d48-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="48d48-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="48d48-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="48d48-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="48d48-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="48d48-123">Exemples</span><span class="sxs-lookup"><span data-stu-id="48d48-123">Examples</span></span>

<span data-ttu-id="48d48-124">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération des fonctionnalités de rendu prises en charge par un appareil](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="48d48-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="48d48-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48d48-125">Requirements</span></span>



| <span data-ttu-id="48d48-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48d48-126">Requirement</span></span> | <span data-ttu-id="48d48-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="48d48-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48d48-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="48d48-128">Header</span></span><br/>  | <dl> <span data-ttu-id="48d48-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="48d48-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="48d48-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="48d48-130">Library</span></span><br/> | <dl> <span data-ttu-id="48d48-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="48d48-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d48-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48d48-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d48-133">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="48d48-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="48d48-134">Récupération des fonctionnalités de rendu prises en charge par un appareil</span><span class="sxs-lookup"><span data-stu-id="48d48-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="48d48-135">**SetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="48d48-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




