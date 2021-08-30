---
title: Classes et associations par défaut
description: Pour certaines catégories, une seule classe peut être associée en tant que classe par défaut.
ms.assetid: 9c48615b-ab10-44e4-a032-49d5ee0c9b01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e63eaa99d4f35c5a7f2451da2c5d9becb38e5af2dcf18aa71cf980e7446e1997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993419"
---
# <a name="default-classes-and-associations"></a>Classes et associations par défaut

Pour certaines catégories, une seule classe peut être associée en tant que classe par défaut. La classe par défaut est sélectionnée chaque fois que cette catégorie particulière d’objet est requise. Bien que cela ne soit peut-être pas utile pour toutes les catégories de composants, l’établissement d’une classe par défaut peut être utile lorsqu’une classe particulière doit être chargée à partir d’une liste de classes possibles sans intervention de l’utilisateur. Les administrateurs définissent la classe qui peut être utilisée en manipulant le registre.

Pour associer une classe par défaut à une catégorie, introduisez une clé CLSID avec le même CLSID que le CATID de la catégorie de composant choisie comme valeur par défaut. Ajoutez ensuite une clé TreatAs à cette clé, en utilisant la valeur du CLSID de la classe par défaut pour la catégorie. Pour utiliser la classe par défaut pour une catégorie de composant, utilisez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject), en spécifiant le CATID pour le paramètre CLSID. Cela permet de rediriger automatiquement le CLSID établi comme valeur par défaut pour cette catégorie. L’entrée de Registre est la suivante :

```
HKEY_CLASSES_ROOT\CLSID
   {catid}
      TreatAs
          = default clsid
```

Pendant l’installation, un composant peut vérifier l’existence de toutes les clés de classe par défaut pour ses catégories et présenter à l’utilisateur les options permettant de remplacer les paramètres actuels.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Association d’icônes à une catégorie](associating-icons-with-a-category.md)
</dt> <dt>

[Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
</dt> <dt>

[Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
</dt> <dt>

[Définition des catégories de composants](defining-component-categories.md)
</dt> <dt>

[Gestionnaire de catégories de composants](the-component-categories-manager.md)
</dt> </dl>

 

 




