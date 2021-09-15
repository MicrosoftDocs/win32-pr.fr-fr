---
description: en savoir plus sur le fonctionnement du composant de création d’images Windows
ms.assetid: c233e25b-bec6-4e67-8fbf-2bf9b70c7522
title: fonctionnement du composant de création d’images Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc9fe31ae4346f2c2d1f0b273e78ed10a0ec7e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312765"
---
# <a name="how-the-windows-imaging-component-works"></a>fonctionnement du composant de création d’images Windows

Cette rubrique contient les sections suivantes :

-   [Découverte et arbitrage](#discovery-and-arbitration)
-   [Décodage](#decoding)
-   [Encodage](#encoding)
-   [Durée de vie d’un codec](#the-lifetime-of-a-codec)
-   [Comment activer un codec avec WIC](#how-to-wic-enabled-a-codec)
-   [Prise en charge du cloisonnement multithread dans WIC](#multi-threaded-apartment-support-in-wic)
-   [Rubriques connexes](#related-topics)

## <a name="discovery-and-arbitration"></a>Découverte et arbitrage

Avant de pouvoir décoder une image, vous devez trouver un codec approprié qui peut décoder ce format d’image. Dans la plupart des systèmes, étant donné que les formats d’images pris en charge sont codés en dur, aucun processus de découverte n’est nécessaire. étant donné que la plateforme WIC (Windows Imaging Component) est extensible, il est nécessaire de pouvoir identifier le format d’une image et de la faire correspondre à un codec approprié.

Pour prendre en charge la découverte au moment de l’exécution, chaque format d’image doit avoir un modèle d’identification qui peut être utilisé pour identifier le décodeur approprié pour ce format. (Il est fortement recommandé, pour les nouveaux formats de fichier, d’utiliser un GUID pour le modèle d’identification, car il est garanti qu’il est unique.) Le modèle d’identification doit être incorporé dans chaque fichier image conforme à ce format d’image. Chaque décodeur a une entrée de Registre qui spécifie le ou les modèles d’identification des formats d’image qu’il peut décoder. Lorsqu’une application doit ouvrir une image, elle demande un décodeur à partir de WIC. WIC recherche les décodeurs disponibles dans le registre et vérifie chaque entrée du Registre pour un modèle d’identification qui correspond au modèle incorporé dans le fichier image. Pour plus d’informations sur les entrées de Registre du décodeur, consultez [entrées de Registre spécifiques au codeur](-wic-decoderregentries.md)

Quand WIC trouve un décodeur unique qui correspond au modèle d’identification dans l’image, il crée une instance du décodeur et lui transmet le fichier image. Si le WIC trouve plusieurs correspondances, il appelle une méthode appelée [**QueryCapability**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability) sur chaque décodeur correspondant pour arbitrer les deux et rechercher la meilleure correspondance. Pour plus d’informations, consultez la section [QueryCapabilities](-wic-imp-iwicbitmapdecoder.md) dans [implémentation de IWICBitmapDecoder](-wic-imp-iwicbitmapdecoder.md).

## <a name="decoding"></a>Décodage

Une fois que le décodeur approprié a été sélectionné et instancié, l’application communique directement avec le décodeur. Le décodeur a plusieurs responsabilités, qu’il implémente par le biais de différentes interfaces. Ces services peuvent être classés comme suit :

-   Services au niveau du conteneur
-   Services au niveau de la trame
-   Services d’énumération des métadonnées
-   Transformations du décodeur natif
-   Notifications de progression et prise en charge de l’annulation
-   Services de traitement brut

Les services au niveau du conteneur incluent la récupération des miniatures de niveau supérieur (si elles sont prises en charge), de l’aperçu, des contextes de couleur, de la palette (le cas échéant) et du format de conteneur, ainsi que l’accès aux trames d’image individuelles dans le conteneur. (Certains conteneurs ne contiennent qu’une seule image, tandis que d’autres, tels que TIFF (Tagged Image File Format), peuvent contenir plusieurs frames.) Cet ensemble de services comprend également des informations sur le décodeur lui-même et ses fonctionnalités par rapport à un fichier image spécifique.

Les frames individuels ont leurs propres miniatures et peuvent également avoir leurs propres contextes de couleur, palettes et autres propriétés, qui sont exposées au niveau du frame. Toutefois, l’opération la plus importante effectuée au niveau de la trame est le décodage réel des bits d’image de ce frame.

WIC fournit des lecteurs de métadonnées pour les formats de métadonnées les plus courants (IFD, EXIF, IPTC, XMP, APP0, APP1 et d’autres formats) et prend également en charge l’extensibilité pour les formats de métadonnées tiers. Cela libère le codec de la responsabilité pour l’analyse des métadonnées. Toutefois, le codec est responsable de l’énumération des blocs de métadonnées et de la demande d’un lecteur de métadonnées pour chaque bloc. WIC effectue la détection pour les gestionnaires de métadonnées de la même façon que pour les codecs, en fonction d’un modèle dans l’en-tête de bloc qui correspond à un modèle dans l’entrée de Registre du gestionnaire de métadonnées. Pour plus d’informations, consultez les [entrées de Registre spécifiques à l’encodeur](-wic-decoderregentries.md)

Les décodeurs ne sont pas requis pour prendre en charge en mode natif les opérations de transformation, mais cela permet des optimisations de performances significatives qui améliorent l’expérience de l’utilisateur final. Par exemple, une application peut créer un pipeline de diverses transformations (mise à l’échelle, rognage, rotation et conversion de format de pixel) pour effectuer une réalisation sur une image avant le rendu de l’image. Pour plus d’informations sur les pipelines de transformation, consultez [IWICBitmapSource](-wic-imp-iwicbitmapsource.md). Après la création d’un pipeline de transformation, l’application demande la transformation finale dans le pipeline pour produire la bitmap qui résulte de l’application de toutes les transformations à la source de l’image. À ce stade, si le décodeur lui-même peut effectuer des opérations de transformation, WIC demande les transformations demandées qu’il peut effectuer. Les transformations demandées que le décodeur ne peut pas effectuer seront exécutées par WIC sur l’image décodée avant d’être renvoyée à l’appelant. Ce pipeline de transformation optimisé offre de meilleures performances que l’exécution de chaque transformation de manière séquentielle dans la mémoire, en particulier quand une partie ou la totalité des transformations peut être accomplie pendant le processus de décodage.

Les notifications de progression et la prise en charge de l’annulation permettent à une application de demander des notifications de progression pour les opérations de longue durée, et permettent également à l’application de donner à l’utilisateur la possibilité d’annuler une opération qui prend trop de temps. Cela est important, car si un utilisateur ne peut pas annuler une opération, il peut penser que le processus a été suspendu et essayer de l’annuler en fermant l’application.

Ces interfaces sont décrites en détail dans la section relative à l' [implémentation d’un décodeur de WIC-Enabled](-wic-implementingwicdecoder.md).

Les services de traitement bruts incluent l’ajustement des paramètres de l’appareil photo, tels que l’exposition, le contraste et la netteté, ou la modification de l’espace colorimétrique avant le traitement des bits bruts.

## <a name="encoding"></a>Encodage

Comme les décodeurs, les encodeurs ont des responsabilités qu’ils implémentent via des interfaces. Les services fournis par les encodeurs sont complémentaires aux services fournis par les décodeurs, sauf qu’ils écrivent des données d’image plutôt que de les lire. Les encodeurs fournissent également des services dans les catégories suivantes :

-   Services au niveau du conteneur
-   Services au niveau de la trame
-   Énumération des métadonnées et services de mise à jour
-   Notification de progression et prise en charge de l’annulation

Les services au niveau du conteneur pour un encodeur incluent la définition de la miniature de niveau supérieur (si prise en charge), de l’aperçu et de la palette (le cas échéant), et l’itération au sein des trames d’image individuelles afin qu’elles puissent être sérialisées dans le conteneur.

Les services au niveau de la trame pour un encodeur reflètent ceux du décodeur, sauf qu’ils écrivent les données de l’image, la miniature et toute palette associée ou autre composant, plutôt que de les lire.

En outre, les services d’énumération des métadonnées pour un encodeur incluent l’itération au sein des blocs de métadonnées à écrire, et l’appel des enregistreurs de métadonnées appropriés pour sérialiser les métadonnées sur le disque.

Ces interfaces sont décrites en détail dans la section relative à l' [implémentation d’un Encodeur WIC-Enabled](-wic-implementingwicencoder.md).

## <a name="the-lifetime-of-a-codec"></a>Durée de vie d’un codec

Un codec WIC est instancié pour gérer une seule image et a généralement une durée de vie réduite. Elle est créée lorsqu’une image est chargée et libérée lorsque l’image est fermée. Une application peut utiliser un grand nombre de codecs simultanément avec des durées de vie qui se chevauchent (le fait de faire défiler un répertoire contenant des centaines d’images) et plusieurs applications peuvent le faire en même temps.

Bien que certains codecs aient une durée de vie limitée à la durée de vie du processus dans lequel ils vivent, ce n’est pas le cas avec les codecs WIC. la galerie de photos Windows Vista, l’explorateur de Windows et la visionneuse de photos, ainsi que de nombreuses autres applications, s’appuient sur WIC et utilisent votre codec pour afficher des images et des miniatures. si la durée de vie de votre codec est limitée à la durée de vie du processus, chaque fois qu’une image ou une miniature était affichée dans le Windows l’explorateur Vista, le codec instancié pour décoder cette image restera en mémoire jusqu’à ce que l’utilisateur redémarre son ordinateur. Si votre CODEC n’est jamais déchargé, ses ressources sont en fait « divulguées », car elles ne peuvent pas être utilisées par un autre composant du système.

## <a name="how-to-wic-enabled-a-codec"></a>Comment activer un codec avec WIC

1.  Implémentez une classe de décodeur au niveau du conteneur et une classe de décodeur au niveau de la trame qui expose les interfaces WIC requises pour décoder les images et itérer au sein des blocs de métadonnées. Cela permet à toutes les applications WIC d’interagir avec votre codec de la même façon qu’elles interagissent avec les formats d’image standard.
2.  Implémentez une classe de codeur au niveau du conteneur et une classe de codeur au niveau de la trame qui expose les interfaces WIC requises pour encoder des images et sérialiser des blocs de métadonnées dans un fichier image.
3.  Si votre format de conteneur n’est pas basé sur un conteneur TIFF ou JPEG, vous devrez peut-être écrire des gestionnaires de métadonnées pour les formats de métadonnées courants (EXIF, XMP). Toutefois, si vous utilisez un format de conteneur basé sur TIFF ou JPEG, cela n’est pas nécessaire, car vous pouvez déléguer aux gestionnaires de métadonnées fournis par le système.
4.  Incorporez un modèle d’identification unique (nous vous recommandons d’utiliser un GUID) dans tous vos fichiers image. Cela permet à votre format d’image d’être mis en correspondance avec votre codec pendant la découverte. Si vous écrivez un wrapper de WIC pour un format d’image existant, vous devez trouver un modèle de bits que l’encodeur écrit toujours dans ses fichiers image qui est propre à ce format d’image, et l’utiliser comme modèle d’identification.)
5.  Inscrivez votre codec au moment de l’installation. Cela permet à votre codec d’être découvert au moment de l’exécution en faisant correspondre le modèle d’identification dans le Registre avec le modèle incorporé dans le fichier image.
6.  à partir de Windows 7, WIC exige que les codecs soient de type cloisonnement COM « Both ». Cela signifie que vous devez effectuer le verrouillage approprié pour gérer les appelants inter-cloisonnement et les appelants dans les scénarios multithread. Pour plus d’informations, consultez la section suivante sur la prise en charge de Multi-Threaded Apartment.
7.  prise en charge des plateformes 64 bits : pour Windows 7, wic exige que les codecs wic tiers soient fournis comme fichiers binaires natifs 32 bits et 64 bits. en outre, le formulaire 32 bits doit être installé et exécuté sur les systèmes 64 bits, et le programme d’installation du codec tiers Windows 7 doit installer à la fois les binaires 32 bits et 64 bits sur les systèmes 64 bits.

## <a name="multi-threaded-apartment-support-in-wic"></a>Prise en charge du cloisonnement multithread dans WIC

Les objets d’un cloisonnement multithread (MTA) peuvent être appelés simultanément par n’importe quel nombre de threads dans le MTA. Cela permet d’améliorer les performances sur les systèmes à plusieurs cœurs et certains scénarios de serveur. En outre, les codecs WIC dans un MTA peuvent appeler d’autres objets dans le MTA sans le coût de marshaling associé à l’appel entre les threads dans différents Apartments STA. dans Windows 7, tous les codecs WIC intégrés ont été mis à jour pour prendre en charge les mta, y compris JPEG, TIFF, PNG, GIF, ICO et BMP. Il est fortement recommandé d’écrire des codecs tiers pour prendre en charge les MTA. Les codecs tiers qui ne prennent pas en charge les MTA entraînent des coûts de performances significatifs dans les applications multithread en raison du marshaling. L’activation de la prise en charge de MTA nécessite une synchronisation appropriée à implémenter dans le codec tiers. L’implémentation exacte de ces techniques de synchronisation dépasse le cadre de ce document. Pour plus d’informations sur la synchronisation des objets COM, consultez [comprendre et utiliser les modèles de threads com](/previous-versions/ms809971(v=msdn.10)).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Introduction (écriture d’un CODEC WIC-Enabled)](-wic-howtowriteacodec-intro.md)
</dt> <dt>

[Implémentation d’un décodeur WIC-Enabled](-wic-implementingwicdecoder.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> </dl>

 

 



