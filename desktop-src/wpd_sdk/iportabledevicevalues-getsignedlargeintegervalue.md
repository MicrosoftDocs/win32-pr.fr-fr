---
description: La méthode GetSignedLargeIntegerValue récupère une valeur LONGLONG (type VT \_ I8) spécifiée par une clé.
ms.assetid: b8d2a0b6-7ca3-4a56-a502-cc18b08df22a
title: 'IPortableDeviceValues :: GetSignedLargeIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5fc41c263ffdef540300a08f88665a6489fa9d41
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537587"
---
# <a name="iportabledevicevaluesgetsignedlargeintegervalue-method"></a><span data-ttu-id="b726c-103">IPortableDeviceValues :: GetSignedLargeIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="b726c-103">IPortableDeviceValues::GetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="b726c-104">La méthode **GetSignedLargeIntegerValue** récupère une valeur **LongLong** (type VT \_ I8) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="b726c-104">The **GetSignedLargeIntegerValue** method retrieves a **LONGLONG** value (type VT\_I8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="b726c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b726c-105">Syntax</span></span>


```C++
HRESULT GetSignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONGLONG       *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="b726c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b726c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b726c-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b726c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b726c-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="b726c-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b726c-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="b726c-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b726c-110">Pointeur vers la valeur **ULong** récupérée.</span><span class="sxs-lookup"><span data-stu-id="b726c-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b726c-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b726c-111">Return value</span></span>

<span data-ttu-id="b726c-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="b726c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b726c-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="b726c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b726c-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="b726c-114">Return code</span></span>                                                                                                            | <span data-ttu-id="b726c-115">Description</span><span class="sxs-lookup"><span data-stu-id="b726c-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b726c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b726c-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="b726c-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b726c-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="b726c-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="b726c-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="b726c-119">La propriété spécifiée par la *clé* n’est pas un type **LongLong** .</span><span class="sxs-lookup"><span data-stu-id="b726c-119">The property specified by *key* is not a **LONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="b726c-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="b726c-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="b726c-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="b726c-121">The property specified by *key* is not in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="b726c-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b726c-122">Requirements</span></span>



| <span data-ttu-id="b726c-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b726c-123">Requirement</span></span> | <span data-ttu-id="b726c-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="b726c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b726c-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="b726c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="b726c-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="b726c-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="b726c-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b726c-127">Library</span></span><br/> | <dl> <span data-ttu-id="b726c-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b726c-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b726c-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b726c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b726c-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="b726c-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b726c-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="b726c-131">**IPortableDeviceValues::SetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-setsignedlargeintegervalue.md)
</dt> </dl>

 

 




