---
title: Création du document ServiceInfo de manière dynamique
description: Création du document ServiceInfo de manière dynamique
ms.assetid: 96937b04-f705-49f6-8ddf-25c98a51dc9a
keywords:
- Windows Media Player Online stores, création d’un document ServiceInfo
- magasins en ligne, créer un document ServiceInfo
- tapez 1 magasins en ligne, création d’un document ServiceInfo
- type 2 magasins en ligne, création d’un document ServiceInfo
- Magasins en ligne du lecteur Windows Media, créer dynamiquement un document ServiceInfo
- magasins en ligne, créer dynamiquement un document ServiceInfo
- tapez 1 magasins en ligne, en créant dynamiquement le document ServiceInfo
- tapez 2 magasins en ligne, en créant dynamiquement le document ServiceInfo
- Windows Media Player Online stores, document ServiceInfo
- magasins en ligne, document ServiceInfo
- type 1 magasins en ligne, document ServiceInfo
- type 2 magasins en ligne, document ServiceInfo
- création dynamique d’un document ServiceInfo
- création du document ServiceInfo
- Document ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90159e72046536cf6b69521586a0640935478eb1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939675"
---
# <a name="creating-the-serviceinfo-document-dynamically"></a><span data-ttu-id="197a3-118">Création du document ServiceInfo de manière dynamique</span><span class="sxs-lookup"><span data-stu-id="197a3-118">Creating the ServiceInfo Document Dynamically</span></span>

<span data-ttu-id="197a3-119">Vous pouvez utiliser ASP pour créer votre document ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="197a3-119">You can use ASP to create your ServiceInfo document.</span></span> <span data-ttu-id="197a3-120">Cela peut vous offrir une plus grande flexibilité dans votre boutique en ligne en utilisant les techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="197a3-120">This can give you greater flexibility in your online store by using the following techniques:</span></span>

-   <span data-ttu-id="197a3-121">Génération dynamique du nom d’hôte pour les URL.</span><span class="sxs-lookup"><span data-stu-id="197a3-121">Dynamically generating the host name for URLs.</span></span>
-   <span data-ttu-id="197a3-122">Modification des URL pour la localisation basée sur les paramètres régionaux et GeoId.</span><span class="sxs-lookup"><span data-stu-id="197a3-122">Changing URLs for localization based on locale and geoid parameters.</span></span>
-   <span data-ttu-id="197a3-123">Ajout dynamique des paramètres de chaîne de requête de l’URL ServiceInfo à d’autres URL, telles que l’URL de la page de navigation.</span><span class="sxs-lookup"><span data-stu-id="197a3-123">Dynamically appending query string parameters from the ServiceInfo URL to other URLs, such as the navigate page URL.</span></span>

<span data-ttu-id="197a3-124">L’exemple de code suivant montre une page ASP simple qui crée dynamiquement un document ServiceInfo :</span><span class="sxs-lookup"><span data-stu-id="197a3-124">The following example code shows a simple ASP page that dynamically creates a ServiceInfo document:</span></span>


```C++
<%
    Dim sHost
    Dim sLocale

    sHost = Request.ServerVariables("HTTP_HOST")
    sLocale = Request.QueryString("locale")
%>

<?xml version="1.0" encoding="utf-8"?>
<ServiceInfo Version="1.00" Key="MyCommerceService">
    <FriendlyName>My Online Store</FriendlyName>
    <ServiceTask1
        URL = "https://<%= sHost %>/service/html/Music.asp">
    </ServiceTask1>
    <ServiceTask2
        URL = "https://<%= sHost %>/service/html/Video.asp">
    </ServiceTask2>
    <ServiceTask3
        URL = "https://<%= sHost %>/service/html/Radio.asp">
    </ServiceTask3>
    <Navigate
        BaseURL = "https://<%= sHost %>/service/html/navigate.asp?myloc<%= sLocale %>">
    </Navigate>
</ServiceInfo>
```



<span data-ttu-id="197a3-125">L’exemple de code précédent utilise ASP pour récupérer le nom d’hôte du serveur Web et créer dynamiquement les URL dans le document.</span><span class="sxs-lookup"><span data-stu-id="197a3-125">The preceding example code uses ASP to retrieve the host name from the web server and dynamically create the URLs in the document.</span></span> <span data-ttu-id="197a3-126">Le code récupère également le paramètre de chaîne de requête *locale* à partir de la demande serviceInfo et l’ajoute à l’URL de la page Navigate.</span><span class="sxs-lookup"><span data-stu-id="197a3-126">The code also retrieves the *locale* query string parameter from the ServiceInfo request and appends it to the URL for the navigate page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="197a3-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="197a3-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="197a3-128">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="197a3-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="197a3-129">**Navigation pour les magasins de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="197a3-129">**Navigation for Type 2 Online Stores**</span></span>](navigation-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="197a3-130">**Document ServiceInfo pour une boutique en ligne de type 1**</span><span class="sxs-lookup"><span data-stu-id="197a3-130">**ServiceInfo Document for a Type 1 Online Store**</span></span>](serviceinfo-document-for-a-type-1-online-store.md)
</dt> <dt>

[<span data-ttu-id="197a3-131">**Document ServiceInfo pour un magasin de type 2 en ligne**</span><span class="sxs-lookup"><span data-stu-id="197a3-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> <dt>

[<span data-ttu-id="197a3-132">**Document ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="197a3-132">**ServiceInfo Document**</span></span>](serviceinfo-document.md)
</dt> </dl>

 

 




