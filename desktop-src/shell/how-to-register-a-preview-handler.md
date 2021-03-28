---
description: Cette rubrique explique comment inscrire un gestionnaire d’aperçus associé à un type de données donné.
ms.assetid: 5f194d29-d09f-4426-a63e-911db65ce700
title: Comment inscrire un gestionnaire d’aperçus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5af9610de1822678521557fc20aa53f4e556e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973131"
---
# <a name="how-to-register-a-preview-handler"></a><span data-ttu-id="616f0-103">Comment inscrire un gestionnaire d’aperçus</span><span class="sxs-lookup"><span data-stu-id="616f0-103">How to Register a Preview Handler</span></span>

<span data-ttu-id="616f0-104">Cette rubrique explique comment inscrire un gestionnaire d’aperçus associé à un type de données donné.</span><span class="sxs-lookup"><span data-stu-id="616f0-104">This topic explains how to register a preview handler associated with a given data type.</span></span> <span data-ttu-id="616f0-105">À des fins d’illustration, les exemples de cette rubrique utilisent un type de fichier. xyz.</span><span class="sxs-lookup"><span data-stu-id="616f0-105">For the purposes of illustration, examples in this topic use a .xyz file type.</span></span> <span data-ttu-id="616f0-106">L’inscription d’un gestionnaire d’aperçus est un enregistrement standard basé sur une association de fichiers.</span><span class="sxs-lookup"><span data-stu-id="616f0-106">Registration of a preview handler is a standard file association-based registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="616f0-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="616f0-107">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="616f0-108">Étape 1 :</span><span class="sxs-lookup"><span data-stu-id="616f0-108">Step 1:</span></span>

<span data-ttu-id="616f0-109">Tout d’abord, une extension de nom de fichier est associée à un ProgID.</span><span class="sxs-lookup"><span data-stu-id="616f0-109">First, a file name extension is associated with a ProgID.</span></span> <span data-ttu-id="616f0-110">L’entrée suivante associe la sous-clé **xyzfile** ProgID à l’extension de nom de fichier. xyz.</span><span class="sxs-lookup"><span data-stu-id="616f0-110">The following entry associates the **xyzfile** ProgID subkey with the .xyz file name extension.</span></span>

```
HKEY_CLASSES_ROOT
   .xyz
      (Default) = [REG_SZ] xyzfile
```

<span data-ttu-id="616f0-111">La sous-clé **xyzfile** ProgID est stockée avec les autres ProgID comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="616f0-111">The **xyzfile** ProgID subkey is stored with the other ProgIDs as shown here:</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
```

<span data-ttu-id="616f0-112">Chaque sous-clé ProgID du gestionnaire d’aperçus contient une sous-clé nommée **shellex** qui contient une sous-clé *toujours* nommée **{8895b1c6-B41F-4c1c-A562-0d564250836f}**.</span><span class="sxs-lookup"><span data-stu-id="616f0-112">Each preview handler ProgID subkey contains a subkey named **shellex** that contains a subkey *always* named **{8895b1c6-b41f-4c1c-a562-0d564250836f}**.</span></span> <span data-ttu-id="616f0-113">La présence de cette sous-clé indique au système que le gestionnaire est un gestionnaire d’aperçus.</span><span class="sxs-lookup"><span data-stu-id="616f0-113">The presence of that subkey tells the system that the handler is a preview handler.</span></span>

<span data-ttu-id="616f0-114">La valeur par défaut de la sous-clé **{8895b1c6-B41F-4c1c-A562-0d564250836f}** est l’identificateur de classe (CLSID) de votre gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="616f0-114">The default value of the **{8895b1c6-b41f-4c1c-a562-0d564250836f}** subkey is the class identifier (CLSID) of your handler.</span></span> <span data-ttu-id="616f0-115">Un exemple de la sous-clé **xyzfile** ProgID est illustré ici, associant un gestionnaire de CLSID {ec3a629a-a47c-4245-BC78-b4b63d0e3154}.</span><span class="sxs-lookup"><span data-stu-id="616f0-115">An example of the **xyzfile** ProgID subkey is shown here, associating a handler of CLSID {ec3a629a-a47c-4245-bc78-b4b63d0e3154}.</span></span>

```
HKEY_CLASSES_ROOT
   xyzfile
      shellex
         {8895b1c6-b41f-4c1c-a562-0d564250836f}
            (Default) = [REG_SZ] {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
```

### <a name="step-2"></a><span data-ttu-id="616f0-116">Étape 2 :</span><span class="sxs-lookup"><span data-stu-id="616f0-116">Step 2:</span></span>

<span data-ttu-id="616f0-117">Ensuite, ajoutez la sous-clé sous **CLSID** pour votre gestionnaire d’aperçus.</span><span class="sxs-lookup"><span data-stu-id="616f0-117">Next, add the subkey under **CLSID** for your preview handler.</span></span> <span data-ttu-id="616f0-118">Un exemple est illustré ici.</span><span class="sxs-lookup"><span data-stu-id="616f0-118">An example is shown here.</span></span> <span data-ttu-id="616f0-119">Une explication des entrées individuelles suit.</span><span class="sxs-lookup"><span data-stu-id="616f0-119">An explanation of individual entries follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
         (Default) = [REG_SZ] Fabricam XYZ Preview Handler
         DisplayName = [REG_SZ] @myhandler.dll,-101
         Icon = [REG_SZ] myhandler.dll,201
         AppID = [REG_SZ] {6d2b5079-2f0b-48dd-ab7f-97cec514d30b}
         InprocServer32
            (Default) = [REG_EXPAND_SZ] %ProgramFiles%\Fabricam\myhandler.dll
            ThreadingModel = [REG_SZ] Apartment
            ProgID = [REG_SZ] xyzfile
            VersionIndependentProgID = [REG_SZ] Version IndependentProgID
```

<span data-ttu-id="616f0-120">La valeur par défaut de votre sous-clé ( **{ec3a629a-A47C-4245-BC78-b4b63d0e3154}**) n’est pas obligatoire ou utilisée.</span><span class="sxs-lookup"><span data-stu-id="616f0-120">The default value for your subkey (here, **{ec3a629a-a47c-4245-bc78-b4b63d0e3154}**) is not required or used.</span></span> <span data-ttu-id="616f0-121">Toutefois, la définition d’une chaîne non localisée peut vous aider à déboguer les problèmes d’inscription.</span><span class="sxs-lookup"><span data-stu-id="616f0-121">However, setting it to a nonlocalized string can help you to debug registration issues.</span></span>

<span data-ttu-id="616f0-122">Le signe moins (-101) dans la ressource. dll de l’entrée DisplayName existe pour des raisons d’héritage.</span><span class="sxs-lookup"><span data-stu-id="616f0-122">The minus sign (-101) in the .dll resource in the DisplayName entry exists for legacy reasons.</span></span> <span data-ttu-id="616f0-123">En revanche, l’entrée d’icône ne nécessite pas de signe moins.</span><span class="sxs-lookup"><span data-stu-id="616f0-123">The Icon entry, on the other hand, does not require a minus sign.</span></span>

<span data-ttu-id="616f0-124">La valeur AppID donne une référence à l’AppID de l’application associée à l’extension de nom de fichier (stockée sous l’AppID **\_ \_ racine de classes HKEY** \\ .</span><span class="sxs-lookup"><span data-stu-id="616f0-124">The AppID value gives a reference to the AppID of the application associated with the file name extension (stored under **HKEY\_CLASSES\_ROOT**\\**APPID**.</span></span> <span data-ttu-id="616f0-125">La valeur utilisée ici ({6d2b5079-2f0b-48dd-AB7F-97cec514d30b}) est l’ID de l’hôte de substitution Prevhost.exe.</span><span class="sxs-lookup"><span data-stu-id="616f0-125">The value used here—{6d2b5079-2f0b-48dd-ab7f-97cec514d30b}—is the ID of the Prevhost.exe surrogate host.</span></span> <span data-ttu-id="616f0-126">les gestionnaires d’aperçus 32 bits doivent utiliser **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} lorsqu’ils sont installés sur des systèmes d’exploitation 64 bits.</span><span class="sxs-lookup"><span data-stu-id="616f0-126">32-bit preview handlers should use **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C} when installed on 64-bit operating systems.</span></span>

<span data-ttu-id="616f0-127">Les entrées sous la sous-clé **InprocServer32** incluent une référence à la sous-clé ProgID de l’extension de nom de fichier, ainsi qu’une entrée pour un [VersionIndependentProgID](../com/versionindependentprogid.md).</span><span class="sxs-lookup"><span data-stu-id="616f0-127">The entries under the **InprocServer32** subkey include a reference back to the file name extension's ProgID subkey as well as an entry for a [VersionIndependentProgID](../com/versionindependentprogid.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="616f0-128">Étape 3 :</span><span class="sxs-lookup"><span data-stu-id="616f0-128">Step 3:</span></span>

<span data-ttu-id="616f0-129">Enfin, le gestionnaire d’aperçus doit être ajouté à la liste de tous les gestionnaires d’aperçus.</span><span class="sxs-lookup"><span data-stu-id="616f0-129">Finally, the preview handler must be added to the list of all preview handlers.</span></span> <span data-ttu-id="616f0-130">Cette liste est utilisée comme une optimisation par le système pour énumérer tous les gestionnaires d’aperçus inscrits à des fins d’affichage.</span><span class="sxs-lookup"><span data-stu-id="616f0-130">This list is used as an optimization by the system to enumerate all registered preview handlers for display purposes.</span></span> <span data-ttu-id="616f0-131">Là encore, la valeur par défaut n’est pas obligatoire, elle facilite simplement le processus de débogage.</span><span class="sxs-lookup"><span data-stu-id="616f0-131">Again, the default value is not required, it simply aids in the debugging process.</span></span>

> [!Note]  
> <span data-ttu-id="616f0-132">Dans Windows 7, si l’application est installée pour tous les utilisateurs de l’ordinateur, utilisez HKEY \_ local \_ machine ; si pour un seul utilisateur, utilisez HKEY \_ Current \_ User.</span><span class="sxs-lookup"><span data-stu-id="616f0-132">In Windows 7, if the application is installed for all users of the computer, use HKEY\_LOCAL\_MACHINE; if for only one user, use HKEY\_CURRENT\_USER.</span></span>

 

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PreviewHandlers
                  {ec3a629a-a47c-4245-bc78-b4b63d0e3154}
                     (Default) = [REG_SZ] Fabricam XYZ Preview Handler
```

## <a name="related-topics"></a><span data-ttu-id="616f0-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="616f0-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="616f0-134">Gestionnaires d’aperçus et hôte de l’interpréteur de commandes</span><span class="sxs-lookup"><span data-stu-id="616f0-134">Preview Handlers and Shell Preview Host</span></span>](preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="616f0-135">Génération de gestionnaires d’aperçus</span><span class="sxs-lookup"><span data-stu-id="616f0-135">Building Preview Handlers</span></span>](building-preview-handlers.md)
</dt> <dt>

[<span data-ttu-id="616f0-136">Instructions du gestionnaire d’aperçus</span><span class="sxs-lookup"><span data-stu-id="616f0-136">Preview Handler Guidelines</span></span>](preview-handler-guidelines.md)
</dt> </dl>

 

 
