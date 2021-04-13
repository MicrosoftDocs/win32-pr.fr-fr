---
title: CPRPOBJ. COTISATIONS
description: Dans l’exemple de composant fournisseur, les méthodes d’objet de propriété, dans cprpobj. cpp, sont répertoriées dans le tableau suivant.
ms.assetid: 88628b9b-12e6-4d64-9a21-b30f7392a5f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 948409cc135daaffa249f8aa0b3729b34799957c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190744"
---
# <a name="cprpobjcpp"></a><span data-ttu-id="3eaac-103">CPRPOBJ. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="3eaac-103">CPRPOBJ.CPP</span></span>

<span data-ttu-id="3eaac-104">Dans l’exemple de composant fournisseur, les méthodes d’objet de propriété, dans cprpobj. cpp, sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3eaac-104">In the example provider component, property object methods, in cprpobj.cpp, are listed in the following table.</span></span>



| <span data-ttu-id="3eaac-105">Méthode</span><span class="sxs-lookup"><span data-stu-id="3eaac-105">Method</span></span>                                                 | <span data-ttu-id="3eaac-106">Description</span><span class="sxs-lookup"><span data-stu-id="3eaac-106">Description</span></span>                                                                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3eaac-107">**CSampleDSProperty::CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="3eaac-107">**CSampleDSProperty::CSampleDSProperty**</span></span>               | <span data-ttu-id="3eaac-108">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="3eaac-108">Standard constructor.</span></span>                                                                                                                          |
| <span data-ttu-id="3eaac-109">**CSampleDSProperty :: ~ CSampleDSProperty**</span><span class="sxs-lookup"><span data-stu-id="3eaac-109">**CSampleDSProperty::~CSampleDSProperty**</span></span>              | <span data-ttu-id="3eaac-110">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="3eaac-110">Standard destructor.</span></span>                                                                                                                           |
| <span data-ttu-id="3eaac-111">**CSampleDSProperty :: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="3eaac-111">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="3eaac-112">Créez un objet de propriété ADS, en recherchant les définitions d’attributs en appelant **SampleDSGetPropertyDefinition**.</span><span class="sxs-lookup"><span data-stu-id="3eaac-112">Create an ADS Property object, looking up the attribute definitions by calling **SampleDSGetPropertyDefinition**.</span></span>                              |
| <span data-ttu-id="3eaac-113">**CSampleDSProperty :: CreateProperty**</span><span class="sxs-lookup"><span data-stu-id="3eaac-113">**CSampleDSProperty::CreateProperty**</span></span>                  | <span data-ttu-id="3eaac-114">À partir de la définition d’attribut, créez un objet de propriété, en définissant la correspondance entre les syntaxes ADS prises en charge et les syntaxes du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3eaac-114">Given the attribute definition, create a property object, setting the correspondence between supported ADS syntaxes and the provider syntaxes.</span></span> |
| <span data-ttu-id="3eaac-115">**CSampleDSProperty::AllocatePropertyObject**</span><span class="sxs-lookup"><span data-stu-id="3eaac-115">**CSampleDSProperty::AllocatePropertyObject**</span></span>          | <span data-ttu-id="3eaac-116">Créez un objet de propriété et chargez ses données de type.</span><span class="sxs-lookup"><span data-stu-id="3eaac-116">Create a property object and load its type data.</span></span>                                                                                               |
| <span data-ttu-id="3eaac-117">**CSampleDSProperty :: QueryInterface**</span><span class="sxs-lookup"><span data-stu-id="3eaac-117">**CSampleDSProperty::QueryInterface**</span></span>                  | <span data-ttu-id="3eaac-118">Retourne le pointeur d’interface demandé, s’il est disponible.</span><span class="sxs-lookup"><span data-stu-id="3eaac-118">Return the requested interface pointer, if available.</span></span>                                                                                          |
| <span data-ttu-id="3eaac-119">Méthodes [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) standard.</span><span class="sxs-lookup"><span data-stu-id="3eaac-119">Standard [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) methods.</span></span>                 |                                                                                                                                                |
| <span data-ttu-id="3eaac-120">Méthodes [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) standard.</span><span class="sxs-lookup"><span data-stu-id="3eaac-120">Standard [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty) methods.</span></span> |                                                                                                                                                |
| <span data-ttu-id="3eaac-121">**MapSyntaxIdtoADsSyntax**</span><span class="sxs-lookup"><span data-stu-id="3eaac-121">**MapSyntaxIdtoADsSyntax**</span></span>                             | <span data-ttu-id="3eaac-122">Définissez la correspondance entre l’ID de syntaxe et la syntaxe ADS.</span><span class="sxs-lookup"><span data-stu-id="3eaac-122">Set the correspondence between the syntax ID and the ADS syntax.</span></span>                                                                               |
| <span data-ttu-id="3eaac-123">**MapSyntaxIdtoSampleDSSyntax**</span><span class="sxs-lookup"><span data-stu-id="3eaac-123">**MapSyntaxIdtoSampleDSSyntax**</span></span>                        | <span data-ttu-id="3eaac-124">Définissez la correspondance entre l’ID de syntaxe et la syntaxe du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="3eaac-124">Set the correspondence between the syntax ID and the provider syntax.</span></span>                                                                          |



 

 

 




