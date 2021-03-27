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
# <a name="how-to-display-a-rooted-view-of-a-file"></a><span data-ttu-id="a5c66-104">Comment afficher une vue enracinée d’un fichier</span><span class="sxs-lookup"><span data-stu-id="a5c66-104">How to Display a Rooted View of a File</span></span>

<span data-ttu-id="a5c66-105">Vous pouvez utiliser une extension d’espace de noms pour permettre aux utilisateurs de parcourir le contenu d’un fichier au lieu de le présenter sous la forme d’un dossier.</span><span class="sxs-lookup"><span data-stu-id="a5c66-105">You can use a namespace extension to allow users to browse the contents of a file rather than have it presented as a folder.</span></span> <span data-ttu-id="a5c66-106">Les extensions de ce type sont généralement utilisées pour afficher le contenu des membres d’un [type de fichier](fa-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="a5c66-106">Extensions of this sort are typically used to display the contents of the members of a [file type](fa-file-types.md).</span></span> <span data-ttu-id="a5c66-107">Par exemple, les membres d’un type de fichier peuvent contenir plusieurs images ou fichiers compressés, organisés dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="a5c66-107">For instance, the members of a file type might contain multiple compressed files or images, organized in a hierarchy.</span></span> <span data-ttu-id="a5c66-108">Au lieu d’écrire une application pour permettre à l’utilisateur d’afficher le contenu d’un fichier de ce type, vous pouvez écrire une extension d’espace de noms et laisser l’Explorateur Windows gérer l’affichage.</span><span class="sxs-lookup"><span data-stu-id="a5c66-108">Rather than write an application to allow the user to view the contents of such a file, you can instead write a namespace extension and let Windows Explorer handle the display.</span></span>

<span data-ttu-id="a5c66-109">Vous devez utiliser une vue enracinée pour que l’extension affiche le contenu d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="a5c66-109">You must use a rooted view in order to have an extension display the contents of a file.</span></span> <span data-ttu-id="a5c66-110">La méthode la plus courante pour fournir une vue enracinée des membres d’un type de fichier consiste à définir un [verbe de menu contextuel](context.md) qui lance une instance de Explorer.exe.</span><span class="sxs-lookup"><span data-stu-id="a5c66-110">The most common way to provide a rooted view of the members of a file type is to define a [shortcut menu verb](context.md) that launches an instance of Explorer.exe.</span></span> <span data-ttu-id="a5c66-111">En faisant de ce verbe le verbe par défaut, un double-clic ouvre également une vue enracinée du fichier.</span><span class="sxs-lookup"><span data-stu-id="a5c66-111">By making this verb the default verb, a double-click will also open a rooted view of the file.</span></span> <span data-ttu-id="a5c66-112">Vous pouvez soit définir un verbe pour tous les membres du type de fichier en [modifiant le registre](context.md), soit définir de manière dynamique les verbes au niveau fichier par fichier en implémentant un [Gestionnaire de menu contextuel](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="a5c66-112">You can either define a verb for all members of the file type by [modifying the registry](context.md), or dynamically define verbs on a file-by-file basis by implementing a [shortcut menu handler](context-menu-handlers.md).</span></span>

## <a name="instructions"></a><span data-ttu-id="a5c66-113">Instructions</span><span class="sxs-lookup"><span data-stu-id="a5c66-113">Instructions</span></span>


<span data-ttu-id="a5c66-114">L’exemple suivant illustre l’utilisation du Registre pour fournir une vue d’ensemble des membres d’un type de fichier en modifiant le registre.</span><span class="sxs-lookup"><span data-stu-id="a5c66-114">The following example illustrates how to use the registry to provide a rooted view of the members of a file type by modifying the registry.</span></span> <span data-ttu-id="a5c66-115">L’exemple d’entrée de Registre est une modification de l’un des exemples de l' [extension des menus contextuels](context.md).</span><span class="sxs-lookup"><span data-stu-id="a5c66-115">The sample registry entry is a modification of one of the examples in [Extending Shortcut Menus](context.md).</span></span> <span data-ttu-id="a5c66-116">Les entrées de registre définissent les fichiers avec une extension de nom de fichier. MYP comme type de fichier et utilisent le verbe **Browse** pour lancer une vue enracinée des membres de ce type.</span><span class="sxs-lookup"><span data-stu-id="a5c66-116">The registry entries define files with an .myp file name extension as a file type, and use the **browse** verb to launch a rooted view of members of that type.</span></span>

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

<span data-ttu-id="a5c66-117">Vous pouvez utiliser le même verbe pour lancer par programmation une vue enracinée d’un membre du type de fichier en appelant la fonction [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) .</span><span class="sxs-lookup"><span data-stu-id="a5c66-117">You can use the same verb to programmatically launch a rooted view of a member of the file type by calling the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5c66-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a5c66-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5c66-119">Spécification de l’emplacement d’une extension d’espace de noms</span><span class="sxs-lookup"><span data-stu-id="a5c66-119">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="a5c66-120">Comment ouvrir une vue enracinée d’un point de jonction dans le registre</span><span class="sxs-lookup"><span data-stu-id="a5c66-120">How to Open a Rooted View of a Junction Point Through the Registry</span></span>](how-to-use-a-junction-point-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="a5c66-121">Comment ouvrir une vue enracinée d’un point de jonction à l’aide d’un fichier de raccourci</span><span class="sxs-lookup"><span data-stu-id="a5c66-121">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> <dt>

[<span data-ttu-id="a5c66-122">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="a5c66-122">**ShellExecute**</span></span>](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea)
</dt> </dl>

 

 



