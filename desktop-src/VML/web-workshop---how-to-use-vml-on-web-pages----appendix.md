---
title: Annexe (VML)
description: Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.
ms.assetid: e18e9388-d8b6-4eee-b4f1-3948830f7986
keywords:
- Atelier Web, espaces de noms
- Atelier Web, styles de comportement
- conception de pages Web, espaces de noms
- conception de pages Web, styles de comportement
- Langage VML (VML), espaces de noms
- VML (langage VML), espaces de noms
- graphiques vectoriels, espaces de noms
- Langage VML (VML), styles de comportement
- VML (langage VML), styles de comportement
- graphiques vectoriels, styles de comportement
- VGX.DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d4e7a6a7e44671b7ee835eea263d9ce36a27d8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383680"
---
# <a name="appendix-vml"></a><span data-ttu-id="76b49-114">Annexe (VML)</span><span class="sxs-lookup"><span data-stu-id="76b49-114">Appendix (VML)</span></span>

<span data-ttu-id="76b49-115">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="76b49-115">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="76b49-116">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="76b49-116">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="76b49-117">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="76b49-117">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="76b49-118">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="76b49-118">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="76b49-119">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="76b49-119">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="76b49-120">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="76b49-120">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="76b49-121">Pour permettre aux navigateurs de savoir comment transférer des données vers un processeur VML spécifique, vous devez taper des informations telles que les espaces de noms et les styles de comportement.</span><span class="sxs-lookup"><span data-stu-id="76b49-121">To let the browsers know how to hand off data to a VML-specific processor, you need to type some information such as namespaces and behavior styles.</span></span> <span data-ttu-id="76b49-122">Vous pouvez ensuite utiliser VML pour taper des graphiques dans la `<BODY>` région.</span><span class="sxs-lookup"><span data-stu-id="76b49-122">You can then use VML to type graphics in the `<BODY>` region.</span></span>

<span data-ttu-id="76b49-123">Dans cette rubrique :</span><span class="sxs-lookup"><span data-stu-id="76b49-123">In this topic:</span></span>

-   [<span data-ttu-id="76b49-124">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="76b49-124">Namespaces</span></span>](#namespaces)
-   [<span data-ttu-id="76b49-125">Styles de comportement</span><span class="sxs-lookup"><span data-stu-id="76b49-125">Behavior Styles</span></span>](#behavior-styles)

## <a name="namespaces"></a><span data-ttu-id="76b49-126">Espaces de noms</span><span class="sxs-lookup"><span data-stu-id="76b49-126">Namespaces</span></span>

<span data-ttu-id="76b49-127">Un mécanisme XML indique l’espace de noms à partir duquel un élément provient.</span><span class="sxs-lookup"><span data-stu-id="76b49-127">An XML mechanism indicates the namespace that an element comes from.</span></span> <span data-ttu-id="76b49-128">Si vous passez de l’analyse en HTML à l’analyse en XML, ce mécanisme indique le commutateur dans le code HTML.</span><span class="sxs-lookup"><span data-stu-id="76b49-128">If you switch from parsing in HTML to parsing in XML, this mechanism indicates the switch within HTML.</span></span>

<span data-ttu-id="76b49-129">Demandez à l’distributeur de votre processeur VML quelles informations sont requises pour l’espace de noms XML.</span><span class="sxs-lookup"><span data-stu-id="76b49-129">Ask the vender of your VML processor what information is required for the XML namespace.</span></span>

<span data-ttu-id="76b49-130">Si vous utilisez Microsoft Internet Explorer pour afficher le VML, tapez toujours la ligne suivante dans la `<HTML>` balise :</span><span class="sxs-lookup"><span data-stu-id="76b49-130">If you use Microsoft Internet Explorer to render VML, always type the following line in the `<HTML>` tag:</span></span>


```HTML
<html xmlns:v="urn:schemas-microsoft-com:vml">
```



<span data-ttu-id="76b49-131">Ces informations indiquent à Internet Explorer de basculer vers l’espace de noms « urn : schemas-microsoft-com : VML » lors de l’analyse d’une balise XML avec un préfixe `v:` , et de transmettre les données résultantes au processeur Vml.</span><span class="sxs-lookup"><span data-stu-id="76b49-131">This information tells Internet Explorer to switch to namespace "urn:schemas-microsoft-com:vml" when parsing an XML tag with a prefix `v:`, and to hand off the resulting data to the VML processor.</span></span>

<span data-ttu-id="76b49-132">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="76b49-132">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="behavior-styles"></a><span data-ttu-id="76b49-133">Styles de comportement</span><span class="sxs-lookup"><span data-stu-id="76b49-133">Behavior Styles</span></span>

<span data-ttu-id="76b49-134">VML est défini dans Microsoft Internet Explorer comme un comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="76b49-134">VML is defined in Microsoft Internet Explorer as a default behavior.</span></span>

<span data-ttu-id="76b49-135">Pour afficher le VML, tapez toujours les lignes suivantes dans la `<HEAD>` région :</span><span class="sxs-lookup"><span data-stu-id="76b49-135">To render VML, always type the following lines in the `<HEAD>` region:</span></span>


```HTML
<style>
v\:* { behavior: url(#default#VML); display:inline-block}
</style>
```



<span data-ttu-id="76b49-136">VML est implémenté dans Internet Explorer par le biais de VGX.DLL.</span><span class="sxs-lookup"><span data-stu-id="76b49-136">VML is implemented in Internet Explorer through VGX.DLL.</span></span> <span data-ttu-id="76b49-137">Si votre installation initiale du navigateur n’incluait pas le comportement VML, vous devrez peut-être l’ajouter en tant qu’option.</span><span class="sxs-lookup"><span data-stu-id="76b49-137">If your initial installation of the browser did not include VML behavior, you may need to add it as an option.</span></span> <span data-ttu-id="76b49-138">Vous n’avez pas besoin d’ajouter une `<object>` balise.</span><span class="sxs-lookup"><span data-stu-id="76b49-138">You do not need to add an `<object>` tag.</span></span>

 

 
