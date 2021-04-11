---
description: Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application. Windows Installer possède de nombreuses actions standard intégrées. Les développeurs de packages d’installation peuvent également créer leurs propres actions personnalisées.
ms.assetid: 33651988-e371-4258-96a7-bcd7d6762161
title: Actions standard
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48ed4f9c2a7fc6671442f6b72cd10889e2fcf5e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202400"
---
# <a name="standard-actions"></a><span data-ttu-id="2a860-105">Actions standard</span><span class="sxs-lookup"><span data-stu-id="2a860-105">Standard Actions</span></span>

<span data-ttu-id="2a860-106">Une action encapsule une fonction typique effectuée pendant l’installation ou la maintenance d’une application.</span><span class="sxs-lookup"><span data-stu-id="2a860-106">An action encapsulates a typical function performed during the installation or maintenance of an application.</span></span> <span data-ttu-id="2a860-107">Windows Installer possède de nombreuses actions standard intégrées.</span><span class="sxs-lookup"><span data-stu-id="2a860-107">Windows Installer has many built-in standard actions.</span></span> <span data-ttu-id="2a860-108">Les développeurs de packages d’installation peuvent également créer leurs propres [actions personnalisées](custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="2a860-108">Developers of installation packages can also author their own [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="2a860-109">Voici quelques exemples d’actions standard du programme d’installation :</span><span class="sxs-lookup"><span data-stu-id="2a860-109">Examples of installer standard actions include:</span></span>

-   <span data-ttu-id="2a860-110">[Action CreateShortcuts](createshortcuts-action.md): gère la création de raccourcis vers des fichiers installés avec l’application actuelle.</span><span class="sxs-lookup"><span data-stu-id="2a860-110">[CreateShortcuts action](createshortcuts-action.md): Manages the creation of shortcuts to files installed with the current application.</span></span> <span data-ttu-id="2a860-111">Cette action utilise la [table de raccourcis](shortcut-table.md) pour ses données.</span><span class="sxs-lookup"><span data-stu-id="2a860-111">This action uses the [Shortcut table](shortcut-table.md) for its data.</span></span>
-   <span data-ttu-id="2a860-112">[Action InstallFiles](installfiles-action.md): copie les fichiers sélectionnés du répertoire source vers le répertoire de destination.</span><span class="sxs-lookup"><span data-stu-id="2a860-112">[InstallFiles action](installfiles-action.md): Copies selected files from the source directory to the destination directory.</span></span> <span data-ttu-id="2a860-113">Cette action utilise la [table de fichiers](file-table.md) pour ses données.</span><span class="sxs-lookup"><span data-stu-id="2a860-113">This action uses the [File table](file-table.md) for its data.</span></span>
-   <span data-ttu-id="2a860-114">[Action WriteRegistryValues](writeregistryvalues-action.md): configure les informations de Registre requises par l’application dans le registre.</span><span class="sxs-lookup"><span data-stu-id="2a860-114">[WriteRegistryValues action](writeregistryvalues-action.md): Sets up registry information the application requires in the registry.</span></span> <span data-ttu-id="2a860-115">Cette action utilise la [table de Registre](registry-table.md) pour ses données.</span><span class="sxs-lookup"><span data-stu-id="2a860-115">This action uses the [Registry table](registry-table.md) for its data.</span></span>

<span data-ttu-id="2a860-116">Les sections suivantes traitent des actions standard.</span><span class="sxs-lookup"><span data-stu-id="2a860-116">The following sections discuss standard actions.</span></span>

-   [<span data-ttu-id="2a860-117">À propos des actions standard</span><span class="sxs-lookup"><span data-stu-id="2a860-117">About Standard Actions</span></span>](about-standard-actions.md)
-   [<span data-ttu-id="2a860-118">Utilisation d’actions standard</span><span class="sxs-lookup"><span data-stu-id="2a860-118">Using Standard Actions</span></span>](using-standard-actions.md)
-   [<span data-ttu-id="2a860-119">Informations de référence sur les actions standard</span><span class="sxs-lookup"><span data-stu-id="2a860-119">Standard Actions Reference</span></span>](standard-actions-reference.md)

 

 



