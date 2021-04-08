---
title: CENUMSCH. COTISATIONS
description: Dans l’exemple de composant fournisseur, l’énumération d’un objet de schéma utilise les méthodes de cenumsch. cpp, énumérées dans le tableau suivant.
ms.assetid: edad1ad1-16b9-40f3-b841-a70aa7fff5d9
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adcc6d053bb698817ff73db876b00640ed00c8ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839229"
---
# <a name="cenumschcpp"></a><span data-ttu-id="fb327-103">CENUMSCH. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="fb327-103">CENUMSCH.CPP</span></span>

<span data-ttu-id="fb327-104">Dans l’exemple de composant fournisseur, l’énumération d’un objet de schéma utilise les méthodes de cenumsch. cpp, énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fb327-104">In the example provider component, the enumeration of a schema object uses the methods, from cenumsch.cpp, listed in the following table.</span></span>



| <span data-ttu-id="fb327-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="fb327-105">Method</span></span>                                        | <span data-ttu-id="fb327-106">Description</span><span class="sxs-lookup"><span data-stu-id="fb327-106">Description</span></span>                                                                                                          |
|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb327-107">**CSampleDSSchemaEnum :: Create**</span><span class="sxs-lookup"><span data-stu-id="fb327-107">**CSampleDSSchemaEnum::Create**</span></span>               | <span data-ttu-id="fb327-108">Créez un objet pour permettre l’énumération d’un objet de classe de schéma ADSI.</span><span class="sxs-lookup"><span data-stu-id="fb327-108">Create an object to allow enumeration of an ADSI schema class object.</span></span>                                                |
| <span data-ttu-id="fb327-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="fb327-109">**CSampleDSSchemaEnum::CSampleDSSchemaEnum**</span></span>  | <span data-ttu-id="fb327-110">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="fb327-110">Standard constructor.</span></span>                                                                                                |
| <span data-ttu-id="fb327-111">**CSampleDSSchemaEnum :: ~ CSampleDSSchemaEnum**</span><span class="sxs-lookup"><span data-stu-id="fb327-111">**CSampleDSSchemaEnum::~CSampleDSSchemaEnum**</span></span> | <span data-ttu-id="fb327-112">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="fb327-112">Standard destructor.</span></span>                                                                                                 |
| <span data-ttu-id="fb327-113">**CSampleDSSchemaEnum :: suivant**</span><span class="sxs-lookup"><span data-stu-id="fb327-113">**CSampleDSSchemaEnum::Next**</span></span>                 | <span data-ttu-id="fb327-114">Récupère le nombre spécifié d’éléments de l’objet de schéma indiqué.</span><span class="sxs-lookup"><span data-stu-id="fb327-114">Retrieve the specified number of elements from the schema object indicated.</span></span>                                          |
| <span data-ttu-id="fb327-115">**CSampleDSSchemaEnum :: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="fb327-115">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="fb327-116">Gérez la récupération des pointeurs d’interfaces vers les objets du type d’objet indiqué.</span><span class="sxs-lookup"><span data-stu-id="fb327-116">Manage retrieving the interfaces pointers to the objects of the object type indicated.</span></span>                               |
| <span data-ttu-id="fb327-117">**CSampleDSSchemaEnum :: EnumObjects**</span><span class="sxs-lookup"><span data-stu-id="fb327-117">**CSampleDSSchemaEnum::EnumObjects**</span></span>          | <span data-ttu-id="fb327-118">Gérer la récupération des pointeurs d’interface vers les objets du type d’objet par défaut.</span><span class="sxs-lookup"><span data-stu-id="fb327-118">Manage retrieving the interface pointers to the objects of the default object type.</span></span>                                  |
| <span data-ttu-id="fb327-119">**CSampleDSSchemaEnum::EnumClasses**</span><span class="sxs-lookup"><span data-stu-id="fb327-119">**CSampleDSSchemaEnum::EnumClasses**</span></span>          | <span data-ttu-id="fb327-120">Gérer la récupération des pointeurs d’interface uniquement sur les objets de classe de schéma contenus dans cet objet.</span><span class="sxs-lookup"><span data-stu-id="fb327-120">Manage retrieving the interface pointers to only the schema class objects contained in this object.</span></span>                  |
| <span data-ttu-id="fb327-121">**CSampleDSSchemaEnum :: GetClassObject,**</span><span class="sxs-lookup"><span data-stu-id="fb327-121">**CSampleDSSchemaEnum::GetClassObject**</span></span>       | <span data-ttu-id="fb327-122">Récupère la définition de classe de schéma suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="fb327-122">Retrieve the next schema class definition; if found, create a schema class object, and return the interface pointer.</span></span> |
| <span data-ttu-id="fb327-123">**CSampleDSSchemaEnum :: EnumProperties,**</span><span class="sxs-lookup"><span data-stu-id="fb327-123">**CSampleDSSchemaEnum::EnumProperties**</span></span>       | <span data-ttu-id="fb327-124">Gérer la récupération des pointeurs d’interface vers les objets de propriété contenus uniquement dans cet objet.</span><span class="sxs-lookup"><span data-stu-id="fb327-124">Manage retrieving the interface pointers to the property objects only contained in this object.</span></span>                      |
| <span data-ttu-id="fb327-125">**CSampleDSSchemaEnum::GetPropertyObject**</span><span class="sxs-lookup"><span data-stu-id="fb327-125">**CSampleDSSchemaEnum::GetPropertyObject**</span></span>    | <span data-ttu-id="fb327-126">Récupère la définition de propriété suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="fb327-126">Retrieve the next property definition; if found, create a schema class object, and return the interface pointer.</span></span>     |
| <span data-ttu-id="fb327-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span><span class="sxs-lookup"><span data-stu-id="fb327-127">**CSampleDSSchemaEnum::EnumSyntaxes**</span></span>         | <span data-ttu-id="fb327-128">Gérer la récupération des pointeurs d’interface vers les objets de syntaxe contenus uniquement dans cet objet.</span><span class="sxs-lookup"><span data-stu-id="fb327-128">Manage retrieving the interface pointers to the syntax objects only contained in this object.</span></span>                        |
| <span data-ttu-id="fb327-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span><span class="sxs-lookup"><span data-stu-id="fb327-129">**CSampleDSSchemaEnum::GetSyntaxObject**</span></span>      | <span data-ttu-id="fb327-130">Récupérer la définition de la syntaxe suivante ; s’il est trouvé, créez un objet de classe de schéma et retournez le pointeur d’interface.</span><span class="sxs-lookup"><span data-stu-id="fb327-130">Retrieve the next syntax definition; if found, create a schema class object, and return the interface pointer.</span></span>       |



 

 

 




