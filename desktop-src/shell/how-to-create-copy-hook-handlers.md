---
description: Utilisation des extensions de Shell pour implémenter un gestionnaire de raccordement de copie.
ms.assetid: 05808281-84fb-402d-9fa1-3a747b29d030
title: Comment créer des gestionnaires de raccordement de copie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1468839eacc10272f8f97a120b98ada6d580bacf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202783"
---
# <a name="how-to-create-copy-hook-handlers"></a><span data-ttu-id="cb6d7-103">Comment créer des gestionnaires de raccordement de copie</span><span class="sxs-lookup"><span data-stu-id="cb6d7-103">How to Create Copy Hook Handlers</span></span>

<span data-ttu-id="cb6d7-104">Les procédures générales d’implémentation et d’inscription d’un gestionnaire d’extensions de Shell sont décrites dans [création de gestionnaires d’extensions de Shell](handlers.md).</span><span class="sxs-lookup"><span data-stu-id="cb6d7-104">The general procedures for implementing and registering a Shell extension handler are discussed in [Creating Shell Extension Handlers](handlers.md).</span></span> <span data-ttu-id="cb6d7-105">Ce document se concentre sur les aspects de l’implémentation qui sont spécifiques aux gestionnaires de raccordement de copie.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-105">This document focuses on those aspects of implementation that are specific to copy hook handlers.</span></span>

-   [<span data-ttu-id="cb6d7-106">Implémentation des gestionnaires de raccordement de copie</span><span class="sxs-lookup"><span data-stu-id="cb6d7-106">Implementing Copy Hook Handlers</span></span>](#step-1-implementing-copy-hook-handlers)
-   [<span data-ttu-id="cb6d7-107">Inscription des gestionnaires de raccordement de copie</span><span class="sxs-lookup"><span data-stu-id="cb6d7-107">Registering Copy Hook Handlers</span></span>](#step-2-registering-copy-hook-handlers)
-   [<span data-ttu-id="cb6d7-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb6d7-108">Related topics</span></span>](#related-topics)

## <a name="instructions"></a><span data-ttu-id="cb6d7-109">Instructions</span><span class="sxs-lookup"><span data-stu-id="cb6d7-109">Instructions</span></span>

### <a name="step-1-implementing-copy-hook-handlers"></a><span data-ttu-id="cb6d7-110">Étape 1 : implémentation des gestionnaires de raccordement de copie</span><span class="sxs-lookup"><span data-stu-id="cb6d7-110">Step 1: Implementing Copy Hook Handlers</span></span>

<span data-ttu-id="cb6d7-111">Comme tous les gestionnaires d’extensions de Shell, les gestionnaires de raccordement de copie sont des objets COM (Component Object Model) in-process implémentés en tant que dll.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-111">Like all Shell extension handlers, copy hook handlers are in-process Component Object Model (COM) objects implemented as DLLs.</span></span> <span data-ttu-id="cb6d7-112">Ils exportent une interface en plus de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cb6d7-112">They export one interface in addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown): [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)).</span></span> <span data-ttu-id="cb6d7-113">L’interpréteur de commandes Initialise le gestionnaire directement, donc il n’est pas nécessaire d’utiliser une interface d’initialisation telle que [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span><span class="sxs-lookup"><span data-stu-id="cb6d7-113">The Shell initializes the handler directly, so there is no need for an initialization interface such as [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit).</span></span>

<span data-ttu-id="cb6d7-114">L’interface [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) a une seule méthode, [**ICopyHook :: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="cb6d7-114">The [**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85)) interface has a single method, [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)).</span></span> <span data-ttu-id="cb6d7-115">Quand un dossier va être déplacé, l’interpréteur de commandes appelle cette méthode.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-115">When a folder is about to be moved, the Shell calls this method.</span></span> <span data-ttu-id="cb6d7-116">Elle transmet diverses informations, notamment :</span><span class="sxs-lookup"><span data-stu-id="cb6d7-116">It passes in a variety of information, including:</span></span>

-   <span data-ttu-id="cb6d7-117">Nom du dossier.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-117">The folder's name.</span></span>
-   <span data-ttu-id="cb6d7-118">Nom de la destination ou du nouveau dossier.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-118">The folder's destination or new name.</span></span>
-   <span data-ttu-id="cb6d7-119">Opération tentée.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-119">The operation that is being attempted.</span></span>
-   <span data-ttu-id="cb6d7-120">Attributs des dossiers source et de destination.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-120">The attributes of the source and destination folders.</span></span>
-   <span data-ttu-id="cb6d7-121">Handle de fenêtre qui peut être utilisé pour afficher une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-121">A window handle that can be used to display a user interface.</span></span>

<span data-ttu-id="cb6d7-122">Quand la méthode [**ICopyHook :: CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) de votre gestionnaire est appelée, elle retourne l’une des trois valeurs suivantes pour indiquer à l’interpréteur comment il doit continuer.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-122">When your handler's [**ICopyHook::CopyCallback**](/previous-versions/windows/desktop/legacy/bb776048(v=vs.85)) method is called, it returns one of the three following values to indicate to the Shell how it should proceed.</span></span>



| <span data-ttu-id="cb6d7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb6d7-123">Value</span></span>    | <span data-ttu-id="cb6d7-124">Description</span><span class="sxs-lookup"><span data-stu-id="cb6d7-124">Description</span></span>                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb6d7-125">IDYES</span><span class="sxs-lookup"><span data-stu-id="cb6d7-125">IDYES</span></span>    | <span data-ttu-id="cb6d7-126">Autorise l’opération.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-126">Allows the operation.</span></span>                                                                                                                            |
| <span data-ttu-id="cb6d7-127">IDNO</span><span class="sxs-lookup"><span data-stu-id="cb6d7-127">IDNO</span></span>     | <span data-ttu-id="cb6d7-128">Empêche l’opération sur ce dossier.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-128">Prevents the operation on this folder.</span></span> <span data-ttu-id="cb6d7-129">L’interpréteur de commandes peut continuer avec toutes les autres opérations qui ont été approuvées, telles qu’une opération de copie par lot.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-129">The Shell can continue with any other operations that have been approved, such as a batch copy operation.</span></span> |
| <span data-ttu-id="cb6d7-130">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="cb6d7-130">IDCANCEL</span></span> | <span data-ttu-id="cb6d7-131">Empêche l’opération en cours et annule toutes les opérations en attente.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-131">Prevents the current operation and cancels any pending operations.</span></span>                                                                               |



 

### <a name="step-2-registering-copy-hook-handlers"></a><span data-ttu-id="cb6d7-132">Étape 2 : inscription des gestionnaires de raccordement de copie</span><span class="sxs-lookup"><span data-stu-id="cb6d7-132">Step 2: Registering Copy Hook Handlers</span></span>

<span data-ttu-id="cb6d7-133">Les gestionnaires de raccordement de copie pour les dossiers sont enregistrés sous la **\_ \_** \\  \\  \\ sous-clé de shellex **CopyHookHandlers** du répertoire racine de la classe HKEY.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-133">Copy hook handlers for folders are registered under the **HKEY\_CLASSES\_ROOT**\\**Directory**\\**shellex**\\**CopyHookHandlers** subkey.</span></span> <span data-ttu-id="cb6d7-134">Créez une sous-clé de **CopyHookHandlers** nommée pour le gestionnaire et définissez la valeur par défaut de la sous-clé sur la forme de chaîne du GUID de l’identificateur de classe (CLSID) du gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-134">Create a subkey of **CopyHookHandlers** named for the handler, and set the subkey's default value to the string form of the handler's class identifier (CLSID) GUID.</span></span>

<span data-ttu-id="cb6d7-135">L’exemple suivant ajoute la sous-clé **MyCopyHandler** à la liste des gestionnaires de raccordement de copie de l’interpréteur de commandes.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-135">The following example adds the **MyCopyHandler** subkey to the Shell's list of copy hook handlers.</span></span>

```
HKEY_CLASSES_ROOT
   Directory
      shellex
         CopyHookHandlers
            MyCopyHandler
               (Default) = {MyCopyHandler CLSID GUID}
```

<span data-ttu-id="cb6d7-136">Les gestionnaires de raccordement de copie pour les objets d’imprimante sont enregistrés de la même façon.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-136">Copy hook handlers for printer objects are registered in essentially the same way.</span></span> <span data-ttu-id="cb6d7-137">La seule différence réside dans le fait que vous devez les inscrire sous la sous-clé des imprimantes **\_ \_ racines de la classe HKEY** \\  .</span><span class="sxs-lookup"><span data-stu-id="cb6d7-137">The only difference is that you must register them under the **HKEY\_CLASSES\_ROOT**\\**Printers** subkey.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6d7-138">Notes</span><span class="sxs-lookup"><span data-stu-id="cb6d7-138">Remarks</span></span>

<span data-ttu-id="cb6d7-139">Normalement, les utilisateurs et les applications peuvent copier, déplacer, supprimer ou renommer des dossiers avec peu de restrictions.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-139">Normally, users and applications can copy, move, delete, or rename folders with few restrictions.</span></span> <span data-ttu-id="cb6d7-140">En implémentant un gestionnaire de raccordement de copie, vous pouvez contrôler si ces opérations ont lieu.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-140">By implementing a copy hook handler, you can control whether these operations take place.</span></span> <span data-ttu-id="cb6d7-141">Par exemple, l’implémentation de ce type de gestionnaire vous permet d’empêcher le renommage ou la suppression de dossiers critiques.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-141">For instance, implementing such a handler allows you to prevent critical folders from being renamed or deleted.</span></span> <span data-ttu-id="cb6d7-142">Les gestionnaires de raccordement de copie peuvent également être implémentés pour les objets d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-142">Copy hook handlers can also be implemented for printer objects.</span></span>

<span data-ttu-id="cb6d7-143">Les gestionnaires de raccordement de copie sont globaux.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-143">Copy hook handlers are global.</span></span> <span data-ttu-id="cb6d7-144">L’interpréteur de commandes appelle tous les gestionnaires enregistrés chaque fois qu’une application ou un utilisateur tente de copier, déplacer, supprimer ou renommer un dossier ou un objet imprimante.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-144">The Shell calls all registered handlers every time an application or user attempts to copy, move, delete, or rename a folder or printer object.</span></span> <span data-ttu-id="cb6d7-145">Le gestionnaire n’effectue pas l’opération elle-même.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-145">The handler does not perform the operation itself.</span></span> <span data-ttu-id="cb6d7-146">Elle l’approuve ou la refuse.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-146">It only approves or vetoes it.</span></span> <span data-ttu-id="cb6d7-147">Si tous les gestionnaires approuvent, l’interpréteur de commandes effectue l’opération.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-147">If all handlers approve, the Shell does the operation.</span></span> <span data-ttu-id="cb6d7-148">Si un gestionnaire refuse l’opération, il est annulé et les gestionnaires restants ne sont pas appelés.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-148">If any handler vetoes the operation, it is canceled and the remaining handlers are not called.</span></span> <span data-ttu-id="cb6d7-149">Les gestionnaires de raccordement de copie ne sont pas informés de la réussite ou de l’échec de l’opération. ils ne peuvent donc pas être utilisés pour surveiller les opérations de fichier.</span><span class="sxs-lookup"><span data-stu-id="cb6d7-149">Copy hook handlers are not informed of the success or failure of the operation, so they cannot be used to monitor file operations.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb6d7-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb6d7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb6d7-151">Création de gestionnaires d’extensions d’environnement</span><span class="sxs-lookup"><span data-stu-id="cb6d7-151">Creating Shell Extension Handlers</span></span>](handlers.md)
</dt> <dt>

<span data-ttu-id="cb6d7-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cb6d7-152">[**ICopyHook**](/previous-versions/windows/desktop/legacy/bb776049(v=vs.85))</span></span>
</dt> </dl>

 

 
