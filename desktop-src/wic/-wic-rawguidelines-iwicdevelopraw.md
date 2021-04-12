---
description: Prise en charge de IWICDevelopRaw
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Prise en charge de IWICDevelopRaw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204208"
---
# <a name="support-for-iwicdevelopraw"></a>Prise en charge de IWICDevelopRaw

Pour permettre aux applications de prendre en charge le traitement brut, les auteurs de codec sont fortement encouragés à implémenter tous les paramètres de [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Pour Windows 7, Windows Imaging Component (WIC) nécessite la prise en charge de tous les [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Si votre format de fichier ne prend pas en charge tous ces paramètres, vous devez modifier le format de votre fichier image.

Pour activer le traitement brut de base dans les applications, les codecs doivent prendre en charge les réglages d’exposition (ExposureCompensationSupport) et de couleur (tels que KelvinWhitePointSupport et TintSupport). En outre, la sortie vers des espaces de couleurs et des formats de pixel spécifiques est fortement recommandée. La prise en charge d’autres ajustements est, bien sûr, encouragée et requise pour Windows 7.

Le codec brut doit fournir une prise en charge de base pour la rotation d’image et l’aperçu rapide. La rotation peut être spécifiée de deux manières différentes :

-   Méthode [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Cette méthode définit l’angle de rotation souhaité pour la sortie des appels suivants à [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) , méthode. L’appelant peut définir l’option dstTransform pour indiquer l’angle de rotation souhaité.

Ces deux approches diffèrent selon les méthodes suivantes :

-   Seuls les paramètres [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) peuvent être rendus persistants entre les instances de l’objet décodeur.
-   [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) s’applique uniquement à cet appel particulier ; Il n’y a aucune persistance de tout type.
-   [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) fournit un contrôle de rotation nettement plus affiné. [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) est soumis à des incréments de 90 degrés.

Si la rotation est spécifiée à la fois dans [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) et [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), l’effet de rotation est cumulatif. Par exemple, si [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) spécifie une rotation de 25 degrés et que [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) spécifie une rotation de 90 degrés, les conditions suivantes doivent se produire :

-   Les appels à [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) doivent appliquer une rotation de 25 degrés (c’est-à-dire, uniquement la quantité spécifiée dans [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Les appels à [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) avec une quantité dstTransform de 90 aboutissent alors à une rotation de 115 degrés (25 + 90).
-   Là encore, seule la rotation de 25 degrés spécifiée via [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRotation**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) peut être persistante.

Dans Windows Vista, les méthodes [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**miniature**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) et [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**GetPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) permettent aux appelants d’obtenir des miniatures incorporées et des images d’aperçu, respectivement. Ils sont destinés à retourner des aperçus et des miniatures précalculés à partir du flux de fichier image. La génération d’aperçus ou de miniatures « à la volée » entraîne des performances médiocres dans l’Explorateur Windows et la visionneuse de photos. Le codec doit également fournir un moyen de retourner rapidement une image de résolution d’écran mise à jour lorsque les utilisateurs exécutent un contrôle interactif des paramètres de traitement.

Les appels à [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**SetRenderMode**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) déterminent les appels suivants à [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) (en privilégiant la vitesse ou la qualité). En outre, l’interface IWICBitmapSourceTransform peut être utilisée pour déterminer si le sous-échantillonnage est nécessaire et peut améliorer les performances lorsqu’il peut être appliqué. La fidélité des couleurs de toutes les images doit être comparable. Lorsque des modifications sont apportées aux paramètres de traitement, tous ces rendus doivent refléter les modifications.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Recommandations de WIC pour les formats d’image RAW Camera](-wic-rawguidelines.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



