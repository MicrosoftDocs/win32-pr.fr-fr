---
title: Installation des visualisations
description: Installation des visualisations
ms.assetid: ca391e38-def5-47da-81f7-94aa96530387
keywords:
- Plug-ins du lecteur Windows Media, visualisations
- plug-ins, visualisations
- visualisations, installation
- visualisations personnalisées, installation
- installation des visualisations
- visualisations, inscription
- visualisations personnalisées, inscription
- Registre, visualisations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f1dc8f33d7b5f5b938bee6c89d946955509ab34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532030"
---
# <a name="installing-visualizations"></a><span data-ttu-id="8ac1a-111">Installation des visualisations</span><span class="sxs-lookup"><span data-stu-id="8ac1a-111">Installing Visualizations</span></span>

<span data-ttu-id="8ac1a-112">Vous devez fournir un processus d’installation pour l’utilisateur de votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-112">You must provide an installation process for the user of your visualization.</span></span> <span data-ttu-id="8ac1a-113">Vous devez également fournir un processus de désinstallation pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-113">You must also provide an uninstall process for the user.</span></span> <span data-ttu-id="8ac1a-114">La version actuelle du lecteur Windows Media n’installe pas les visualisations à partir de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-114">The current version of Windows Media Player does not install visualizations from the user interface.</span></span>

## <a name="installing-to-the-visualization-folder"></a><span data-ttu-id="8ac1a-115">Installation dans le dossier visualisation</span><span class="sxs-lookup"><span data-stu-id="8ac1a-115">Installing to the Visualization Folder</span></span>

<span data-ttu-id="8ac1a-116">Il est recommandé d’installer toutes les visualisations dans le sous-dossier visualisations du dossier où le lecteur Windows Media est installé.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-116">It is recommended that you install all visualizations in the Visualizations subfolder of the folder where Windows Media Player is installed.</span></span>

## <a name="registering-your-visualization"></a><span data-ttu-id="8ac1a-117">Inscription de votre visualisation</span><span class="sxs-lookup"><span data-stu-id="8ac1a-117">Registering Your Visualization</span></span>

<span data-ttu-id="8ac1a-118">Les visualisations sont des DLL COM et suivent toutes les règles normales d’installation et de suppression.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-118">Visualizations are COM DLLs and follow all the normal rules of installation and removal.</span></span> <span data-ttu-id="8ac1a-119">Vous pouvez utiliser regsvr32.exe ou d’autres outils d’installation pour inscrire votre visualisation.</span><span class="sxs-lookup"><span data-stu-id="8ac1a-119">You can use regsvr32.exe or other installation tools to register your visualization.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8ac1a-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8ac1a-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ac1a-121">**À propos des visualisations personnalisées**</span><span class="sxs-lookup"><span data-stu-id="8ac1a-121">**About Custom Visualizations**</span></span>](about-custom-visualizations.md)
</dt> </dl>

 

 




