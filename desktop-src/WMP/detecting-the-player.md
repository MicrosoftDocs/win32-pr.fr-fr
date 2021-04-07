---
title: Détection du lecteur
description: Détection du lecteur
ms.assetid: dc034226-578a-45de-9463-e1798fef874e
keywords:
- Windows Media Player Online stores, détection des joueurs
- magasins en ligne, détection des joueurs
- tapez 1 magasins en ligne, détection des joueurs
- tapez 2 magasins en ligne, détection des joueurs
- Windows Media Player Online stores, détection de lecteur
- magasins en ligne, détection de lecteur
- types 1 magasins en ligne, détection de lecteur
- type 2 magasins en ligne, détection de lecteur
- détection de lecteur
- détection des joueurs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb919e790b07ccf5d8df587abd63d2344534b16b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940041"
---
# <a name="detecting-the-player"></a><span data-ttu-id="9edb8-113">Détection du lecteur</span><span class="sxs-lookup"><span data-stu-id="9edb8-113">Detecting the Player</span></span>

<span data-ttu-id="9edb8-114">Lorsque vous créez une page Web pour votre boutique en ligne, vous pouvez décider que vous souhaitez que les utilisateurs puissent afficher la page dans un navigateur Web ou dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9edb8-114">When creating a webpage for your online store, you may decide that you want users to be able to view the page in a Web browser or in Windows Media Player.</span></span> <span data-ttu-id="9edb8-115">Vous pouvez utiliser un script ASP pour déterminer si votre page Web est hébergée dans le lecteur.</span><span class="sxs-lookup"><span data-stu-id="9edb8-115">You can use an ASP script to determine whether your webpage is hosted in the Player.</span></span>

<span data-ttu-id="9edb8-116">L’exemple de code suivant récupère le paramètre de version de la chaîne de requête d’URL pour déterminer si la page est hébergée dans le lecteur Windows Media :</span><span class="sxs-lookup"><span data-stu-id="9edb8-116">The following example code retrieves the version parameter from the URL query string to determine whether the page is hosted in Windows Media Player:</span></span>


```C++
<%
    Dim sVersion

    sVersion = Trim(Request.QueryString("version")) 
 
    If sVersion = "" Then   
        Response.Write "Not hosted in Windows Media Player"
    Else 
        Response.Write "Hosted in Windows Media Player<BR>"
        Response.Write "Version is " & sVersion
    End If
%>
```



<span data-ttu-id="9edb8-117">Notez que le code précédent suppose que le paramètre de version existe dans la chaîne de requête lorsqu’il est hébergé dans le lecteur Windows Media.</span><span class="sxs-lookup"><span data-stu-id="9edb8-117">Note that the preceding code assumes that the version parameter exists in the query string when hosted in Windows Media Player.</span></span> <span data-ttu-id="9edb8-118">Cela est vrai pour les pages ouvertes par l’utilisateur, mais peut ne pas être vrai pour les pages ouvertes à l’aide de **External. NavigateTaskPaneURL**.</span><span class="sxs-lookup"><span data-stu-id="9edb8-118">This is true for pages opened by the user, but may not be true for pages opened by using **External.NavigateTaskPaneURL**.</span></span> <span data-ttu-id="9edb8-119">Pour que la chaîne de requête de version existe lors de la navigation par programmation, vous devez ajouter le paramètre version à l’appel de méthode ou ajouter dynamiquement la version à l’URL de base de l’élément **Navigate** de votre document serviceInfo.</span><span class="sxs-lookup"><span data-stu-id="9edb8-119">For the version query string to exist when navigating programmatically, you must add the version parameter to the method call or dynamically append the version to the base URL of the **Navigate** element of your ServiceInfo document.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9edb8-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9edb8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9edb8-121">**Création du document ServiceInfo de manière dynamique**</span><span class="sxs-lookup"><span data-stu-id="9edb8-121">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="9edb8-122">**External. NavigateTaskPaneURL**</span><span class="sxs-lookup"><span data-stu-id="9edb8-122">**External.NavigateTaskPaneURL**</span></span>](external-navigatetaskpaneurl.md)
</dt> <dt>

[<span data-ttu-id="9edb8-123">**Informations communes aux magasins en ligne de type 1 et de type 2**</span><span class="sxs-lookup"><span data-stu-id="9edb8-123">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




