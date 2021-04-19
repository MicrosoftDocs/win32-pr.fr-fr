---
description: .
ms.assetid: 254A1C0D-B24B-4014-8D15-662FC7F2AB81
title: Utiliser la balise meta pour garantir la compatibilité future
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e965711053a7108c69295ac737953a05536a76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523720"
---
# <a name="use-the-meta-tag-to-ensure-future-compatibility"></a><span data-ttu-id="7e444-103">Utiliser la balise meta pour garantir la compatibilité future</span><span class="sxs-lookup"><span data-stu-id="7e444-103">Use the Meta Tag to Ensure Future Compatibility</span></span>

<span data-ttu-id="7e444-104">Windows Internet Explorer 8 vous permet de contrôler les modes de compatibilité des documents. vous pouvez donc demander au navigateur de restituer les pages Web de la même façon que les versions antérieures du navigateur.</span><span class="sxs-lookup"><span data-stu-id="7e444-104">Windows Internet Explorer 8 enables you to control document compatibility modes, so you can instruct the browser to render webpages in the same way as older browser versions.</span></span> <span data-ttu-id="7e444-105">Vous pouvez également choisir le moment de la mise à jour de la page Web, tout en continuant à utiliser et à fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="7e444-105">You can also choose when to update the webpage, while it continues to be usable and function correctly.</span></span>

## <a name="setting-the-meta-element"></a><span data-ttu-id="7e444-106">Définition de l’élément meta</span><span class="sxs-lookup"><span data-stu-id="7e444-106">Setting the Meta Element</span></span>

<span data-ttu-id="7e444-107">L’élément **meta** comprend un attribut **content** qui vous permet de spécifier le mode dans lequel le contenu est restitué pour la page Web, comme le montre le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="7e444-107">The **meta** element includes a **content** attribute that enables you to specify the mode that content is rendered in for the webpage, as the following table shows.</span></span>



| <span data-ttu-id="7e444-108">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e444-108">Value</span></span> | <span data-ttu-id="7e444-109">Mode de rendu</span><span class="sxs-lookup"><span data-stu-id="7e444-109">Rendering mode</span></span>                                                 |
|-------|----------------------------------------------------------------|
| <span data-ttu-id="7e444-110">IE = 9</span><span class="sxs-lookup"><span data-stu-id="7e444-110">IE=9</span></span>  | <span data-ttu-id="7e444-111">Utiliser le mode de rendu des normes Windows Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="7e444-111">Use the Windows Internet Explorer 9 standards rendering mode</span></span>   |
| <span data-ttu-id="7e444-112">IE = 8</span><span class="sxs-lookup"><span data-stu-id="7e444-112">IE=8</span></span>  | <span data-ttu-id="7e444-113">Utiliser le mode de rendu des normes d’Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="7e444-113">Use the Internet Explorer 8 standards rendering mode</span></span>           |
| <span data-ttu-id="7e444-114">IE = 7</span><span class="sxs-lookup"><span data-stu-id="7e444-114">IE=7</span></span>  | <span data-ttu-id="7e444-115">Utiliser le mode de rendu des normes Windows Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="7e444-115">Use the Windows Internet Explorer 7 standards rendering mode</span></span>   |
| <span data-ttu-id="7e444-116">IE=5</span><span class="sxs-lookup"><span data-stu-id="7e444-116">IE=5</span></span>  | <span data-ttu-id="7e444-117">Utiliser le mode de rendu des normes de Microsoft Internet Explorer 5</span><span class="sxs-lookup"><span data-stu-id="7e444-117">Use the Microsoft Internet Explorer 5 standards rendering mode</span></span> |



 

<span data-ttu-id="7e444-118">Pour plus d’informations sur la compatibilité et l’en-tête X-UA-compatible, consultez Définition de la [compatibilité des documents](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) dans MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="7e444-118">For more information about compatibility and the X-UA-Compatible header, see [Defining Document Compatibility](/previous-versions/windows/internet-explorer/ie-developer/compatibility/cc288325(v=vs.85)) in the MSDN Library.</span></span>

<span data-ttu-id="7e444-119">L’exemple de code suivant montre comment forcer l’affichage d’une page Web en mode Internet Explorer 8.</span><span class="sxs-lookup"><span data-stu-id="7e444-119">The following code example demonstrates how to force a webpage to be rendered in Internet Explorer 8 mode.</span></span>


```HTML
<html>
   <head>
   <!-- Mimic Internet Explorer 8 -->
      <title>My Web Page</title>
      <meta http-equiv="X-UA-Compatible" content="IE=EmulateIE8" />
   </head>
   <body>
      <p>Content goes here.</p>
   </body>
</html>
```



## <a name="using-an-http-header"></a><span data-ttu-id="7e444-120">Utilisation d’un en-tête HTTP</span><span class="sxs-lookup"><span data-stu-id="7e444-120">Using an HTTP Header</span></span>

<span data-ttu-id="7e444-121">De nombreux sites Web contiennent des milliers (ou des dizaines de milliers) de pages Web individuelles, ce qui signifie que la définition de l’élément **meta** sur chaque document est irréalisable.</span><span class="sxs-lookup"><span data-stu-id="7e444-121">Many websites contain thousands (or tens of thousands) of individual webpages so setting the **meta** element on each document is impractical.</span></span> <span data-ttu-id="7e444-122">Si vous souhaitez définir l’élément **meta** pour toutes les pages ou une collection de pages sélectionnées par dossier, vous pouvez modifier la configuration de votre serveur à la place et ajouter les métadonnées X-UA-Compatible dans l' [en-tête http](/previous-versions/cc817572(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="7e444-122">If you want to set the **meta** element for all pages or a collection of pages that are selected by folder, you can adjust your server configuration instead and add the X-UA-Compatible metadata in the [HTTP header](/previous-versions/cc817572(v=msdn.10)).</span></span>

<span data-ttu-id="7e444-123">Pour les sites qui requièrent différentes valeurs d’élément **méta** pour les pages sur le même serveur, il existe plusieurs outils qui génèrent et insèrent automatiquement l’élément **meta** approprié.</span><span class="sxs-lookup"><span data-stu-id="7e444-123">For sites that require different **meta** element values for pages on the same server, there are several tools that automatically generate and insert the appropriate **meta** element for you.</span></span> <span data-ttu-id="7e444-124">Par exemple, l’utilitaire [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) de Aggiorno insère et supprime la fonctionnalité de balise de compatibilité d’Internet Explorer 8 et peut aider votre site à respecter des normes de compatibilité spécifiques.</span><span class="sxs-lookup"><span data-stu-id="7e444-124">For example, the [ArtinSoft Web Tools](https://www.mobilize.net/what-is-aggiorno-ie8-compatibility-tagging.aspx) utility from Aggiorno inserts and removes the Internet Explorer 8 compatibility tag feature and can help your site meet specific compatibility standards.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e444-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e444-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e444-126">Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité</span><span class="sxs-lookup"><span data-stu-id="7e444-126">Fixing Compatibility Issues in Web Applications by Using Compatibility View</span></span>](remediating-web-applications-with-compatibility-view.md)
</dt> </dl>

 

 
