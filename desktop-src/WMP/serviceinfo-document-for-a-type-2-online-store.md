---
title: Document ServiceInfo pour un magasin de type 2 en ligne
description: Document ServiceInfo pour un magasin de type 2 en ligne
ms.assetid: ca83e9bf-c7fb-4212-8fa2-1fae11ed26e9
keywords:
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fb558661332ab08edd2057fa024a1a0e2034b9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029355"
---
# <a name="serviceinfo-document-for-a-type-2-online-store"></a><span data-ttu-id="e5a5c-107">Document ServiceInfo pour un magasin de type 2 en ligne</span><span class="sxs-lookup"><span data-stu-id="e5a5c-107">ServiceInfo Document for a Type 2 Online Store</span></span>

<span data-ttu-id="e5a5c-108">Les fournisseurs de magasin en ligne de type 2 doivent fournir à Microsoft l’URL d’un document XML qui décrit le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-108">Type 2 online store providers must provide Microsoft with the URL of an XML document that describes the online store.</span></span> <span data-ttu-id="e5a5c-109">Le lecteur Windows Media 10 et le lecteur Windows Media 11 utilisent ce document pour déterminer comment configurer l’interface utilisateur pour héberger le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-109">Windows Media Player 10 and Windows Media Player 11 use this document to determine how to configure the user interface to host the online store.</span></span>

<span data-ttu-id="e5a5c-110">Dans le lecteur Windows Media 10, le document ServiceInfo fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5a5c-110">In Windows Media Player 10, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="e5a5c-111">Informations sur la configuration des volets de tâches que le lecteur Windows Media affiche lorsque le magasin en ligne est actif.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-111">Information about how to configure the task panes that Windows Media Player displays when the online store is active.</span></span> <span data-ttu-id="e5a5c-112">Un magasin en ligne peut avoir un, deux ou trois volets de tâches.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-112">An online store can have one, two, or three task panes.</span></span>
-   <span data-ttu-id="e5a5c-113">Informations utilisées pour configurer les boutons du volet de tâches, tels que le texte du bouton, la couleur du bouton et des info-bulles pour les boutons.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-113">Information used to configure the task pane buttons, such as the button text, the button color, and tool tips for the buttons.</span></span>
-   <span data-ttu-id="e5a5c-114">URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-114">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="e5a5c-115">URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-115">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>
-   <span data-ttu-id="e5a5c-116">Informations sur la façon dont le programme d’installation du lecteur Windows Media doit configurer la première boutique en ligne visible par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-116">Information about how Windows Media Player setup should configure the first online store the user sees.</span></span>

<span data-ttu-id="e5a5c-117">Dans le lecteur Windows Media 11, le document ServiceInfo fournit les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="e5a5c-117">In Windows Media Player 11, the ServiceInfo document provides the following:</span></span>

-   <span data-ttu-id="e5a5c-118">Informations utilisées pour configurer le bouton de l’onglet magasins en ligne, tels que le texte du bouton et l’info-bulle pour le bouton.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-118">Information used to configure the button for Online Stores tab, such as the button text and the tool tip for the button.</span></span>
-   <span data-ttu-id="e5a5c-119">URL pour les images affichées par le lecteur Windows Media pour identifier le magasin en ligne.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-119">URLs for images that Windows Media Player displays to identify the online store.</span></span>
-   <span data-ttu-id="e5a5c-120">URL des pages Web, fournies par le magasin en ligne, que le lecteur Windows Media héberge dans son interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-120">URLs of webpages, provided by the online store, that Windows Media Player hosts in its user interface.</span></span>

<span data-ttu-id="e5a5c-121">Lorsque vous commencez à développer votre magasin en ligne, vous devez fournir à Microsoft l’URL de votre document ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-121">When you start developing your online store, you must provide Microsoft with the URL to your ServiceInfo document.</span></span> <span data-ttu-id="e5a5c-122">Pendant la phase de développement, votre magasin en ligne s’affiche dans le lecteur Windows Media uniquement lorsqu’une clé de Registre spéciale est définie.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-122">During the development phase, your online store will appear in Windows Media Player only when a special registry key is set.</span></span>

<span data-ttu-id="e5a5c-123">Une fois votre magasin en ligne publié, le scénario ususal est que le lecteur Windows Media récupère automatiquement votre document ServiceInfo à partir du Web.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-123">After your online store is published, the ususal scenario is that Windows Media Player retrieves your ServiceInfo document from the Web automatically.</span></span> <span data-ttu-id="e5a5c-124">Dans certains cas, toutefois, le lecteur Windows Media récupère le document ServiceInfo sur l’ordinateur de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-124">In some cases, however, Windows Media Player retrieves the ServiceInfo document from the user's computer.</span></span> <span data-ttu-id="e5a5c-125">Pour plus d’informations, consultez [définition du magasin en ligne initial](setting-the-initial-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="e5a5c-125">For more information, see [Setting the Initial Online Store](setting-the-initial-online-store.md).</span></span>

<span data-ttu-id="e5a5c-126">Lorsque le lecteur Windows Media récupère le document ServiceInfo à partir du Web, il ajoute une chaîne de requête à l’URL.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-126">When Windows Media Player retrieves the ServiceInfo document from the Web, it appends a query string to the URL.</span></span> <span data-ttu-id="e5a5c-127">La chaîne de requête contient des paramètres qui fournissent des informations sur les paramètres régionaux de l’utilisateur et la version du lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-127">The query string contains parameters that provide information about the user's locale and the Windows Media Player version.</span></span>

<span data-ttu-id="e5a5c-128">Vous pouvez créer des documents ServiceInfo statiques ou dynamiques.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-128">You can create static or dynamic ServiceInfo documents.</span></span> <span data-ttu-id="e5a5c-129">Un document ServiceInfo statique a une extension de nom de fichier. Xml.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-129">A static ServiceInfo document has an .xml file name extension.</span></span> <span data-ttu-id="e5a5c-130">Un document ServiceInfo dynamique est une page ASP dont l’extension de nom de fichier est. asp ou. aspx.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-130">A dynamic ServiceInfo document is an ASP page and has an .asp or .aspx file name extension.</span></span>

<span data-ttu-id="e5a5c-131">Tous les éléments disponibles dans le document ServiceInfo ne peuvent pas être utilisés par chaque magasin en ligne, et certains éléments sont facultatifs pour tous les magasins en ligne.</span><span class="sxs-lookup"><span data-stu-id="e5a5c-131">Not all the elements available for use in the ServiceInfo document can be used by every online store, and some elements are optional for all online stores.</span></span> <span data-ttu-id="e5a5c-132">Pour plus d’informations sur les types de magasins en ligne que vous pouvez créer et les fonctionnalités disponibles pour chaque type, consultez [Windows Media Player Online stores](windows-media-player-online-stores.md).</span><span class="sxs-lookup"><span data-stu-id="e5a5c-132">For information about the types of online stores you can create and the features available for each type, see [Windows Media Player Online Stores](windows-media-player-online-stores.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5a5c-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5a5c-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5a5c-134">**À propos des magasins en ligne de type 2**</span><span class="sxs-lookup"><span data-stu-id="e5a5c-134">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="e5a5c-135">**Création du document ServiceInfo de manière dynamique**</span><span class="sxs-lookup"><span data-stu-id="e5a5c-135">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="e5a5c-136">**Exemple de document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="e5a5c-136">**Example ServiceInfo Document for a Type 2 Online Store**</span></span>](example-serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="e5a5c-137">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="e5a5c-137">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




