---
description: instructions d’implémentation pour la sérialisation de IWICDevelopRaw Paramètres
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: instructions d’implémentation pour la sérialisation de IWICDevelopRaw Paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119b6377fc8b75aa9763e8141e17ef79832a2aef5f010c2783a412cef0133788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118709829"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>instructions d’implémentation pour la sérialisation de IWICDevelopRaw Paramètres

L’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) expose les paramètres que l’application peut utiliser pour modifier le traitement de l’image brute. Les paramètres doivent pouvoir être sérialisés afin d’être conservés entre les sessions. Bien que cette opération puisse être effectuée de plusieurs façons, il est recommandé d’encoder ces données d’une manière qui est cohérente avec d’autres métadonnées.

Voici quelques recommandations générales en matière d’implémentation :

-   Tous les paramètres effectués via [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (par exemple, rotation ou balance des blancs) doivent éviter le remplacement du paramètre d’appareil photo ou des données « à la capture », sauf si la balise est couramment utilisée comme « paramètre actuel ». Par exemple, les balises d’orientation EXIF peuvent être utilisées pour conserver la rotation.
-   Il est préférable de ne pas avoir à enregistrer la totalité du fichier (y compris les données de pixels de la mosaïque) chaque fois que les paramètres [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) sont demandés pour être sérialisés.
-   Le processus de sérialisation des paramètres [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) suit généralement cet ordre d’événements. L’application :

    1.  Instancie une [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) sur un fichier brut.
    2.  Appelle [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) pour obtenir un [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) pour le frame brut.
    3.  Appelle QueryInterface sur l’interface IWICBitmapFrameDecode pour l’interface IWICDevelopRaw.
    4.  Appelle [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**GetCurrentParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), qui retourne une interface IPropertyBag2 avec toutes les propriétés actuelles stockées dans celui-ci.

        À ce stade du processus, l’objectif est de sérialiser les paramètres de l’interface IPropertyBag2 dans le fichier brut. Pour ce faire, vous devez utiliser un encodeur, et ainsi de suite, qui est détaillé dans les étapes suivantes.

    5.  Crée un [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) pour le fichier brut.
    6.  Appelle [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), en passant un nouveau flux (vide) à encoder.
    7.  Appelle [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) pour créer un IWICBITMAPFRAMEENCODE pour le frame brut.
    8.  Appelle [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)et passe dans l’interface IPropertyBag2 de l’étape 4.
    9.  Appelle [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**WriteSource**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) avec [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) à partir du cadre d’image brute du décodeur.
    10. Appelle [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Le codec sérialise ensuite les propriétés dans le IPropertyBag2 de l’étape 8 dans le fichier. La méthode la plus courante pour sérialiser les propriétés est supposée être en les écrivant sous forme de métadonnées dans le fichier.
    11. Appelle [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Appelle IStream :: commit sur le flux à l’étape 6.

    Les paramètres sont sérialisés dans le fichier.

    Cette méthode entraîne le coût de la réécriture de l’intégralité du fichier brut chaque fois que les paramètres sont sérialisés. Cela peut être évité si vous implémentez [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) ou si votre format de fichier image prend en charge XMP ou EXIF, car WIC fournit des [**IWICFastMetadataEncoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) pour ces deux formats. En outre, si votre codec écrit des modifications à la fin du fichier image, vous n’aurez pas à réécrire la totalité du fichier image.

-   Les jeux de paramètres sont chargés à partir de l’État sérialisé lorsque l’application définit l’énumération [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) sur la méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**LoadParameterSet**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) . L’indicateur [**WICRawParameterSet. WICUserAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) fait référence au dernier jeu de paramètres enregistré. par conséquent, une charge avec cet indicateur doit entraîner la restauration des paramètres au dernier état enregistré.
-   Lors du chargement initial, le dernier jeu de paramètres enregistré doit être chargé, le cas échéant. Si ce n’est pas le cas, les paramètres « As-Shot » doivent être utilisés comme présélections sur les variables de l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Ces paramètres de prise en charge peuvent également être chargés à l’aide de l’indicateur [**WICRawParameterSet. WICAsShotParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) .
-   L’identificateur [**WICRawParameterSet. WICAutoAdjustedParameterSet**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) est destiné à représenter un paramètre « Auto ». Le concepteur de codec peut choisir l’une des méthodes suivantes pour définir les paramètres [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) lorsque ce paramètre est défini :

    -   Effectuez une optimisation algorithmique de certains paramètres, tels que l’exposition ou la couleur. Il s’agit de la façon dont les fonctions automatiques dans les éditeurs d’images classiques sont basées principalement sur l’analyse des données en pixels.
    -   Définissez les paramètres de l’appareil photo comme s’il s’agissait d’un paramètre automatique. Cela est utile si l’image a été capturée sur un paramètre manuel et permet à l’utilisateur de remplacer les paramètres manuels.
    -   Ne rien faire. Tous les contrôles ne doivent pas être définis lorsque l’option auto est sélectionnée et il est possible de ne pas modifier les paramètres.

la galerie de photos Windows Vista et les outils d’édition Galerie de photos Windows Live et d’autres applications de modification utilisent la charge de paramètre automatique [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) quand l’utilisateur sélectionne la correction automatique pour tous les réglages de contrôle de codec normaux, tels que la couleur et l’exposition, pour obtenir les meilleurs résultats.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



