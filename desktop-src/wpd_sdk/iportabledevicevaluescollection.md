---
description: L’interface IPortableDeviceValuesCollection contient une collection d’interfaces IPortableDeviceValues indexées de base zéro.
ms.assetid: 8bce9d27-f240-41ec-acf4-fefccdd95e9f
title: Interface IPortableDeviceValuesCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: cebe15dc9a4f4347eb58563e9b43240464565a4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533725"
---
# <a name="iportabledevicevaluescollection-interface"></a><span data-ttu-id="eefc1-103">Interface IPortableDeviceValuesCollection</span><span class="sxs-lookup"><span data-stu-id="eefc1-103">IPortableDeviceValuesCollection interface</span></span>

<span data-ttu-id="eefc1-104">L’interface **IPortableDeviceValuesCollection** contient une collection d’interfaces **IPortableDeviceValues** indexées de base zéro.</span><span class="sxs-lookup"><span data-stu-id="eefc1-104">The **IPortableDeviceValuesCollection** interface holds a collection of zero-based indexed **IPortableDeviceValues** interfaces.</span></span> <span data-ttu-id="eefc1-105">Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDeviceValuesCollection**.</span><span class="sxs-lookup"><span data-stu-id="eefc1-105">This interface can be retrieved from a method, or if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceValuesCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="eefc1-106">Membres</span><span class="sxs-lookup"><span data-stu-id="eefc1-106">Members</span></span>

<span data-ttu-id="eefc1-107">L’interface **IPortableDeviceValuesCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="eefc1-107">The **IPortableDeviceValuesCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="eefc1-108">**IPortableDeviceValuesCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="eefc1-108">**IPortableDeviceValuesCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="eefc1-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eefc1-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="eefc1-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="eefc1-110">Methods</span></span>

<span data-ttu-id="eefc1-111">L’interface **IPortableDeviceValuesCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="eefc1-111">The **IPortableDeviceValuesCollection** interface has these methods.</span></span>



| <span data-ttu-id="eefc1-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="eefc1-112">Method</span></span>                                                       | <span data-ttu-id="eefc1-113">Description</span><span class="sxs-lookup"><span data-stu-id="eefc1-113">Description</span></span>                                                                         |
|:-------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="eefc1-114">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="eefc1-114">**Add**</span></span>](iportabledevicevaluescollection-add.md)           | <span data-ttu-id="eefc1-115">Ajoute un élément à la collection</span><span class="sxs-lookup"><span data-stu-id="eefc1-115">Adds an item to the collection</span></span><br/>                                           |
| [<span data-ttu-id="eefc1-116">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="eefc1-116">**Clear**</span></span>](iportabledevicevaluescollection-clear.md)       | <span data-ttu-id="eefc1-117">Libère tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="eefc1-117">Releases all items from the collection.</span></span><br/>                                  |
| [<span data-ttu-id="eefc1-118">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="eefc1-118">**GetAt**</span></span>](iportabledevicevaluescollection-getat.md)       | <span data-ttu-id="eefc1-119">Récupère un élément de la collection par un index de base zéro.</span><span class="sxs-lookup"><span data-stu-id="eefc1-119">Retrieves an item from the collection by a zero-based index.</span></span><br/>             |
| [<span data-ttu-id="eefc1-120">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="eefc1-120">**GetCount**</span></span>](iportabledevicevaluescollection-getcount.md) | <span data-ttu-id="eefc1-121">Récupère le nombre d’éléments dans la collection.</span><span class="sxs-lookup"><span data-stu-id="eefc1-121">Retrieves the number of items in the collection.</span></span><br/>                         |
| [<span data-ttu-id="eefc1-122">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="eefc1-122">**RemoveAt**</span></span>](iportabledevicevaluescollection-removeat.md) | <span data-ttu-id="eefc1-123">Supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="eefc1-123">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="eefc1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eefc1-124">Requirements</span></span>



| <span data-ttu-id="eefc1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eefc1-125">Requirement</span></span> | <span data-ttu-id="eefc1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="eefc1-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eefc1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="eefc1-127">Header</span></span><br/>  | <dl> <span data-ttu-id="eefc1-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="eefc1-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="eefc1-129">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="eefc1-129">Library</span></span><br/> | <dl> <span data-ttu-id="eefc1-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eefc1-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eefc1-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eefc1-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eefc1-132">**Interfaces de collection**</span><span class="sxs-lookup"><span data-stu-id="eefc1-132">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

