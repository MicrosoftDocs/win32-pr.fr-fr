---
title: Installation à partir du Web en ligne
description: Installation à partir du Web en ligne
ms.assetid: 891483b0-6ba4-4ed4-b043-c6c109dc696b
keywords:
- Windows Media Player Online stores, installation à partir du Web en ligne
- magasins en ligne, installation à partir du Web en ligne
- tapez 1 magasins en ligne, installation à partir du Web en ligne
- tapez 2 magasins en ligne, installation à partir du Web en ligne
- Windows Media Player Online stores, en ligne installe à partir du Web
- magasins en ligne, installations en ligne à partir du Web
- tapez 1 magasins en ligne, installations en ligne à partir du Web
- tapez 2 magasins en ligne, installations en ligne à partir du Web
- installation de magasins en ligne à partir du Web en ligne
- installations en ligne de magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd342d3fc79cf3012d5bc290561a9b63167e044f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106540746"
---
# <a name="installing-from-the-web-while-online"></a><span data-ttu-id="4ac4c-113">Installation à partir du Web en ligne</span><span class="sxs-lookup"><span data-stu-id="4ac4c-113">Installing from the Web While Online</span></span>

<span data-ttu-id="4ac4c-114">Les utilisateurs peuvent installer le lecteur Windows Media en tant que téléchargement Web tout en étant connecté à Internet.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-114">Users can install Windows Media Player as a Web download while connected to the Internet.</span></span> <span data-ttu-id="4ac4c-115">Dans ce cas, Microsoft peut configurer le magasin en ligne initial que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-115">In this case, Microsoft can configure the initial online store that you specify.</span></span>

<span data-ttu-id="4ac4c-116">Pour redistribuer le lecteur Windows Media de cette manière, utilisez l’URL suivante :</span><span class="sxs-lookup"><span data-stu-id="4ac4c-116">To redistribute Windows Media Player in this manner, use the following URL:</span></span>

<span data-ttu-id="4ac4c-117"> https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale =*localID*&service =*clé*</span><span class="sxs-lookup"><span data-stu-id="4ac4c-117">https://go.microsoft.com/fwlink/p/?linkid=32981&SV=*version*&UserLocale=*localID*&Service=*key*</span></span>

<span data-ttu-id="4ac4c-118">Dans l’URL précédente, définissez *Key* sur le nom de clé de votre magasin en ligne et définissez *LocaleID* sur l’identificateur des paramètres régionaux dans lesquels votre magasin fournit le service.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-118">In the preceding URL, set *key* to the key name for your online store, and set *localeID* to the identifier of the locale where your store provides service.</span></span> <span data-ttu-id="4ac4c-119">Définissez la *version* sur 2 pour le lecteur Windows Media 11 sur Windows XP ou 1 pour le lecteur Windows Media 10.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-119">Set *version* to 2 for Windows Media Player 11 on Windows XP or 1 for Windows Media Player 10.</span></span> <span data-ttu-id="4ac4c-120">L’URL installe le lecteur Windows Media et définit le magasin actif initial sur celui spécifié par la *clé*.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-120">The URL installs Windows Media Player and sets the initial active store to the one specified by *key*.</span></span>

<span data-ttu-id="4ac4c-121">L’exemple suivant montre une URL qui installe le lecteur Windows Media 11 et définit Proseware comme magasin actif initial.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-121">The following example shows a URL that installs Windows Media Player 11 and sets Proseware as the initial active store.</span></span> <span data-ttu-id="4ac4c-122">La valeur de 409 pour *LocaleID* indique que Proseware fournit le service dans le États-Unis.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-122">The value of 409 for *localeID* indicates that Proseware provides service in the United States.</span></span>

https://go.microsoft.com/fwlink/p/?linkid=32981&SV=2&UserLocale=409&Service=Proseware

<span data-ttu-id="4ac4c-123">Si le document ServiceInfo du magasin en ligne comprend un élément installer, le programme d’installation du lecteur Windows Media personnalisera le processus d’installation.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-123">If the ServiceInfo document for the online store includes an Install element, Windows Media Player setup will customize the setup process.</span></span> <span data-ttu-id="4ac4c-124">À l’aide des valeurs d’attribut, le programme d’installation affiche votre contrat de licence utilisateur final (CLUF) et votre déclaration de confidentialité, et récupère et installe également votre fichier. cab sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-124">Using the attribute values, setup displays your End User License Agreement (EULA) and your privacy statement, and also retrieves and installs your .cab file to the user's computer.</span></span> <span data-ttu-id="4ac4c-125">Par exemple, vous pouvez utiliser cette fonctionnalité pour installer la dernière version d’un objet COM requis par votre magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="4ac4c-125">For example, you can use this feature to install the latest version of a COM object that your online store requires.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ac4c-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4ac4c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ac4c-127">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="4ac4c-127">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="4ac4c-128">**Élément d’installation**</span><span class="sxs-lookup"><span data-stu-id="4ac4c-128">**Install Element**</span></span>](install-element.md)
</dt> <dt>

[<span data-ttu-id="4ac4c-129">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="4ac4c-129">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> <dt>

[<span data-ttu-id="4ac4c-130">**Définition de la boutique en ligne initiale**</span><span class="sxs-lookup"><span data-stu-id="4ac4c-130">**Setting the Initial Online Store**</span></span>](setting-the-initial-online-store.md)
</dt> </dl>

 

 




