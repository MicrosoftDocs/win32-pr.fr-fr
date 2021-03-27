---
description: Vous pouvez utiliser une extension d’espace de noms pour permettre aux utilisateurs de parcourir le contenu d’un fichier au lieu de le présenter sous la forme d’un dossier. Les extensions de ce type sont généralement utilisées pour afficher le contenu des membres d’un type de fichier.
title: Comment afficher une vue enracinée d’un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30ee16f3ce50cd79800dd98aa53256591d1f79d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864929"
---
# <a name="how-to-display-a-rooted-view-of-a-file"></a>Comment afficher une vue enracinée d’un fichier

Vous pouvez utiliser une extension d’espace de noms pour permettre aux utilisateurs de parcourir le contenu d’un fichier au lieu de le présenter sous la forme d’un dossier. Les extensions de ce type sont généralement utilisées pour afficher le contenu des membres d’un [type de fichier](fa-file-types.md). Par exemple, les membres d’un type de fichier peuvent contenir plusieurs images ou fichiers compressés, organisés dans une hiérarchie. Au lieu d’écrire une application pour permettre à l’utilisateur d’afficher le contenu d’un fichier de ce type, vous pouvez écrire une extension d’espace de noms et laisser l’Explorateur Windows gérer l’affichage.

Vous devez utiliser une vue enracinée pour que l’extension affiche le contenu d’un fichier. La méthode la plus courante pour fournir une vue enracinée des membres d’un type de fichier consiste à définir un [verbe de menu contextuel](context.md) qui lance une instance de Explorer.exe. En faisant de ce verbe le verbe par défaut, un double-clic ouvre également une vue enracinée du fichier. Vous pouvez soit définir un verbe pour tous les membres du type de fichier en [modifiant le registre](context.md), soit définir de manière dynamique les verbes au niveau fichier par fichier en implémentant un [Gestionnaire de menu contextuel](context-menu-handlers.md).

## <a name="instructions"></a>Instructions


L’exemple suivant illustre l’utilisation du Registre pour fournir une vue d’ensemble des membres d’un type de fichier en modifiant le registre. L’exemple d’entrée de Registre est une modification de l’un des exemples de l' [extension des menus contextuels](context.md). Les entrées de registre définissent les fichiers avec une extension de nom de fichier. MYP comme type de fichier et utilisent le verbe **Browse** pour lancer une vue enracinée des membres de ce type.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      Shell
         (Default) = browse
         browse
            command
               (Default) = %SYSTEMROOT%\explorer.exe /e,/root,{Extension CLSID}, "%1"
```

Vous pouvez utiliser le même verbe pour lancer par programmation une vue enracinée d’un membre du type de fichier en appelant la fonction [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Spécification de l’emplacement d’une extension d’espace de noms](nse-junction.md)
</dt> <dt>

[Comment ouvrir une vue enracinée d’un point de jonction dans le registre](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



