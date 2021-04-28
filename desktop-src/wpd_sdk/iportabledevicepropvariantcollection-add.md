---
description: 'IPortableDevicePropVariantCollection :: Add, méthode-la méthode Add ajoute un élément à la collection.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'IPortableDevicePropVariantCollection :: Add, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112457"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="efd20-103">IPortableDevicePropVariantCollection :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="efd20-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="efd20-104">La méthode **Add** ajoute un élément à la collection.</span><span class="sxs-lookup"><span data-stu-id="efd20-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="efd20-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="efd20-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="efd20-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="efd20-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efd20-107">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="efd20-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efd20-108">Pointeur vers un nouvel objet **PROPVARIANT** à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="efd20-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="efd20-109">Cette méthode copie le **PROPVARIANT** dans la collection. vous devez donc libérer votre copie locale de la variable en appelant **PropVariantClear** après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="efd20-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efd20-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="efd20-110">Return value</span></span>

<span data-ttu-id="efd20-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="efd20-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="efd20-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="efd20-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="efd20-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="efd20-113">Return code</span></span>                                                                          | <span data-ttu-id="efd20-114">Description</span><span class="sxs-lookup"><span data-stu-id="efd20-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="efd20-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="efd20-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="efd20-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="efd20-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="efd20-117">Notes </span><span class="sxs-lookup"><span data-stu-id="efd20-117">Remarks</span></span>

<span data-ttu-id="efd20-118">Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la définition et la récupération  d’une mémoire tampon de taille zéro ou nulle ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="efd20-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="efd20-119">Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="efd20-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="efd20-120">Si un appelant tente d’ajouter un élément d’un autre VARTYPE contenu dans la collection et que la valeur PROPVARIANT ne peut pas être modifiée automatiquement par cette interface, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="efd20-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="efd20-121">Pour modifier manuellement le type de collection, appelez [**IPortableDevicePropVariantCollection :: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="efd20-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="efd20-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="efd20-122">Examples</span></span>

<span data-ttu-id="efd20-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération d’un identificateur d’objet à partir d’un identificateur unique persistant](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="efd20-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="efd20-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efd20-124">Requirements</span></span>



| <span data-ttu-id="efd20-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efd20-125">Requirement</span></span> | <span data-ttu-id="efd20-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="efd20-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efd20-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="efd20-127">Header</span></span><br/>  | <dl> <span data-ttu-id="efd20-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="efd20-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="efd20-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="efd20-129">Library</span></span><br/> | <dl> <span data-ttu-id="efd20-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="efd20-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efd20-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efd20-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efd20-132">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="efd20-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="efd20-133">Déplacement du contenu sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="efd20-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="efd20-134">Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="efd20-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




