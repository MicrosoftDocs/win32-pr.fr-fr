---
description: La méthode GetBufferValue récupère une valeur de tableau d’octets (type \_ VT \| VT \_ UI1) spécifiée par une clé.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'IPortableDeviceValues :: GetBufferValue, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525608"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="5035f-103">IPortableDeviceValues :: GetBufferValue, méthode</span><span class="sxs-lookup"><span data-stu-id="5035f-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="5035f-104">La méthode **GetBufferValue** récupère une valeur de **tableau d’octets** (type VT \_ \| VT \_ UI1) spécifiée par une clé.</span><span class="sxs-lookup"><span data-stu-id="5035f-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5035f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5035f-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="5035f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5035f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5035f-107">*clé* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5035f-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5035f-108">Clé **REFPROPERTYKEY** qui spécifie l’élément à récupérer.</span><span class="sxs-lookup"><span data-stu-id="5035f-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5035f-109">*ppValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5035f-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5035f-110">Pointeur vers la **valeur d’octet \* *_ récupérée. L’appelant est chargé de libérer la mémoire en appelant _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="5035f-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="5035f-111">*pcbValue* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5035f-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5035f-112">Pointeur vers la taille de *ppValue*, en octets.</span><span class="sxs-lookup"><span data-stu-id="5035f-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5035f-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5035f-113">Return value</span></span>

<span data-ttu-id="5035f-114">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5035f-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5035f-115">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5035f-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5035f-116">Code de retour</span><span class="sxs-lookup"><span data-stu-id="5035f-116">Return code</span></span>                                                                                                            | <span data-ttu-id="5035f-117">Description</span><span class="sxs-lookup"><span data-stu-id="5035f-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5035f-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5035f-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="5035f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="5035f-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5035f-120"><dt>**\_TYPEMISMATCH DISP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5035f-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="5035f-121">La propriété spécifiée par la *clé* n’est pas un type **Byte** \* .</span><span class="sxs-lookup"><span data-stu-id="5035f-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="5035f-122"><dt>**HRESULT \_ à partir de \_ Win32 (erreur \_ \_ introuvable)**</dt></span><span class="sxs-lookup"><span data-stu-id="5035f-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="5035f-123">La propriété spécifiée par la *clé* ne figure pas dans la collection.</span><span class="sxs-lookup"><span data-stu-id="5035f-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5035f-124">Notes</span><span class="sxs-lookup"><span data-stu-id="5035f-124">Remarks</span></span>

<span data-ttu-id="5035f-125">La récupération d’une mémoire tampon **null** ou d’une mémoire tampon de taille zéro n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="5035f-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="5035f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5035f-126">Requirements</span></span>



| <span data-ttu-id="5035f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5035f-127">Requirement</span></span> | <span data-ttu-id="5035f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="5035f-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5035f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="5035f-129">Header</span></span><br/>  | <dl> <span data-ttu-id="5035f-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5035f-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5035f-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="5035f-131">Library</span></span><br/> | <dl> <span data-ttu-id="5035f-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5035f-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5035f-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5035f-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5035f-134">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5035f-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5035f-135">**IPortableDeviceValues::SetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="5035f-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




