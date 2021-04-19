---
description: La création de votre codec sur la plateforme WIC (Windows Imaging Component) permet à toutes les applications basées sur WIC d’obtenir la même prise en charge de plate-forme pour votre format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusion (écriture d’un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527924"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a>Conclusion (écriture d’un codec WIC-Enabled)

La création de votre codec sur la plateforme WIC (Windows Imaging Component) permet à toutes les applications basées sur WIC d’obtenir la même prise en charge de plate-forme pour votre format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme. Il permet également à la Galerie de photos Windows Vista, à l’Explorateur Windows et à la visionneuse de photos d’afficher des miniatures et des aperçus d’images dans votre format à l’aide du décodeur que vous fournissez. Pour les formats bruts, il permet aux applications de création d’images plus sophistiquées de tirer parti des fonctionnalités de traitement brut de votre décodeur. En fonction des options d’encodeur que vous prenez en charge, vous pouvez également exposer des fonctionnalités uniques de votre encodeur pour permettre aux applications de tirer pleinement parti des fonctionnalités avancées de votre format d’image.

Le développement d’un codec avec WIC activé nécessite que vous implémentiez de nouvelles interfaces. Dans de nombreux cas, vous pouvez écrire un wrapper pour votre codec existant qui implémente ces interfaces. Lorsque vous installez votre codec, vous devez créer des entrées de Registre pour que votre codec soit détectable par la plateforme WIC et l’associer aux gestionnaires de métadonnées appropriés. Vous devez également appeler une API pour effacer le cache de miniatures des miniatures par défaut (vides) qui peuvent avoir été précédemment associées à des images dans votre format. Si vous le souhaitez, vous pouvez activer la Galerie de photos Windows Vista pour fournir aux utilisateurs un lien leur permettant de télécharger votre codec lorsque la Galerie de photos rencontre une image avec votre extension de nom de fichier. Pour ce faire, vous devez fournir à Microsoft des informations sur l’extension de nom de fichier de votre codec et l’URL de votre site de téléchargement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Installation et inscription du CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



