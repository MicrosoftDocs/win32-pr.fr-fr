---
title: Forum aux questions sur VML
description: Forum aux questions sur VML
ms.assetid: f7f2ce12-facf-4042-b2a7-acaa3e25816a
keywords:
- Langage VML (VML), FAQ
- VML (langage VML), FAQ
- graphiques vectoriels, FAQ
- Langage VML (VML), Forum aux questions
- VML (langage VML), Forum aux questions
- graphiques vectoriels, Forum aux questions
- Langage VML (VML), différences GIF
- VML (langage VML), différences GIF
- Langage VML (VML), différences PNG
- VML (langage VML), différences PNG
- graphiques vectoriels, différences au format raster
- Langage VML (VML), XML
- VML (langage VML), XML
- graphiques vectoriels, XML
- Langage VML (VML), animation
- VML (langage VML), animation
- graphiques vectoriels, animation
- Langage VML (VML), Macromedia Flash
- VML (langage VML), Macromedia Flash
- graphiques vectoriels, Macromedia Flash
- formats raster
- animation
- Macromedia Flash
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e108f2055e7a0fbae1c5ed542fe68c59ec9b212b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941205"
---
# <a name="frequently-asked-questions-about-vml"></a><span data-ttu-id="fb922-126">Forum aux questions sur VML</span><span class="sxs-lookup"><span data-stu-id="fb922-126">Frequently Asked Questions About VML</span></span>

<span data-ttu-id="fb922-127">Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="fb922-127">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="fb922-128">Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.</span><span class="sxs-lookup"><span data-stu-id="fb922-128">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="fb922-129">Depuis le 2011 décembre, cette rubrique a été archivée.</span><span class="sxs-lookup"><span data-stu-id="fb922-129">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="fb922-130">Par conséquent, il n’est plus activement conservé.</span><span class="sxs-lookup"><span data-stu-id="fb922-130">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="fb922-131">Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="fb922-131">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="fb922-132">Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="fb922-132">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

## <a name="does-vml-compete-with-gif-and-png"></a><span data-ttu-id="fb922-133">VML est-il compétitif avec GIF et PNG ?</span><span class="sxs-lookup"><span data-stu-id="fb922-133">Does VML compete with GIF and PNG?</span></span>

<span data-ttu-id="fb922-134">Non.</span><span class="sxs-lookup"><span data-stu-id="fb922-134">No.</span></span> <span data-ttu-id="fb922-135">GIF et PNG sont des formats raster (ou mappés en bits) qui peuvent être utilisés pour stocker des graphiques vectoriels.</span><span class="sxs-lookup"><span data-stu-id="fb922-135">Both GIF and PNG are raster (or bit-mapped) formats that can be used to store vector graphics.</span></span> <span data-ttu-id="fb922-136">Les formats raster stockent tous les pixels, tandis que les formats vectoriels tels que VML utilisent des descriptions ou des contours mathématiques pour décrire les graphiques.</span><span class="sxs-lookup"><span data-stu-id="fb922-136">Raster formats store every pixel, whereas vector formats such as VML use mathematical descriptions or outlines to describe the graphics.</span></span> <span data-ttu-id="fb922-137">Les graphiques vectoriels stockés dans un format vectoriel sont plus compacts que ceux stockés dans les formats raster, ce qui accélère les temps de téléchargement pour les utilisateurs Web.</span><span class="sxs-lookup"><span data-stu-id="fb922-137">Vector graphics stored in a vector-based format are more compact than those stored in raster formats, resulting in faster download times for Web users.</span></span>

<span data-ttu-id="fb922-138">En outre, les graphiques VML sont remis en ligne à la page HTML au lieu de s’appuyer sur des fichiers externes, comme c’est le cas avec GIF et PNG aujourd’hui.</span><span class="sxs-lookup"><span data-stu-id="fb922-138">In addition, VML graphics are delivered inline to the HTML page rather than relying on external files, as is the case with GIF and PNG today.</span></span> <span data-ttu-id="fb922-139">Cela permet aux graphiques VML de mettre à l’échelle et d’interagir avec d’autres éléments de page Web lorsque la page est redimensionnée, ce qui améliore l’expérience de l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="fb922-139">This allows VML graphics to scale and interact with other Web page elements as the page is resized, thus improving the end-user experience.</span></span>

<span data-ttu-id="fb922-140">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fb922-140">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a><span data-ttu-id="fb922-141">Pourquoi Microsoft prend-il en charge une autre norme XML lorsque le XML n’est pas utilisé et est-il assez jeune ?</span><span class="sxs-lookup"><span data-stu-id="fb922-141">Why is Microsoft supporting another XML-based standard when XML is hardly in use and is young enough as it is?</span></span>

<span data-ttu-id="fb922-142">XML est un moyen puissant et simple de représenter des données structurées sur le Web, et complète le HTML pour l’affichage.</span><span class="sxs-lookup"><span data-stu-id="fb922-142">XML is a powerful yet simple way to represent structured data on the Web, and fully complements HTML for display.</span></span> <span data-ttu-id="fb922-143">VML est un exemple des nombreux formats basés sur XML et spécifiques à l’application qui seront développés et implémentés dans les prochains mois.</span><span class="sxs-lookup"><span data-stu-id="fb922-143">VML is one example of the many application-specific, XML-based formats that will be developed and implemented in the coming months.</span></span> <span data-ttu-id="fb922-144">Par exemple, dans la prochaine version d’Office, VML sera utilisé pour annoter des documents HTML, afin de conserver les informations de mise en forme des graphiques d’art Office entre le format de fichier Office natif et HTML, ce qui permet aux utilisateurs d’Office de basculer en toute transparence entre les deux formats.</span><span class="sxs-lookup"><span data-stu-id="fb922-144">For instance, in the next version of Office, VML will be used to annotate HTML documents -- to preserve formatting information of Office Art graphics between the native Office file format and HTML, thus enabling Office users to switch seamlessly between the two formats.</span></span>

<span data-ttu-id="fb922-145">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fb922-145">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="who-will-support-vml"></a><span data-ttu-id="fb922-146">Qui prend en charge VML ?</span><span class="sxs-lookup"><span data-stu-id="fb922-146">Who will support VML?</span></span>

<span data-ttu-id="fb922-147">Nous pensons que de nombreux fournisseurs prennent en charge VML.</span><span class="sxs-lookup"><span data-stu-id="fb922-147">We expect many vendors to support VML.</span></span> <span data-ttu-id="fb922-148">Par exemple, Autodesk, Hewlett-Packard, Macromedia et VISIO ont promis la prise en charge de VML dans les futures versions de leurs produits.</span><span class="sxs-lookup"><span data-stu-id="fb922-148">For example, Autodesk, Hewlett-Packard, Macromedia, and VISIO have pledged support for VML in future versions of their products.</span></span> <span data-ttu-id="fb922-149">Microsoft a promis la prise en charge de VML dans les futures versions de ses plateformes, telles qu’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="fb922-149">Microsoft has pledged support for VML in future versions of its platforms such as Internet Explorer.</span></span> <span data-ttu-id="fb922-150">En outre, VML sera utilisé dans la prochaine génération d’Office pour permettre l’aller-retour entre le format Office et HTML.</span><span class="sxs-lookup"><span data-stu-id="fb922-150">In addition, VML will be used in the next generation of Office to enable "round-tripping" between the Office format and HTML.</span></span>

<span data-ttu-id="fb922-151">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fb922-151">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-support-animation"></a><span data-ttu-id="fb922-152">VML prend-il en charge l’animation ?</span><span class="sxs-lookup"><span data-stu-id="fb922-152">Does VML support animation?</span></span>

<span data-ttu-id="fb922-153">Non, ce n’est pas le moment.</span><span class="sxs-lookup"><span data-stu-id="fb922-153">No, it currently doesn't.</span></span> <span data-ttu-id="fb922-154">Toutefois, nous travaillons en collaboration avec nos partenaires VML pour ajouter la fonctionnalité d’animation au format VML.</span><span class="sxs-lookup"><span data-stu-id="fb922-154">However, we are working with our VML partners to add animation capability into the VML format.</span></span> <span data-ttu-id="fb922-155">Comme VML est basé sur XML, le jeu de balises peut facilement être étendu pour des fonctionnalités supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="fb922-155">Since VML is based on XML, the tag set can be easily extended for additional functionality.</span></span>

<span data-ttu-id="fb922-156">[![retour au début ](images/top.gif) en haut](#top)</span><span class="sxs-lookup"><span data-stu-id="fb922-156">[![back to top](images/top.gif) Back to top](#top)</span></span>

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a><span data-ttu-id="fb922-157">Le format VML remplace-t-il Macromedia Flash ?</span><span class="sxs-lookup"><span data-stu-id="fb922-157">Does VML replace Macromedia Flash?</span></span> <span data-ttu-id="fb922-158">N’est-ce pas que Macromedia envoie simplement son format Flash pour les graphiques vectoriels au W3C ?</span><span class="sxs-lookup"><span data-stu-id="fb922-158">Didn't Macromedia just submit their Flash format for vector graphics to the W3C?</span></span>

<span data-ttu-id="fb922-159">Non.</span><span class="sxs-lookup"><span data-stu-id="fb922-159">No.</span></span> <span data-ttu-id="fb922-160">VML est un format de remise et d’échange textuel pour les graphiques vectoriels, tandis que Flash est un format binaire pour la remise de graphiques et d’animations vectoriels.</span><span class="sxs-lookup"><span data-stu-id="fb922-160">VML is a text-based interchange and delivery format for vector graphics, whereas Flash is a binary format for the delivery of vector-based graphics and animation.</span></span>

<span data-ttu-id="fb922-161">Macromedia n’a pas envoyé son format de fichier au W3C.</span><span class="sxs-lookup"><span data-stu-id="fb922-161">Macromedia did not submit their file format to the W3C.</span></span> <span data-ttu-id="fb922-162">Toutefois, ils ont ouvert leur format de fichier pour les développeurs d’applications, les développeurs Web et les utilisateurs finaux.</span><span class="sxs-lookup"><span data-stu-id="fb922-162">However, they did open their file format up for application developers, Web developers and end users.</span></span> <span data-ttu-id="fb922-163">Consultez la rubrique <https://www.macromedia.com> (éventuellement en anglais) pour plus d'informations.</span><span class="sxs-lookup"><span data-stu-id="fb922-163">See <https://www.macromedia.com> for more information.</span></span>

[<span data-ttu-id="fb922-164">Retour à la vue d’ensemble du VML</span><span class="sxs-lookup"><span data-stu-id="fb922-164">Back to the VML overview</span></span>](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 