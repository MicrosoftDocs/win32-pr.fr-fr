---
title: utilisation de HTML avec Lecteur Windows Media
description: utilisation de HTML avec Lecteur Windows Media
ms.assetid: 321d4396-511b-4f0d-9ee9-8bdddceedc0e
keywords:
- Lecteur Windows Media, HTML
- modèle objet Lecteur Windows Media, HTML
- modèle objet, HTML
- contrôle ActiveX Lecteur Windows Media, HTML pour le modèle objet
- contrôle ActiveX, HTML pour le modèle objet
- Lecteur Windows Media contrôle Mobile ActiveX, HTML pour le modèle objet
- Lecteur Windows Media Mobile, HTML pour le modèle objet
- HTML avec Lecteur Windows Media
- Incorporation de pages Web, HTML
- incorporation, pages Web
- commandes de script
- Retournement d’URL
- diffusion multimédia enrichie
- prise en charge d'un navigateur
- affichage des pages Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7cd96932573802d0a75f95a437b2c7284b3de44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324265"
---
# <a name="using-html-with-windows-media-player"></a>utilisation de HTML avec Lecteur Windows Media

## <a name="overview"></a>Vue d’ensemble

l’utilisation de HTML avec Lecteur Windows Media est un excellent moyen de combiner des fichiers audio et vidéo avec du texte et des graphiques. vous pouvez incorporer le contrôle Lecteur Windows Media dans une page web lorsque vous souhaitez compléter votre contenu statique ou créer des applications Web avec des médias numériques. si vous souhaitez compléter vos fichiers multimédias numériques à l’aide de HTML, vous pouvez, en revanche, afficher les pages web en mode complet du lecteur en les référençant dans Windows les sélections de métafichiers media.

si vous écrivez des programmes personnalisés qui incorporent le contrôle Lecteur Windows Media en mode distant, vous pouvez également contrôler les pages web affichées dans les différents volets du mode complet du lecteur lorsque vos utilisateurs détachent le contrôle. Cela vous permet de préserver la continuité entre les États ancrés et non ancrés.

## <a name="web-embedding"></a>Incorporation de sites Web

vous pouvez utiliser le contrôle Lecteur Windows Media dans le cadre d’une page web que vous créez. consultez [incorporation du contrôle Lecteur Windows Media dans une Page Web](embedding-the-windows-media-player-control-in-a-web-page.md).

## <a name="script-commands-and-url-flipping"></a>Commandes de script et retournement d’URL

Les commandes de script sont des paires texte/valeur que vous pouvez incorporer dans vos fichiers multimédias numériques ou vos flux. vous pouvez utiliser des commandes de script personnalisées uniquement pour déclencher le code de script, tout en laissant Lecteur Windows Media gérer automatiquement d’autres commandes de script.

si vous disposez de plusieurs pages web qui accompagnent une présentation multimédia numérique, les commandes de script d’URL peuvent automatiquement modifier la page dans une trame pendant que le contrôle de Lecteur Windows Media continue de reproduire des médias numériques dans une autre image. C’est ce que l’on appelle le basculement d’URL et est un excellent moyen de créer un diaporama multimédia. d’autres commandes de script gérées automatiquement vous permettent de basculer la lecture vers un fichier ou un flux de média différent, d’afficher du texte de sous-titrage ou de déclencher des événements tels que des insertions de publicités définies dans une sélection de métafichier multimédia Windows.

Pour plus d’informations sur le basculement d’URL, consultez [création de présentations Web-Based](creating-web-based-presentations.md).

## <a name="rich-media-streaming"></a>Diffusion multimédia enrichie

Le basculement d’URL fonctionne mieux avec les pages simples qui sont chargées rapidement. Avec des pages plus complexes, plusieurs composants sont transférés individuellement, ce qui complique la synchronisation de l’affichage des pages avec des médias numériques. Pour permettre des présentations multimédias complexes, des pages Web peuvent être ajoutées à un flux multimédia et transmises au lecteur de la même façon que des données audio et vidéo. Cela vous permet de synchroniser les composants de votre présentation beaucoup plus facilement, en particulier sur les connexions à faible vitesse.

Pour plus d’informations sur la diffusion multimédia en continu, consultez [création de présentations Web-Based](creating-web-based-presentations.md).

## <a name="browser-support"></a>Prise en charge des navigateurs

vous pouvez incorporer le contrôle Lecteur Windows Media dans Microsoft Internet Explorer, Firefox et Netscape Navigator, bien que le processus soit légèrement différent pour chacun. Vous pouvez également créer des pages Web conçues pour fonctionner avec les trois navigateurs.

Avec Internet Explorer et Firefox, vous incorporez le contrôle à l’aide de l’élément objet HTML. le navigateur requiert toutefois une approche différente, car il ne prend pas directement en charge les contrôles ActiveX. Avec Navigator, vous utilisez l’élément APPLET pour incorporer une applet Java spéciale dans la page. cette applet gère la communication avec le contrôle ActiveX du lecteur.

pour plus d’informations sur la prise en charge de firefox, consultez [utilisation du contrôle de Lecteur Windows Media avec firefox](using-the-windows-media-player-control-with-firefox.md).

pour plus d’informations sur la prise en charge de netscape Navigator, consultez [utilisation de Lecteur Windows Media avec netscape 7,1](using-windows-media-player-with-netscape-7-1.md).

## <a name="displaying-web-pages-in-the-full-mode-of-the-player"></a>Affichage des pages Web en mode complet du lecteur

vous pouvez étendre les fonctionnalités de Lecteur Windows Media ou fournir une vue personnalisée des informations qui accompagnent vos médias numériques en affichant des pages web en mode complet du lecteur. il s’agit de la fonctionnalité HTMLView de Windows les fichiers multimédias. les fichiers de données vous offrent un contrôle parfait sur le contenu de la sélection, ce qui vous permet de passer en toute transparence entre les clips, d’insérer des publications et d’afficher des images fixes dans Lecteur Windows Media. Pour afficher les pages Web en mode complet du lecteur, vous utilisez l’élément PARAM pour ajouter des références d’URL à vos entrées de playlist ou à des sélections entières.

pour plus d’informations sur l’utilisation des pages Web dans les fichiers de pagination, consultez [affichage des Pages Web dans les Lecteur Windows Media](displaying-web-pages-in-windows-media-player.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos du modèle objet Player**](about-the-player-object-model.md)
</dt> </dl>

 

 




