---
title: Gestionnaire de catégories de composants
description: Gestionnaire de catégories de composants
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462195"
---
# <a name="the-component-categories-manager"></a><span data-ttu-id="f9bc4-103">Gestionnaire de catégories de composants</span><span class="sxs-lookup"><span data-stu-id="f9bc4-103">The Component Categories Manager</span></span>

<span data-ttu-id="f9bc4-104">Pour faciliter la gestion des catégories de composants et garantir la cohérence du Registre, le système fournit le gestionnaire de catégories de composants, un objet COM avec un CLSID de CLSID \_ StdComponentCategoriesMgr.</span><span class="sxs-lookup"><span data-stu-id="f9bc4-104">To facilitate the handling of component categories and to guarantee consistency of the registry, the system provides the Component Categories Manager, a COM object with a CLSID of CLSID\_StdComponentCategoriesMgr.</span></span> <span data-ttu-id="f9bc4-105">Cet objet COM fournit les interfaces suivantes :</span><span class="sxs-lookup"><span data-stu-id="f9bc4-105">This COM object provides the following interfaces:</span></span>

-   [<span data-ttu-id="f9bc4-106">**ICatInformation**</span><span class="sxs-lookup"><span data-stu-id="f9bc4-106">**ICatInformation**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [<span data-ttu-id="f9bc4-107">**ICatRegister**</span><span class="sxs-lookup"><span data-stu-id="f9bc4-107">**ICatRegister**</span></span>](/windows/desktop/api/ComCat/nn-comcat-icatregister)

<span data-ttu-id="f9bc4-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fournit des méthodes pour obtenir des informations sur les catégories implémentées ou requises par une certaine classe et fournit des informations sur les catégories inscrites sur un ordinateur donné.</span><span class="sxs-lookup"><span data-stu-id="f9bc4-108">[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) provides methods for obtaining information about the categories implemented or required by a certain class and provides information about the categories registered on a given machine.</span></span>

<span data-ttu-id="f9bc4-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fournit des méthodes pour inscrire et annuler l’enregistrement des informations de catégorie de composants dans le registre.</span><span class="sxs-lookup"><span data-stu-id="f9bc4-109">[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) provides methods for registering and unregistering component category information in the registry.</span></span> <span data-ttu-id="f9bc4-110">Cela comprend à la fois les noms explicites des catégories et les catégories implémentées ou requises par un composant ou une classe donnée.</span><span class="sxs-lookup"><span data-stu-id="f9bc4-110">This includes both the human-readable names of categories and the categories implemented or required by a given component or class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f9bc4-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f9bc4-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9bc4-112">Association d’icônes à une catégorie</span><span class="sxs-lookup"><span data-stu-id="f9bc4-112">Associating Icons with a Category</span></span>](associating-icons-with-a-category.md)
</dt> <dt>

[<span data-ttu-id="f9bc4-113">Catégorisation par fonctionnalités de composant</span><span class="sxs-lookup"><span data-stu-id="f9bc4-113">Categorizing by Component Capabilities</span></span>](categorizing-by-component-capabilities.md)
</dt> <dt>

[<span data-ttu-id="f9bc4-114">Catégorisation par fonctionnalités de conteneur</span><span class="sxs-lookup"><span data-stu-id="f9bc4-114">Categorizing by Container Capabilities</span></span>](categorizing-by-container-capabilities.md)
</dt> <dt>

[<span data-ttu-id="f9bc4-115">Classes et associations par défaut</span><span class="sxs-lookup"><span data-stu-id="f9bc4-115">Default Classes and Associations</span></span>](default-classes-and-associations.md)
</dt> <dt>

[<span data-ttu-id="f9bc4-116">Définition des catégories de composants</span><span class="sxs-lookup"><span data-stu-id="f9bc4-116">Defining Component Categories</span></span>](defining-component-categories.md)
</dt> </dl>

 

 




