---
description: Vous pouvez utiliser le registre pour spécifier que la navigation dans un point de jonction ouvre une vue enracinée plutôt que l’affichage par défaut du contenu de l’extension associée.
title: Comment ouvrir une vue enracinée d’un point de jonction dans le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202775"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="d495c-103">Comment ouvrir une vue enracinée d’un point de jonction dans le registre</span><span class="sxs-lookup"><span data-stu-id="d495c-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="d495c-104">Vous pouvez utiliser le registre pour spécifier que la navigation dans un point de jonction ouvre une vue enracinée plutôt que l’affichage par défaut du contenu de l’extension associée.</span><span class="sxs-lookup"><span data-stu-id="d495c-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="d495c-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="d495c-105">Instructions</span></span>


<span data-ttu-id="d495c-106">Pour spécifier que l’exploration dans un point de jonction doit ouvrir une vue enracinée, ajoutez la commande **Open** \\ **Command** et **Explorez** \\ les sous-clés de **commande** dans la sous-clé **CLSID** de votre extension, avec les valeurs par défaut assignées aux lignes de commande indiquées ici :</span><span class="sxs-lookup"><span data-stu-id="d495c-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

<span data-ttu-id="d495c-107">Une fois que vous avez ajouté ces valeurs, une instance de Explorer.exe est lancée pour afficher le contenu de l’extension sous la forme d’une vue avec une racine lorsque l’utilisateur sélectionne le point de jonction.</span><span class="sxs-lookup"><span data-stu-id="d495c-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d495c-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d495c-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d495c-109">Spécification de l’emplacement d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="d495c-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="d495c-110">Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci</span><span class="sxs-lookup"><span data-stu-id="d495c-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



