---
title: Installation à partir d’un CD-ROM en ligne
description: Installation à partir d’un CD-ROM en ligne
ms.assetid: 4cf34f0e-caa0-42d1-b99a-51bbb7f0a7df
keywords:
- Windows Media Player Online stores, installation à partir du CD-ROM en ligne
- magasins en ligne, installation à partir du CD-ROM en ligne
- tapez 1 magasins en ligne, installation à partir du CD-ROM en ligne
- tapez 2 magasins en ligne, installation à partir du CD-ROM en ligne
- Windows Media Player Online stores, installations en ligne à partir du CD
- magasins en ligne, installations en ligne à partir du CD
- tapez 1 magasins en ligne, installations en ligne à partir du CD
- type 2 magasins en ligne, installations en ligne à partir du CD
- Windows Media Player Online stores, CD s’installe en ligne
- magasins en ligne, CD-ROM s’installe en ligne
- tapez 1 magasins en ligne, CD installions en ligne
- tapez 2 magasins en ligne, CD installions en ligne
- installation de magasins en ligne à partir d’un CD en ligne
- Installation à partir de CD de magasins en ligne en ligne
- installations en ligne de magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd57015e64dece444b1a91afebe3144bee117caa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106532031"
---
# <a name="installing-from-a-cd-while-online"></a><span data-ttu-id="2ca5a-118">Installation à partir d’un CD-ROM en ligne</span><span class="sxs-lookup"><span data-stu-id="2ca5a-118">Installing from a CD While Online</span></span>

<span data-ttu-id="2ca5a-119">Les utilisateurs peuvent installer le lecteur Windows Media à partir d’un CD tout en étant connecté à Internet.</span><span class="sxs-lookup"><span data-stu-id="2ca5a-119">Users can install Windows Media Player from a CD while connected to the Internet.</span></span> <span data-ttu-id="2ca5a-120">Dans ce cas, le programme d’installation de Windows Media Player localise le document ServiceInfo spécifié par le paramètre de ligne de commande *serviceInfo* .</span><span class="sxs-lookup"><span data-stu-id="2ca5a-120">When this happens, Windows Media Player setup locates the ServiceInfo document specified by the *ServiceInfo* command line parameter.</span></span> <span data-ttu-id="2ca5a-121">Si l’attribut de **clé** correspond au paramètre de ligne de commande *DefaultService* , le programme d’installation inspecte l’élément d’installation pour personnaliser le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="2ca5a-121">If the **Key** attribute matches the *DefaultService* command line parameter, setup inspects the Install element to customize the setup process.</span></span> <span data-ttu-id="2ca5a-122">À l’aide des valeurs d’attribut, le programme d’installation affiche votre contrat de licence utilisateur final (CLUF) et votre déclaration de confidentialité, et récupère et installe également votre fichier. cab sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ca5a-122">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="2ca5a-123">Par exemple, vous pouvez utiliser cette fonctionnalité pour installer la dernière version d’un objet COM requis par votre magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="2ca5a-123">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

<span data-ttu-id="2ca5a-124">Une fois installé, le lecteur Windows Media définit le magasin en ligne initial à l’aide du nom de clé que vous avez spécifié pour le paramètre de ligne de commande *DefaultService* .</span><span class="sxs-lookup"><span data-stu-id="2ca5a-124">After it is installed, Windows Media Player sets the initial online store using the key name you specified for the *DefaultService* command line parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ca5a-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2ca5a-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ca5a-126">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="2ca5a-126">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="2ca5a-127">**Élément d’installation**</span><span class="sxs-lookup"><span data-stu-id="2ca5a-127">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="2ca5a-128">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="2ca5a-128">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="2ca5a-129">**Définition de la boutique en ligne initiale**</span><span class="sxs-lookup"><span data-stu-id="2ca5a-129">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> <dt>

[<span data-ttu-id="2ca5a-130">**Paramètres de ligne de commande d’installation pour les magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="2ca5a-130">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




