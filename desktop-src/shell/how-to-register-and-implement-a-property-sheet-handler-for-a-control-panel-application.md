---
description: De nombreuses applications du panneau de configuration affichent une feuille de propriétés de propriétés pour permettre aux utilisateurs d’afficher et de modifier divers paramètres de périphérique et système.
title: Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour une application du panneau de configuration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864917"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>Comment inscrire et implémenter un gestionnaire de feuille de propriétés pour une application du panneau de configuration

De nombreuses applications du panneau de configuration affichent une feuille de propriétés de propriétés pour permettre aux utilisateurs d’afficher et de modifier divers paramètres de périphérique et système. Deux de ces applications (souris et affichage) permettent aux gestionnaires de feuille de propriétés de remplacer une ou plusieurs de leurs pages par une page personnalisée. La capture d’écran suivante montre la feuille de propriétés propriétés de la **souris** .

![feuille de propriétés propriétés de la souris](images/propsheethandler3.jpg)

Les gestionnaires de feuille de propriétés pour les applications du panneau de configuration sont similaires à ceux des types de fichiers, avec deux exceptions principales :

-   Elles sont appelées par une application du panneau de configuration, et non par l’interpréteur de commandes.
-   Ils sont enregistrés différemment.

## <a name="what-you-need-to-know"></a>Ce que vous devez savoir

### <a name="technologies"></a>Technologies

-   Shell

### <a name="prerequisites"></a>Prérequis

-   Comprendre le panneau de configuration
-   Compréhension des menus contextuels

## <a name="instructions"></a>Instructions

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>Étape 1 : inscription d’un gestionnaire de feuille de propriétés pour une application du panneau de configuration

Un gestionnaire de feuille de propriétés d’application du panneau de configuration doit être inscrit sous la sous-clé du panneau de configuration. Cette clé peut être dans l’un des deux emplacements, selon que le gestionnaire doit être par utilisateur ou par ordinateur. Pour l’inscription par utilisateur, la sous-clé du panneau de configuration est **HKEY \_ Current \_ User** \\ **Control Panel**. La macro REGSTR \_ chemin d’accès \_ ControlPanel, telle que définie dans REGSTR. h, peut être utilisée dans le code à la place de « panneau de configuration ». Pour l’inscription par ordinateur, l’emplacement est le suivant :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

Ce chemin d’accès peut être référencé dans le code sous la forme HKEY \_ local \_ machine \\ REGSTR \_ path \_ CONTROLSFOLDER, à l’aide de la \_ \_ macro CONTROLSFOLDER Path REGSTR définie dans REGSTR. h.

Les applications du panneau de configuration qui permettent aux gestionnaires de feuille de propriétés de remplacer des pages ont une sous-clé sous la sous-clé du panneau de configuration, nommée pour l’application, telle que la souris et l’affichage. La sous-clé de l’application doit avoir une sous-clé **shellex** avec une sous-clé **PropertySheetHandlers** . Pour inscrire un gestionnaire de feuilles de propriétés, ajoutez son GUID à la sous-clé **PropertySheetHandlers** associée à l’application du panneau de configuration. Pour ce faire, créez une sous-clé de la sous-clé **PropertySheetHandlers** , nommée pour le gestionnaire de feuille de propriétés, et définissez sa valeur par défaut sur la forme de chaîne du GUID du gestionnaire.

L’exemple suivant inscrit un gestionnaire de feuille de propriétés pour l’application du panneau de configuration de la souris sur chaque ordinateur. Pour l’inscrire au niveau de chaque utilisateur, remplacez **HKEY \_ local \_ machine** \\ **REGSTR \_ path \_ CONTROLSFOLDER** par **HKEY \_ Current \_ User** \\ **REGSTR \_ path \_ ControlPanel**.

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>Étape 2 : implémentation d’un gestionnaire de feuille de propriétés pour une application du panneau de configuration

La procédure d’implémentation d’un gestionnaire de feuilles de propriétés du panneau de configuration est très similaire à celle décrite dans [comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md). La principale différence est que désormais, [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) a besoin d’une implémentation sans jeton au lieu de [**IShellPropSheetExt :: AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).

Quand une application du panneau de configuration est sur le présent d’afficher sa feuille de propriétés, elle appelle la méthode [**IShellPropSheetExt :: ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) du gestionnaire de feuilles de propriétés une fois pour chaque page qui peut être remplacée. Le paramètre *uPageID* est défini sur l’ID de la page. Les ID des pages disponibles sont définis dans Cplext. h. Les ID actuellement disponibles sont répertoriés dans le tableau suivant. 

| ID de page                      | Description         | Application du panneau de configuration |
|------------------------------|---------------------|---------------------------|
| CPLPAGE \_ boutons de la souris \_      | Page boutons    | Souris                     |
| CPLPAGE \_ souris \_ PTRMOTION    | La page de mouvement     | Souris                     |
| \_roulette de la souris CPLPAGE \_        | Page de la roulette      | Souris                     |
| \_Vitesse du clavier CPLPAGE \_     | Page Vitesse      | Clavier                  |
| \_ \_ arrière-plan d’affichage CPLPAGE | Page d’arrière-plan | Afficher                   |



 

## <a name="remarks"></a>Notes

La procédure de création et de remplacement d’une page est identique à celle de l’ajout d’une page. Pour plus d’informations, consultez [comment inscrire et implémenter un gestionnaire de feuille de propriétés pour un type de fichier](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md).

 

 



