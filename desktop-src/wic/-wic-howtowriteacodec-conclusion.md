---
description: la création de votre codec sur la plateforme wic (Windows Imaging Component) permet à toutes les applications basées sur wic d’obtenir la même prise en charge de plateforme pour le format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusion (écriture d’un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5288438ea518e1776562b288184067df6d82c326eb6786b163f20e90c6febc05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118205820"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusion (écriture d’un codec WIC-Enabled)

la création de votre codec sur la plateforme wic (Windows Imaging Component) permet à toutes les applications basées sur wic d’obtenir la même prise en charge de plateforme pour le format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme. il permet également à la galerie de photos Windows Vista, à l’explorateur de Windows et à la visionneuse de photos d’afficher des miniatures et des aperçus d’images dans votre format à l’aide du décodeur que vous fournissez. Pour les formats bruts, il permet aux applications de création d’images plus sophistiquées de tirer parti des fonctionnalités de traitement brut de votre décodeur. En fonction des options d’encodeur que vous prenez en charge, vous pouvez également exposer des fonctionnalités uniques de votre encodeur pour permettre aux applications de tirer pleinement parti des fonctionnalités avancées de votre format d’image.

Le développement d’un codec avec WIC activé nécessite que vous implémentiez de nouvelles interfaces. Dans de nombreux cas, vous pouvez écrire un wrapper pour votre codec existant qui implémente ces interfaces. Lorsque vous installez votre codec, vous devez créer des entrées de Registre pour que votre codec soit détectable par la plateforme WIC et l’associer aux gestionnaires de métadonnées appropriés. Vous devez également appeler une API pour effacer le cache de miniatures des miniatures par défaut (vides) qui peuvent avoir été précédemment associées à des images dans votre format. si vous le souhaitez, vous pouvez activer la galerie de photos Windows Vista pour fournir aux utilisateurs un lien leur permettant de télécharger votre codec lorsque la galerie de photos rencontre une image avec votre extension de nom de fichier. Pour ce faire, vous devez fournir à Microsoft des informations sur l’extension de nom de fichier de votre codec et l’URL de votre site de téléchargement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Installation et inscription du CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



