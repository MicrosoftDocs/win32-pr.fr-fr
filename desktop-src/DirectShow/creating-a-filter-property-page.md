---
description: Création d’une page de propriétés de filtre
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Création d’une page de propriétés de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516549"
---
# <a name="creating-a-filter-property-page"></a><span data-ttu-id="fddb1-103">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="fddb1-103">Creating a Filter Property Page</span></span>

<span data-ttu-id="fddb1-104">Cette section décrit comment créer une page de propriétés pour un filtre DirectShow personnalisé, à l’aide de la classe [**CBasePropertyPage**](cbasepropertypage.md) .</span><span class="sxs-lookup"><span data-stu-id="fddb1-104">This section describes how to create a property page for a custom DirectShow filter, using the [**CBasePropertyPage**](cbasepropertypage.md) class.</span></span> <span data-ttu-id="fddb1-105">L’exemple de code de cette section montre toutes les étapes nécessaires à la création d’une page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="fddb1-105">The example code in this section shows all the steps needed to create a property page.</span></span> <span data-ttu-id="fddb1-106">L’exemple montre une page de propriétés pour un filtre d’effet de vidéo hypothétique qui prend en charge une propriété de saturation.</span><span class="sxs-lookup"><span data-stu-id="fddb1-106">The example shows a property page for a hypothetical video effect filter that supports a saturation property.</span></span> <span data-ttu-id="fddb1-107">La page de propriétés possède un curseur, que l’utilisateur peut déplacer pour ajuster le niveau de saturation du filtre.</span><span class="sxs-lookup"><span data-stu-id="fddb1-107">The property page has a slider, which the user can move to adjust the filter's saturation level.</span></span>

<span data-ttu-id="fddb1-108">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="fddb1-108">This section contains the following topics:</span></span>

-   [<span data-ttu-id="fddb1-109">Étape 1. Définir un mécanisme pour définir la propriété</span><span class="sxs-lookup"><span data-stu-id="fddb1-109">Step 1. Define a Mechanism for Setting the Property</span></span>](step-1--define-a-mechanism-for-setting-the-property.md)
-   [<span data-ttu-id="fddb1-110">Étape 2. Implémenter ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="fddb1-110">Step 2. Implement ISpecifyPropertyPages</span></span>](step-2--implement-ispecifypropertypages.md)
-   [<span data-ttu-id="fddb1-111">Étape 3. Prendre en charge QueryInterface</span><span class="sxs-lookup"><span data-stu-id="fddb1-111">Step 3. Support QueryInterface</span></span>](step-3--support-queryinterface.md)
-   [<span data-ttu-id="fddb1-112">Étape 4. Créer la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="fddb1-112">Step 4. Create the Property Page</span></span>](step-4--create-the-property-page.md)
-   [<span data-ttu-id="fddb1-113">Étape 5. Stocker un pointeur vers le filtre</span><span class="sxs-lookup"><span data-stu-id="fddb1-113">Step 5. Store a Pointer to the Filter</span></span>](step-5--store-a-pointer-to-the-filter.md)
-   [<span data-ttu-id="fddb1-114">Étape 6. Initialiser la boîte de dialogue</span><span class="sxs-lookup"><span data-stu-id="fddb1-114">Step 6. Initialize the Dialog</span></span>](step-6--initialize-the-dialog.md)
-   [<span data-ttu-id="fddb1-115">Étape 7. Gérer les messages de fenêtre</span><span class="sxs-lookup"><span data-stu-id="fddb1-115">Step 7. Handle Window Messages</span></span>](step-7--handle-window-messages.md)
-   [<span data-ttu-id="fddb1-116">Étape 8. Appliquer les modifications de propriété</span><span class="sxs-lookup"><span data-stu-id="fddb1-116">Step 8. Apply Property Changes</span></span>](step-8--apply-property-changes.md)
-   [<span data-ttu-id="fddb1-117">Étape 9. Déconnecter la page de propriétés</span><span class="sxs-lookup"><span data-stu-id="fddb1-117">Step 9. Disconnect the Property Page</span></span>](step-9--disconnect-the-property-page.md)
-   [<span data-ttu-id="fddb1-118">Étape 10. Prise en charge de l’inscription COM</span><span class="sxs-lookup"><span data-stu-id="fddb1-118">Step 10. Support COM Registration</span></span>](step-10--support-com-registration.md)

## <a name="related-topics"></a><span data-ttu-id="fddb1-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fddb1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fddb1-120">Écriture de filtres DirectShow</span><span class="sxs-lookup"><span data-stu-id="fddb1-120">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



