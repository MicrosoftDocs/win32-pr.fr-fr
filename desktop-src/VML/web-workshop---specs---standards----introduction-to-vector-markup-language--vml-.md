---
title: Langage VML (VML)
description: Langage VML (VML)
ms.assetid: 1f30d60f-3d4f-43e4-9a2b-424a5ee8f852
keywords:
- Langage VML (VML), à propos de
- VML (langage VML), à propos de
- graphiques vectoriels, à propos de
- graphismes vectoriels, langage VML (VML)
- Langage VML (VML), World Wide Web Consortium (W3C)
- VML (langage VML), World Wide Web Consortium (W3C)
- graphismes vectoriels, World Wide Web Consortium (W3C)
- graphiques vectoriels, avantages VML
- Langage VML (VML), avantages
- VML (langage VML), avantages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0ba51fd041f36915eaafe20201876653f597e04
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/10/2021
ms.locfileid: "106525781"
---
# <a name="vector-markup-language-vml"></a><span data-ttu-id="16ed6-113">Langage VML (VML)</span><span class="sxs-lookup"><span data-stu-id="16ed6-113">Vector Markup Language (VML)</span></span>

<span data-ttu-id="16ed6-114">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="16ed6-114">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="16ed6-115">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="16ed6-115">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!NOTE]
> <span data-ttu-id="16ed6-116">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="16ed6-116">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="16ed6-117">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="16ed6-117">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="16ed6-118">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="16ed6-118">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="16ed6-119">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="16ed6-119">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

<span data-ttu-id="16ed6-120">Langage VML (VML) est un format d’échange, de modification et de remise basé sur XML pour les graphiques vectoriels de haute qualité sur le Web, qui répond aux besoins des utilisateurs de la productivité et des professionnels de la conception graphique.</span><span class="sxs-lookup"><span data-stu-id="16ed6-120">Vector Markup Language (VML) is an XML-based exchange, editing, and delivery format for high-quality vector graphics on the Web that meets the needs of both productivity users and graphic design professionals.</span></span> <span data-ttu-id="16ed6-121">XML est un langage basé sur du texte simple, flexible et ouvert qui complète HTML.</span><span class="sxs-lookup"><span data-stu-id="16ed6-121">XML is an emerging simple, flexible, and open text-based language that complements HTML.</span></span> <span data-ttu-id="16ed6-122">(Consultez la [section XML](/documentation/?frame=true) de MSDN Library pour obtenir des informations détaillées sur XML.)</span><span class="sxs-lookup"><span data-stu-id="16ed6-122">(See the [XML section](/documentation/?frame=true) of the MSDN Library for detailed information on XML.)</span></span>

<span data-ttu-id="16ed6-123">VML est actuellement pris en charge par Microsoft Internet Explorer version 5,0 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="16ed6-123">VML is currently supported by Microsoft Internet Explorer version 5.0 or later.</span></span>

<span data-ttu-id="16ed6-124">VML a été proposé au W3C comme standard pour les graphiques vectoriels sur le Web (voir [langage VML (VML)](https://www.w3.org/TR/NOTE-VML)).</span><span class="sxs-lookup"><span data-stu-id="16ed6-124">VML has been proposed to the W3C as a standard for vector graphics on the Web (see [Vector Markup Language (VML)](https://www.w3.org/TR/NOTE-VML)).</span></span> <span data-ttu-id="16ed6-125">Microsoft continue à s’engager dans le développement et l’implémentation de technologies basées sur XML, en collaboration avec les principaux partenaires de l’industrie (AutoDesk, Hewlett-Packard, Macromedia, Visio) et le W3C pour anticiper les normes basées sur le Web.</span><span class="sxs-lookup"><span data-stu-id="16ed6-125">Microsoft is continuing to lead the charge in the development and implementation of XML-based technologies, working with leading industry partners (AutoDesk, Hewlett-Packard, Macromedia, Visio) and the W3C to advance Web-based standards.</span></span> <span data-ttu-id="16ed6-126">Nous nous attendons à travailler avec le W3C pour atteindre un format standard pour les graphiques vectoriels sur le Web.</span><span class="sxs-lookup"><span data-stu-id="16ed6-126">We expect to work with the W3C to ultimately drive to one standard format for vector graphics on the Web.</span></span>

<span data-ttu-id="16ed6-127">VML est également pris en charge par Microsoft Office 2000 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="16ed6-127">VML is also supported by Microsoft Office 2000 or later.</span></span> <span data-ttu-id="16ed6-128">Microsoft Word, Microsoft Excel et Microsoft PowerPoint peuvent être utilisés pour créer des graphiques VML.</span><span class="sxs-lookup"><span data-stu-id="16ed6-128">Microsoft Word, Microsoft Excel, and Microsoft PowerPoint can be used to create VML graphics.</span></span>

### <a name="using-vml"></a><span data-ttu-id="16ed6-129">Utilisation de VML</span><span class="sxs-lookup"><span data-stu-id="16ed6-129">Using VML</span></span>

<span data-ttu-id="16ed6-130">Pour utiliser VML dans vos pages Web, utilisez un élément style pour importer le comportement VML, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="16ed6-130">To use VML in your web pages, use a style element to import the VML behavior, as shown in the following code.</span></span>

```
<style>v\: * { behavior:url(#default#VML); display:inline-block }</style>
```

<span data-ttu-id="16ed6-131">Ensuite, déclarez l’espace de noms VML, comme indiqué dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="16ed6-131">Next, declare the VML namespace, as shown in the following code sample.</span></span>

```
<xml:namespace ns="urn:schemas-microsoft-com:vml" prefix="v" />
```

<span data-ttu-id="16ed6-132">Enfin, ajoutez des éléments VML pour définir des effets visuels.</span><span class="sxs-lookup"><span data-stu-id="16ed6-132">Finally, add VML elements to define visuals effects.</span></span> <span data-ttu-id="16ed6-133">Par exemple, le code VML suivant crée un ovale rouge.</span><span class="sxs-lookup"><span data-stu-id="16ed6-133">For example, the following VML code creates a red oval.</span></span>

```
<v:oval style="width:100pt;height:50pt" fillcolor="red">
</v:oval>
```

> [!NOTE]
> <span data-ttu-id="16ed6-134">Pour de meilleurs résultats lors de l’utilisation de documents en mode strict, assurez-vous que le balisage est valide et bien formé.</span><span class="sxs-lookup"><span data-stu-id="16ed6-134">For best results when using strict mode documents, be sure that your markup is valid and well-formed.</span></span> <span data-ttu-id="16ed6-135">Pour plus d’informations, consultez le. Page de référence DOCTYPE.</span><span class="sxs-lookup"><span data-stu-id="16ed6-135">For more information, please see the !DOCTYPE reference page.</span></span>


### <a name="benefits-of-vml"></a><span data-ttu-id="16ed6-136">Avantages du VML</span><span class="sxs-lookup"><span data-stu-id="16ed6-136">Benefits of VML</span></span>

-   <span data-ttu-id="16ed6-137">VML facilite la création pour les utilisateurs et les auteurs de productivité.</span><span class="sxs-lookup"><span data-stu-id="16ed6-137">VML makes authoring easier for productivity users and authors.</span></span> <span data-ttu-id="16ed6-138">Il facilite l’échange (par couper-coller) et la modification ultérieure des graphiques vectoriels entre une grande variété d’applications de conception et de productivité.</span><span class="sxs-lookup"><span data-stu-id="16ed6-138">It facilitates the exchange (via cut and paste) and subsequent editing of vector graphics between a wide variety of productivity and design applications.</span></span>
-   <span data-ttu-id="16ed6-139">VML offre des téléchargements de graphiques plus rapides et une meilleure expérience utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16ed6-139">VML provides faster graphic downloads and a better user experience.</span></span> <span data-ttu-id="16ed6-140">Il permet de fournir des graphiques vectoriels de grande qualité, entièrement intégrés et évolutifs au Web, dans un format texte ouvert.</span><span class="sxs-lookup"><span data-stu-id="16ed6-140">It allows the delivery of high-quality, fully integrated, scalable vector graphics to the Web, in an open text-based format.</span></span> <span data-ttu-id="16ed6-141">Plutôt que de référencer des graphiques en tant que fichiers externes, les graphiques VML sont remis en ligne avec la page HTML, ce qui leur permet d’interagir et de s’adapter à l’interaction de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="16ed6-141">Rather than referencing graphics as external files, VML graphics are delivered inline with the HTML page, allowing them to interact and scale with user interaction.</span></span>
-   <span data-ttu-id="16ed6-142">VML est ouvert et basé sur des normes.</span><span class="sxs-lookup"><span data-stu-id="16ed6-142">VML is open and standards-based.</span></span> <span data-ttu-id="16ed6-143">Il s’agit d’un format XML.</span><span class="sxs-lookup"><span data-stu-id="16ed6-143">It is an XML-based format.</span></span> <span data-ttu-id="16ed6-144">XML 1,0 est un langage textuel, simple et ouvert pour la description des données structurées sur le Web, qui complète le HTML en vue de son affichage.</span><span class="sxs-lookup"><span data-stu-id="16ed6-144">XML 1.0 is an open, simple, text-based language for describing structured data on the Web, and complements HTML for display.</span></span> <span data-ttu-id="16ed6-145">VML prend également en charge d’autres normes W3C, telles que feuilles de style en cascade 2,0 (CSS), qui spécifient les informations de style et le positionnement 2D, ainsi que le Document Object Model (DOM), qui permet aux développeurs d’interagir de manière cohérente avec les éléments de page en tant qu’objets.</span><span class="sxs-lookup"><span data-stu-id="16ed6-145">VML also supports other W3C standards, such as Cascading Style Sheets 2.0 (CSS), which specifies style information and 2-D positioning, as well as the Document Object Model (DOM), which allows developers to interact consistently with page elements as objects.</span></span>

### <a name="for-additional-information"></a><span data-ttu-id="16ed6-146">Pour plus d’informations</span><span class="sxs-lookup"><span data-stu-id="16ed6-146">For additional information</span></span>

<span data-ttu-id="16ed6-147">Consultez les liens ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="16ed6-147">See the links below:</span></span>

-   <span data-ttu-id="16ed6-148">Pour obtenir des réponses aux questions fréquemment posées sur VML, consultez le [FAQ VML](frequently-asked-questions-about-vml.md).</span><span class="sxs-lookup"><span data-stu-id="16ed6-148">For answers to frequently asked questions about VML, see the [VML FAQ](frequently-asked-questions-about-vml.md).</span></span>
-   <span data-ttu-id="16ed6-149">Pour obtenir un didacticiel sur l’utilisation de VML sur les pages Web, consultez [comment utiliser VML sur des pages Web](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), qui complète la [spécification VML](https://www.w3.org/TR/NOTE-datetime.html) soumise au W3C.</span><span class="sxs-lookup"><span data-stu-id="16ed6-149">For a tutorial on using VML on Web pages, see [How to Use VML on Web Pages](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md), which complements the [VML specification](https://www.w3.org/TR/NOTE-datetime.html) submitted to the W3C.</span></span>
-   <span data-ttu-id="16ed6-150">Pour plus d’informations sur les types de données VML, consultez le document [types VML de base](basic-vml-types.md) .</span><span class="sxs-lookup"><span data-stu-id="16ed6-150">For information on VML data types, see the [Basic VML Types](basic-vml-types.md) document.</span></span>
-   <span data-ttu-id="16ed6-151">Pour obtenir une référence complète sur VML, y compris des informations sur l’utilisation de VML avec les balises et les scripts, consultez la [référence VML](msdn-online-vml-introduction.md).</span><span class="sxs-lookup"><span data-stu-id="16ed6-151">For the complete reference on VML, including information on how to use VML with tags as well as scripting, see the [VML Reference](msdn-online-vml-introduction.md).</span></span>