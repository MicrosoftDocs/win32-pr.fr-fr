---
title: Pour créer une configuration de redistribution
description: Pour créer une configuration de redistribution
ms.assetid: cf2c8fa1-cfd6-47cc-b572-ba1b95d59105
keywords:
- Windows Media Format SDK, redistribution de logiciels
- Format de systèmes avancés (ASF), redistribution de logiciels
- ASF (format des systèmes avancés), redistribution de logiciels
- Windows Media Format SDK, redistribution
- Format de systèmes avancés (ASF), redistribution
- ASF (format des systèmes avancés), redistribution
- redistribution de logiciels, création
- redistribution de logiciels, WMFDist.exe
- redistribution, création
- redistribution, WMFDist.exe
- WMFDist.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70f0c2f241d8c1ad164bc14608103f423a7aba78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196704"
---
# <a name="to-create-a-redistribution-setup"></a><span data-ttu-id="c83ca-114">Pour créer une configuration de redistribution</span><span class="sxs-lookup"><span data-stu-id="c83ca-114">To Create a Redistribution Setup</span></span>

1.  <span data-ttu-id="c83ca-115">Faites en sorte que votre routine d’installation installe les fichiers de votre application et effectuez les paramètres requis avant d’appeler le package de redistribution.</span><span class="sxs-lookup"><span data-stu-id="c83ca-115">Have your setup routine install your application files and make required settings before invoking the redistribution package.</span></span>
2.  <span data-ttu-id="c83ca-116">Installez WMFDist.exe.</span><span class="sxs-lookup"><span data-stu-id="c83ca-116">Install WMFDist.exe.</span></span> <span data-ttu-id="c83ca-117">Vous pouvez utiliser l’indicateur/Q : A pour effectuer une installation silencieuse et sans assistance et supprimer l’interface utilisateur de la configuration de la redistribution lors de l’installation de votre application.</span><span class="sxs-lookup"><span data-stu-id="c83ca-117">You can use the /Q:A flag to do a quiet, unattended installation and suppress the user interface of the redistribution setup during the installation of your application.</span></span> <span data-ttu-id="c83ca-118">Votre routine doit ensuite déterminer si le redémarrage est nécessaire à la fin.</span><span class="sxs-lookup"><span data-stu-id="c83ca-118">Your routine must then detect whether restarting is needed at the end.</span></span>

    <span data-ttu-id="c83ca-119">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="c83ca-119">For example:</span></span>

    ```C++
    WMFDist.exe /Q:A
    ```

    

## <a name="related-topics"></a><span data-ttu-id="c83ca-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c83ca-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c83ca-121">**Redistribution de logiciels**</span><span class="sxs-lookup"><span data-stu-id="c83ca-121">**Software Redistribution**</span></span>](software-redistribution.md)
</dt> </dl>

 

 




