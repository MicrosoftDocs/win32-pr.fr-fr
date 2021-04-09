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
# <a name="frequently-asked-questions-about-vml"></a>Forum aux questions sur VML

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

## <a name="does-vml-compete-with-gif-and-png"></a>VML est-il compétitif avec GIF et PNG ?

Non. GIF et PNG sont des formats raster (ou mappés en bits) qui peuvent être utilisés pour stocker des graphiques vectoriels. Les formats raster stockent tous les pixels, tandis que les formats vectoriels tels que VML utilisent des descriptions ou des contours mathématiques pour décrire les graphiques. Les graphiques vectoriels stockés dans un format vectoriel sont plus compacts que ceux stockés dans les formats raster, ce qui accélère les temps de téléchargement pour les utilisateurs Web.

En outre, les graphiques VML sont remis en ligne à la page HTML au lieu de s’appuyer sur des fichiers externes, comme c’est le cas avec GIF et PNG aujourd’hui. Cela permet aux graphiques VML de mettre à l’échelle et d’interagir avec d’autres éléments de page Web lorsque la page est redimensionnée, ce qui améliore l’expérience de l’utilisateur final.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="why-is-microsoft-supporting-another-xml-based-standard-when-xml-is-hardly-in-use-and-is-young-enough-as-it-is"></a>Pourquoi Microsoft prend-il en charge une autre norme XML lorsque le XML n’est pas utilisé et est-il assez jeune ?

XML est un moyen puissant et simple de représenter des données structurées sur le Web, et complète le HTML pour l’affichage. VML est un exemple des nombreux formats basés sur XML et spécifiques à l’application qui seront développés et implémentés dans les prochains mois. Par exemple, dans la prochaine version d’Office, VML sera utilisé pour annoter des documents HTML, afin de conserver les informations de mise en forme des graphiques d’art Office entre le format de fichier Office natif et HTML, ce qui permet aux utilisateurs d’Office de basculer en toute transparence entre les deux formats.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="who-will-support-vml"></a>Qui prend en charge VML ?

Nous pensons que de nombreux fournisseurs prennent en charge VML. Par exemple, Autodesk, Hewlett-Packard, Macromedia et VISIO ont promis la prise en charge de VML dans les futures versions de leurs produits. Microsoft a promis la prise en charge de VML dans les futures versions de ses plateformes, telles qu’Internet Explorer. En outre, VML sera utilisé dans la prochaine génération d’Office pour permettre l’aller-retour entre le format Office et HTML.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="does-vml-support-animation"></a>VML prend-il en charge l’animation ?

Non, ce n’est pas le moment. Toutefois, nous travaillons en collaboration avec nos partenaires VML pour ajouter la fonctionnalité d’animation au format VML. Comme VML est basé sur XML, le jeu de balises peut facilement être étendu pour des fonctionnalités supplémentaires.

[![retour au début ](images/top.gif) en haut](#top)

## <a name="does-vml-replace-macromedia-flash-didnt-macromedia-just-submit-their-flash-format-for-vector-graphics-to-the-w3c"></a>Le format VML remplace-t-il Macromedia Flash ? N’est-ce pas que Macromedia envoie simplement son format Flash pour les graphiques vectoriels au W3C ?

Non. VML est un format de remise et d’échange textuel pour les graphiques vectoriels, tandis que Flash est un format binaire pour la remise de graphiques et d’animations vectoriels.

Macromedia n’a pas envoyé son format de fichier au W3C. Toutefois, ils ont ouvert leur format de fichier pour les développeurs d’applications, les développeurs Web et les utilisateurs finaux. Consultez la rubrique <https://www.macromedia.com> (éventuellement en anglais) pour plus d'informations.

[Retour à la vue d’ensemble du VML](web-workshop---specs---standards----how-to-use-vml-on-web-pages.md)

 

 