---
description: La méthode GetType récupère le type de données des éléments de la collection.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'IPortableDevicePropVariantCollection :: GetType, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541321"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="aaab0-103">IPortableDevicePropVariantCollection :: GetType, méthode</span><span class="sxs-lookup"><span data-stu-id="aaab0-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="aaab0-104">La méthode **GetType** récupère le type de données des éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="aaab0-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="aaab0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaab0-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="aaab0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaab0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aaab0-107">*Pvt* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="aaab0-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aaab0-108">Valeur d’énumération **VarType** du kit de développement Platform SDK qui indique le type de données de tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="aaab0-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aaab0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="aaab0-109">Return value</span></span>

<span data-ttu-id="aaab0-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aaab0-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aaab0-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="aaab0-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aaab0-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="aaab0-112">Return code</span></span>                                                                               | <span data-ttu-id="aaab0-113">Description</span><span class="sxs-lookup"><span data-stu-id="aaab0-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="aaab0-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aaab0-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="aaab0-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="aaab0-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="aaab0-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="aaab0-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="aaab0-117">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="aaab0-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aaab0-118">Notes</span><span class="sxs-lookup"><span data-stu-id="aaab0-118">Remarks</span></span>

<span data-ttu-id="aaab0-119">Tous les éléments stockés dans un **IPortableDevicePropVariantCollection** sont du même type.</span><span class="sxs-lookup"><span data-stu-id="aaab0-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="aaab0-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="aaab0-120">Requirements</span></span>



| <span data-ttu-id="aaab0-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="aaab0-121">Requirement</span></span> | <span data-ttu-id="aaab0-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="aaab0-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aaab0-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="aaab0-123">Header</span></span><br/>  | <dl> <span data-ttu-id="aaab0-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="aaab0-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="aaab0-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="aaab0-125">Library</span></span><br/> | <dl> <span data-ttu-id="aaab0-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aaab0-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aaab0-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aaab0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aaab0-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="aaab0-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




