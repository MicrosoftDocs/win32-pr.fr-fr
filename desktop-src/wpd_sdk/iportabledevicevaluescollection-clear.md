---
description: La méthode Clear libère tous les éléments de la collection.
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'IPortableDeviceValuesCollection :: Clear, méthode (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540156"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="523e1-103">IPortableDeviceValuesCollection :: Clear, méthode</span><span class="sxs-lookup"><span data-stu-id="523e1-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="523e1-104">La méthode **Clear** libère tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="523e1-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="523e1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="523e1-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="523e1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="523e1-106">Parameters</span></span>

<span data-ttu-id="523e1-107">Cette méthode n’a aucun paramètre.</span><span class="sxs-lookup"><span data-stu-id="523e1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="523e1-108">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="523e1-108">Return value</span></span>

<span data-ttu-id="523e1-109">La méthode retourne un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="523e1-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="523e1-110">Les valeurs possibles sont notamment celles figurant dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="523e1-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="523e1-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="523e1-111">Return code</span></span>                                                                          | <span data-ttu-id="523e1-112">Description</span><span class="sxs-lookup"><span data-stu-id="523e1-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="523e1-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="523e1-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="523e1-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="523e1-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="523e1-115">Notes</span><span class="sxs-lookup"><span data-stu-id="523e1-115">Remarks</span></span>

<span data-ttu-id="523e1-116">La méthode libère toute la mémoire allouée pour les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="523e1-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="523e1-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="523e1-117">Requirements</span></span>



| <span data-ttu-id="523e1-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="523e1-118">Requirement</span></span> | <span data-ttu-id="523e1-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="523e1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="523e1-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="523e1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="523e1-121"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="523e1-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="523e1-122">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="523e1-122">Library</span></span><br/> | <dl> <span data-ttu-id="523e1-123"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="523e1-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="523e1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="523e1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="523e1-125">**Interface IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="523e1-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




