---
description: L’interface IPortableDeviceKeyCollection contient une collection de valeurs PROPERTYKEY. Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler CoCreate avec CLSID \_ PortableDeviceKeyCollection.
ms.assetid: 2460f5bc-6b1c-4e3b-bdb9-faaa6d6c87fd
title: Interface IPortableDeviceKeyCollection (PortableDeviceTypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: c246fabe7ced72a5aad6d30101df8035a159a923
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526759"
---
# <a name="iportabledevicekeycollection-interface"></a><span data-ttu-id="c8ff9-104">Interface IPortableDeviceKeyCollection</span><span class="sxs-lookup"><span data-stu-id="c8ff9-104">IPortableDeviceKeyCollection interface</span></span>

<span data-ttu-id="c8ff9-105">L’interface **IPortableDeviceKeyCollection** contient une collection de valeurs **PROPERTYKEY** .</span><span class="sxs-lookup"><span data-stu-id="c8ff9-105">The **IPortableDeviceKeyCollection** interface holds a collection of **PROPERTYKEY** values.</span></span> <span data-ttu-id="c8ff9-106">Cette interface peut être récupérée à partir d’une méthode ou, si un nouvel objet est requis, appeler **CoCreate** avec **CLSID \_ PortableDeviceKeyCollection**.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-106">This interface can be retrieved from a method or, if a new object is required, call **CoCreate** with **CLSID\_PortableDeviceKeyCollection**.</span></span>

## <a name="members"></a><span data-ttu-id="c8ff9-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c8ff9-107">Members</span></span>

<span data-ttu-id="c8ff9-108">L’interface **IPortableDeviceKeyCollection** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c8ff9-108">The **IPortableDeviceKeyCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c8ff9-109">**IPortableDeviceKeyCollection** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c8ff9-109">**IPortableDeviceKeyCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="c8ff9-110">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8ff9-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c8ff9-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c8ff9-111">Methods</span></span>

<span data-ttu-id="c8ff9-112">L’interface **IPortableDeviceKeyCollection** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-112">The **IPortableDeviceKeyCollection** interface has these methods.</span></span>



| <span data-ttu-id="c8ff9-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c8ff9-113">Method</span></span>                                                    | <span data-ttu-id="c8ff9-114">Description</span><span class="sxs-lookup"><span data-stu-id="c8ff9-114">Description</span></span>                                                                         |
|:----------------------------------------------------------|:------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8ff9-115">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-115">**Add**</span></span>](iportabledevicekeycollection-add.md)           | <span data-ttu-id="c8ff9-116">Ajoute une clé de propriété à la collection.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-116">Adds a property key to the collection.</span></span><br/>                                   |
| [<span data-ttu-id="c8ff9-117">**Effacé**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-117">**Clear**</span></span>](iportabledevicekeycollection-clear.md)       | <span data-ttu-id="c8ff9-118">Supprime tous les éléments de la collection.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-118">Deletes all items from the collection.</span></span><br/>                                   |
| [<span data-ttu-id="c8ff9-119">**GetAt**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-119">**GetAt**</span></span>](iportabledevicekeycollection-getat.md)       | <span data-ttu-id="c8ff9-120">Récupère une **PROPERTYKEY** de la collection par index.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-120">Retrieves a **PROPERTYKEY** from the collection by index.</span></span><br/>                |
| [<span data-ttu-id="c8ff9-121">**GetCount**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-121">**GetCount**</span></span>](iportabledevicekeycollection-getcount.md) | <span data-ttu-id="c8ff9-122">Récupère le nombre de clés de cette collection.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-122">Retrieves the number of keys in this collection.</span></span><br/>                         |
| [<span data-ttu-id="c8ff9-123">**RemoveAt**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-123">**RemoveAt**</span></span>](iportabledevicekeycollection-removeat.md) | <span data-ttu-id="c8ff9-124">Supprime l’élément stocké à l’emplacement spécifié par l’index donné.</span><span class="sxs-lookup"><span data-stu-id="c8ff9-124">Removes the element stored at the location specified by the given index.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c8ff9-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c8ff9-125">Requirements</span></span>



| <span data-ttu-id="c8ff9-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c8ff9-126">Requirement</span></span> | <span data-ttu-id="c8ff9-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="c8ff9-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ff9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="c8ff9-128">Header</span></span><br/>  | <dl> <span data-ttu-id="c8ff9-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ff9-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="c8ff9-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c8ff9-130">Library</span></span><br/> | <dl> <span data-ttu-id="c8ff9-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c8ff9-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ff9-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c8ff9-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ff9-133">**Interfaces de collection**</span><span class="sxs-lookup"><span data-stu-id="c8ff9-133">**Collection Interfaces**</span></span>](collection-interfaces.md)
</dt> </dl>

 

