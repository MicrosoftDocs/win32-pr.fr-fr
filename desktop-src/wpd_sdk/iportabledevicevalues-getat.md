---
description: La méthode GetAt récupère une valeur de la collection à l’aide de l’index de base zéro fourni.
ms.assetid: d52675f0-55b4-43ef-bb1d-ff6aa8a70647
title: 'IPortableDeviceValues :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44126b69dc4e8720fde687d47dc70dd97e104c72
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540505"
---
# <a name="iportabledevicevaluesgetat-method"></a><span data-ttu-id="5b68e-103">IPortableDeviceValues :: GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="5b68e-103">IPortableDeviceValues::GetAt method</span></span>

<span data-ttu-id="5b68e-104">La méthode **GetAt** récupère une valeur de la collection à l’aide de l’index de base zéro fourni.</span><span class="sxs-lookup"><span data-stu-id="5b68e-104">The **GetAt** method retrieves a value from the collection using the supplied zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b68e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b68e-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]      const DWORD       index,
  [in, out]       PROPERTYKEY *pKey,
  [in, out]       PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5b68e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b68e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b68e-107">*index* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b68e-107">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b68e-108">**Valeur DWORD** qui spécifie un index de base zéro dans la collection.</span><span class="sxs-lookup"><span data-stu-id="5b68e-108">A **DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="5b68e-109">A-la  \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b68e-109">*pKey* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b68e-110">Pointeur **PROPERTYKEY** facultatif qui récupère la clé de l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="5b68e-110">An optional **PROPERTYKEY** pointer that retrieves the key of the specified item.</span></span>

</dd> <dt>

<span data-ttu-id="5b68e-111">*pValue* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="5b68e-111">*pValue* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b68e-112">**PROPVARIANT** facultatif qui récupère la valeur de l’élément spécifié.</span><span class="sxs-lookup"><span data-stu-id="5b68e-112">An optional **PROPVARIANT** that retrieves the value of the specified item.</span></span> <span data-ttu-id="5b68e-113">L’appelant doit libérer la mémoire en appelant **PropVariantClear** lorsqu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="5b68e-113">The caller must free the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b68e-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b68e-114">Return value</span></span>

<span data-ttu-id="5b68e-115">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5b68e-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5b68e-116">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5b68e-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5b68e-117">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5b68e-117">Return code</span></span>                                                                                  | <span data-ttu-id="5b68e-118">Description</span><span class="sxs-lookup"><span data-stu-id="5b68e-118">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="5b68e-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5b68e-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="5b68e-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b68e-120">The method succeeded.</span></span><br/>                  |
| <dl> <span data-ttu-id="5b68e-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="5b68e-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="5b68e-122">Un numéro d’index non valide a été spécifié.</span><span class="sxs-lookup"><span data-stu-id="5b68e-122">An invalid index number was specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5b68e-123">Notes</span><span class="sxs-lookup"><span data-stu-id="5b68e-123">Remarks</span></span>

<span data-ttu-id="5b68e-124">Si une propriété indique une valeur de type VT \_ inconnu, la propriété sera l’un des appareils mobiles Windows ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) ou [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span><span class="sxs-lookup"><span data-stu-id="5b68e-124">If a property indicates a value of type VT\_UNKNOWN, the property will be one of the Windows Portable Devices ([**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md), [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md), [**IPortableDeviceValues**](iportabledevicevalues.md) or [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)).</span></span> <span data-ttu-id="5b68e-125">Aucune autre interface ne peut être retournée par les appareils mobiles Windows.</span><span class="sxs-lookup"><span data-stu-id="5b68e-125">No other interfaces can be returned by Windows Portable Devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b68e-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b68e-126">Requirements</span></span>



| <span data-ttu-id="5b68e-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b68e-127">Requirement</span></span> | <span data-ttu-id="5b68e-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b68e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b68e-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b68e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5b68e-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b68e-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5b68e-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5b68e-131">Library</span></span><br/> | <dl> <span data-ttu-id="5b68e-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5b68e-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b68e-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5b68e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b68e-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5b68e-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5b68e-135">**IPortableDeviceValues :: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="5b68e-135">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> </dl>

 

 




