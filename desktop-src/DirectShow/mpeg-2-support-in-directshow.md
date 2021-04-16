---
description: Prise en charge MPEG-2 dans DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Prise en charge MPEG-2 dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f42b0d49159a28b3ad29a0141c296c0fd0076fdd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522196"
---
# <a name="mpeg-2-support-in-directshow"></a>Prise en charge MPEG-2 dans DirectShow

Cette section décrit les composants que vous pouvez utiliser pour lire du contenu MPEG-2 dans DirectShow.

> [!Note]  
> Bien que la vidéo DVD soit basée sur MPEG-2, cette section ne décrit pas la lecture ou la navigation sur DVD. Pour plus d’informations sur les DVD dans DirectShow, consultez [applications DVD](dvd-applications.md).

 

Les données MPEG-2 peuvent provenir d’un fichier local ou d’une source Live, telle qu’une diffusion réseau ou un appareil D-VHS. La lecture de fichier est appelée *mode par extraction* , car le filtre de l’analyseur extrait les données du fichier dans le graphique de filtre. Les sources en direct sont appelées *mode Push* , car le filtre source pousse les données dans le graphique.

DirectShow fournit deux filtres qui peuvent analyser les flux système MPEG-2 :

-   [Démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) (« demux ») : ce filtre prend en charge le mode Push pour les flux de programme et les flux de transport. Dans Windows XP et versions ultérieures, il prend également en charge le mode par extraction pour les flux de programme.
-   [Séparateur MPEG-2](mpeg-2-splitter.md): ce filtre prend en charge le mode par extraction pour les flux de programme sur les plateformes de niveau inférieur. Ce filtre est déconseillé dans Windows XP et versions ultérieures.

Pour utiliser le séparateur MPEG-2 demux ou MPEG-2, vous devez disposer de décodeurs vidéo et audio MPEG-2 compatibles DirectShow acceptant les flux élémentaires (PES).

Cette section contient les rubriques suivantes :

-   [Vue d’ensemble des systèmes MPEG-2](overview-of-mpeg-2-systems.md)
-   [Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Utilisation du séparateur MPEG-2](using-the-mpeg-2-splitter.md)
-   [Exemples de propriétés MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



