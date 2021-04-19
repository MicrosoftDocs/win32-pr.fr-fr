---
description: Lorsque vous installez un codec, vous devez l’inscrire dans le registre. Vous devez également vous assurer que le cache de miniatures est mis à jour si des images dans votre format existent déjà sur l’ordinateur.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Installation et inscription du codec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522045"
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

[Intégration à la Galerie de photos Windows et à l’Explorateur Windows](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a>Mise à jour du cache de miniatures lors de l’installation de votre codec

Lorsqu’un codec est installé, le programme d’installation doit appeler la fonction suivante après avoir écrit ses entrées de registre.


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



Cet appel informe Windows que de nouvelles informations d’association de fichiers sont disponibles. Si des images dans votre format d’image existent déjà sur l’ordinateur, le cache de miniatures contiendra des miniatures par défaut, car aucun décodeur n’était disponible pour extraire les miniatures lorsque les images ont été acquises pour la première fois. Lorsque vous notifiez Windows qu’une nouvelle association de fichiers est disponible, le cache de miniatures ignore les miniatures vides et extrait les miniatures réelles des fichiers qui peuvent maintenant être décodés.

## <a name="making-your-wic-enabled-codec-available-to-users"></a>Mise à la disposition des utilisateurs de votre codec WIC-Enabled

Si vous êtes un fabricant d’appareils photo, vous pouvez expédier vos codecs bruts dans le boîtier avec vos appareils photo. Vous pouvez également poster vos codecs sur la page de téléchargement de votre site Web. Toutefois, si un utilisateur acquiert un fichier image dans votre format à partir d’une autre source, telle qu’un ami, un partenaire commercial ou un autre site Web, il peut ne pas savoir où obtenir le codec pour le décoder.

En raison de ce problème, Windows offre aux utilisateurs de votre format d’image un moyen plus simple de rechercher votre codec et de le télécharger sur leur ordinateur, en commençant par Windows Vista. Si la Galerie de photos Windows reconnaît une extension de nom de fichier en tant que format d’image et que le codec pour ce format n’est pas installé, une boîte de dialogue indique à l’utilisateur que la photo ne peut pas être affichée et demande si l’utilisateur souhaite télécharger le logiciel requis pour l’afficher. Lorsque l’utilisateur accepte, un site Web hébergé par Microsoft s’affiche avec un lien vers le site de téléchargement du fabricant du codec. (Si vous le souhaitez, vous pouvez demander que les utilisateurs soient directement dirigés vers votre site de téléchargement.)

Si vous souhaitez que les extensions de nom de fichier de votre format d’image soient reconnues par la Galerie de photos Windows afin que les utilisateurs puissent être dirigés vers votre site de téléchargement, vous devez effectuer les opérations suivantes :

1.  Fournissez un site de téléchargement pour votre codec. (Vous pouvez avoir une page distincte pour chaque codec que vous fournissez ou une page qui fournit des téléchargements pour tous vos codecs).

    Le site de téléchargement doit être localisé et facilement consultable par le modèle d’appareil photo.

2.  Fournissez à Microsoft une liste d’extensions pour vos formats d’image et les URL de vos sites de téléchargement.

Vous devez informer Microsoft des extensions pour les nouveaux codecs que vous développez à l’avenir, ainsi que des modifications apportées aux URL de vos sites de téléchargement, afin que les nouvelles informations puissent être ajoutées à la Galerie de photos Windows.

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

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



