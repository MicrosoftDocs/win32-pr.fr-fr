---
description: Prise en charge de MPEG-2 dans DirectShow
ms.assetid: a4fe4cc9-86a5-4c83-94be-8901b97c8280
title: Prise en charge de MPEG-2 dans DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9feaa24ea36b6f5e00e0f6ecd5db49ce37181f9d6d7348b3cfa27e64f7f2d84
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075799"
---
# <a name="mpeg-2-support-in-directshow"></a>Prise en charge de MPEG-2 dans DirectShow

Cette section décrit les composants que vous pouvez utiliser pour lire du contenu MPEG-2 dans DirectShow.

> [!Note]  
> Bien que la vidéo DVD soit basée sur MPEG-2, cette section ne décrit pas la lecture ou la navigation sur DVD. pour plus d’informations sur les dvd dans DirectShow, consultez [Applications dvd](dvd-applications.md).

 

Les données MPEG-2 peuvent provenir d’un fichier local ou d’une source Live, telle qu’une diffusion réseau ou un appareil D-VHS. La lecture de fichier est appelée *mode par extraction* , car le filtre de l’analyseur extrait les données du fichier dans le graphique de filtre. Les sources en direct sont appelées *mode Push* , car le filtre source pousse les données dans le graphique.

DirectShow fournit deux filtres qui peuvent analyser les flux système MPEG-2 :

-   [Démultiplexeur MPEG-2](mpeg-2-demultiplexer.md) (« demux ») : ce filtre prend en charge le mode Push pour les flux de programme et les flux de transport. dans Windows XP et versions ultérieures, il prend également en charge le mode par extraction pour les flux de programme.
-   [Séparateur MPEG-2](mpeg-2-splitter.md): ce filtre prend en charge le mode par extraction pour les flux de programme sur les plateformes de niveau inférieur. ce filtre est déconseillé dans Windows XP et versions ultérieures.

pour utiliser le séparateur mpeg-2 demux ou mpeg-2, vous devez disposer de décodeurs audio et vidéo mpeg-2 compatibles DirectShow qui acceptent les flux élémentaires (PES) paquets.

Cette section contient les rubriques suivantes :

-   [Vue d’ensemble des systèmes MPEG-2](overview-of-mpeg-2-systems.md)
-   [Utilisation du démultiplexeur MPEG-2](using-the-mpeg-2-demultiplexer.md)
-   [Utilisation du séparateur MPEG-2](using-the-mpeg-2-splitter.md)
-   [Exemples de propriétés MPEG](mpeg-sample-properties.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de filtre de l’analyseur PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 



