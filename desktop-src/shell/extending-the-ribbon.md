---
description: Découvrez comment étendre le ruban de l’Explorateur Windows.
title: Extension du ruban
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525323"
---
# <a name="extending-the-ribbon"></a><span data-ttu-id="6e2c7-103">Extension du ruban</span><span class="sxs-lookup"><span data-stu-id="6e2c7-103">Extending the Ribbon</span></span>

<span data-ttu-id="6e2c7-104">Dans l’Explorateur Windows, le ruban permet de rendre les activités de gestion des fichiers de l’utilisateur final courantes plus simples et plus détectables, mais il existe des modifications ouverts pour les développeurs d’applications.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-104">In Windows Explorer, the Ribbon helps make common end-user file management activities easier and more discoverable, but there are changes afoot for app developers.</span></span> <span data-ttu-id="6e2c7-105">Par exemple, l’ancienne barre de commandes était librement extensible, mais le ruban est plus restreint pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-105">For example, the old command bar was freely extensible but the Ribbon is more restricted at this time.</span></span> <span data-ttu-id="6e2c7-106">En outre, le ruban n’est pas affiché par défaut pour toutes les extensions d’espace de noms. vous devez donc vous abonner pour obtenir le ruban. dans le cas contraire, vous recevez l’ancienne barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-106">Also, the Ribbon is not shown by default for all namespace extensions, so you have to opt in to get the Ribbon; otherwise, you get the older command bar.</span></span>

<span data-ttu-id="6e2c7-107">Les actions disponibles pour les utilisateurs sur le ruban se répartissent en trois catégories d’extensibilité :</span><span class="sxs-lookup"><span data-stu-id="6e2c7-107">Actions available to users on the Ribbon fall into three extensibility categories:</span></span>

-   <span data-ttu-id="6e2c7-108">L’extensibilité n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-108">Extensibility is not needed.</span></span> <span data-ttu-id="6e2c7-109">Exemples : copier, coller, supprimer.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-109">Examples: Copy, Paste, Delete.</span></span> <span data-ttu-id="6e2c7-110">Windows gère ces verbes pour vous.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-110">Windows handles these verbs for you.</span></span>
-   <span data-ttu-id="6e2c7-111">L’extensibilité n’est pas autorisée actuellement : des exemples : zip, Close session et d’autres actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-111">Extensibility is not currently allowed: Examples: Zip, Close Session, and other custom actions.</span></span> <span data-ttu-id="6e2c7-112">Utilisez le menu contextuel pour couvrir ces scénarios.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-112">Use the context menu to cover these scenarios.</span></span>
-   <span data-ttu-id="6e2c7-113">L’extensibilité est intégrée à l’action elle-même.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-113">Extensibility is built into the action itself.</span></span> <span data-ttu-id="6e2c7-114">Exemples : recherche, courrier électronique, impression, nouvel élément.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-114">Examples: Search, Email, Print, New Item.</span></span> <span data-ttu-id="6e2c7-115">Vous devez vous inscrire pour que ces verbes incluent votre application ou le format de fichier dans le ruban.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-115">You need to register for these verbs to include your app or file format in the Ribbon .</span></span>

<span data-ttu-id="6e2c7-116">Ce document décrit comment vous pouvez vous abonner pour accéder au ruban et comment s’inscrire pour gérer des verbes de ruban spécifiques.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-116">This document describes how you can opt-in to get the Ribbon, and how to register to handle specific Ribbon verbs.</span></span>

## <a name="opting-in-to-the-ribbon"></a><span data-ttu-id="6e2c7-117">S’abonner au ruban</span><span class="sxs-lookup"><span data-stu-id="6e2c7-117">Opting in to the Ribbon</span></span>

<span data-ttu-id="6e2c7-118">Pour s’abonner au ruban, votre implémentation de [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) doit spécifier le **\_ ruban EP** dans [**IExplorerPaneVisibility :: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) et retourner **EPS \_ force** \| **EPS \_ par défaut \_**.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-118">To opt in to the Ribbon, your [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) implementation should specify **EP\_Ribbon** in [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) and return **EPS\_FORCE** \| **EPS\_DEFAULT\_ON**.</span></span>

## <a name="extending-the-ribbon-for-file-extensions"></a><span data-ttu-id="6e2c7-119">Extension du ruban pour les extensions de fichier</span><span class="sxs-lookup"><span data-stu-id="6e2c7-119">Extending the Ribbon for File Extensions</span></span>

<span data-ttu-id="6e2c7-120">Ces boutons de ruban sont extensibles en fonction des extensions de fichier :</span><span class="sxs-lookup"><span data-stu-id="6e2c7-120">These Ribbon buttons are extensible based on file extensions:</span></span>

-   <span data-ttu-id="6e2c7-121">Extraire tout</span><span class="sxs-lookup"><span data-stu-id="6e2c7-121">Extract All</span></span>
-   <span data-ttu-id="6e2c7-122">Montage \| de la gravure (ISO)</span><span class="sxs-lookup"><span data-stu-id="6e2c7-122">Mount \| Burn (an ISO)</span></span>
-   <span data-ttu-id="6e2c7-123">Lire \| lire tout \| Ajouter à la sélection (verbe : emqueue)</span><span class="sxs-lookup"><span data-stu-id="6e2c7-123">Play \| Play All \| Add to Playlist (verb: Enqueue)</span></span>
-   <span data-ttu-id="6e2c7-124">Ouvrir</span><span class="sxs-lookup"><span data-stu-id="6e2c7-124">Open</span></span>
-   <span data-ttu-id="6e2c7-125">Modifier</span><span class="sxs-lookup"><span data-stu-id="6e2c7-125">Edit</span></span>
-   <span data-ttu-id="6e2c7-126">Propriétés</span><span class="sxs-lookup"><span data-stu-id="6e2c7-126">Properties</span></span>

<span data-ttu-id="6e2c7-127">Lorsque vous vous inscrivez pour gérer statiquement les verbes pertinents pour les nouveaux types de fichiers, le ruban gère les verbes de manière appropriée.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-127">When you register to statically handle the relevant verbs for new file types, the Ribbon handles the verbs appropriately.</span></span> <span data-ttu-id="6e2c7-128">Vous vous inscrivez comme vous le feriez pour les verbes de menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-128">You register just as you would for context menu verbs.</span></span> <span data-ttu-id="6e2c7-129">Pour plus d’informations sur les associations de fichiers et l’inscription pour les verbes, consultez [verbes et associations de fichiers](fa-verbs.md) et [création de gestionnaires de menu contextuel](context-menu-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c7-129">For more information about file associations and registering for verbs, see [Verbs and File Associations](fa-verbs.md) and [Creating Shortcut Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="registering-as-a-default-handler-for-actionids"></a><span data-ttu-id="6e2c7-130">Inscription en tant que gestionnaire par défaut pour ActionIds</span><span class="sxs-lookup"><span data-stu-id="6e2c7-130">Registering as a Default Handler for ActionIds</span></span>

<span data-ttu-id="6e2c7-131">Tout d’abord, inscrivez votre ProgId sous la sous-clé AssocActionId appropriée.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-131">First, register your ProgId under the appropriate AssocActionId subkey.</span></span> <span data-ttu-id="6e2c7-132">Chaque sous-clé AssocActionId représente un verbe ou une action que les utilisateurs peuvent appeler à partir du ruban.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-132">Each AssocActionId subkey represents a verb or action that users can invoke from the Ribbon.</span></span> <span data-ttu-id="6e2c7-133">Dans cet exemple, l’application s’inscrit pour l’ActionID ZipSelection pour étendre le bouton « extraire tout » sur le ruban.</span><span class="sxs-lookup"><span data-stu-id="6e2c7-133">In this example, the app registers for the ZipSelection ActionID to extend the "Extract All" button on the Ribbon.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

<span data-ttu-id="6e2c7-134">Une fois l’inscription terminée, vous devez vous inscrire pour gérer les protocoles de la même façon que vous le feriez normalement, comme décrit dans [programmes par défaut](default-programs.md).</span><span class="sxs-lookup"><span data-stu-id="6e2c7-134">Once that registration is complete, you must then register to handle protocols just as you normally would, as described in [Default Programs](default-programs.md).</span></span>

 

 



