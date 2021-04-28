---
description: 'IPortableDeviceValuesCollection :: GetAt, méthode-la méthode GetAt récupère un élément de la collection à l’aide d’un index de base zéro.'
ms.assetid: b219b052-a74b-466a-a2ee-d2e9c466f393
title: 'IPortableDeviceValuesCollection :: GetAt, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 2ad10a7b9cc3c252a0cee4cb71df05cb108e0a18
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083253"
---
# <a name="iportabledevicevaluescollectiongetat-method"></a><span data-ttu-id="91957-103">IPortableDeviceValuesCollection :: GetAt, méthode</span><span class="sxs-lookup"><span data-stu-id="91957-103">IPortableDeviceValuesCollection::GetAt method</span></span>

<span data-ttu-id="91957-104">La méthode **GetAt** récupère un élément de la collection à l’aide d’un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="91957-104">The **GetAt** method retrieves an item from the collection by a zero-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="91957-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91957-105">Syntax</span></span>


```C++
HRESULT GetAt(
  [in]  const DWORD                 dwIndex,
  [out]       IPortableDeviceValues **ppValues
);
```



## <a name="parameters"></a><span data-ttu-id="91957-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91957-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91957-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91957-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91957-108">**Valeur DWORD** qui spécifie un index de base zéro dans la collection.</span><span class="sxs-lookup"><span data-stu-id="91957-108">**DWORD** that specifies a zero-based index in the collection.</span></span>

</dd> <dt>

<span data-ttu-id="91957-109">*ppValues* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91957-109">*ppValues* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91957-110">Adresse d’une variable qui reçoit un pointeur vers une interface [**IPortableDeviceValues**](iportabledevicevalues.md) à partir de la collection.</span><span class="sxs-lookup"><span data-stu-id="91957-110">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface from the collection.</span></span> <span data-ttu-id="91957-111">L’appelant est responsable de l’appel de **Release** sur cette interface lorsqu’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="91957-111">The caller is responsible for calling **Release** on this interface when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91957-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="91957-112">Return value</span></span>

<span data-ttu-id="91957-113">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="91957-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="91957-114">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="91957-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="91957-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="91957-115">Return code</span></span>                                                                                  | <span data-ttu-id="91957-116">Description</span><span class="sxs-lookup"><span data-stu-id="91957-116">Description</span></span>                                                                      |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91957-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="91957-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="91957-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="91957-118">The method succeeded.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="91957-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="91957-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="91957-120">L’index de base zéro qui a été passé était hors limites.</span><span class="sxs-lookup"><span data-stu-id="91957-120">The zero-based index that was passed in was out of range.</span></span><br/>             |
| <dl> <span data-ttu-id="91957-121"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="91957-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="91957-122">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="91957-122">A required pointer argument was **NULL**.</span></span><br/>                             |
| <dl> <span data-ttu-id="91957-123"><dt>**E \_ inattendu**</dt></span><span class="sxs-lookup"><span data-stu-id="91957-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="91957-124">La collection contient un pointeur **IPortableDeviceValues** **null** .</span><span class="sxs-lookup"><span data-stu-id="91957-124">The collection contains a **NULL** **IPortableDeviceValues** pointer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="91957-125">Notes </span><span class="sxs-lookup"><span data-stu-id="91957-125">Remarks</span></span>

<span data-ttu-id="91957-126">Toutes les modifications apportées aux valeurs dans l’interface récupérée seront apportées à la version stockée dans la collection.</span><span class="sxs-lookup"><span data-stu-id="91957-126">Any changes that are made to values in the retrieved interface will be made to the version stored in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="91957-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91957-127">Requirements</span></span>



| <span data-ttu-id="91957-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91957-128">Requirement</span></span> | <span data-ttu-id="91957-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="91957-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91957-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="91957-130">Header</span></span><br/>  | <dl> <span data-ttu-id="91957-131"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="91957-131"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="91957-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="91957-132">Library</span></span><br/> | <dl> <span data-ttu-id="91957-133"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="91957-133"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91957-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="91957-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91957-135">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="91957-135">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




