---
title: Redistribution de logiciels
description: Redistribution de logiciels
ms.assetid: 443df640-e74c-4903-b801-f4bd42a04659
keywords:
- Windows Media Format SDK, redistribution de logiciels
- Format de systèmes avancés (ASF), redistribution de logiciels
- ASF (format des systèmes avancés), redistribution de logiciels
- Windows Media Format SDK, redistribution
- Format de systèmes avancés (ASF), redistribution
- ASF (format des systèmes avancés), redistribution
- redistribution de logiciels, à propos de
- redistribution, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d51f332f5b0e038293a1dbe1dbf59015931d67e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672517"
---
# <a name="software-redistribution"></a><span data-ttu-id="3fbd1-111">Redistribution de logiciels</span><span class="sxs-lookup"><span data-stu-id="3fbd1-111">Software Redistribution</span></span>

<span data-ttu-id="3fbd1-112">L’inclusion du logiciel Windows Media format dans une installation d’application est appelée redistribution.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-112">The inclusion of Windows Media Format software in an application setup is known as redistribution.</span></span> <span data-ttu-id="3fbd1-113">Le kit de développement logiciel (SDK) Windows Media Format inclut un package d’installation qui peut être inclus dans le programme d’installation de votre application.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-113">The Windows Media Format SDK includes an installation package which can be included with your application setup.</span></span> <span data-ttu-id="3fbd1-114">Le package d’installation est un fichier exécutable nommé wmfdist95.exe.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-114">The installation package is an executable file named wmfdist95.exe.</span></span> <span data-ttu-id="3fbd1-115">Lorsque vous installez le kit de développement logiciel (SDK) Windows Media format, le package d’installation est copié dans le \\ dossier Redist du répertoire d’installation (c : \\ WMSDK \\ wmfsdk par défaut).</span><span class="sxs-lookup"><span data-stu-id="3fbd1-115">When you install the Windows Media Format SDK, the installation package is copied to the \\Redist folder of the install directory (c:\\wmsdk\\wmfsdk by default).</span></span>

<span data-ttu-id="3fbd1-116">Les sections suivantes fournissent des procédures et d’autres informations sur la configuration de la redistribution de logiciels.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-116">The following sections provide procedures and other information for software redistribution setup.</span></span>



| <span data-ttu-id="3fbd1-117">Section</span><span class="sxs-lookup"><span data-stu-id="3fbd1-117">Section</span></span>                                                                            | <span data-ttu-id="3fbd1-118">Description</span><span class="sxs-lookup"><span data-stu-id="3fbd1-118">Description</span></span>                                                                                                                                                                      |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fbd1-119">Pour créer une configuration de redistribution</span><span class="sxs-lookup"><span data-stu-id="3fbd1-119">To Create a Redistribution Setup</span></span>](to-create-a-redistribution-setup.md)           | <span data-ttu-id="3fbd1-120">Décrit la procédure de création d’une configuration d’application.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-120">Describes the procedure for creating an application setup.</span></span>                                                                                                                       |
| [<span data-ttu-id="3fbd1-121">Détection de l’état de l’installation</span><span class="sxs-lookup"><span data-stu-id="3fbd1-121">Detecting Setup Status</span></span>](detecting-setup-status.md)                               | <span data-ttu-id="3fbd1-122">Fournit un exemple de code qui vérifie l’état de l’installation dans le registre pour déterminer si le package de redistribution doit être installé.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-122">Provides example code that checks the registry for installation status to determine whether the redistribution package needs to be installed.</span></span>                                    |
| [<span data-ttu-id="3fbd1-123">Exemple de code pour la configuration de la redistribution</span><span class="sxs-lookup"><span data-stu-id="3fbd1-123">Example Code for Redistribution Setup</span></span>](example-code-for-redistribution-setup.md) | <span data-ttu-id="3fbd1-124">Fournit un exemple de code qui peut être utilisé dans votre routine d’installation pour exécuter les packages de redistribution en mode silencieux et notifier votre routine d’installation lorsque l’ordinateur doit être redémarré.</span><span class="sxs-lookup"><span data-stu-id="3fbd1-124">Provides example code that can be used in your setup routine to run the redistribution packages in quiet mode and notify your setup routine when the computer must be restarted.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3fbd1-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3fbd1-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fbd1-126">**Considérations relatives aux projets**</span><span class="sxs-lookup"><span data-stu-id="3fbd1-126">**Project Considerations**</span></span>](project-considerations.md)
</dt> </dl>

 

 




