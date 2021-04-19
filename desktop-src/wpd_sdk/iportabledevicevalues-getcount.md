---
description: La méthode GetCount récupère le nombre d’éléments dans la collection.
ms.assetid: 89266483-4211-43d2-a306-68c70f1e7026
title: 'IPortableDeviceValues :: GetCount, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetCount
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 710348b2f2626d39efcbdf68373d1e556ecc335c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533468"
---
# <a name="iportabledevicevaluesgetcount-method"></a><span data-ttu-id="962df-103">IPortableDeviceValues :: GetCount, méthode</span><span class="sxs-lookup"><span data-stu-id="962df-103">IPortableDeviceValues::GetCount method</span></span>

<span data-ttu-id="962df-104">La méthode **GetCount** récupère le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="962df-104">The **GetCount** method retrieves the number of items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="962df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="962df-105">Syntax</span></span>


```C++
HRESULT GetCount(
  [in] DWORD *pcelt
);
```



## <a name="parameters"></a><span data-ttu-id="962df-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="962df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962df-107">*pcelt* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="962df-107">*pcelt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="962df-108">Pointeur vers une **valeur DWORD** qui contient le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="962df-108">Pointer to a **DWORD** that contains the number of items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962df-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="962df-109">Return value</span></span>

<span data-ttu-id="962df-110">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="962df-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="962df-111">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="962df-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="962df-112">Code de retour</span><span class="sxs-lookup"><span data-stu-id="962df-112">Return code</span></span>                                                                          | <span data-ttu-id="962df-113">Description</span><span class="sxs-lookup"><span data-stu-id="962df-113">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="962df-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="962df-114"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="962df-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="962df-115">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="962df-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="962df-116">Requirements</span></span>



| <span data-ttu-id="962df-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="962df-117">Requirement</span></span> | <span data-ttu-id="962df-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="962df-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="962df-119">En-tête</span><span class="sxs-lookup"><span data-stu-id="962df-119">Header</span></span><br/>  | <dl> <span data-ttu-id="962df-120"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="962df-120"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="962df-121">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="962df-121">Library</span></span><br/> | <dl> <span data-ttu-id="962df-122"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="962df-122"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="962df-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="962df-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962df-124">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="962df-124">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




