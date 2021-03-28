---
description: Montre comment inscrire un verbe qui étend le &\# 0034 ; Sync&\# 0034 ; et &\# 0034 ; Partagez&\# 0034 ; verbes dans la barre de commandes de l’Explorateur Windows.
title: Verbes Sync et Share
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 78267C74-7597-4b98-9DAE-89F2FD515C6B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 734d59ce7b527ad068c03be9083ca67dfca20667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973747"
---
# <a name="sync-and-share-verbs"></a><span data-ttu-id="e7eb5-103">Verbes Sync et Share</span><span class="sxs-lookup"><span data-stu-id="e7eb5-103">Sync and Share Verbs</span></span>

<span data-ttu-id="e7eb5-104">Montre comment inscrire un verbe qui étend les verbes « Sync » et « Share » dans la barre de commandes de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-104">Demonstrates how to register a verb that extends the "Sync" and "Share" verbs in the Windows Explorer Command Bar.</span></span>

<span data-ttu-id="e7eb5-105">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e7eb5-106">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7eb5-106">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="e7eb5-107">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-107">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="e7eb5-108">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-108">Running the Sample</span></span>](#running-the-sample)
-   [<span data-ttu-id="e7eb5-109">Suppression de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-109">Removing the Sample</span></span>](#removing-the-sample)

## <a name="requirements"></a><span data-ttu-id="e7eb5-110">Spécifications</span><span class="sxs-lookup"><span data-stu-id="e7eb5-110">Requirements</span></span>



| <span data-ttu-id="e7eb5-111">Produit</span><span class="sxs-lookup"><span data-stu-id="e7eb5-111">Product</span></span>                                | <span data-ttu-id="e7eb5-112">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="e7eb5-112">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="e7eb5-113">Windows</span><span class="sxs-lookup"><span data-stu-id="e7eb5-113">Windows</span></span>                                | <span data-ttu-id="e7eb5-114">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e7eb5-114">Windows 7</span></span>               |
| <span data-ttu-id="e7eb5-115">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="e7eb5-115">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="e7eb5-116">7.0</span><span class="sxs-lookup"><span data-stu-id="e7eb5-116">7.0</span></span>                     |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="e7eb5-117">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-117">Downloading the Sample</span></span>

| <span data-ttu-id="e7eb5-118">Emplacement</span><span class="sxs-lookup"><span data-stu-id="e7eb5-118">Location</span></span>      | <span data-ttu-id="e7eb5-119">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="e7eb5-119">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7eb5-120">GitHub</span><span class="sxs-lookup"><span data-stu-id="e7eb5-120">GitHub</span></span>  | [<span data-ttu-id="e7eb5-121">Exemple SyncAndShareVerbs</span><span class="sxs-lookup"><span data-stu-id="e7eb5-121">SyncAndShareVerbs sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/SyncAndShareVerbs) |

## <a name="running-the-sample"></a><span data-ttu-id="e7eb5-122">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-122">Running the Sample</span></span>

<span data-ttu-id="e7eb5-123">Pour exécuter l’exemple (Sync) :</span><span class="sxs-lookup"><span data-stu-id="e7eb5-123">To run the sample (sync):</span></span>

1.  <span data-ttu-id="e7eb5-124">Accédez au répertoire qui contient le `sync.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-124">Navigate to the directory that contains the `sync.reg` file</span></span>
2.  <span data-ttu-id="e7eb5-125">Tapez `sync.reg ` sur la ligne de commande ou double-cliquez sur l’icône pour l' `sync.reg` inscrire.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-125">Type `sync.reg ` at the command line, or double-click the icon for `sync.reg` register it.</span></span>
3.  <span data-ttu-id="e7eb5-126">Ouvrez l’Explorateur Windows et sélectionnez un fichier.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-126">Open the Windows Explorer and select a file.</span></span>
4.  <span data-ttu-id="e7eb5-127">Cliquez sur l’option **synchronisation** dans la barre de commandes et sélectionnez une sous-option, par exemple **Paint**.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-127">Click the **Sync** option in the Command Bar and select a suboption such as **Paint**.</span></span>

<span data-ttu-id="e7eb5-128">Pour exécuter l’exemple (partage) :</span><span class="sxs-lookup"><span data-stu-id="e7eb5-128">To run the sample (share):</span></span>

1.  <span data-ttu-id="e7eb5-129">Accédez au répertoire qui contient le `share.reg` fichier.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-129">Navigate to the directory that contains the `share.reg` file.</span></span>
2.  <span data-ttu-id="e7eb5-130">Tapez `share.reg` sur la ligne de commande ou double-cliquez sur l’icône pour l' `share.reg` inscrire.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-130">Type `share.reg` at the command line, or double-click the icon for `share.reg` register it.</span></span>
3.  <span data-ttu-id="e7eb5-131">Ouvrez l’Explorateur Windows et sélectionnez un fichier.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-131">Open Windows Explorer and select a file.</span></span> <span data-ttu-id="e7eb5-132">Cliquez sur l’option **partager** dans la barre de commandes.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-132">Click the **Share** option in the Command Bar.</span></span>
4.  <span data-ttu-id="e7eb5-133">Cliquez sur l’option **partager avec** dans la barre de commandes et sélectionnez une sous-option, par exemple **Paint**.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-133">Click the **Share with** option in the Command Bar and select a suboption such as **Paint**.</span></span>

## <a name="removing-the-sample"></a><span data-ttu-id="e7eb5-134">Suppression de l'exemple</span><span class="sxs-lookup"><span data-stu-id="e7eb5-134">Removing the Sample</span></span>

<span data-ttu-id="e7eb5-135">Pour supprimer l’exemple (Sync) :</span><span class="sxs-lookup"><span data-stu-id="e7eb5-135">To remove the sample (sync):</span></span>

1.  <span data-ttu-id="e7eb5-136">Accédez au répertoire qui contient le fichier Uninstallsync. reg.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-136">Navigate to the directory that contains the Uninstallsync.reg file.</span></span>
2.  <span data-ttu-id="e7eb5-137">Tapez `uninstallsync.reg` sur la ligne de commande ou double-cliquez sur l’icône de `uninstallsync.reg` .</span><span class="sxs-lookup"><span data-stu-id="e7eb5-137">Type `uninstallsync.reg` at the command line, or double-click the icon for `uninstallsync.reg`.</span></span>

<span data-ttu-id="e7eb5-138">Pour supprimer l’exemple (partage) :</span><span class="sxs-lookup"><span data-stu-id="e7eb5-138">To remove the sample (share):</span></span>

1.  <span data-ttu-id="e7eb5-139">Accédez au répertoire qui contient le fichier Uninstallshare. reg.</span><span class="sxs-lookup"><span data-stu-id="e7eb5-139">Navigate to the directory that contains the Uninstallshare.reg file.</span></span>
2.  <span data-ttu-id="e7eb5-140">Tapez `uninstallshare.reg` sur la ligne de commande ou double-cliquez sur l’icône pour `uninstallshare.reg.`</span><span class="sxs-lookup"><span data-stu-id="e7eb5-140">Type `uninstallshare.reg` at the command line, or double-click the icon for `uninstallshare.reg.`</span></span>

 

 



