---
description: le composant WIC (Windows imaging Component) est une plateforme extensible pour l’imagerie numérique sur les systèmes d’exploitation Windows Vista et Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Introduction (écriture d’un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127530253"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a>Introduction (écriture d’un codec WIC-Enabled)

le composant WIC (Windows imaging Component) est une plateforme extensible pour l’imagerie numérique sur les systèmes d’exploitation Windows Vista et Windows 7. WIC est également disponible sur Windows XP et Windows Server 2003, dans le cadre de Microsoft .NET Framework 3,0 ou en tant que composant distinct que vous pouvez redistribuer. Toute application utilisant le WIC peut accéder à des images, les afficher, les traiter et les imprimer dans n’importe quel format d’image qui fournit un codec WIC, à l’aide d’un ensemble unique d’interfaces cohérentes qui éliminent la nécessité d’une connaissance spécialisée de formats spécifiques.

l’explorateur Windows vista, Windows galerie de photos vista, la galerie de photos en direct et la visionneuse de photos Windows 7 sont basés sur WIC. après l’installation d’un codec WIC activé sur un système Windows Vista ou Windows 7, le système d’exploitation offre le même niveau de prise en charge pour le format d’image associé que pour les formats d’image standard fournis avec la plateforme. Étant donné que vous écrivez le codec pour votre propre format d’image, vous pouvez garantir une qualité cohérente partout où votre format d’image est utilisé et vous bénéficiez des avantages de la prise en charge complète des plateformes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[fonctionnement du composant de création d’images Windows](-wic-howwicworks.md)
</dt> <dt>

Comment écrire un CODEC WIC-Enabled
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



