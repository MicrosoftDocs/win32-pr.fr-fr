---
title: Document ServiceInfo pour une boutique en ligne de type 1
description: Document ServiceInfo pour une boutique en ligne de type 1
ms.assetid: 9ca424a1-c29a-4078-8d56-9d0fea52f150
keywords:
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d47ce17cf2494a84193116fc340f843934b6f073
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029357"
---
# <a name="serviceinfo-document-for-a-type-1-online-store"></a><span data-ttu-id="fce87-107">Document ServiceInfo pour une boutique en ligne de type 1</span><span class="sxs-lookup"><span data-stu-id="fce87-107">ServiceInfo Document for a Type 1 Online Store</span></span>

<span data-ttu-id="fce87-108">Les magasins en ligne de type 1 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="fce87-108">Type 1 online stores must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="fce87-109">Le lecteur Windows Media 11 utilise ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="fce87-109">Windows Media Player 11 uses this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="fce87-110">Le document ServiceInfo pour un magasin de type 1 fournit les informations suivantes au lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="fce87-110">The ServiceInfo document for a type 1 store provides the following information to Windows Media Player:</span></span>

-   <span data-ttu-id="fce87-111">Informations utilisées pour configurer le bouton **magasins en ligne** (également appelé onglet), tel que le texte du bouton, la couleur du bouton et l’info-bulle pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="fce87-111">Information used to configure the **Online Stores** button (also called a tab), such as the button text, the button color, and the tooltip for the button.</span></span>
-   <span data-ttu-id="fce87-112">URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="fce87-112">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="fce87-113">URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fce87-113">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="fce87-114">URL où le lecteur Windows Media peut récupérer le plug-in de la Banque en ligne afin que le plug-in puisse être installé sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="fce87-114">URL where Windows Media Player can retrieve the online store's plug-in so that the plug-in can be installed on the user's computer.</span></span>

<span data-ttu-id="fce87-115">Lorsque le lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL.</span><span class="sxs-lookup"><span data-stu-id="fce87-115">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="fce87-116">La chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux et l’emplacement géographique de l’utilisateur, ainsi que sur la version du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="fce87-116">The query string contains parameters that provide information about the user's locale and geographic location and the version of Windows Media Player.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fce87-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fce87-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fce87-118">**À propos des magasins en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="fce87-118">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="fce87-119">**Création du document ServiceInfo de manière dynamique**</span><span class="sxs-lookup"><span data-stu-id="fce87-119">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="fce87-120">**Exemple de document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="fce87-120">**Example ServiceInfo Document for a Type 1 Online Store**</span></span>](example-serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="fce87-121">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="fce87-121">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




