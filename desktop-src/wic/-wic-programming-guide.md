---
title: Guide de programmation WIC
description: Décrit comment utiliser les API WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393679"
---
# <a name="wic-programming-guide"></a>Guide de programmation WIC

Cette section contient des rubriques conceptuelles qui décrivent comment utiliser les API WIC (Windows Imaging Component).

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                 | Description                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)<br/> | Le WIC fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.<br/>                                                                                                                       |
| [Vue d’ensemble de l’API WIC](-wic-api.md)<br/>                                           | Le WIC fournit une API COM (Component Object Model) à utiliser en C et C++.<br/>                                                                                                                            |
| [Décodage d’images numériques](-wic-decoder-portal.md)<br/>                         | Cette section contient des rubriques conceptuelles et des procédures qui décrivent les décodeurs de bitmap WIC utilisés lors du décodage d’images numériques.<br/>                                                                            |
| [Utilisation des données image](-wic-bitmapsources-portal.md)<br/>                          | Cette section contient des rubriques conceptuelles et des procédures qui décrivent les sources bitmap WIC et comment les manipuler.<br/>                                                                                            |
| [Encodage de données image](encoding-bitmaps-to-digital-images.md)<br/>              | Cette section contient des rubriques conceptuelles et des procédures qui décrivent des encodeurs de bitmap WIC utilisés pour encoder des images numériques.<br/>                                                                              |
| [Codecs WIC natifs](native-wic-codecs.md)<br/>                                 | Cette section contient des informations sur les codecs de création d’images natives disponibles dans WIC.<br/>                                                                                                                        |
| [Traitement des métadonnées de l’image](-wic-metadata-portal.md)<br/>                      | Cette section contient des rubriques conceptuelles qui décrivent le système de métadonnées WIC.<br/>                                                                                                                             |
| [Prise en charge d’JPEG YCbCr](jpeg-ycbcr-support.md)<br/>                               | À partir de Windows 8.1, le codec [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG prend en charge la lecture et l’écriture des données d’image dans son format natif YC<sub>b</sub>C<sub>r</sub> . <br/> |
| [Gestion des couleurs](-wic-colormanagement.md)<br/>                               | WIC simplifie la gestion des couleurs en fournissant l’interface [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) et l’interface [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .<br/>          |
| [Développement de composants](-wic-component-development.md)<br/>                    | Le WIC est une plateforme extensible qui fournit une API de bas niveau pour les images numériques.<br/>                                                                                                                          |



 

## <a name="see-also"></a>Voir aussi

[Référence WIC](-wic-codec-reference.md)


[Exemples WIC](-wic-samples.md)


 

 




