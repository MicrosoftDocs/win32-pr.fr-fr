---
description: Comment implémenter et inscrire un gestionnaire de suppression.
title: Comment créer des gestionnaires de suppression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 081b4349ba36a12670458a453b0622475d59d755
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202782"
---
# <a name="how-to-create-drop-handlers"></a><span data-ttu-id="9c2dd-103">Comment créer des gestionnaires de suppression</span><span class="sxs-lookup"><span data-stu-id="9c2dd-103">How to Create Drop Handlers</span></span>

<span data-ttu-id="9c2dd-104">Par défaut, les fichiers ne sont pas des cibles de dépôt.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-104">By default, files are not drop targets.</span></span> <span data-ttu-id="9c2dd-105">Vous pouvez transformer les membres d’un [type de fichier](fa-file-types.md) en cibles de dépôt en implémentant et en inscrivant un *Gestionnaire de suppression*.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-105">You can make the members of a [file type](fa-file-types.md) into drop targets by implementing and registering a *drop handler*.</span></span>

<span data-ttu-id="9c2dd-106">Si un gestionnaire de suppression est inscrit pour un type de fichier, il est appelé chaque fois qu’un objet est glissé ou supprimé sur un membre du type de fichier.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-106">If a drop handler is registered for a file type, it is called whenever an object is dragged over or dropped on a member of the file type.</span></span> <span data-ttu-id="9c2dd-107">L’interpréteur de commandes gère l’opération en appelant les méthodes appropriées sur l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-107">The Shell manages the operation by calling the appropriate methods on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

<span data-ttu-id="9c2dd-108">Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9c2dd-108">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="9c2dd-109">Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de suppression.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-109">This document focuses on those aspects of implementation that are specific to drop handlers.</span></span>

## <a name="instructions"></a><span data-ttu-id="9c2dd-110">Instructions</span><span class="sxs-lookup"><span data-stu-id="9c2dd-110">Instructions</span></span>

### <a name="step-1-implementing-drop-handlers"></a><span data-ttu-id="9c2dd-111">Étape 1 : implémentation des gestionnaires de suppression</span><span class="sxs-lookup"><span data-stu-id="9c2dd-111">Step 1: Implementing Drop Handlers</span></span>

<span data-ttu-id="9c2dd-112">Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de suppression sont des objets COM (Component Object Model) in-process implémentés en tant que dll.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-112">Like all Shell extension handlers, drop handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="9c2dd-113">Elles exportent deux interfaces en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) et [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span><span class="sxs-lookup"><span data-stu-id="9c2dd-113">They export two interfaces in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) and [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget).</span></span>

<span data-ttu-id="9c2dd-114">L’interpréteur de commandes Initialise le gestionnaire via son interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) .</span><span class="sxs-lookup"><span data-stu-id="9c2dd-114">The Shell initializes the handler through its [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) interface.</span></span> <span data-ttu-id="9c2dd-115">Elle utilise cette interface pour demander l’identificateur de classe du gestionnaire (CLSID) et lui fournit le nom du fichier.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-115">It uses this interface to request the handler's class identifier (CLSID) and provides it with the file's name.</span></span> <span data-ttu-id="9c2dd-116">Pour obtenir une description générale de l’implémentation des gestionnaires d’extensions de Shell, y compris l’interface **IPersistFile** , consultez [création de gestionnaires d’extension de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9c2dd-116">For a general discussion of how to implement Shell extension handlers, including the **IPersistFile** interface, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="9c2dd-117">Une fois le gestionnaire Drop initialisé, l’interpréteur de commandes appelle la méthode appropriée sur l’interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-117">Once the drop handler is initialized, the Shell calls the appropriate method on the handler's [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) interface.</span></span>

### <a name="step-2-registering-drop-handlers"></a><span data-ttu-id="9c2dd-118">Étape 2 : inscription des gestionnaires de suppression</span><span class="sxs-lookup"><span data-stu-id="9c2dd-118">Step 2: Registering Drop Handlers</span></span>

<span data-ttu-id="9c2dd-119">Les gestionnaires de suppression sont inscrits sous la sous-clé de ce type de fichier.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-119">Drop handlers are registered under this file type's subkey.</span></span>

```
HKEY_CLASSES_ROOT
   ProgID
      shellex
         DropHandler
```

<span data-ttu-id="9c2dd-120">Créez une sous-clé de **DropHandler** nommée pour le gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID CLSID du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-120">Create a subkey of **DropHandler** named for the handler, and set the subkey's default value to the string form of the handler's CLSID GUID.</span></span> <span data-ttu-id="9c2dd-121">Pour obtenir une présentation générale de l’inscription des gestionnaires d’extensions de Shell, consultez [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="9c2dd-121">For a general discussion of how to register Shell extension handlers, see [Creating Shell Extension Handlers](handlers.md).</span></span>

<span data-ttu-id="9c2dd-122">L’exemple suivant illustre les entrées de Registre qui activent un gestionnaire Drop pour un exemple de type de fichier. MYP.</span><span class="sxs-lookup"><span data-stu-id="9c2dd-122">The following example illustrates registry entries that enable a drop handler for an example .myp file type.</span></span>

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      shellex
         DropHandler
            (Default) = {00000000-1111-2222-3333-444444444444}
```

## <a name="related-topics"></a><span data-ttu-id="9c2dd-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9c2dd-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c2dd-124">Création de gestionnaires d’extensions d’environnement</span><span class="sxs-lookup"><span data-stu-id="9c2dd-124">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

[<span data-ttu-id="9c2dd-125">**IDropTarget**</span><span class="sxs-lookup"><span data-stu-id="9c2dd-125">**IDropTarget**</span></span>](/windows/win32/api/oleidl/nn-oleidl-idroptarget)
</dt> <dt>

[<span data-ttu-id="9c2dd-126">**IPersistFile**</span><span class="sxs-lookup"><span data-stu-id="9c2dd-126">**IPersistFile**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> </dl>

 

 
