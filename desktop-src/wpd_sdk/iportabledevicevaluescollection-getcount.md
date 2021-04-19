---
description: La méthode GetCount récupère le nombre d’éléments dans la collection.
ms.assetid: c7b80a54-9e74-42d9-9155-cfcb2a92d324
title: 'IPortableDeviceValuesCollection :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5d1eabdcf73d65b42ccff980b15bb15514c3b322
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525134"
---
# <a name="iportabledevicevaluescollectiongetcount-method"></a><span data-ttu-id="308da-103">IPortableDeviceValuesCollection :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="308da-103">IPortableDeviceValuesCollection::GetCount method</span></span>

<span data-ttu-id="308da-104">La méthode **GetCount** récupère le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="308da-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="308da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="308da-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcElems
);
```



## <a name="parameters"></a><span data-ttu-id="308da-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="308da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="308da-107">*pcElems* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="308da-107">*pcElems* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="308da-108">Pointeur vers une **valeur DWORD** qui contient le nombre d’interfaces **IPortableDeviceValues** dans la collection.</span><span class="sxs-lookup"><span data-stu-id="308da-108">Pointer to a **DWORD** that contains the number of **IPortableDeviceValues** interfaces in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="308da-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="308da-109">Return value</span></span>

<span data-ttu-id="308da-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="308da-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="308da-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="308da-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="308da-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="308da-112">Return code</span></span>                                                                               | <span data-ttu-id="308da-113">Description</span><span class="sxs-lookup"><span data-stu-id="308da-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="308da-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="308da-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="308da-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="308da-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="308da-116"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="308da-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="308da-117">Un argument de pointeur obligatoire était **null**.</span><span class="sxs-lookup"><span data-stu-id="308da-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="308da-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="308da-118">Requirements</span></span>



| <span data-ttu-id="308da-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="308da-119">Requirement</span></span> | <span data-ttu-id="308da-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="308da-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="308da-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="308da-121">Header</span></span><br/>  | <dl> <span data-ttu-id="308da-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="308da-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="308da-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="308da-123">Library</span></span><br/> | <dl> <span data-ttu-id="308da-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="308da-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="308da-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="308da-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="308da-126">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="308da-126">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




