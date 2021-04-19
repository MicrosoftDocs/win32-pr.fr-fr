---
description: La méthode ChangeType convertit tous les éléments de la collection au format VARTYPE spécifié.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'IPortableDevicePropVariantCollection :: ChangeType, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529898"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="d05d7-103">IPortableDevicePropVariantCollection :: ChangeType, méthode</span><span class="sxs-lookup"><span data-stu-id="d05d7-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="d05d7-104">La méthode **ChangeType** convertit tous les éléments de la collection au format VarType spécifié.</span><span class="sxs-lookup"><span data-stu-id="d05d7-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="d05d7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d05d7-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="d05d7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d05d7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d05d7-107">*VT* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d05d7-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d05d7-108">Spécifie le **VarType** vers lequel vous souhaitez convertir tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="d05d7-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="d05d7-109">Les exemples de types incluent VT \_ UI4 et VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="d05d7-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d05d7-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d05d7-110">Return value</span></span>

<span data-ttu-id="d05d7-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d05d7-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d05d7-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d05d7-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d05d7-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d05d7-113">Return code</span></span>                                                                          | <span data-ttu-id="d05d7-114">Description</span><span class="sxs-lookup"><span data-stu-id="d05d7-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d05d7-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d05d7-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d05d7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d05d7-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d05d7-117">Notes</span><span class="sxs-lookup"><span data-stu-id="d05d7-117">Remarks</span></span>

<span data-ttu-id="d05d7-118">Si cette méthode échoue, la collection peut être laissée dans un état intermédiaire, avec certains membres convertis et certains non convertis.</span><span class="sxs-lookup"><span data-stu-id="d05d7-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="d05d7-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d05d7-119">Requirements</span></span>



| <span data-ttu-id="d05d7-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d05d7-120">Requirement</span></span> | <span data-ttu-id="d05d7-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="d05d7-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05d7-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="d05d7-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d05d7-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d05d7-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d05d7-124">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d05d7-124">Library</span></span><br/> | <dl> <span data-ttu-id="d05d7-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d05d7-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d05d7-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d05d7-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d05d7-127">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="d05d7-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




