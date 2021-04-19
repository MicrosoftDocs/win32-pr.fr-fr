---
description: La méthode Add ajoute un élément à la collection.
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
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542639"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="47bc9-103">IPortableDevicePropVariantCollection :: Add, méthode</span><span class="sxs-lookup"><span data-stu-id="47bc9-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="47bc9-104">La méthode **Add** ajoute un élément à la collection.</span><span class="sxs-lookup"><span data-stu-id="47bc9-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="47bc9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47bc9-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="47bc9-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47bc9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47bc9-107">*pValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="47bc9-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47bc9-108">Pointeur vers un nouvel objet **PROPVARIANT** à ajouter à la collection.</span><span class="sxs-lookup"><span data-stu-id="47bc9-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="47bc9-109">Cette méthode copie le **PROPVARIANT** dans la collection. vous devez donc libérer votre copie locale de la variable en appelant **PropVariantClear** après avoir appelé cette méthode.</span><span class="sxs-lookup"><span data-stu-id="47bc9-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47bc9-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="47bc9-110">Return value</span></span>

<span data-ttu-id="47bc9-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="47bc9-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="47bc9-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="47bc9-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="47bc9-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="47bc9-113">Return code</span></span>                                                                          | <span data-ttu-id="47bc9-114">Description</span><span class="sxs-lookup"><span data-stu-id="47bc9-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="47bc9-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="47bc9-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="47bc9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="47bc9-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="47bc9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="47bc9-117">Remarks</span></span>

<span data-ttu-id="47bc9-118">Lorsque le VARTYPE de *pValue* est VT \_ Vector ou VT \_ UI1, la définition et la récupération  d’une mémoire tampon de taille zéro ou nulle ne sont pas prises en charge.</span><span class="sxs-lookup"><span data-stu-id="47bc9-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="47bc9-119">Par exemple, ni pValue. CAUB. pElems = **null** , ni pValue. CAUB. cElems = 0 n’est autorisé.</span><span class="sxs-lookup"><span data-stu-id="47bc9-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="47bc9-120">Si un appelant tente d’ajouter un élément d’un autre VARTYPE contenu dans la collection et que la valeur PROPVARIANT ne peut pas être modifiée automatiquement par cette interface, cette méthode échoue.</span><span class="sxs-lookup"><span data-stu-id="47bc9-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="47bc9-121">Pour modifier manuellement le type de collection, appelez [**IPortableDevicePropVariantCollection :: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="47bc9-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="47bc9-122">Exemples</span><span class="sxs-lookup"><span data-stu-id="47bc9-122">Examples</span></span>

<span data-ttu-id="47bc9-123">Pour obtenir un exemple d’utilisation de cette méthode, consultez [récupération d’un identificateur d’objet à partir d’un identificateur unique persistant](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="47bc9-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="47bc9-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="47bc9-124">Requirements</span></span>



| <span data-ttu-id="47bc9-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="47bc9-125">Requirement</span></span> | <span data-ttu-id="47bc9-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="47bc9-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47bc9-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="47bc9-127">Header</span></span><br/>  | <dl> <span data-ttu-id="47bc9-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="47bc9-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="47bc9-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="47bc9-129">Library</span></span><br/> | <dl> <span data-ttu-id="47bc9-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="47bc9-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47bc9-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47bc9-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47bc9-132">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="47bc9-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="47bc9-133">Déplacement du contenu sur l’appareil</span><span class="sxs-lookup"><span data-stu-id="47bc9-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="47bc9-134">Récupération d’un identificateur d’objet à partir d’un identificateur unique persistant</span><span class="sxs-lookup"><span data-stu-id="47bc9-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




