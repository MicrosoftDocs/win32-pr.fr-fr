---
title: Classes et associations par défaut
description: Pour certaines catégories, une seule classe peut être associée en tant que classe par défaut.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 871c537535c57da0809effbe3ee8ec086a88fd5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379614"
---
# <a name="default-classes-and-associations"></a><span data-ttu-id="7c490-103">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="7c490-103">Default Classes and Associations</span></span>

<span data-ttu-id="7c490-104">Pour certaines catégories, une seule classe peut être associée en tant que classe par défaut.</span><span class="sxs-lookup"><span data-stu-id="7c490-104">For certain categories, a single class can be associated as the default class.</span></span> <span data-ttu-id="7c490-105">La classe par défaut est sélectionnée chaque fois que cette catégorie particulière d’objet est requise.</span><span class="sxs-lookup"><span data-stu-id="7c490-105">The default class is selected whenever that particular category of object is required.</span></span> <span data-ttu-id="7c490-106">Bien que cela ne soit peut-être pas utile pour toutes les catégories de composants, l’établissement d’une classe par défaut peut être utile lorsqu’une classe particulière doit être chargée à partir d’une liste de classes possibles sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="7c490-106">While this may not be useful for all component categories, establishing a default class can be helpful when a particular class must be loaded from a list of possible classes without user intervention.</span></span> <span data-ttu-id="7c490-107">Les administrateurs définissent la classe qui peut être utilisée en manipulant le registre.</span><span class="sxs-lookup"><span data-stu-id="7c490-107">Administrators define which class can be used by manipulating the registry.</span></span>

<span data-ttu-id="7c490-108">Pour associer une classe par défaut à une catégorie, introduisez une clé CLSID avec le même CLSID que le CATID de la catégorie de composant choisie comme valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="7c490-108">To associate a default class with a category, introduce a CLSID key with the same CLSID as the CATID of the component category chosen as the default.</span></span> <span data-ttu-id="7c490-109">Ajoutez ensuite une clé TreatAs à cette clé, en utilisant la valeur du CLSID de la classe par défaut pour la catégorie.</span><span class="sxs-lookup"><span data-stu-id="7c490-109">Then add a TreatAs key to this key, using the value for the CLSID of the default class for the category.</span></span> <span data-ttu-id="7c490-110">Pour utiliser la classe par défaut pour une catégorie de composant, utilisez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), en spécifiant le CATID pour le paramètre CLSID.</span><span class="sxs-lookup"><span data-stu-id="7c490-110">To use the default class for a component category, use [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), specifying the CATID for the CLSID parameter.</span></span> <span data-ttu-id="7c490-111">Cela permet de rediriger automatiquement le CLSID établi comme valeur par défaut pour cette catégorie.</span><span class="sxs-lookup"><span data-stu-id="7c490-111">This automatically redirects to the CLSID established as the default for this category.</span></span> <span data-ttu-id="7c490-112">L’entrée de Registre est la suivante :</span><span class="sxs-lookup"><span data-stu-id="7c490-112">The registry entry is as follows:</span></span>

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

<span data-ttu-id="7c490-113">Pendant l’installation, un composant peut vérifier l’existence de toutes les clés de classe par défaut pour ses catégories et présenter à l’utilisateur les options permettant de remplacer les paramètres actuels.</span><span class="sxs-lookup"><span data-stu-id="7c490-113">During installation, a component can check for the existence of any default class keys for its categories and present the user with options for overriding the current settings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c490-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c490-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c490-115">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="7c490-115">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="7c490-116">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="7c490-116">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7c490-117">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="7c490-117">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="7c490-118">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="7c490-118">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> <dt>

[<span data-ttu-id="7c490-119">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="7c490-119">The Component Categories Manager</span></span>](the-component-categories-manager.md)
</dt> </dl>

 

 




