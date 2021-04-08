---
title: CPROPS. COTISATIONS
description: Dans l’exemple de composant fournisseur, vous trouverez un exemple d’implémentation de cache de propriété dans cProps. cpp. Les méthodes prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: 51c9aa05-ca30-4d61-b3e3-d2f17a02b28f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77b9f4fddfea6900fd8d7a06bee9979744eefd30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839217"
---
# <a name="cpropscpp"></a><span data-ttu-id="d5aac-104">CPROPS. COTISATIONS</span><span class="sxs-lookup"><span data-stu-id="d5aac-104">CPROPS.CPP</span></span>

<span data-ttu-id="d5aac-105">Dans l’exemple de composant fournisseur, vous trouverez un exemple d’implémentation de cache de propriété dans cProps. cpp.</span><span class="sxs-lookup"><span data-stu-id="d5aac-105">In the example provider component, an example of a property cache implementation can be found in cprops.cpp.</span></span> <span data-ttu-id="d5aac-106">Les méthodes prises en charge sont répertoriées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="d5aac-106">Supported methods are listed in the following table.</span></span>



| <span data-ttu-id="d5aac-107">Méthode</span><span class="sxs-lookup"><span data-stu-id="d5aac-107">Method</span></span>                                           | <span data-ttu-id="d5aac-108">Description</span><span class="sxs-lookup"><span data-stu-id="d5aac-108">Description</span></span>                                                                                                         |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5aac-109">**CPropertyCache :: AddProperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-109">**CPropertyCache::addproperty**</span></span>                  | <span data-ttu-id="d5aac-110">Étendez le cache des propriétés en ajoutant un nouveau.</span><span class="sxs-lookup"><span data-stu-id="d5aac-110">Extend the property cache by adding a new one.</span></span>                                                                      |
| <span data-ttu-id="d5aac-111">**CPropertyCache::updateproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-111">**CPropertyCache::updateproperty**</span></span>               | <span data-ttu-id="d5aac-112">Recherchez la propriété, libérez son contenu et utilisez de nouvelles valeurs à la place. Marquez ensuite le cache modifié pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d5aac-112">Look up the property, free its contents, and use new values instead; then mark the cache changed for this property.</span></span> |
| <span data-ttu-id="d5aac-113">**CPropertyCache::findproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-113">**CPropertyCache::findproperty**</span></span>                 | <span data-ttu-id="d5aac-114">Recherchez cette propriété par nom ; enregistrez son index.</span><span class="sxs-lookup"><span data-stu-id="d5aac-114">Look up this property by name; save its index.</span></span>                                                                      |
| <span data-ttu-id="d5aac-115">**CPropertyCache :: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-115">**CPropertyCache::getproperty**</span></span>                  | <span data-ttu-id="d5aac-116">Recherchez la propriété dans le cache si elle est disponible, sinon appelez **GetInfo**.</span><span class="sxs-lookup"><span data-stu-id="d5aac-116">Find the property in the cache if available, otherwise call **GetInfo**.</span></span> <span data-ttu-id="d5aac-117">Définissez l’index et copiez-les dans les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5aac-117">Set the index and copy in the new values.</span></span>  |
| <span data-ttu-id="d5aac-118">**CPropertyCache ::p utproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-118">**CPropertyCache::putproperty**</span></span>                  | <span data-ttu-id="d5aac-119">Recherchez la propriété.</span><span class="sxs-lookup"><span data-stu-id="d5aac-119">Find the property.</span></span> <span data-ttu-id="d5aac-120">Libérez ce qui était là et placez les nouvelles valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5aac-120">Free what was there and put in new values.</span></span>                                                       |
| <span data-ttu-id="d5aac-121">**CPropertyCache::CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="d5aac-121">**CPropertyCache::CPropertyCache**</span></span>               | <span data-ttu-id="d5aac-122">Constructeur standard.</span><span class="sxs-lookup"><span data-stu-id="d5aac-122">Standard constructor.</span></span>                                                                                               |
| <span data-ttu-id="d5aac-123">**CPropertyCache :: ~ CPropertyCache**</span><span class="sxs-lookup"><span data-stu-id="d5aac-123">**CPropertyCache::~CPropertyCache**</span></span>              | <span data-ttu-id="d5aac-124">Destructeur standard.</span><span class="sxs-lookup"><span data-stu-id="d5aac-124">Standard destructor.</span></span>                                                                                                |
| <span data-ttu-id="d5aac-125">**CPropertyCache::createpropertycache**</span><span class="sxs-lookup"><span data-stu-id="d5aac-125">**CPropertyCache::createpropertycache**</span></span>          | <span data-ttu-id="d5aac-126">Créez le cache.</span><span class="sxs-lookup"><span data-stu-id="d5aac-126">Create the cache.</span></span>                                                                                                   |
| <span data-ttu-id="d5aac-127">**CPropertyCache::unboundgetproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-127">**CPropertyCache::unboundgetproperty**</span></span>           | <span data-ttu-id="d5aac-128">Recherchez la propriété dans le cache et affectez-lui ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="d5aac-128">Find the property in the cache and set it to these values.</span></span>                                                          |
| <span data-ttu-id="d5aac-129">**CPropertyCache::SampleDSMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="d5aac-129">**CPropertyCache::SampleDSMarshallProperties**</span></span>   | <span data-ttu-id="d5aac-130">Marshaler les données et les valeurs de propriété.</span><span class="sxs-lookup"><span data-stu-id="d5aac-130">Marshal property data and values.</span></span>                                                                                   |
| <span data-ttu-id="d5aac-131">**CPropertyCache::marshallproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-131">**CPropertyCache::marshallproperty**</span></span>             | <span data-ttu-id="d5aac-132">Marshale une propriété.</span><span class="sxs-lookup"><span data-stu-id="d5aac-132">Marshal a property.</span></span>                                                                                                 |
| <span data-ttu-id="d5aac-133">**CPropertyCache::SampleDSUnMarshallProperties**</span><span class="sxs-lookup"><span data-stu-id="d5aac-133">**CPropertyCache::SampleDSUnMarshallProperties**</span></span> | <span data-ttu-id="d5aac-134">Données et valeurs de propriété démarshalées.</span><span class="sxs-lookup"><span data-stu-id="d5aac-134">Unmarshal property data and values.</span></span>                                                                                 |
| <span data-ttu-id="d5aac-135">**CPropertyCache::unmarshallproperty**</span><span class="sxs-lookup"><span data-stu-id="d5aac-135">**CPropertyCache::unmarshallproperty**</span></span>           | <span data-ttu-id="d5aac-136">Démarshaler une propriété.</span><span class="sxs-lookup"><span data-stu-id="d5aac-136">Unmarshal a property.</span></span>                                                                                               |



 

 

 




