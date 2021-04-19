---
description: La méthode Clear supprime tous les éléments de la collection.
ms.assetid: 4350ae43-16be-4cf2-816d-719349b12654
title: 'IPortableDeviceValues :: Clear, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 45c04319b5691e3bbcfb56d5a447cf2eb60bfaac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537448"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="767bf-103">IPortableDeviceValues :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="767bf-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="767bf-104">La méthode **Clear** supprime tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="767bf-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="767bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="767bf-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="767bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="767bf-106">Parameters</span></span>

<span data-ttu-id="767bf-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="767bf-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="767bf-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="767bf-108">Return value</span></span>

<span data-ttu-id="767bf-109">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="767bf-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="767bf-110">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="767bf-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="767bf-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="767bf-111">Return code</span></span>                                                                          | <span data-ttu-id="767bf-112">Description</span><span class="sxs-lookup"><span data-stu-id="767bf-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="767bf-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="767bf-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="767bf-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="767bf-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="767bf-115">Notes</span><span class="sxs-lookup"><span data-stu-id="767bf-115">Remarks</span></span>

<span data-ttu-id="767bf-116">Cette méthode libère la mémoire pour tous les éléments alloués dynamiquement dans la collection.</span><span class="sxs-lookup"><span data-stu-id="767bf-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="767bf-117">Pour les interfaces, elle appelle **Release**.</span><span class="sxs-lookup"><span data-stu-id="767bf-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="767bf-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="767bf-118">Requirements</span></span>



| <span data-ttu-id="767bf-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="767bf-119">Requirement</span></span> | <span data-ttu-id="767bf-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="767bf-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="767bf-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="767bf-121">Header</span></span><br/>  | <dl> <span data-ttu-id="767bf-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="767bf-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="767bf-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="767bf-123">Library</span></span><br/> | <dl> <span data-ttu-id="767bf-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="767bf-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="767bf-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="767bf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="767bf-126">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="767bf-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




