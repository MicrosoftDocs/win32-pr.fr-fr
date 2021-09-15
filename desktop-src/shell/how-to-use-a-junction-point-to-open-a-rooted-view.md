---
description: Vous pouvez utiliser le registre pour spécifier que la navigation dans un point de jonction ouvre une vue enracinée plutôt que l’affichage par défaut du contenu de l’extension associée.
title: Comment ouvrir une vue enracinée d’un point de jonction dans le registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412478"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>Comment ouvrir une vue enracinée d’un point de jonction dans le registre

Vous pouvez utiliser le registre pour spécifier que la navigation dans un point de jonction ouvre une vue enracinée plutôt que l’affichage par défaut du contenu de l’extension associée.

## <a name="instructions"></a>Instructions


Pour spécifier que l’exploration dans un point de jonction doit ouvrir une vue enracinée, ajoutez la commande **Open** \\ **Command** et **Explorez** \\ les sous-clés de **commande** dans la sous-clé **CLSID** de votre extension, avec les valeurs par défaut assignées aux lignes de commande indiquées ici :

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

Une fois que vous avez ajouté ces valeurs, une instance de Explorer.exe est lancée pour afficher le contenu de l’extension sous la forme d’une vue avec une racine lorsque l’utilisateur sélectionne le point de jonction.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de l’emplacement d’une extension d’espace de noms](nse-junction.md)
</dt> <dt>

[Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



