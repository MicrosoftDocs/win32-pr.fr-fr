---
title: Association d’icônes à une catégorie
description: Association d’icônes à une catégorie
ms.assetid: 5e5c3c10-07cf-4a34-9822-97ec940b3117
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98c7a662ab3aaf578f037ff246207d03e4fcd688
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363539"
---
# <a name="associating-icons-with-a-category"></a>Association d’icônes à une catégorie

La création d’une interface utilisateur qui permet à l’utilisateur de sélectionner des catégories de composants dans une catégorie nécessite la possibilité d’afficher une image significative pour une catégorie particulière. Pour associer une icône à une catégorie de composant, créez une clé pour le CATID de la catégorie et remplissez cette clé avec une sous-clé [DefaultIcon](defaulticon.md) . L’entrée de Registre est la suivante :

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\DefaultIcon = "c:\hello\icons.dll,1"
 
```

Le nom de fichier référencé par la clé DefaultIcon peut être un fichier EXE ou une DLL (DLL de ressources uniquement).

Pour associer une petite image de la boîte à outils à une petite image de la boîte à outils, créez une clé dans le **\_ \_ \\ CLSID racine des classes HKEY** pour le CATID de la catégorie et remplissez cette clé avec une sous-clé [ToolboxBitmap32](toolboxbitmap32.md) , comme illustré dans l’exemple suivant :

``` syntax
HKEY_CLASSES_ROOT\CLSID\{...catid...}\ToolBoxBitmap32 = "c:\goodbye\mycomponent.dll,42"
 
```

Le nom de fichier référencé par la clé [ToolboxBitmap32](toolboxbitmap32.md) peut également être un fichier exe ou DLL (dll de ressources uniquement).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Catégorisation par fonctionnalités de composant](categorizing-by-component-capabilities.md)
</dt> <dt>

[Catégorisation par fonctionnalités de conteneur](categorizing-by-container-capabilities.md)
</dt> <dt>

[Classes et associations par défaut](default-classes-and-associations.md)
</dt> <dt>

[Définition des catégories de composants](defining-component-categories.md)
</dt> <dt>

[**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation)
</dt> <dt>

[**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister)
</dt> <dt>

[Gestionnaire de catégories de composants](the-component-categories-manager.md)
</dt> </dl>

 

 




