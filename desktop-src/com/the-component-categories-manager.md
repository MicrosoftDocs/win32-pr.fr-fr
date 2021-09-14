---
title: Gestionnaire de catégories de composants
description: Gestionnaire de catégories de composants
ms.assetid: bd43ef98-2299-4c8a-9f35-bf9aceb074ab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fdf301e1b344bbc2403fd656dd90447ccffc357
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221740"
---
# <a name="the-component-categories-manager"></a>Gestionnaire de catégories de composants

Pour faciliter la gestion des catégories de composants et garantir la cohérence du Registre, le système fournit le gestionnaire de catégories de composants, un objet COM avec un CLSID de CLSID \_ StdComponentCategoriesMgr. Cet objet COM fournit les interfaces suivantes :

-   [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
-   [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) fournit des méthodes pour obtenir des informations sur les catégories implémentées ou requises par une certaine classe et fournit des informations sur les catégories inscrites sur un ordinateur donné.

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) fournit des méthodes pour inscrire et annuler l’enregistrement des informations de catégorie de composants dans le registre. Cela comprend à la fois les noms explicites des catégories et les catégories implémentées ou requises par un composant ou une classe donnée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Association d’icônes à une catégorie](associating-icons-with-a-category.md)
</dt> <dt>

[Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
</dt> <dt>

[Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes et associations par défaut](default-classes-and-associations.md)
</dt> <dt>

[Définition des catégories de composants](defining-component-categories.md)
</dt> </dl>

 

 




