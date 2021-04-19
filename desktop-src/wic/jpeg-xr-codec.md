---
description: Le codec XR JPEG natif est disponible via le composant WIC (Windows Imaging Component). Le format JPEG XR, que le codec prend en charge, est conçu pour la photographie numérique des consommateurs et des professionnels.
ms.assetid: CB8D1A5F-B544-462E-8927-F45512CED873
title: Vue d’ensemble du codec XR JPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f32ffa397667b325d4e49eadf4d8ce42d49e8a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520695"
---
# <a name="jpeg-xr-codec-overview"></a>Vue d’ensemble du codec XR JPEG

Le codec XR JPEG natif est disponible via le composant WIC (Windows Imaging Component). Le format JPEG XR, que le codec prend en charge, est conçu pour la photographie numérique des consommateurs et des professionnels.

Le format JPEG XR peut atteindre jusqu’à deux fois l’efficacité de la compression du format JPEG d’origine, avec des artefacts de compression moins perceptibles. Les fonctionnalités des XR JPEG sont les suivantes :

-   Prise en charge des images monochrome, RVB, CMJN et n-Channel
-   formats d’entier 8, 16 et 32 bits
-   Des formats à plage dynamique élevée, à large gamme, utilisant des valeurs de couleur à virgule fixe ou à virgule flottante
-   Décodage progressif
-   Encodage avec ou sans perte utilisant le même algorithme de compression
-   Prise en charge du décodage des régions d’intérêt dans les grandes images

Le format JPEG XR est défini dans les documents standard suivants :

-   ITU-T T. 832 : *Information Technology – système de codage d’images JPEG XR-spécification de codage d’image*
-   ISO/IEC 29199-2:2010 : *technologies de l’information : système de codage d’image XR JPEG, partie 2 : spécification de codage d’image*

La norme JPEG XR est en grande partie basée sur le format de [photo HD](hdphoto-format-overview.md) , mais il existe des différences entre les deux formats. Dans Windows 8, le codec de photo HD a été mis à jour pour prendre en charge les XR JPEG. Désormais, l’encodeur génère toujours un flux de bits conforme XR JPEG. Le décodeur peut décoder des images JPEG XR et HD.

Des améliorations significatives des performances, par rapport au codec photo HD, ont été apportées au codec XR JPEG. Par exemple, le décodage d’image de sous-résolution, tel que la génération de miniatures, a été amélioré, ainsi que le décodage d’image de faible résolution. Nous vous recommandons d’utiliser le format JPEG XR au lieu du format HD photo.

## <a name="codec-information"></a>Informations sur le codec



|                     |                                                                         |
|---------------------|-------------------------------------------------------------------------|
| Extension de nom de fichier | « JXR » et « WDP »                                                         |
| GUID du conteneur      | **GUID \_ ContainerFormatWmp**                                            |
| GUID du décodeur        | **CLSID \_ WICWmpDecoder**                                                |
| GUID de l’encodeur        | **CLSID \_ WICWmpEncoder**                                                |
| Prise en charge des profils     | L’encodeur et le décodeur prennent en charge jusqu’au profil principal et jusqu’au niveau 128. |



 

## <a name="codec-features"></a>Fonctionnalités du codec

### <a name="high-dynamic-range"></a>Plage dynamique élevée

Le XR JPEG prend en charge les images de plage haute dynamique, à l’aide de couleurs à virgule flottante ou à virgule fixe. Dans ces formats de couleurs, la plage numérique d’un pixel est supérieure à la plage visible. vous pouvez donc ajuster les couleurs au-dessus ou en dessous de la plage visible pendant les phases de traitement intermédiaires.

-   Fixed-point : dans une représentation à virgule fixe, 0 représente le noir et 1,0 représente la saturation maximale. Le codec XR JPEG prend en charge les formats à virgule fixe 16 bits et 32 bits. Pour 16 bits, 1,0 = 0x2000h, qui donne 13 bits pour la plage visible \[ 0... 1 \] . La plage totale est comprise entre – 4,0 et + 3,999, et est mappée de manière linéaire. Pour 32 bits, 1,0 = 0x01000000h, la plage visible est de 24 bits, tandis que la plage totale est comprise entre – 128 et + 127,999.
-   Virgule flottante : dans une représentation à virgule flottante, 0 représente le noir et 1,0 représente la saturation maximale. Le codec XR JPEG prend en charge les formats à virgule flottante 16 bits et 32 bits.

### <a name="tiles"></a>Vignettes

Un frame peut être partitionné en sous-régions rectangulaires appelées *vignettes*. Une vignette est une zone d’une image qui contient des tableaux rectangulaires de blocs macros. Les vignettes permettent de décoder les zones de l’image sans traiter l’intégralité de l’image.

Pendant l’encodage, sélectionnez le nombre de vignettes en définissant les propriétés **HorizontalTileSlices** et **VerticalTileSlices** . La taille minimale de la vignette est 16 × 16 pixels. L’encodeur ajuste le nombre de vignettes pour maintenir cette restriction. Il existe une surcharge de stockage et de traitement associée à chaque vignette. vous devez donc prendre en compte le nombre de vignettes nécessaires pour des scénarios particuliers.

### <a name="image-stream-output"></a>Sortie de flux d’image

La norme JPEG-XR définit deux parties d’un fichier JPEG-XR :

-   Flux de bits d’image, défini dans le corps de la norme.
-   Conteneur d’images. Le fichier contient des métadonnées EXIF et XMP, et est défini dans l’annexe A de la norme.

Il est possible, et autorisé par la norme, d’incorporer le flux d’image à l’intérieur d’un autre type de conteneur de fichiers. L’encodeur prend en charge un mode de diffusion en continu, qui génère le flux binaire d’image brut sans conteneur d’images. Une application peut stocker le flux binaire dans un autre format de conteneur.

Pour activer le mode de diffusion en continu uniquement, définissez la propriété **StreamOnly** .

### <a name="image-quality-settings"></a>Paramètres de qualité de l’image

Plusieurs propriétés de codec contrôlent la qualité de l’image de sortie à partir de l’encodeur.

-   [ImageQuality](#imagequality) est une propriété commune aux codecs WIC. Elle spécifie la qualité de l’image en tant que valeur à virgule flottante unique comprise entre 0,0 et 1,0.
-   Les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) permettent de mieux contrôler les paramètres de qualité.

Pour utiliser les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) , affectez à la propriété [UseCodecOptions](#usecodecoptions) la **\_ valeur variant true**.

Si [UseCodecOptions](#usecodecoptions) a la valeur **Variant \_ false** (la valeur de **type Variant \_ false** est la valeur par défaut), l’encodeur utilise la propriété [ImageQuality](#imagequality) . L’encodeur mappe la valeur de ImageQuality à la [qualité](#image-quality-settings), au [chevauchement](#overlap)et à l' [échantillonnage](#subsampling) par le biais d’une table de recherche.

L’encodeur ne prend pas en charge la propriété **CompressionQuality** .

### <a name="compressed-domain-transcode"></a>Transcodage de domaine compressé

Le codec XR JPEG peut effectuer certaines transformations d’image sans décoder les données compressées et les encoder. Les opérations de domaine compressées sont très efficaces et évitent toute perte de qualité supplémentaire courante lorsque vous décodez et recodez une image compressée avec perte.

Les opérations de domaine compressées suivantes sont prises en charge :

-   Rogner une zone de l’image.
-   Faire pivoter ou retourner l’image.
-   Ignorez les données de fréquence pour créer un fichier image plus petit.
-   Réorganisez l’image entre l’ordre spatial et l’ordre des fréquences.

L’encodeur XR JPEG utilise le transcodage de domaine compressé, si possible, lorsque l’image source est une image JPEG XR. Lorsque l’encodeur effectue une opération de domaine compressé, il ignore les propriétés de codec suivantes : [AlphaQuality](#alphaquality), [ImageQuality](#imagequality), [InterleavedAlpha](#interleavedalpha), disposant d’un[chevauchement](#overlap) [sans perte](#lossless)et [qualité](#image-quality-settings). Si les propriétés [HorizontalTileSlices](/windows) et [VerticalTileSlices](/windows) sont présentes, vous devez les affecter à zéro. Vous ne pouvez pas modifier la taille des vignettes d’une image dans le cadre d’un transcodage de domaine compressé.

La liste de suivi décrit comment effectuer les transformations d’image.

-   Pour rogner l’image, définissez la région souhaitée dans le paramètre [**WICRect**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) de la méthode **WriteSource** .
-   Pour faire pivoter ou retourner l’image, définissez la propriété [BitmapTransform](#bitmaptransform) .
-   Pour ignorer les données de fréquence dans l’image, définissez la propriété [ImageDataDiscard](#imagedatadiscard) . Pour ignorer les données de fréquence dans le canal alpha, définissez la propriété [AlphaDataDiscard](#alphadatadiscard) . L’abandon des données de fréquence réduit la taille des fichiers encodés et peut réduire la résolution.
-   Pour modifier l’organisation de l’image entre la fréquence et le classement spatial, définissez la propriété [FrequencyOrdering](/windows) .

Pour désactiver le transcodage de domaine compressé et forcer l’encodeur à recoder l’image, définissez [UseCodecOptions](#usecodecoptions) sur **Variant \_ true** et affectez à [CompressedDomainTranscode](#compresseddomaintranscode) la valeur **Variant \_ false**.

## <a name="encoder-options"></a>Options de l’encodeur

Pour définir les propriétés d’encodage, utilisez l’interface [**IPropertyBag2**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768192(v=vs.85)) . Pour plus d’informations, consultez la [vue d’ensemble de l’encodage](-wic-creating-encoder.md).

La liste suivante spécifie les options de l’encodeur.

-   [AlphaDataDiscard](#alphadatadiscard)
-   [AlphaQuality](#alphaquality)
-   [BitmapTransform](#bitmaptransform)
-   [CompressedDomainTranscode](#compresseddomaintranscode)
-   [FrequencyOrder](#frequencyorder)
-   [HorizontalTileSlices](#horizontaltileslices)
-   [IgnoreOverlap](#ignoreoverlap)
-   [ImageDataDiscard](#imagedatadiscard)
-   [ImageQuality](#imagequality)
-   [InterleavedAlpha](#interleavedalpha)
-   [Lossless](#lossless)
-   [Éviter](#overlap)
-   [ProgressiveMode](#progressivemode)
-   [Qualité](#image-quality-settings)
-   [StreamOnly](#streamonly)
-   [Sous-échantillonnage](#subsampling)
-   [UseCodecOptions](#usecodecoptions)
-   [VerticalTileSlices](#verticaltileslices)

### <a name="alphadatadiscard"></a>AlphaDataDiscard

Définit la quantité de données de fréquence alpha à ignorer pendant un transcodage de domaine compressé.



| Type de données | VARTYPE     | Plage | Default |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 – 4   | Aucun    |



 

Cette propriété s’applique uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true** et si l’image contient un canal alpha planaire ou un canal alpha entrelacé ; sinon, elle est ignorée.

Pour les images qui contiennent un canal alpha planaire, les valeurs suivantes sont valides.



| Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Aucune donnée de fréquence image n'est ignorée.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| 1     | Les flexbits sont ignorés. Cela réduit arbitrairement la qualité du canal alpha planaire pour l’image transcodée. , sans modification de la résolution effective. La réduction exacte de la taille et de la qualité des fichiers dépend de nombreux facteurs et ne peut pas être spécifiée exactement.                                                                                                                                                                                           |
| 2     | La bande de données de fréquence à passage élevé est ignorée, y compris le flexbits. Cela réduit efficacement la résolution du canal alpha planaire par un facteur de 4 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc 4x4 de pixels de canal alpha. En règle générale, vous devez définir cette valeur uniquement lorsque la propriété [ImageDataDiscard](#imagedatadiscard) a la même valeur.                            |
| 3     | Les bandes de données de fréquence à passage rapide et à faible passage sont ignorées, y compris flexbits. Ce ffectively réduit la résolution du canal alpha planaire par un facteur de 16 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque 16x16 bloc macro de pixels de canal alpha. En règle générale, vous devez définir cette valeur uniquement lorsque la propriété [ImageDataDiscard](#imagedatadiscard) a la même valeur. |
| 4     | Le canal alpha est complètement ignoré. Le format de pixel de l’image transcodée est modifié pour refléter la suppression du canal alpha.                                                                                                                                                                                                                                                                                                                                |



 

Pour les images qui contiennent un canal alpha entrelacé, la valeur suivante est valide.



| Valeur | Description                                                                                                                                 |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------|
| 4     | Le canal alpha est complètement ignoré. Le format de pixel de l’image transcodée est modifié pour refléter la suppression du canal alpha. |



 

Pour Alpha entrelacé, sauf si cette propriété a la valeur 4, le canal alpha est traité de la même façon que les données de l’image, en fonction de la valeur de la propriété [ImageDataDiscard](#imagedatadiscard) .

### <a name="alphaquality"></a>AlphaQuality

Définit la qualité de compression pour l’image de canal alpha planaire.



| Type de données | VARTYPE     | Plage | Default |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 1 – 255 | 1       |



 

Cette propriété s’applique lorsque l’image a un canal alpha et que la propriété [InterleavedAlpha](#interleavedalpha) a la **\_ valeur false variant**. La valeur 1 indique le mode sans perte. L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.

### <a name="bitmaptransform"></a>BitmapTransform

Spécifie si l’image est pivotée ou retournée quand elle est décodée.



| Type de données | VARTYPE     | Plage                                                                     | Default                       |
|-----------|-------------|---------------------------------------------------------------------------|-------------------------------|
| **UCHAR** | **\_UI1 VT** | [**WICBitmapTransformOptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicbitmaptransformoptions) | **WICBitmapTransformRotate0** |



 

### <a name="compresseddomaintranscode"></a>CompressedDomainTranscode

Active ou désactive le transcodage du domaine compressé.



| Type de données         | VARTYPE      | Default           |
|-------------------|--------------|-------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ true** |



 

Pour désactiver les opérations de domaine compressé, affectez la valeur **\_ false** à cette propriété.

### <a name="frequencyorder"></a>FrequencyOrder

Active l’encodage dans l’ordre des fréquences. Les implémentations d’appareils des encodeurs XR JPEG peuvent organiser un fichier dans l’ordre spatial pour réduire la mémoire requise lors de l’encodage.



| Type de données         | VARTYPE      | Default           |
|-------------------|--------------|-------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ true** |



 

-   **Variante \_ TRUE**: ordre des fréquences. Les données de fréquence la plus basse apparaissent en premier dans le fichier, et le contenu de l’image est regroupé par sa fréquence plutôt que par son orientation spatiale. L’organisation d’un fichier par ordre de fréquence offre les meilleures performances pour tout décodage basé sur les fréquences.
-   **Variante \_ FALSe**: ordre spatial. L’ordre spatial réduit la mémoire requise pendant l’encodage

L’ordre des fréquences est recommandé, sauf si vous avez des raisons spécifiques aux performances ou à l’application d’utiliser l’ordre spatial.

### <a name="horizontaltileslices"></a>HorizontalTileSlices

Définit le nombre de mosaïques horizontales.



| Type de données  | VARTYPE     | Plage  | Default                      |
|------------|-------------|--------|------------------------------|
| **USHORT** | **\_UI2 VT** | de 0 à 4 095 | (largeur d’image – 1)  >> 8 |



 

La valeur est le nombre de sous-divisions horizontales ; autrement dit, le nombre de vignettes horizontales – 1.

### <a name="ignoreoverlap"></a>IgnoreOverlap

Spécifie comment l’encodeur gère les limites des vignettes pendant un transcodage de domaine compressé.



| Type de données         | VARTYPE      | Default            |
|-------------------|--------------|--------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ false** |



 

Cette propriété est appliquée uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true** et qu’un transcodage de sous-région d’une ou plusieurs vignettes est effectué.

L’opération par défaut pour un transcodage de région consiste à développer la région demandée pour inclure les pixels environnants requis pour le décodage du chevauchement des bords de la région. Si cette propriété a la valeur **Variant \_ true**, le codec ignore les pixels environnants, et seules les vignettes sélectionnées sont extraites. Si l’image source n’est pas en mosaïque ou si la région demandée contient des vignettes partielles, ce paramètre est ignoré.

### <a name="imagedatadiscard"></a>ImageDataDiscard

Définit la quantité de données de fréquence d’image à ignorer pendant un transcodage de domaine compressé.



| Type de données | VARTYPE     | Plage | Default |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 – 3   | 0       |



 

Cette propriété s’applique uniquement si la propriété [CompressedDomainTranscode](#compresseddomaintranscode) a la valeur **Variant \_ true**; sinon, elle est ignorée.



| Valeur | Description                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0     | Aucune donnée de fréquence image n'est ignorée.                                                                                                                                                                                                                                                                                                                                                                             |
| 1     | Les flexbits sont ignorés. Cela réduit arbitrairement la qualité de l’image transcodée sans modifier la résolution effective de l’image. La réduction exacte de la taille et de la qualité des fichiers dépend de nombreux facteurs et ne peut pas être spécifiée exactement. Cette valeur retourne une erreur spécifiée pour un canal alpha entrelacé.                                                                                |
| 2     | La bande de données de fréquence à passage élevé est ignorée, y compris le flexbits. Cela réduit la résolution de l’image transcodée par un facteur de 4 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc 4x4 de pixels. Par conséquent, l’image transcodée doit être sous-échantillonnée en conséquence chaque fois qu’elle est décodée.                             |
| 3     | Les bandes de données de fréquence à passage rapide et à faible passage sont ignorées, y compris flexbits. Cela réduit la résolution de l’image transcodée par un facteur de 16 dans les deux dimensions. Les dimensions réelles de l’image transcodée restent les mêmes, mais l’image perd tous les détails dans chaque bloc macro de 16 x 16 pixels. Par conséquent, l’image transcodée doit être sous-échantillonnée en conséquence chaque fois qu’elle est décodée. |



 

Si l’image contient un canal alpha entrelacé, la valeur de [ImageDataDiscard](#imagedatadiscard) est appliquée au canal alpha, sauf si la propriété [AlphaDataDiscard](#alphadatadiscard) est définie sur 4, auquel cas le canal alpha est ignoré.

Pour une composante alpha planaire, les données de fréquence qui sont ignorées sont contrôlées par la propriété [AlphaDataDiscard](#alphadatadiscard) .

### <a name="imagequality"></a>ImageQuality

Définit la qualité de l’image.



| Type de données | VARTYPE    | Plage | Default |
|-----------|------------|-------|---------|
| **FLOAT** | **VT \_ R4** | 0 – 1.0 | 0.9     |



 

Le niveau 1,0 donne une compression mathématiquement sans perte.

Le niveau 0,0 est le paramètre de qualité le plus bas.

### <a name="interleavedalpha"></a>InterleavedAlpha

Spécifie s’il faut encoder l’alpha entrelacé ou le plan alpha entrelacé.



| Type de données         | VARTYPE      | Default            |
|-------------------|--------------|--------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ false** |



 

-   **Variante \_ TRUE**: alpha entrelacé. Les informations de canal alpha sont encodées sous la forme d’un canal entrelacé supplémentaire, sans corrélation avec les canaux de contenu d’image. Ce mode est utile pour décoder alpha simultanément avec l’image lorsque l’image est diffusée en continu.
-   VARIANTE \_ false : alpha planaire. Un canal alpha planaire est encodé sous la forme d’une image distincte. Les données d’image et le canal alpha sont décodés indépendamment. Si vous le souhaitez, vous pouvez définir le niveau de qualité du canal alpha en définissant la propriété [AlphaQuality](#alphaquality) .

L’alpha entrelacé est pris en charge uniquement pour certains formats de pixel RVB. L’alpha planaire est pris en charge pour tout format d’image qui définit un canal alpha.

### <a name="lossless"></a>Lossless

Active la compression des pertes.



| Type de données         | VARTYPE      | Default        |
|-------------------|--------------|----------------|
| **VARIANT \_ booléen** | **VT \_ bool** | VARIANTE \_ false |



 

Si la valeur est **\_ true**, l’encodeur utilise la compression sans perte. Lorsque la valeur **Variant est \_ true**, cette propriété remplace la propriété [ImageQuality](#imagequality) .

### <a name="overlap"></a>Chevauchement

Définit le niveau de filtrage de chevauchement. Avec le filtrage de chevauchement, les coefficients de transformation sont appliqués entre les limites Block et bloc macro. Cela peut réduire les artefacts de blocage.



| Type de données | VARTYPE     | Plage | Default |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 0 – 4   | 1       |



 



| Valeur | Description                                   |
|-------|-----------------------------------------------|
| 0     | Aucun chevauchement.                                   |
| 1     | Un niveau de chevauchement, une mosaïque floue. (valeur par défaut). |
| 2     | Deux niveaux de chevauchement, mosaïques floues.           |
| 3     | Un niveau de chevauchement, une mosaïque matérielle             |
| 4     | Deux niveaux de chevauchement, en mosaïque matérielle.           |



 

Définitions :

-   Un niveau de chevauchement : les valeurs encodées des blocs 4x4 sont modifiées en fonction des blocs voisins.
-   Deux niveaux de chevauchement : le premier niveau de chevauchement est appliqué. En outre, les valeurs encodées de 16x16 blocs macros sont modifiées en fonction du blocs macros voisin.
-   Mosaïque douce : le filtrage de chevauchement est appliqué à travers les limites des vignettes.
-   Mosaïque matérielle : le filtrage de chevauchement n’est pas appliqué sur les limites de la vignette. Les vignettes matérielles peuvent introduire des artefacts visuels avec les limites de la vignette.

Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.

### <a name="progressivemode"></a>ProgressiveMode

Active ou désactive l’encodage progressif.



| Type de données         | VARTYPE      | Default            |
|-------------------|--------------|--------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ false** |



 



| Valeur              | Description                |
|--------------------|----------------------------|
| **VARIANTE \_ true**  | Mode séquentiel (par défaut). |
| **VARIANTE \_ false** | Mode progressive.          |



 

### <a name="quality"></a>Qualité

Définit la qualité de compression.



| Type de données | VARTYPE     | Plage | Default |
|-----------|-------------|-------|---------|
| **UCHAR** | **\_UI1 VT** | 1 – 255 | 1       |



 

La valeur 1 indique le mode sans perte. L’augmentation des valeurs entraîne des taux de compression supérieurs et une qualité d’image inférieure.

Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.

### <a name="streamonly"></a>StreamOnly

Active ou désactive le mode de diffusion en continu uniquement.



| Type de données         | VARTYPE      | Default            |
|-------------------|--------------|--------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ false** |



 



| Valeur              | Description                                                            |
|--------------------|------------------------------------------------------------------------|
| **VARIANTE \_ true**  | L’encodeur génère le flux d’images brutes sans métadonnées.             |
| **VARIANTE \_ false** | L’encodeur génère le format de conteneur (flux d’image et métadonnées). |



 

### <a name="subsampling"></a>Sous-échantillonnage

Définit le sous-échantillonnage de chrominance. Cette propriété s’applique uniquement aux images RVB.



| Type de données | VARTYPE     | Plage | Default                                                  |
|-----------|-------------|-------|----------------------------------------------------------|
| **UCHAR** | **\_UI1 VT** | 0 – 3   | 3 Si [ImageQuality](#imagequality) > 0,8 ; sinon 1 |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>3</td>
<td>encodage 4:4:4. Préserve la résolution complète de Chroma.</td>
</tr>
<tr class="even">
<td>2</td>
<td>encodage 4:2:2. La résolution Chroma est 1/2 de la résolution de luminance.</td>
</tr>
<tr class="odd">
<td>1</td>
<td>encodage 4:2:0. La résolution Chroma est 1/4 de la résolution de luminance.</td>
</tr>
<tr class="even">
<td>0</td>
<td>Encodage 4:0:0. Ignore toutes les valeurs de chrominance et conserve uniquement la luminance.
<blockquote>
[!Note]<br />
Ce mode n’est pas recommandé, car le codec utilise une définition de luminance légèrement modifiée pour améliorer les performances. Au lieu de cela, il est préférable de convertir l’image en monochrome avant l’encodage.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

4:2:2 et 4:2:0 conservent les détails de la luminance aux dépens des détails des couleurs.

Si vous définissez cette propriété, affectez également à [UseCodecOptions](#usecodecoptions) la valeur **Variant \_ true**.

### <a name="usecodecoptions"></a>UseCodecOptions

Spécifie s’il faut utiliser les propriétés [Quality](#image-quality-settings), [chevauchement](#overlap)et [subéchantillonner](#subsampling) à la place de la propriété [ImageQuality](#imagequality) générique.



| Type de données         | VARTYPE      | Default            |
|-------------------|--------------|--------------------|
| **VARIANT \_ booléen** | **VT \_ bool** | **VARIANTE \_ false** |



 

### <a name="verticaltileslices"></a>VerticalTileSlices

Définit le nombre de mosaïques horizontales.



| Type de données  | VARTYPE     | Plage  | Default                       |
|------------|-------------|--------|-------------------------------|
| **USHORT** | **\_UI2 VT** | de 0 à 4 095 | (hauteur d’image – 1)  >> 8 |



 

La valeur est le nombre de sous-divisions verticales ; autrement dit, le nombre de vignettes verticales – 1.

## <a name="supported-color-formats"></a>Formats de couleurs pris en charge

Pour plus d’informations sur ces formats, consultez [formats de pixel natifs](-wic-codec-native-pixel-formats.md).

-   **Formats RGB d’entier**
    -   GUID \_ WICPixelFormat24bppRGB
    -   GUID \_ WICPixelFormat24bppBGR
    -   GUID \_ WICPixelFormat32bppBGR
    -   GUID \_ WICPixelFormat48bppRGB
    -   GUID \_ WICPixelFormat32bppBGRA
    -   GUID \_ WICPixelFormat64bppRGBA
    -   GUID \_ WICPixelFormat32bppPBGRA
    -   GUID \_ WICPixelFormat64bppPRGBA
-   **Formats RGB à virgule fixe**
    -   GUID \_ WICPixelFormat48bppRGBFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBFixedPoint
    -   GUID \_ WICPixelFormat96bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBFixedPoint
    -   GUID \_ WICPixelFormat128bppRGBAFixedPoint
-   **Formats RGB à virgule flottante**
    -   GUID \_ WICPixelFormat48bppRGBHalf
    -   GUID \_ WICPixelFormat64bppRGBHalf
    -   GUID \_ WICPixelFormat128bppRGBFloat
    -   GUID \_ WICPixelFormat64bppRGBAFixedPoint
    -   GUID \_ WICPixelFormat64bppRGBAHalf
    -   GUID \_ WICPixelFormat128bppRGBAFloat
    -   GUID \_ WICPixelFormat128bppPRGBAFloat
-   **Formats de nuances de gris**
    -   GUID \_ WICPixelFormat8bppGray
    -   GUID \_ WICPixelFormat16bppGray
    -   GUID \_ WICPixelFormat16bppGrayFixedPoint
    -   GUID \_ WICPixelFormat16bppGrayHalf
    -   GUID \_ WICPixelFormat32bppGrayFixedPoint
    -   GUID \_ WICPixelFormat32bppGrayFloat
-   **Formats compactés**
    -   GUID \_ WICPixelFormat16bppBGR555
    -   GUID \_ WICPixelFormat16bppBGR565
    -   GUID \_ WICPixelFormat32bppBGR101010
    -   GUID \_ WICPixelFormat32bppRGBE
-   **Formats CMJN**
    -   GUID \_ WICPixelFormat40bppCMYKAlpha
    -   GUID \_ WICPixelFormat64bppCMYK
    -   GUID \_ WICPixelFormat80bppCMYKAlpha
-   **Formats N-Channel**
    -   GUID \_ WICPixelFormat32bpp4Channels
    -   GUID \_ WICPixelFormat40bpp5Channels
    -   GUID \_ WICPixelFormat48bpp6Channels
    -   GUID \_ WICPixelFormat56bpp7Channels
    -   GUID \_ WICPixelFormat64bpp8Channels
    -   GUID \_ WICPixelFormat32bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat40bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat56bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat64bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat72bpp8ChannelsAlpha
    -   GUID \_ WICPixelFormat48bpp3Channels
    -   GUID \_ WICPixelFormat64bpp4Channels
    -   GUID \_ WICPixelFormat80bpp5Channels
    -   GUID \_ WICPixelFormat96bpp6Channels
    -   GUID \_ WICPixelFormat128bpp8Channels
    -   GUID \_ WICPixelFormat64bpp3ChannelsAlpha
    -   GUID \_ WICPixelFormat80bpp4ChannelsAlpha
    -   GUID \_ WICPixelFormat96bpp5ChannelsAlpha
    -   GUID \_ WICPixelFormat112bpp6ChannelsAlpha
    -   GUID \_ WICPixelFormat128bpp7ChannelsAlpha
    -   GUID \_ WICPixelFormat144bpp8ChannelsAlpha

 

 
