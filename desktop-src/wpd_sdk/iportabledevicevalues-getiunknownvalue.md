---
description: La méthode GetIUnknownValue récupère une valeur d’interface IUnknown (type VT \_ Unknown) spécifiée par une clé.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'IPortableDeviceValues :: GetIUnknownValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537914"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="9f510-103">IPortableDeviceValues :: GetIUnknownValue, méthode</span><span class="sxs-lookup"><span data-stu-id="9f510-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="9f510-104">La méthode **GetIUnknownValue** récupère une valeur d’interface **IUnknown** (type VT \_ Unknown) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="9f510-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f510-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9f510-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="9f510-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9f510-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f510-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9f510-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f510-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="9f510-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="9f510-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9f510-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f510-110">Adresse d’une variable qui reçoit un pointeur vers l’interface **IUnknown** récupérée.</span><span class="sxs-lookup"><span data-stu-id="9f510-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="9f510-111">L’appelant est responsable de l’appel de **Release** sur l’interface récupérée.</span><span class="sxs-lookup"><span data-stu-id="9f510-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f510-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9f510-112">Return value</span></span>

<span data-ttu-id="9f510-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="9f510-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9f510-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="9f510-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9f510-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9f510-115">Return code</span></span>                                                                                                            | <span data-ttu-id="9f510-116">Description</span><span class="sxs-lookup"><span data-stu-id="9f510-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9f510-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9f510-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="9f510-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f510-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="9f510-119"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9f510-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="9f510-120">La propriété spécifiée par la *clé* n’est pas une interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="9f510-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="9f510-121"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="9f510-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="9f510-122">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="9f510-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="9f510-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9f510-123">Requirements</span></span>



| <span data-ttu-id="9f510-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9f510-124">Requirement</span></span> | <span data-ttu-id="9f510-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9f510-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f510-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="9f510-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9f510-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="9f510-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="9f510-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9f510-128">Library</span></span><br/> | <dl> <span data-ttu-id="9f510-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f510-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f510-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9f510-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f510-131">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="9f510-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="9f510-132">**IPortableDeviceValues::SetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="9f510-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




