---
title: Propriétés et attributs ADSI
description: Les attributs sont parfois appelés propriétés. Cela peut entraîner une confusion. Cette documentation utilise les définitions suivantes pour les propriétés et les attributs.
ms.assetid: 8e391d36-5a8d-4960-805a-0caf281cab80
ms.tgt_platform: multiple
keywords:
- Propriétés et attributs ADSI ADSI
- ADSI ADSI, utilisation, accès et manipulation des données, des propriétés et des attributs
- propriétés ADSI
- attributs ADSI
- propriétés ADSI, définition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10c7b1dca9882f53b7fa746121ed431ace7f9af7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510591"
---
# <a name="adsi-properties-and-attributes"></a><span data-ttu-id="89f50-110">Propriétés et attributs ADSI</span><span class="sxs-lookup"><span data-stu-id="89f50-110">ADSI Properties and Attributes</span></span>

<span data-ttu-id="89f50-111">Les attributs sont parfois appelés propriétés.</span><span class="sxs-lookup"><span data-stu-id="89f50-111">Attributes are sometimes referred to as properties.</span></span> <span data-ttu-id="89f50-112">Cela peut entraîner une confusion.</span><span class="sxs-lookup"><span data-stu-id="89f50-112">This can cause confusion.</span></span> <span data-ttu-id="89f50-113">Cette documentation utilise les définitions suivantes pour les propriétés et les attributs.</span><span class="sxs-lookup"><span data-stu-id="89f50-113">This documentation uses the following definitions for properties and attributes.</span></span>

<span data-ttu-id="89f50-114">Les propriétés sont des valeurs nommées associées à un objet de programmation.</span><span class="sxs-lookup"><span data-stu-id="89f50-114">Properties are named values associated with a programming object.</span></span> <span data-ttu-id="89f50-115">Par exemple, l’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) expose des propriétés telles que [**Class**](iads-property-methods.md) et **Name**.</span><span class="sxs-lookup"><span data-stu-id="89f50-115">For example, the [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface exposes properties such as [**Class**](iads-property-methods.md) and **Name**.</span></span>

<span data-ttu-id="89f50-116">Les attributs sont les données associées aux objets dans un service d’annuaire.</span><span class="sxs-lookup"><span data-stu-id="89f50-116">Attributes are the data associated with objects in a directory service.</span></span> <span data-ttu-id="89f50-117">Par exemple, un objet utilisateur aura un attribut appelé **CN** qui contient une chaîne qui est le nom unique commun ou relatif de l’objet.</span><span class="sxs-lookup"><span data-stu-id="89f50-117">For example, a user object will have an attribute called **cn** which contains a string that is the common or relative distinguished name of the object.</span></span> <span data-ttu-id="89f50-118">Les attributs sont accessibles par le biais de méthodes d’interface ADSI comme [**IADs. obten**](/windows/desktop/api/Iads/nf-iads-iads-get) et [**IADs. put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span><span class="sxs-lookup"><span data-stu-id="89f50-118">Attributes are accessible through ADSI interface methods such as [**IADs.Get**](/windows/desktop/api/Iads/nf-iads-iads-get) and [**IADs.Put**](/windows/desktop/api/Iads/nf-iads-iads-put).</span></span>

<span data-ttu-id="89f50-119">Pour plus d’informations sur les propriétés et les attributs ADSI, consultez :</span><span class="sxs-lookup"><span data-stu-id="89f50-119">For more information about ADSI properties and attributes, see:</span></span>

-   [<span data-ttu-id="89f50-120">Le cache des attributs ADSI</span><span class="sxs-lookup"><span data-stu-id="89f50-120">The ADSI Attribute Cache</span></span>](the-adsi-attribute-cache.md)
-   [<span data-ttu-id="89f50-121">Attributs Single et multiple value</span><span class="sxs-lookup"><span data-stu-id="89f50-121">Single vs. Multiple Value Attributes</span></span>](single-vs--multiple-value-attributes.md)
-   [<span data-ttu-id="89f50-122">Active Directory attributs opérationnels</span><span class="sxs-lookup"><span data-stu-id="89f50-122">Active Directory Operational Attributes</span></span>](active-directory-operational-attributes.md)

 

 




