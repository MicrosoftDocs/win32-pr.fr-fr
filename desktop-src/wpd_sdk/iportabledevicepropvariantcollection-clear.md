---
description: La méthode Clear libère, puis supprime tous les éléments de la collection. La collection est considérée comme vide après l’appel de cette méthode.
ms.assetid: f4b46713-8224-443a-99cc-13fa75e59e5d
title: 'IPortableDevicePropVariantCollection :: Clear, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fa7c2a8dddeb74b5ac666da2561bd6ee6536821a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526576"
---
# <a name="iportabledevicepropvariantcollectionclear-method"></a><span data-ttu-id="c0648-104">IPortableDevicePropVariantCollection :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="c0648-104">IPortableDevicePropVariantCollection::Clear method</span></span>

<span data-ttu-id="c0648-105">La méthode **Clear** libère, puis supprime tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="c0648-105">The **Clear** method frees, and then removes, all items from the collection.</span></span> <span data-ttu-id="c0648-106">La collection est considérée comme vide après l’appel de cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c0648-106">The collection is considered empty after calling this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0648-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0648-107">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="c0648-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0648-108">Parameters</span></span>

<span data-ttu-id="c0648-109">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="c0648-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c0648-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c0648-110">Return value</span></span>

<span data-ttu-id="c0648-111">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c0648-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c0648-112">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c0648-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c0648-113">Code de retour</span><span class="sxs-lookup"><span data-stu-id="c0648-113">Return code</span></span>                                                                          | <span data-ttu-id="c0648-114">Description</span><span class="sxs-lookup"><span data-stu-id="c0648-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c0648-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c0648-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c0648-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="c0648-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c0648-117">Notes</span><span class="sxs-lookup"><span data-stu-id="c0648-117">Remarks</span></span>

<span data-ttu-id="c0648-118">Après l’appel de **Clear**, la collection est considérée comme étant sans type, ce qui signifie que le VarType auquel elle a été précédemment définie ne restreint plus les opérations **Add** .</span><span class="sxs-lookup"><span data-stu-id="c0648-118">After calling **Clear**, the collection is considered type-less, meaning that the VARTYPE it was previously set to is no longer restricting **Add** operations.</span></span> <span data-ttu-id="c0648-119">Un appel à **Add** après l’appel de **Clear** est considéré comme « First » **Add** pour cette collection.</span><span class="sxs-lookup"><span data-stu-id="c0648-119">A call to **Add** after calling **Clear** is considered the "first" **Add** for this collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0648-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0648-120">Requirements</span></span>



| <span data-ttu-id="c0648-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0648-121">Requirement</span></span> | <span data-ttu-id="c0648-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0648-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0648-123">En-tête</span><span class="sxs-lookup"><span data-stu-id="c0648-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c0648-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0648-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0648-125">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c0648-125">Library</span></span><br/> | <dl> <span data-ttu-id="c0648-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c0648-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0648-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c0648-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0648-128">**Interface IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="c0648-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




