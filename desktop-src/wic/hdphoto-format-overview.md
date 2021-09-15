---
description: cette rubrique fournit des informations sur le codec de Photo HD natif disponible via le composant WIC (Windows Imaging Component).
ms.assetid: C73752AB-3D6E-4D92-9FDE-CB68B6A9743C
title: Vue d’ensemble du format photo HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c526667c6bf77d340e895bdb66dc073134c33d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411164"
---
# <a name="hd-photo-format-overview"></a>Vue d’ensemble du format photo HD

cette rubrique fournit des informations sur le codec de Photo HD natif disponible via le composant WIC (Windows Imaging Component).

> [!IMPORTANT]
>
> Le format HD photo est une implémentation pré-standard du format JPEG XR. Le format XR JPEG a été entièrement implémenté dans Windows 8. Pour plus d’informations, consultez [vue d’ensemble du codec XR JPEG](jpeg-xr-codec.md) .

 

Cette rubrique contient les sections suivantes.

-   [Identité du codec](#codec-identity)
-   [Encodage](#encoding)
    -   [Options de l’encodeur](#encoder-options)
-   [Décodage](#decoding)
    -   [Support IWICBitmapSourceTransform](#iwicbitmapsourcetransform-support)

## <a name="codec-identity"></a>Identité du codec

Le tableau suivant fournit des informations d’identification du codec.



|   Composant            | Description                                                                     |
|------------------------|---------------------------------------------------------------------------------|
| Nom (s) formel (s)         | photo HD, Windows Media photo                                                   |
| Extension (s) de nom de fichier | WDP                                                                             |
| type MIME              | image/vnd. ms-photo                                                              |
| Signature (s) de fichier      | Quatre premiers octets : 0x4949bc00 (version 0 ; version préliminaire), 0x4949bc01 (version 1,0) |



 

Le tableau suivant répertorie les GUID utilisés pour identifier les composants de codec de photo HD natifs.



| Composant        | Nom convivial            | GUID                                |
|------------------|--------------------------|-------------------------------------|
| Format de conteneur | GUID \_ ContainerFormatWmp | 57a37caa-367a-4540-916bf183c5093a4b |
| Décodeur          | CLSID \_ WICWmpDecoder     | a26cec36-234C-4950-ae16e34aace71d0d |
| Encodeur          | CLSID \_ WICWmpEncoder     | ac4ce3cb-e1c1-44cd-82155a1665509ec2 |



 

## <a name="encoding"></a>Encodage

L’API d’encodage WIC est conçue pour être indépendante du codec et l’encodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur l’encodage d’image à l’aide de l’API WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

### <a name="encoder-options"></a>Options de l’encodeur

Les codecs compatibles avec WIC diffèrent au niveau de l’option d’encodage. Les options d’encodeur reflètent les fonctionnalités d’un encodeur d’image et chaque codec natif prend en charge un ensemble de ces options d’encodeur. Les options d’encodeur peuvent être des options prises en charge par le WIC de base disponibles pour tous les codes WIC activés (mais pas nécessairement pris en charge) ou les options spécifiques aux codecs conçues par le codec de format d’image. Pour gérer ces options d’encodage pendant le processus d’encodage, WIC utilise l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations sur l’utilisation de l’interface **IPropertyBag2** pour l’encodage WIC, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

Le codec photo HD utilise à la fois les options de base du WIC et fournit plusieurs options d’encodage spécifiques aux photos HD. Le tableau suivant répertorie les options de codeur prises en charge par le codec de photo HD natif.

Options de l’encodeur WIC de base

| Nom de la propriété | VARTYPE | Plage de valeurs | Valeur par défaut |
|---------------|---------|-------------|---------------|
| [ImageQuality](#imagequality-option) | VT \_ R4 | 0-1,0 | 0.9 |
| [Lossless](#lossless-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [BitmapTransform](#bitmaptransform-option) | \_UI1 VT | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |   [**WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) |

Options de l’encodeur spécifique aux photos HD

| Nom de la propriété | VARTYPE | Plage de valeurs | Valeur par défaut |
|---------------|---------|-------------|---------------|
| [UseCodecOptions](#usecodecoptions-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [Qualité](#quality-option) | \_UI1 VT | 1 - 255 | 10 |
| [Éviter](#overlap-option) | \_UI1 VT | 0 - 2 | 1 |
| [Sous-échantillonnage](#subsampling-option) | \_UI1 VT | 0 - 3 | 3 si ImageQuality > 0,8 ; sinon 1 ; |
| [HorizontalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (largeur d’image – 1)  >> 8 |
| [VerticalTileSlices](#horizontaltileslices-verticaltileslices-options) | \_UI2 VT | 0 - 4095 | (hauteur d’image – 1)  >> 8 |
| [FrequencyOrder](#frequencyorder-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [InterleavedAlpha](#interleavedalpha-option) | VT \_ bool | **true**, **false** | **FALSE** |
| [AlphaQuality](#alphaquality-option) | \_UI1 VT | 1 - 255 | 1 |
| [CompressedDomainTranscode](#compresseddomaintranscode-option) | VT \_ bool | **true**, **false** | **TRUE** |
| [ImageDataDiscard](#imagedatadiscard-option) | \_UI1 VT | 0 - 3 | 0 |
| [AlphaDataDiscard](#alphadatadiscard-option) | \_UI1 VT | 0 - 4 | non utilisée. |
| [IgnoreOverlap](#ignoreoverlap-option) | VT \_ bool | **true**, **false** | **FALSE** |


Si une option d’encodeur est présente dans la liste d’options [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) que le codec ne prend pas en charge, elle est ignorée.

### <a name="imagequality-option"></a>Option ImageQuality

Spécifie la fidélité de l’image souhaitée. 0,0 indique la fidélité la plus faible possible et 1,0 spécifie la fidélité la plus élevée. Pour le format d’image HD photo, une valeur 1,0 entraîne une compression mathématiquement sans perte.

La valeur par défaut est 0,9.

### <a name="compressionquality-option"></a>Option CompressionQuality

Spécifie la qualité de compression souhaitée. 0,0 indique le schéma de compression efficace disponible. En règle générale, ce schéma produit une sortie plus rapide mais de plus grande taille. La valeur 1,0 spécifie le schéma de compression le plus efficace disponible, ce qui produit généralement un encodage plus long, mais une sortie plus petite.

La photo HD ne prend pas en charge cette option d’encodeur. Cette valeur est ignorée si elle est présente dans la liste de paramètres [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) .

### <a name="lossless-option"></a>Option Lossless

Spécifie s’il faut utiliser le mode de compression des pertes. Pour le format d’image HD photo, cette valeur remplace la valeur de l’option [ImageQuality](#imagequality-option) .

La valeur par défaut est **FALSE**.

### <a name="bitmaptransform-option"></a>Option BitmapTransform

Spécifie la façon dont l’image est transformée lors du décodage de l’image. Vous devez définir cette option sur l’une des valeurs d’énumération [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

La valeur par défaut est [**WICBitmapTransformOptions :: WICBitmapTransformRotate0**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions).

### <a name="usecodecoptions-option"></a>Option UseCodecOptions

Si la valeur est \_ true, il s’agit des options de [qualité](#quality-option), de [chevauchement](#overlap-option)et de sous- [échantillonnage](#subsampling-option) au lieu de la valeur de l’option.

La valeur par défaut est **FALSE**.

### <a name="quality-option"></a>Option de qualité

Spécifie la qualité de compression de l’image. La valeur 1 indique le mode sans perte. L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.

La valeur par défaut est 10.

### <a name="overlap-option"></a>Option de chevauchement

Spécifie le niveau de traitement du chevauchement.

Le tableau suivant répertorie les niveaux de traitement de chevauchement disponibles.



| Valeur | Description                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Aucun traitement de chevauchement n'est activé.                                                                                                                                                           |
| 1     | Un niveau de traitement de chevauchement est activé, modifiant les valeurs encodées de blocs 4x4 en fonction des valeurs des blocs voisins.                                                                       |
| 2     | Deux niveaux de traitement de chevauchement sont activés. Outre le traitement de premier niveau, les valeurs encodées des blocs de macro 16x16 sont modifiées en fonction des valeurs des blocs de macros voisins. |



 

La valeur par défaut est 1.

### <a name="subsampling-option"></a>Option de sous-échantillonnage

Spécifie une compression supplémentaire dans l’espace de chrominance. De cette façon, vous pouvez conserver les détails de la luminance aux dépens des détails des couleurs. Cette option s’applique uniquement aux images RVB.

Le tableau suivant répertorie les options de sous-échantillonnage disponibles.



| Valeur | Description                                                                                                                                                                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 3     | l’encodage 4:4:4 préserve la résolution complète de Chroma.                                                                                                                                                                                                                                            |
| 2     | l’encodage 4:2:2 réduit la résolution chromatique à 1/2 de la résolution de luminance.                                                                                                                                                                                                                      |
| 1     | l’encodage 4:2:0 réduit la résolution chromatique à 1/4 de la résolution de luminance.                                                                                                                                                                                                                      |
| 0     | 4:0:0 l’encodage ignore tout le contenu de chroma et conserve uniquement la luminance. Étant donné que le codec utilise une définition de luminance légèrement modifiée pour améliorer les performances, nous vous recommandons de convertir une image RVB en monochrome avant l’encodage, plutôt que d’utiliser ce mode de sous-échantillonnage de chrominance. |



 

La valeur par défaut est 3 Si [ImageQuality](#imagequality-option) > 0,8 ; sinon 1.

### <a name="horizontaltileslices-verticaltileslices-options"></a>Options HorizontalTileSlices, VerticalTileSlices

Spécifiez les mosaïques horizontale et verticale de l’image avant d’effectuer un encodage de compression pour les performances optimales du décodage de la région. En divisant l’image en mosaïques rectangulaires pendant l’encodage, vous pouvez décoder les régions de l’image sans traiter l’intégralité du flux de données compressées. La valeur par défaut 0 spécifie aucune sous-division, donc la totalité de l’image est traitée comme une seule vignette. La valeur 1 pour chaque paramètre crée une seule division verticale et horizontale unique, en divisant efficacement l’image en quatre mosaïques de taille égale. La valeur maximale de 4095 pour chaque paramètre divise l’image en lignes de vignette 4096 avec 4096 vignettes par ligne. En d’autres termes, les valeurs de paramètre sont égales au nombre de vignettes horizontales et verticales (respectivement) moins 1. La largeur ou la hauteur d’une vignette ne peut jamais être inférieure à 16 pixels. l’encodeur photo HD peut donc ajuster ce paramètre pour maintenir la taille de mosaïque minimale requise. Étant donné qu’il y a un stockage et une surcharge de traitement associées à chaque vignette, vous devez choisir ces valeurs avec soin pour respecter le scénario spécifique.

[HorizontalTileSlices](/windows): la valeur par défaut est (largeur d’image – 1)  >> 8.

[VerticalTileSlices](/windows): la valeur par défaut est (hauteur d’image – 1)  >> 8.

### <a name="frequencyorder-option"></a>Option FrequencyOrder

Spécifie que l’image doit être encodée dans l’ordre des fréquences. Les données de fréquence la plus basse apparaissent en premier dans le fichier, et le contenu de l’image est regroupé par sa fréquence plutôt que par son orientation spatiale. L’organisation d’un fichier par ordre de fréquence offre les meilleures performances pour tout décodage basé sur les fréquences et, par conséquent, nous vous recommandons de le faire. Les implémentations d’appareils des encodeurs de photos HD peuvent organiser un fichier dans l’ordre spatial pour réduire l’encombrement mémoire requis lors de l’encodage.

La valeur par défaut est **true** et nous recommandons que les applications et les appareils utilisent toujours l’ordre des fréquences, à moins que vous n’ayez des raisons de performances ou spécifiques à l’application d’utiliser l’ordre spatial.

### <a name="interleavedalpha-option"></a>Option InterleavedAlpha

Si cette option a la **valeur true** , le codec doit encoder les informations de canal alpha en tant que canal entrelacé supplémentaire, sans corrélation avec les canaux de contenu d’image. Ce mode est utile lorsque vous devez décoder alpha simultanément avec l’image dans un scénario de diffusion en continu.

Si vous affectez la valeur **false** à ce paramètre, un canal alpha planaire est encodé sous la forme d’une image distincte avec sa propre valeur de qualité facultative. En utilisant un canal alpha planaire, vous pouvez décoder les données d’image et le canal alpha indépendamment. Les canaux alpha entrelacés sont pris en charge uniquement pour certains formats de pixel RVB. Vous pouvez associer un canal alpha planaire à n’importe quel format d’image qui définit un canal alpha.

La valeur par défaut est **FALSE**.

### <a name="alphaquality-option"></a>Option AlphaQuality

Spécifie la qualité de compression pour l’image de canal alpha planaire. La valeur 1 définit le mode sans perte. L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.

La valeur par défaut est 1.

### <a name="compresseddomaintranscode-option"></a>Option CompressedDomainTranscode

À l’aide de la photo HD, vous pouvez effectuer un certain nombre d’opérations de transformation de fichier sans avoir à décoder les données compressées et à les réécrire dans le fichier de destination. Les opérations de domaine compressées sont très efficaces et évitent toute perte de qualité supplémentaire courante lorsque vous décodez et recodez une image compressée avec perte.

Les opérations de domaine compressées suivantes sont prises en charge :

-   Rogner une zone de l’image.
-   Effectue une transformation de rotation/retournement.
-   Ignorer les données de fréquence (ce qui permet de créer un fichier image plus petit.)
-   Réorganisez l’image entre un ordre séquentiel et une fréquence séquentielle.

L’encodeur photo HD effectue une opération de transcodage de domaine compressée lorsqu’il encode une image de photo HD à l’aide d’un décodeur photo HD comme source d’image. En fonction des options d’encodage que vous avez sélectionnées, le codec utilise une opération de domaine compressé si possible. Si une application choisit d’empêcher explicitement toute opération de transcodage de domaine compressée, vous devez affecter à l’option *UseCodecOptions* la valeur **true** et l’option *CompressedDomainTranscode* la **valeur false**.

Lorsque le codec effectue une opération de domaine compressé, seuls certains paramètres de l’encodeur et certains paramètres de propriété sont autorisés.

-   Les options de codage de base [ImageQuality](#imagequality-option), [CompressionQuality](/windows) et [Lossless](#lossless-option) sont ignorées.
-   La [qualité](#quality-option), le [chevauchement](#overlap-option), [InterleavedAlpha](#interleavedalpha-option) et [AlphaQuality](#alphaquality-option) des options d’encodeur spécifiques aux photos HD sont ignorées.
-   S’il est présent, les options [HorizontalTileSlices](/windows) et [VerticalTileSlices](/windows) doivent être définies sur zéro. La taille de la vignette d’une image ne peut pas être modifiée dans le cadre d’un transcodage de domaine compressé.
-   Vous pouvez modifier l’organisation de l’image entre la fréquence et le classement spatial en spécifiant la valeur appropriée des options [FrequencyOrdering](/windows) .
-   Une rotation Cardinal et/ou une opération de retournement horizontale/verticale peuvent être effectuées en fonction de la valeur spécifiée dans l’option d’encodeur [BitmapTransform](#bitmaptransform-option) .
-   L’image peut être rognée en spécifiant la région souhaitée à l’aide du paramètre [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) de la méthode d’encodeur **WriteSource** .
-   Les données image et/ou alpha peuvent être ignorées en spécifiant les valeurs appropriées dans les options [ImageDataDiscard](#imagedatadiscard-option) et/ou [AlphaDataDiscard](#alphadatadiscard-option) , ce qui réduit la taille des fichiers encodés et réduit efficacement la résolution de la nouvelle image.

La valeur par défaut est **true** et nous recommandons que les applications et les appareils utilisent toujours l’ordre de fréquence, sauf si vous avez des raisons de performances ou d’application spécifiques à utiliser l’ordre spatial.

### <a name="imagedatadiscard-option"></a>Option ImageDataDiscard

Ce paramètre est valide uniquement si l’option [CompressedDomainTranscode](#compresseddomaintranscode-option) a la **valeur true**; dans le cas contraire, elle est ignorée. [ImageDataDiscard](#imagedatadiscard-option) spécifie la quantité de données d’image à ignorer pendant un transcodage de domaine compressé. Si l’image contient un canal alpha entrelacé, ce rejet de données s’applique également au canal alpha, avec les exceptions, comme décrit plus loin dans cette section.

Les valeurs suivantes sont autorisées.



| Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Aucune donnée de fréquence image n'est ignorée.                                                                                                                                                                                                                                                                                                                                                                                        |
| 1     | Les FlexBits sont ignorés, ce qui rend une réduction arbitraire de la qualité de l’image transcodée sans modifier la résolution effective de l’image. La réduction exacte de la taille des fichiers ou la réduction de la qualité spécifique dépend de nombreux facteurs et ne peuvent pas être spécifiés ou prédits. Ce valuereturns une erreur si vous le spécifiez pour un canal alpha entrelacé.                                                    |
| 2     | La bande de données de fréquence haut est ignorée (ce qui comprend également le FlexBits), ce qui réduit efficacement la résolution de l’image transcodée à l’aide d’un facteur de 4 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais elles perdent tous les détails dans chaque bloc 4x4 de pixels. Par conséquent, vous devez faire en sorte d’échantillonner l’image transcodée en conséquence chaque fois que vous la décodez.                            |
| 3     | Les bandes de données de fréquence haut et passe-bas sont ignorées (ce qui comprend également le FlexBits), ce qui réduit efficacement la résolution de l’image transcodée par un facteur de 16 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais elles perdent tous les détails dans chaque bloc macro de pixels de 16 x 16. Par conséquent, vous devez faire en sorte d’échantillonner l’image transcodée en conséquence chaque fois que vous la décodez. |



 

La valeur par défaut est 0.

### <a name="alphadatadiscard-option"></a>Option AlphaDataDiscard

Cette option est valide uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode-option) a la **valeur true** et que l’image contient un canal alpha à l’aide de plans ou entrelacés ; dans le cas contraire, elle est ignorée. Il spécifie la quantité de données de fréquence alpha à ignorer pendant un transcodage de domaine compressé. Les valeurs suivantes sont autorisées pour un canal alpha planaire.



| Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Aucune donnée de fréquence image n'est ignorée.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 1     | Les FlexBits sont ignorés, ce qui rend une réduction arbitraire de la qualité du canal alpha planaire pour l’image transcodée sans modifier la résolution effective. La réduction exacte de la taille des fichiers ou la réduction de la qualité spécifique dépend de nombreux facteurs et ne peuvent pas être spécifiés ou prédits.                                                                                                                                                                                                                                                |
| 2     | La bande de données de fréquence haut est ignorée (ce qui comprend également le FlexBits), ce qui réduit efficacement la résolution du canal alpha Planar de l’image transcodée par un facteur de 4 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails du canal alpha planaire dans chaque bloc 4x4 de pixels. Par conséquent, l’image transcodée doit être échantillonnée en conséquence chaque fois qu’elle est décodée. En règle générale, vous devez définir cette valeur uniquement lorsque vous définissez ImageDataDiscard propertyto la même valeur. |
| 3     | Les bandes de données de fréquence haut et passe-bas sont ignorées (ce qui comprend également le FlexBits), ce qui réduit efficacement la résolution de l’image transcodée par un facteur de 16 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc macro de 16 x 16 pixels. Par conséquent, l’image transcodée doit être échantillonnée en conséquence chaque fois qu’elle est décodée. En règle générale, vous devez définir cette valeur uniquement lorsque vous affectez la même valeur à la propriété ImageDataDiscard.               |
| 4     | Le canal alpha est complètement ignoré. Le format de pixel de l’image transcodée est modifié pour refléter la suppression du canal alpha.                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Pour les images qui contiennent des canaux alpha entrelacés, sauf si cette propriété a la valeur 4, le canal alpha est traité de la même façon que les données de l’image, en fonction de la valeur de la propriété ImageDataDiscard. Si cette propriété a la valeur 4, le canal alpha entrelacé est complètement ignoré et le format de pixel de l’image transcodée est modifié en conséquence.

Pas de valeur par défaut.

### <a name="ignoreoverlap-option"></a>Option IgnoreOverlap

Cette option est valide uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode-option) a la **valeur true** et qu’un transcodage de sous-région d’une ou plusieurs vignettes est demandé. L’opération par défaut pour un transcodage de région (ou Decode) consiste à développer la région demandée pour inclure les pixels environnants requis pour le décodage du chevauchement des bords de la région. Lorsque ce paramètre est défini sur **true**, les pixels environnants sont ignorés et seule la mosaïque ou les vignettes sélectionnées sont extraites. Là encore, la région demandée doit correspondre exactement aux coordonnées d’une ou plusieurs vignettes. Si l’image source n’est pas en mosaïque ou si la région demandée spécifie des vignettes partielles, ce paramètre est ignoré.

La valeur par défaut est **FALSE**.

## <a name="decoding"></a>Décodage

L’API de décodage WIC est conçue pour être indépendante du codec et le décodage d’image pour les codecs compatibles avec WIC est fondamentalement identique. Pour plus d’informations sur le décodage d’image, consultez la [vue d’ensemble du décodage](-wic-creating-decoder.md). Pour plus d’informations sur l’utilisation des données d’image décodées, consultez [vue d’ensemble des sources bitmap](-wic-bitmapsources.md).

### <a name="iwicbitmapsourcetransform-support"></a>Support IWICBitmapSourceTransform

En plus des interfaces qui doivent être des codecs compatibles avec WIC, le décodeur photo HD natif prend également en charge [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform). L’interface **IWICBitmapSourceTransform** fournit une option avancée pour décoder un flux de bits d’image. Au lieu de simplement retourner une image complète à l’aide de [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode), l’interface **IWICBitmapSourceTransform** active les options suivantes du décodeur.

-   Décodez une sous-région rectangulaire de l’image.
-   Décoder à une résolution inférieure
-   Décoder dans un format de pixel différent
-   Effectuer une transformation (rotation/retournement) lors du décodage

Le codec de photo HD natif offre le niveau de prise en charge suivant pour l’interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) .

### <a name="doessupporttransform"></a>DoesSupportTransform

L’implémentation native prend en charge toutes les transformations [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) .

### <a name="getclosestsize"></a>GetClosestSize

Pour les demandes inférieures à 1/2 la dimension de l’image source dans les deux dimensions, la photo HD retourne la plus grande taille d’image entière suivante qui est divisible uniformément par un facteur de deux. Pour toutes les autres tailles demandées, la photo HD retourne les dimensions de l’image d’origine.

### <a name="getclosestpixelformat"></a>GetClosestPixelFormat

La photo HD retourne le format de pixel de l’image encodée.

### <a name="copypixels"></a>CopyPixels

La photo HD accepte toute région demandée spécifiée par le paramètre [**WICRect**](/windows/desktop/api/Wincodec/ns-wincodec-wicrect) et retourne cette partie de l’image.

Les paramètres *uiWidth* et *uiHeight* doivent spécifier des dimensions telles qu’elles sont retournées par la fonction [**GetClosestSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize) . Toutes les autres valeurs retournent une erreur.

Le paramètre *pguidDstFormat* doit spécifier le format de pixel retourné par la fonction [**GetClosestPixelFormat**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat) . Toute autre valeur retourne une erreur.

La photo HD accepte toute valeur autorisée pour le paramètre *dstTransform* . Notez que les valeurs autorisées par WIC pour ce paramètre sont différentes de celles utilisées par la photo HD pour la balise de métadonnées de transformation.

 

 
