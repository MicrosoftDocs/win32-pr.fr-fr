---
description: 'IPortableDeviceValues :: Clear, méthode-la méthode Clear supprime tous les éléments de la collection.'
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
ms.openlocfilehash: 8e1df59cd972bc470607ac2b49d05f43dba8b3a7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109897"
---
# <a name="iportabledevicevaluesclear-method"></a><span data-ttu-id="88da0-103">IPortableDeviceValues :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="88da0-103">IPortableDeviceValues::Clear method</span></span>

<span data-ttu-id="88da0-104">La méthode **Clear** supprime tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="88da0-104">The **Clear** method deletes all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="88da0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="88da0-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="88da0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="88da0-106">Parameters</span></span>

<span data-ttu-id="88da0-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="88da0-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="88da0-108">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="88da0-108">Return value</span></span>

<span data-ttu-id="88da0-109">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="88da0-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="88da0-110">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="88da0-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="88da0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="88da0-111">Return code</span></span>                                                                          | <span data-ttu-id="88da0-112">Description</span><span class="sxs-lookup"><span data-stu-id="88da0-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="88da0-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="88da0-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="88da0-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="88da0-115">Notes </span><span class="sxs-lookup"><span data-stu-id="88da0-115">Remarks</span></span>

<span data-ttu-id="88da0-116">Cette méthode libère la mémoire pour tous les éléments alloués dynamiquement dans la collection.</span><span class="sxs-lookup"><span data-stu-id="88da0-116">This method frees the memory for all dynamically allocated items in the collection.</span></span> <span data-ttu-id="88da0-117">Pour les interfaces, elle appelle **Release**.</span><span class="sxs-lookup"><span data-stu-id="88da0-117">For interfaces, it calls **Release**.</span></span>

## <a name="requirements"></a><span data-ttu-id="88da0-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="88da0-118">Requirements</span></span>



| <span data-ttu-id="88da0-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="88da0-119">Requirement</span></span> | <span data-ttu-id="88da0-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="88da0-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88da0-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="88da0-121">Header</span></span><br/>  | <dl> <span data-ttu-id="88da0-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="88da0-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="88da0-123">Library</span></span><br/> | <dl> <span data-ttu-id="88da0-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88da0-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88da0-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="88da0-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88da0-126">**Interface IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="88da0-126">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> </dl>

 

 




