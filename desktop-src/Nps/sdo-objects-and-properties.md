---
title: Objets et propriétés
description: Les caractéristiques d’un objet dans SDO sont déterminées par les propriétés de l’objet et les valeurs associées à ces propriétés.
ms.assetid: 9faa7759-cad5-4429-94b0-6cba145cfadb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efed7720388e61b9d6131acafd4b9bda17694d29
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510079"
---
# <a name="objects-and-properties"></a><span data-ttu-id="cff32-103">Objets et propriétés</span><span class="sxs-lookup"><span data-stu-id="cff32-103">Objects and Properties</span></span>

<span data-ttu-id="cff32-104">Les caractéristiques d’un objet dans SDO sont déterminées par les propriétés de l’objet et les valeurs associées à ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="cff32-104">The characteristics of an object in SDO are determined by the object's properties, and the values associated with those properties.</span></span> <span data-ttu-id="cff32-105">Contrairement à d’autres modèles objet, les objets SDO eux-mêmes n’ont pas de méthodes.</span><span class="sxs-lookup"><span data-stu-id="cff32-105">Unlike some other object models, SDO objects themselves do not have methods.</span></span> <span data-ttu-id="cff32-106">Toutefois, les objets SDO exposent des interfaces COM qui fournissent des méthodes.</span><span class="sxs-lookup"><span data-stu-id="cff32-106">However, SDO objects do expose COM interfaces that provide methods.</span></span>

<span data-ttu-id="cff32-107">Les objets dans SDO exposent l’interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) qui fournit des méthodes pour manipuler les propriétés des objets.</span><span class="sxs-lookup"><span data-stu-id="cff32-107">Objects in SDO expose the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface that provides methods for manipulating the objects properties.</span></span> <span data-ttu-id="cff32-108">Pour accéder aux propriétés de l’objet, obtenez une interface **ISdo** pour l’objet et utilisez les méthodes de l’interface [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) et [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) pour récupérer et définir les valeurs des propriétés.</span><span class="sxs-lookup"><span data-stu-id="cff32-108">To access the object's properties, obtain an **ISdo** interface for the object, and use the [**GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) and [**PutProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-putproperty) interface methods to retrieve and set values for the properties.</span></span> <span data-ttu-id="cff32-109">La rubrique [récupération d’un utilisateur SDO contient un](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) exemple de code qui illustre l’obtention de l’interface **ISdo** pour un objet utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cff32-109">The topic [Retrieving a User SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contains sample code that demonstrates obtaining the **ISdo** interface for a User object.</span></span>

<span data-ttu-id="cff32-110">Après avoir apporté des modifications aux propriétés d’un objet, utilisez la méthode [**ISdo :: apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) pour écrire les modifications dans le stockage persistant de l’objet.</span><span class="sxs-lookup"><span data-stu-id="cff32-110">After making changes to the properties of an object, use the [**ISdo::Apply**](/windows/desktop/api/sdoias/nf-sdoias-isdo-apply) method to write the changes to persistent storage for the object.</span></span> <span data-ttu-id="cff32-111">Vous pouvez annuler les modifications apportées aux propriétés d’un objet avant d’appeler **ISdo :: apply** en appelant la méthode [**ISdo :: Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) .</span><span class="sxs-lookup"><span data-stu-id="cff32-111">You can cancel changes made to an object's properties before you call **ISdo::Apply** by calling the [**ISdo::Restore**](/windows/desktop/api/sdoias/nf-sdoias-isdo-restore) method.</span></span> <span data-ttu-id="cff32-112">Cette méthode restaure les valeurs des propriétés d’un objet à partir d’un stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="cff32-112">This method restores the values of an object's properties from persistent storage.</span></span>

<span data-ttu-id="cff32-113">Le tableau suivant présente les types d’énumération qui énumèrent les propriétés de certains objets dans SDO.</span><span class="sxs-lookup"><span data-stu-id="cff32-113">The following table shows the enumeration types that enumerate the properties of some of the objects in SDO.</span></span>



| <span data-ttu-id="cff32-114">Object</span><span class="sxs-lookup"><span data-stu-id="cff32-114">Object</span></span>                                 | <span data-ttu-id="cff32-115">Type d'énumération</span><span class="sxs-lookup"><span data-stu-id="cff32-115">Enumeration type</span></span>                                       |
|----------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="cff32-116">Tous les objets SDO</span><span class="sxs-lookup"><span data-stu-id="cff32-116">All SDO objects</span></span>                        | [<span data-ttu-id="cff32-117">**IASCOMMONPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="cff32-117">**IASCOMMONPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iascommonproperties) |
| <span data-ttu-id="cff32-118">Objet utilisateur</span><span class="sxs-lookup"><span data-stu-id="cff32-118">User Object</span></span>                            | [<span data-ttu-id="cff32-119">**USERPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="cff32-119">**USERPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-userproperties)           |
| <span data-ttu-id="cff32-120">Objet de service (serveur de stratégie réseau)</span><span class="sxs-lookup"><span data-stu-id="cff32-120">Service Object (Network Policy Server)</span></span> | [<span data-ttu-id="cff32-121">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="cff32-121">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)             |
| <span data-ttu-id="cff32-122">Objet de protocole RADIUS Microsoft</span><span class="sxs-lookup"><span data-stu-id="cff32-122">Microsoft RADIUS Protocol Object</span></span>       | [<span data-ttu-id="cff32-123">**RADIUSPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="cff32-123">**RADIUSPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-radiusproperties)       |



 

> [!Note]  
> <span data-ttu-id="cff32-124">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="cff32-124">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

## <a name="collections"></a><span data-ttu-id="cff32-125">Regroupements</span><span class="sxs-lookup"><span data-stu-id="cff32-125">Collections</span></span>

<span data-ttu-id="cff32-126">Les objets sont souvent regroupés dans des collections.</span><span class="sxs-lookup"><span data-stu-id="cff32-126">Objects are often grouped into collections.</span></span> <span data-ttu-id="cff32-127">L’API SDO fournit des fonctionnalités, via l’interface de [**collection ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) , pour énumérer les objets dans une collection et pour ajouter et supprimer des objets d’une collection.</span><span class="sxs-lookup"><span data-stu-id="cff32-127">The SDO API provides functionality, through the [**ISdo Collection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection) interface, to enumerate the objects in a collection and to add and delete objects from a collection.</span></span>

<span data-ttu-id="cff32-128">L’accès à une collection est obtenu en extrayant une propriété de collection sur l’objet qui contient la collection.</span><span class="sxs-lookup"><span data-stu-id="cff32-128">Access to a collection is obtained by retrieving a collection property on the object that contains the collection.</span></span> <span data-ttu-id="cff32-129">Pour plus d’informations, consultez la section [hiérarchie du modèle objet](/windows/desktop/Nps/sdo-object-model-hierarchy).</span><span class="sxs-lookup"><span data-stu-id="cff32-129">For more information, see the section [Object Model Hierarchy](/windows/desktop/Nps/sdo-object-model-hierarchy).</span></span>

<span data-ttu-id="cff32-130">Le type de données pour toutes les propriétés qui correspondent aux collections est VT \_ Dispatch.</span><span class="sxs-lookup"><span data-stu-id="cff32-130">The data type for all properties that correspond to collections is VT\_DISPATCH.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cff32-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cff32-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cff32-132">Hiérarchie du modèle objet SDO</span><span class="sxs-lookup"><span data-stu-id="cff32-132">SDO Object Model Hierarchy</span></span>](/windows/desktop/Nps/sdo-object-model-hierarchy)
</dt> <dt>

[<span data-ttu-id="cff32-133">Attributs pris en charge par SDO</span><span class="sxs-lookup"><span data-stu-id="cff32-133">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 