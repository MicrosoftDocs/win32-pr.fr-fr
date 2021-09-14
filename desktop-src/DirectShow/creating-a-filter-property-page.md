---
description: Création d’une page de propriétés de filtre
ms.assetid: 028e2c4e-0241-4057-8514-d3e9b456ab6e
title: Création d’une page de propriétés de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cc19bf918ba47c53a04e34f5e5292bfdc716eca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006689"
---
# <a name="creating-a-filter-property-page"></a>Création d’une page de propriétés de filtre

cette section décrit comment créer une page de propriétés pour un filtre de DirectShow personnalisé, à l’aide de la classe [**CBasePropertyPage**](cbasepropertypage.md) . L’exemple de code de cette section montre toutes les étapes nécessaires à la création d’une page de propriétés. L’exemple montre une page de propriétés pour un filtre d’effet de vidéo hypothétique qui prend en charge une propriété de saturation. La page de propriétés possède un curseur, que l’utilisateur peut déplacer pour ajuster le niveau de saturation du filtre.

Cette section contient les rubriques suivantes :

-   [Étape 1. Définir un mécanisme pour définir la propriété](step-1--define-a-mechanism-for-setting-the-property.md)
-   [Étape 2. Implémenter ISpecifyPropertyPages](step-2--implement-ispecifypropertypages.md)
-   [Étape 3. Prendre en charge QueryInterface](step-3--support-queryinterface.md)
-   [Étape 4. Créer la page de propriétés](step-4--create-the-property-page.md)
-   [Étape 5. Stocker un pointeur vers le filtre](step-5--store-a-pointer-to-the-filter.md)
-   [Étape 6. Initialiser la boîte de dialogue](step-6--initialize-the-dialog.md)
-   [Étape 7. Gérer les messages de fenêtre](step-7--handle-window-messages.md)
-   [Étape 8. Appliquer les modifications de propriété](step-8--apply-property-changes.md)
-   [Étape 9. Déconnecter la page de propriétés](step-9--disconnect-the-property-page.md)
-   [Étape 10. Prise en charge de l’inscription COM](step-10--support-com-registration.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



