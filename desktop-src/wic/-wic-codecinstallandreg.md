---
description: Lorsque vous installez un codec, vous devez l’inscrire dans le registre. Vous devez également vous assurer que le cache de miniatures est mis à jour si des images dans votre format existent déjà sur l’ordinateur.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installation et inscription du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc13a2d937e82eae3517b9b20440f4acbb10b16af3fa0b872eb0ddd6c2a8d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965178"
---
# <a name="codec-installation-and-registration"></a>Installation et inscription du codec

Lorsque vous installez un codec, vous devez l’inscrire dans le registre. Vous devez également vous assurer que le cache de miniatures est mis à jour si des images dans votre format existent déjà sur l’ordinateur.

Cette rubrique contient les sections suivantes :

-   [Inscription d’un codec](#registering-a-codec)
-   [Mise à jour du cache de miniatures lors de l’installation de votre codec](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [Mise à la disposition des utilisateurs de votre codec WIC-Enabled](#making-your-wic-enabled-codec-available-to-users)
-   [Rubriques connexes](#related-topics)

## <a name="registering-a-codec"></a>Inscription d’un codec

Lorsque vous inscrivez un codec, vous inscrivez en fait deux composants : l’encodeur et le décodeur. Vous devez également créer des entrées de Registre pour inscrire votre format de conteneur auprès des gestionnaires de métadonnées pour les formats de métadonnées pris en charge par votre format d’image.

Les rubriques suivantes décrivent les entrées de registre dont vous avez besoin pour inscrire votre codec :

[Entrées de Registre générales](-wic-generalregentries.md)

[Entrées de Registre spécifiques à l’encodeur](-wic-encoderregentries.md)

[Entrées de Registre spécifiques au décodeur](-wic-decoderregentries.md)

[intégration avec Windows galerie de photos et l’explorateur de Windows](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Mise à jour du cache de miniatures lors de l’installation de votre codec

Lorsqu’un codec est installé, le programme d’installation doit appeler la fonction suivante après avoir écrit ses entrées de registre.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



cet appel avertit Windows que de nouvelles informations d’association de fichiers sont disponibles. Si des images dans votre format d’image existent déjà sur l’ordinateur, le cache de miniatures contiendra des miniatures par défaut, car aucun décodeur n’était disponible pour extraire les miniatures lorsque les images ont été acquises pour la première fois. lorsque vous notifiez Windows qu’une nouvelle association de fichiers est disponible, le cache de miniatures ignore les miniatures vides et extrait les miniatures réelles des fichiers qui peuvent maintenant être décodés.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Mise à la disposition des utilisateurs de votre codec WIC-Enabled

Si vous êtes un fabricant d’appareils photo, vous pouvez expédier vos codecs bruts dans le boîtier avec vos appareils photo. Vous pouvez également poster vos codecs sur la page de téléchargement de votre site Web. Toutefois, si un utilisateur acquiert un fichier image dans votre format à partir d’une autre source, telle qu’un ami, un partenaire commercial ou un autre site Web, il peut ne pas savoir où obtenir le codec pour le décoder.

en raison de ce problème, Windows offre un moyen plus simple pour les utilisateurs de votre format d’image de rechercher votre codec et de le télécharger sur leur ordinateur, en commençant par Windows Vista. si la galerie de photos Windows reconnaît une extension de nom de fichier en tant que format d’image et que le codec pour ce format n’est pas installé, une boîte de dialogue indique à l’utilisateur que la Photo ne peut pas être affichée et demande si l’utilisateur souhaite télécharger le logiciel requis pour l’afficher. Lorsque l’utilisateur accepte, un site Web hébergé par Microsoft s’affiche avec un lien vers le site de téléchargement du fabricant du codec. (Si vous le souhaitez, vous pouvez demander que les utilisateurs soient directement dirigés vers votre site de téléchargement.)

si vous souhaitez que les extensions de nom de fichier de votre format d’image soient reconnues par l’Windows galerie de photos afin que les utilisateurs puissent être dirigés vers votre site de téléchargement, vous devez effectuer les opérations suivantes :

1.  Fournissez un site de téléchargement pour votre codec. (Vous pouvez avoir une page distincte pour chaque codec que vous fournissez ou une page qui fournit des téléchargements pour tous vos codecs).

    Le site de téléchargement doit être localisé et facilement consultable par le modèle d’appareil photo.

2.  Fournissez à Microsoft une liste d’extensions pour vos formats d’image et les URL de vos sites de téléchargement.

vous devez informer Microsoft des extensions pour les nouveaux codecs que vous développez à l’avenir, ainsi que des modifications apportées aux url de vos sites de téléchargement, afin que les nouvelles informations puissent être ajoutées à la galerie de photos Windows.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Implémentation de IWICMetadataBlockWriter](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[Conclusion (écriture d’un CODEC WIC-Enabled)](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



