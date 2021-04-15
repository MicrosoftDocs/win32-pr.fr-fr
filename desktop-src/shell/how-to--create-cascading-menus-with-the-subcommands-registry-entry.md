---
description: Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes dans le registre pour créer des menus en cascade à l’aide de la procédure indiquée dans cette rubrique.
title: Créer des menus en cascade avec l’entrée de Registre subcommandes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8b1168daae5ea927f079c66eb436c099f8b3d96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991569"
---
# <a name="how-to-create-cascading-menus-with-the-subcommands-registry-entry"></a><span data-ttu-id="59b75-103">Comment créer des menus en cascade avec l’entrée de Registre subcommandes</span><span class="sxs-lookup"><span data-stu-id="59b75-103">How to Create Cascading Menus with the SubCommands Registry Entry</span></span>

<span data-ttu-id="59b75-104">Dans Windows 7 et versions ultérieures, vous pouvez utiliser l’entrée de sous-commandes dans le registre pour créer des menus en cascade à l’aide de la procédure indiquée dans cette rubrique.</span><span class="sxs-lookup"><span data-stu-id="59b75-104">In Windows 7 and later, you can use the SubCommands entry in the registry to create cascading menus by using the procedure given in this topic.</span></span>

## <a name="instructions"></a><span data-ttu-id="59b75-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="59b75-105">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="59b75-106">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="59b75-106">Step 1:</span></span>

<span data-ttu-id="59b75-107">Créez une sous-clé sous **HKEY \_ classes \_ racine** \\ *ProgID* \\ **Shell**, où *ProgID* est le type de fichier pour lequel vous souhaitez ajouter un menu en cascade.</span><span class="sxs-lookup"><span data-stu-id="59b75-107">Create a new subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**, where *ProgID* is the file type for which you want to add a cascading menu.</span></span> <span data-ttu-id="59b75-108">Vous pouvez nommer cette nouvelle sous-clé comme vous le souhaitez.</span><span class="sxs-lookup"><span data-stu-id="59b75-108">You can name this new subkey anything you'd like.</span></span> <span data-ttu-id="59b75-109">Dans le reste de cette rubrique, nous allons l’appeler *CascadeMenu*, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="59b75-109">For the remainder of this topic, we'll call it *CascadeMenu*, as shown in the following example.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
```

### <a name="step-2"></a><span data-ttu-id="59b75-110">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="59b75-110">Step 2:</span></span>

<span data-ttu-id="59b75-111">Ajoutez une entrée nommée « MUIVerb », de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, à la sous-clé *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="59b75-111">Add an entry named "MUIVerb", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="59b75-112">Assignez cette entrée à une valeur de chaîne comme « menu Test cascade ».</span><span class="sxs-lookup"><span data-stu-id="59b75-112">Assign this entry a string value such as "Test Cascade Menu".</span></span> <span data-ttu-id="59b75-113">Normalement, cette chaîne est fournie en tant que référence de ressource sous la forme « @file , ressource ».</span><span class="sxs-lookup"><span data-stu-id="59b75-113">Normally, this string is provided as a resource reference in the form "@file, resource".</span></span> <span data-ttu-id="59b75-114">La valeur (par défaut) de la sous-clé *CascadeMenu* ne doit pas être définie.</span><span class="sxs-lookup"><span data-stu-id="59b75-114">The (Default) value for the *CascadeMenu* subkey should not be set.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         CascadeMenu
            (Default)
            MUIVerb = Test Cascade Menu
```

### <a name="step-3"></a><span data-ttu-id="59b75-115">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="59b75-115">Step 3:</span></span>

<span data-ttu-id="59b75-116">Ajoutez une entrée nommée « sous-commandes », de type **reg \_ SZ** ou **reg \_ expand \_ SZ**, à la sous-clé *CascadeMenu* .</span><span class="sxs-lookup"><span data-stu-id="59b75-116">Add an entry named "SubCommands", of type **REG\_SZ** or **REG\_EXPAND\_SZ**, to the *CascadeMenu* subkey.</span></span> <span data-ttu-id="59b75-117">Assignez cette entrée à une liste délimitée par des points-virgules des verbes qui doivent apparaître dans le menu, dans leur ordre d’apparition souhaité.</span><span class="sxs-lookup"><span data-stu-id="59b75-117">Assign this entry a semicolon-delimited list of the verbs that should appear on the menu, in their desired order of appearance.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      Shell
         CascadeMenu
            SubCommands = Windows.delete;Windows.properties;Windows.rename;Windows.cut;Windows.copy;Windows.paste
```

### <a name="step-4"></a><span data-ttu-id="59b75-118">Étape 4 :</span><span class="sxs-lookup"><span data-stu-id="59b75-118">Step 4:</span></span>

<span data-ttu-id="59b75-119">Remplissez la sous-clé **CommandStore** avec des implémentations de verbe pour toutes les méthodes d’implémentation de verbe statique personnalisées que vous avez utilisées dans votre entrée de sous-commandes ; par exemple :</span><span class="sxs-lookup"><span data-stu-id="59b75-119">Populate the **CommandStore** subkey with verb implementations for any custom static verb implementation methods that you've used in your SubCommands entry; for example:</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="59b75-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="59b75-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59b75-121">Création de menus en cascade statiques</span><span class="sxs-lookup"><span data-stu-id="59b75-121">Creating Static Cascading Menus</span></span>](creating-static-cascading-menus.md)
</dt> </dl>

 

 



