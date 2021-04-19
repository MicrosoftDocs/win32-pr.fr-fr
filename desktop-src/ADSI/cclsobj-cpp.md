---
title: CCLSOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les fonctions de l’objet de classe de schéma sont contenues dans cclsobj. cpp.
ms.assetid: e8cdef8e-c031-49e0-9496-871064aec8bd
ms.tgt_platform: multiple
keywords:
- CSampleDSClass
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f23c198413819627ce1fcb5a605bd8e45faae0ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510999"
---
# <a name="cclsobjcpp"></a><span data-ttu-id="c3be9-104">CCLSOBJ. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="c3be9-104">CCLSOBJ.CPP</span></span>

<span data-ttu-id="c3be9-105">Dans l’exemple de composant fournisseur, les fonctions de l’objet de classe de schéma sont contenues dans cclsobj. cpp.</span><span class="sxs-lookup"><span data-stu-id="c3be9-105">In the example provider component, the functions for the schema class object are contained in cclsobj.cpp.</span></span>

<span data-ttu-id="c3be9-106">La classe **CSampleDSClass** est définie dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="c3be9-106">The **CSampleDSClass** class is defined in this file.</span></span> <span data-ttu-id="c3be9-107">**CSampleDSClass** est défini avec les méthodes et les propriétés énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="c3be9-107">**CSampleDSClass** is defined with methods and properties listed in the following table.</span></span>



| <span data-ttu-id="c3be9-108">Méthode</span><span class="sxs-lookup"><span data-stu-id="c3be9-108">Method</span></span>                      | <span data-ttu-id="c3be9-109">Description</span><span class="sxs-lookup"><span data-stu-id="c3be9-109">Description</span></span>                                                                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3be9-110">**CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="c3be9-110">**CSampleDSClass**</span></span>          | <span data-ttu-id="c3be9-111">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="c3be9-111">Standard constructor.</span></span>                                                                                                                                                                                      |
| <span data-ttu-id="c3be9-112">**~ CSampleDSClass**</span><span class="sxs-lookup"><span data-stu-id="c3be9-112">**~CSampleDSClass**</span></span>         | <span data-ttu-id="c3be9-113">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="c3be9-113">Standard destructor.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="c3be9-114">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="c3be9-114">**CreateClass**</span></span>             | <span data-ttu-id="c3be9-115">Créez un objet de classe de schéma ADs.</span><span class="sxs-lookup"><span data-stu-id="c3be9-115">Create an ADs schema class object.</span></span> <span data-ttu-id="c3be9-116">Recherchez les définitions d’attribut en appelant **SampleDSGetClassDefinition**.</span><span class="sxs-lookup"><span data-stu-id="c3be9-116">Lookup attribute definitions by calling **SampleDSGetClassDefinition**.</span></span>                                                                                                 |
| <span data-ttu-id="c3be9-117">**CreateClass**</span><span class="sxs-lookup"><span data-stu-id="c3be9-117">**CreateClass**</span></span>             | <span data-ttu-id="c3be9-118">Créez un objet de classe de schéma, en fonction des définitions d’attributs, en définissant des attributs connus, tels que ceux répertoriés dans [**IADsClass :: MandatoryAttributes**](iadsclass-property-methods.md).</span><span class="sxs-lookup"><span data-stu-id="c3be9-118">Create a schema class object, given the attribute definitions, setting known attributes, such as those listed in [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md).</span></span>                     |
| <span data-ttu-id="c3be9-119">**AllocateClassObject**</span><span class="sxs-lookup"><span data-stu-id="c3be9-119">**AllocateClassObject**</span></span>     | <span data-ttu-id="c3be9-120">Créez un objet de classe de schéma et chargez ses données de type.</span><span class="sxs-lookup"><span data-stu-id="c3be9-120">Create a schema class object and load its type data.</span></span>                                                                                                                                                       |
| <span data-ttu-id="c3be9-121">**QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="c3be9-121">**QueryInterface**</span></span>          | <span data-ttu-id="c3be9-122">Retourne le pointeur d’interface demandé, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="c3be9-122">Return the requested interface pointer, if available.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c3be9-123">Méthodes IADs standard.</span><span class="sxs-lookup"><span data-stu-id="c3be9-123">Standard IADs methods.</span></span>      | <span data-ttu-id="c3be9-124">Méthodes d’interface [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard incluses dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="c3be9-124">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) interface methods included in this file.</span></span>                                                                                                                                     |
| <span data-ttu-id="c3be9-125">Méthodes IADsClass standard.</span><span class="sxs-lookup"><span data-stu-id="c3be9-125">Standard IADsClass methods.</span></span> | <span data-ttu-id="c3be9-126">Méthodes d’interface [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) standard incluses dans ce fichier.</span><span class="sxs-lookup"><span data-stu-id="c3be9-126">Standard [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface methods included in this file.</span></span>                                                                                                                           |
| <span data-ttu-id="c3be9-127">**CreatePropertyList**</span><span class="sxs-lookup"><span data-stu-id="c3be9-127">**CreatePropertyList**</span></span>      | <span data-ttu-id="c3be9-128">Créez une liste de propriétés associées à cette classe de schéma en appelant **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="c3be9-128">Create a list of properties associated with this schema class by calling **CreatePropertyEntry**.</span></span>                                                                                                          |
| <span data-ttu-id="c3be9-129">**CreatePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="c3be9-129">**CreatePropertyEntry**</span></span>     | <span data-ttu-id="c3be9-130">Créez un objet de propriété dans cette classe de schéma.</span><span class="sxs-lookup"><span data-stu-id="c3be9-130">Create one property object in this schema class.</span></span>                                                                                                                                                           |
| <span data-ttu-id="c3be9-131">**FreePropertyEntry**</span><span class="sxs-lookup"><span data-stu-id="c3be9-131">**FreePropertyEntry**</span></span>       | <span data-ttu-id="c3be9-132">Libérez l’entrée dans **CreatePropertyEntry**.</span><span class="sxs-lookup"><span data-stu-id="c3be9-132">Free the entry made in **CreatePropertyEntry**.</span></span>                                                                                                                                                            |
| <span data-ttu-id="c3be9-133">**MakeVariantFromPropList**</span><span class="sxs-lookup"><span data-stu-id="c3be9-133">**MakeVariantFromPropList**</span></span> | <span data-ttu-id="c3be9-134">Créez un tableau de VARIANTs à partir de la liste de propriétés créée par **CreatePropertyList**.</span><span class="sxs-lookup"><span data-stu-id="c3be9-134">Create an array of VARIANTS from the property list created by **CreatePropertyList**.</span></span> <span data-ttu-id="c3be9-135">Peut être utilisé dans l’implémentation de [**IADsClass :: MandatoryAttributes**](iadsclass-property-methods.md) , et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="c3be9-135">Can be used in the implementation of [**IADsClass::MandatoryAttributes**](iadsclass-property-methods.md) and so on.</span></span> |



 

 

 




