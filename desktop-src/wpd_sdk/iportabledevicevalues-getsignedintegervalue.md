---
description: La méthode GetSignedIntegerValue récupère une valeur LONG (type VT \_ I4) spécifiée par une clé.
ms.assetid: d2291a64-d0b3-4a30-a37c-2b6cd9880a11
title: 'IPortableDeviceValues :: GetSignedIntegerValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetSignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2fe0c2f8714d3fa28f61624924eba169f9f1c5d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537685"
---
# <a name="iportabledevicevaluesgetsignedintegervalue-method"></a><span data-ttu-id="50d98-103">IPortableDeviceValues :: GetSignedIntegerValue, méthode</span><span class="sxs-lookup"><span data-stu-id="50d98-103">IPortableDeviceValues::GetSignedIntegerValue method</span></span>

<span data-ttu-id="50d98-104">La méthode **GetSignedIntegerValue** récupère une valeur **long** (type VT \_ I4) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="50d98-104">The **GetSignedIntegerValue** method retrieves a **LONG** value (type VT\_I4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="50d98-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50d98-105">Syntax</span></span>


```C++
HRESULT GetSignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] LONG           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="50d98-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="50d98-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50d98-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="50d98-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50d98-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="50d98-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="50d98-109">*pValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="50d98-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="50d98-110">Pointeur vers la valeur **long** récupérée.</span><span class="sxs-lookup"><span data-stu-id="50d98-110">Pointer to the retrieved **LONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50d98-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="50d98-111">Return value</span></span>

<span data-ttu-id="50d98-112">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="50d98-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="50d98-113">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="50d98-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="50d98-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="50d98-114">Return code</span></span>                                                                                                            | <span data-ttu-id="50d98-115">Description</span><span class="sxs-lookup"><span data-stu-id="50d98-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="50d98-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50d98-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="50d98-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="50d98-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="50d98-118"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="50d98-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="50d98-119">La propriété spécifiée par la *clé* n’est pas de type **long** .</span><span class="sxs-lookup"><span data-stu-id="50d98-119">The property specified by *key* is not a **LONG** type.</span></span><br/>   |
| <dl> <span data-ttu-id="50d98-120"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="50d98-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="50d98-121">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="50d98-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="50d98-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50d98-122">Requirements</span></span>



| <span data-ttu-id="50d98-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50d98-123">Requirement</span></span> | <span data-ttu-id="50d98-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="50d98-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50d98-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="50d98-125">Header</span></span><br/>  | <dl> <span data-ttu-id="50d98-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="50d98-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="50d98-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="50d98-127">Library</span></span><br/> | <dl> <span data-ttu-id="50d98-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50d98-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50d98-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50d98-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50d98-130">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="50d98-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="50d98-131">**IPortableDeviceValues::SetSignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="50d98-131">**IPortableDeviceValues::SetSignedIntegerValue**</span></span>](iportabledevicevalues-setsignedintegervalue.md)
</dt> </dl>

 

 




