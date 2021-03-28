---
description: Montre comment appeler la fonction ShellExecute à partir du processus de l’Explorateur Windows.
title: Exécution dans l’Explorateur, exemple
ms.topic: article
ms.date: 05/31/2018
ms.assetid: D307B22A-E4A3-4215-B28E-F48A721260A1
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7a511f7ccc7edd218edd405de163501afd530f46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973298"
---
# <a name="execute-in-explorer-sample"></a><span data-ttu-id="4d290-103">Exécution dans l’Explorateur, exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-103">Execute In Explorer Sample</span></span>

<span data-ttu-id="4d290-104">Montre comment appeler la fonction [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) à partir du processus de l’Explorateur Windows.</span><span class="sxs-lookup"><span data-stu-id="4d290-104">Demonstrates how to call the [**ShellExecute**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecutea) function from the Windows Explorer process.</span></span> <span data-ttu-id="4d290-105">Cela est utile lors du lancement d’un processus non élevé à partir d’un processus avec élévation de privilèges.</span><span class="sxs-lookup"><span data-stu-id="4d290-105">This is useful when launching an unelevated process from an elevated process.</span></span>

<span data-ttu-id="4d290-106">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d290-106">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d290-107">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4d290-107">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="4d290-108">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-108">Downloading the Sample</span></span>](#downloading-the-sample)
-   [<span data-ttu-id="4d290-109">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-109">Building the Sample</span></span>](#building-the-sample)
-   [<span data-ttu-id="4d290-110">Exécution de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-110">Running the Sample</span></span>](#running-the-sample)

## <a name="requirements"></a><span data-ttu-id="4d290-111">Spécifications</span><span class="sxs-lookup"><span data-stu-id="4d290-111">Requirements</span></span>



| <span data-ttu-id="4d290-112">Produit</span><span class="sxs-lookup"><span data-stu-id="4d290-112">Product</span></span>                                | <span data-ttu-id="4d290-113">Version minimale du produit</span><span class="sxs-lookup"><span data-stu-id="4d290-113">Minimum Product Version</span></span> |
|----------------------------------------|-------------------------|
| <span data-ttu-id="4d290-114">Windows</span><span class="sxs-lookup"><span data-stu-id="4d290-114">Windows</span></span>                                | <span data-ttu-id="4d290-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d290-115">Windows Vista</span></span>           |
| <span data-ttu-id="4d290-116">Kit de développement logiciel Windows</span><span class="sxs-lookup"><span data-stu-id="4d290-116">Windows Software Development Kit (SDK)</span></span> | <span data-ttu-id="4d290-117">7.0</span><span class="sxs-lookup"><span data-stu-id="4d290-117">7.0</span></span>                     |



 

<span data-ttu-id="4d290-118">Pour obtenir des spécifications supplémentaires, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4d290-118">For additional requirements, see the Readme file included with the sample.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="4d290-119">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-119">Downloading the Sample</span></span>

| <span data-ttu-id="4d290-120">Emplacement</span><span class="sxs-lookup"><span data-stu-id="4d290-120">Location</span></span>      | <span data-ttu-id="4d290-121">URL du chemin</span><span class="sxs-lookup"><span data-stu-id="4d290-121">Path URL</span></span>                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d290-122">GitHub</span><span class="sxs-lookup"><span data-stu-id="4d290-122">GitHub</span></span>  | [<span data-ttu-id="4d290-123">Exemple ExecInExplorer</span><span class="sxs-lookup"><span data-stu-id="4d290-123">ExecInExplorer sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ExecInExplorer) |

## <a name="building-the-sample"></a><span data-ttu-id="4d290-124">Génération de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-124">Building the Sample</span></span>

<span data-ttu-id="4d290-125">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4d290-125">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

## <a name="running-the-sample"></a><span data-ttu-id="4d290-126">Exécution de l'exemple</span><span class="sxs-lookup"><span data-stu-id="4d290-126">Running the Sample</span></span>

<span data-ttu-id="4d290-127">Pour obtenir des instructions sur la façon de générer l’exemple, consultez le fichier Lisez-moi inclus dans l’exemple.</span><span class="sxs-lookup"><span data-stu-id="4d290-127">For instructions about how to build the sample, see the Readme file included with the sample.</span></span>

 

 



