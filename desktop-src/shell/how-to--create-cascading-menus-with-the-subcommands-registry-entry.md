---
description: dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes dans le registre pour créer des menus en cascade à l’aide de la procédure indiquée dans cette rubrique.
title: Créer des menus en cascade avec l’entrée de Registre subcommandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f12eb473d45a3d3aef1b7cf8e7f6cc51a0d97aa5b9e60ee39681c80af459988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111799"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a>Comment créer des menus en cascade avec l’entrée de Registre subcommandes

dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes dans le registre pour créer des menus en cascade à l’aide de la procédure indiquée dans cette rubrique.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell**, où *ProgID* est le type de fichier pour lequel vous souhaitez ajouter un menu en cascade. Vous pouvez nommer cette nouvelle sous-clé comme vous le souhaitez. Dans le reste de cette rubrique, nous allons l’appeler *CascadeMenu*, comme illustré dans l’exemple suivant.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a>Étape 2 :

Ajoutez une entrée nommée « MUIVerb », de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, à la sous-clé *CascadeMenu* . Assignez cette entrée à une valeur de chaîne comme « menu Test cascade ». Normalement, cette chaîne est fournie en tant que référence de ressource sous la forme « @file , ressource ». La valeur (par défaut) de la sous-clé *CascadeMenu* ne doit pas être définie.

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a>Étape 3 :

Ajoutez une entrée nommée « sous-commandes », de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, à la sous-clé *CascadeMenu* . Assignez cette entrée à une liste délimitée par des points-virgules des verbes qui doivent apparaître dans le menu, dans leur ordre d’apparition souhaité.

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a>Étape 4 :

Remplissez la sous-clé **CommandStore** avec des implémentations de verbe pour toutes les méthodes d’implémentation de verbe statique personnalisées que vous avez utilisées dans votre entrée de sous-commandes ; par exemple :

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  CommandStore
                     Shell
                        VerbName
                           command
                              (Default) = notepad.exe %1
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de menus en cascade statiques](creating-static-cascading-menus.md)
</dt> </dl>

 

 



