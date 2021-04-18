---
title: Co-Branding des magasins en ligne
description: Co-Branding des magasins en ligne
ms.assetid: b564845a-a4e0-4fe6-90cb-63ef320c7e52
keywords:
- Windows Media Player Online stores, co-personnalisation
- magasins en ligne, co-personnalisation
- tapez 1 magasins en ligne, co-personnalisation
- tapez 2 magasins en ligne, co-personnalisation
- Co-personnalisation des magasins en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cae110d3ed04e864f1b617cb4fd6fcdee3b1f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512045"
---
# <a name="co-branding-online-stores"></a><span data-ttu-id="29c6a-108">Co-Branding des magasins en ligne</span><span class="sxs-lookup"><span data-stu-id="29c6a-108">Co-Branding Online Stores</span></span>

<span data-ttu-id="29c6a-109">Les fabricants d’ordinateurs personnels qui ne fonctionnent pas avec un magasin de musique peuvent cohabiter avec les fournisseurs de magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="29c6a-109">Personal computer OEMs who do not operate a music store can co-brand with online store providers.</span></span> <span data-ttu-id="29c6a-110">Le programme d’installation du lecteur Windows Media prend en charge le paramètre de ligne de commande ServiceExtra pour permettre aux OEM de matériel de définir un attribut personnalisé que le magasin en ligne peut utiliser pour identifier le fabricant OEM qui a installé le magasin en ligne initial.</span><span class="sxs-lookup"><span data-stu-id="29c6a-110">Windows Media Player setup supports the ServiceExtra command line parameter to enable hardware OEMs to set a custom attribute that the online store can use to identify which OEM installed the initial online store.</span></span>

<span data-ttu-id="29c6a-111">Par exemple, si un créateur d’ordinateur nommé Fabrikam souhaite définir le magasin en ligne initial sur le magasin de musique Proseware, il peut utiliser la ligne de commande suivante pour installer le lecteur Windows Media 10 :</span><span class="sxs-lookup"><span data-stu-id="29c6a-111">For example, if a computer maker named Fabrikam wants to set the initial online store to the Proseware music store, it might use the following command line to install Windows Media Player 10:</span></span>


```C++
MP10Setup.exe /q:A /c:"setup_wm.exe /Q /R:N /DefaultService:Proseware /ServiceInfo:c:\Proseware\service_info_local.xml /ServiceExtra:OEM=Fabrikam"
```



<span data-ttu-id="29c6a-112">Lorsque le lecteur Windows Media est installé de cette manière, le lecteur ajoute la chaîne ServiceExtra chaque fois qu’il ouvre le service proseware.</span><span class="sxs-lookup"><span data-stu-id="29c6a-112">When Windows Media Player is installed in this manner, the Player appends the ServiceExtra string each time it opens the Proseware service.</span></span> <span data-ttu-id="29c6a-113">L’exemple suivant montre l’URL que le lecteur Windows Media envoie au service Proseware pour récupérer le document ServiceInfo :</span><span class="sxs-lookup"><span data-stu-id="29c6a-113">The following example shows the URL that Windows Media Player would send to the Proseware service to retrieve the ServiceInfo document:</span></span>


```C++
https://www.proseware.com/XML/serviceinfo.asp?OEM=Fabrikam
```



<span data-ttu-id="29c6a-114">Le magasin en ligne Proseware peut ensuite utiliser la chaîne de requête pour déterminer quel OEM a installé le lecteur Windows Media et retourner un document ServiceInfo généré dynamiquement qui pointe vers la version comarquée du magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="29c6a-114">The Proseware online store can then use the query string to determine which OEM installed Windows Media Player and return a dynamically generated ServiceInfo document that points to the co-branded version of the online store.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29c6a-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="29c6a-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29c6a-116">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="29c6a-116">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="29c6a-117">**Paramètres de ligne de commande d’installation pour les magasins en ligne**</span><span class="sxs-lookup"><span data-stu-id="29c6a-117">**Setup Command-line Parameters for Online Stores**</span></span>](setup-command-line-parameters-for-online-stores.md)
</dt> </dl>

 

 




