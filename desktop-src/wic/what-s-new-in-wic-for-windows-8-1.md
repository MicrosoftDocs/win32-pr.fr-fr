---
description: Le composant WIC (Windows Imaging Component) a été mis à jour avec les nouvelles versions de Windows. Cette rubrique fournit une présentation rapide de ces nouvelles fonctionnalités.
ms.assetid: 710B71CE-6FCC-46DA-A65C-6E4FC6A04275
title: Nouveautés de WIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b8b3783ac2fd8ef6a971f785cec80f868a6b80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522451"
---
# <a name="whats-new-in-wic"></a>Nouveautés de WIC

Le composant WIC (Windows Imaging Component) a été mis à jour avec les nouvelles versions de Windows. Cette rubrique fournit une présentation rapide de ces nouvelles fonctionnalités.

## <a name="whats-new-for-windows-10-version-1507"></a>Nouveautés de Windows 10, version 1507

### <a name="access-to-low-level-jpeg-data-for-wic-decoding-and-encoding"></a>Accès aux données JPEG de bas niveau pour le décodage et l’encodage WIC

À partir de Windows 10, la version 1507, WIC fournit l’accès aux structures de données JPEG de bas niveau, y compris les tables de Huffman et de quantification. Pour plus d'informations, voir les rubriques suivantes :

-   Interface [**IWICJpegFrameDecode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframedecode)
-   Interface [**IWICJpegFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicjpegframeencode)

### <a name="jpeg-indexing"></a>Indexation JPEG

L’indexation JPEG est une technique qui améliore considérablement les performances de l’accès aléatoire aux petites sous-régions d’une grande image JPEG, au détriment de l’utilisation de la mémoire supplémentaire. L’indexation JPEG peut être exploitée par n’importe quel appelant de WIC.

L’interface [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic) est conçue pour tirer parti de l’indexation JPEG si elle est activée. Par exemple, l’API ID2D1ImageSource demande uniquement les sections nécessaires de l’image dans un scénario tel que le panoramique et le zoom pour une image de grande résolution. Pour plus d'informations, voir les rubriques suivantes :

-   [**IWICJpegFrameDecode :: SetIndexing**](/windows/win32/api/Wincodec/nf-wincodec-iwicjpegframedecode-setindexing) , méthode
-   Interface [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)

## <a name="whats-new-for-windows-81"></a>Nouveautés de Windows 8.1

### <a name="support-for-jpeg-ycbcr-images"></a>Prise en charge des images JPEG YCbCr

À partir de Windows 8.1, WIC prend en charge le décodage, la transformation et l’encodage des données d’image Y’CbCr JPEG dans leur format natif. Cela permet aux applications de réduire considérablement le temps de traitement et la consommation de mémoire pour certaines opérations d’acquisition d’images lors de l’utilisation de fichiers JPEG encodés Y’CbCr. Pour plus d'informations, voir les rubriques suivantes :

-   [](-wic-sample-d2d-viewer.md)[Effet YCbCr](../direct2d/ycbcr-effect.md) de Direct2D
-   Interface [**IWICPlanarBitmapSourceTransform**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)
-   Interface [**IWICPlanarBitmapFrameEncode**](/windows/win32/api/Wincodec/nn-wincodec-iwicplanarbitmapframeencode)

### <a name="support-for-block-compressed-formats-dds-files"></a>Prise en charge des formats compressés par blocs (fichiers DDS)

À partir de Windows 8.1, WIC ajoute un nouveau codec qui prend en charge les images DDS encodées aux formats suivants : DXGI \_ format \_ BC1 \_ UNORM, DXGI \_ format \_ BC2 \_ UNORM et dxgi \_ format \_ \_ BC3 UNORM. Les données compressées de bloc DDS sont accessibles sous forme décodée à l’aide d’interfaces WIC standard, ou directement accessibles à l’aide de nouvelles interfaces DDS spécifiques. Pour plus d'informations, voir les rubriques suivantes :

-   Interface [**IWICDdsDecoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsdecoder)
-   Interface [**IWICDdsEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicddsencoder)

## <a name="whats-new-for-windows-8"></a>Nouveautés de Windows 8

Dans Windows 8, WIC a été mis à jour avec plusieurs nouvelles fonctionnalités. La version mise à jour de WIC est également disponible sur Windows 7 et Windows Server 2008 R2 via la [mise à jour de plateforme pour Windows 7](../direct3darticles/platform-update-for-windows-7.md), disponible via la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838).

### <a name="improved-direct2d-integration"></a>Amélioration de l’intégration de Direct2D

WIC dans Windows 8 fournit ces API pour améliorer l’intégration de Direct2D avec WIC :

-   [**IWICImageEncoder**](/windows/win32/api/Wincodec/nn-wincodec-iwicimageencoder) : nouvelle interface qui peut encoder le contenu de [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) Direct2D en [IWICBitmapFrameEncode](-wic-imp-iwicbitmapframeencode.md). Les méthodes de cette interface prennent un pointeur vers [**WICImageParameters**](/windows/win32/api/Wincodec/ns-wincodec-wicimageparameters), qui sont des paramètres pour contrôler l’encodage.
-   [**IWICImagingFactory2**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory2) -nouvelle fabrique WIC avec la méthode [**CreateImageEncoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) . Cette interface hérite de la fabrique WIC d’origine, [**IWICImagingFactory**](/windows/win32/api/Wincodec/nn-wincodec-iwicimagingfactory), et est créée de la même façon.

### <a name="changes-to-bmp-codec-alpha-support"></a>Modifications apportées à la prise en charge alpha du codec BMP

WIC dans Windows 8 prend en charge le chargement de fichiers image [**BITMAPV5HEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapv5header) en tant qu’images au format [WICPixelFormat32bppBGRA](-wic-codec-native-pixel-formats.md). En outre, l’encodeur BMP prend en charge une nouvelle valeur booléenne, l’option d’encodeur « EnableV5Header32bppBGRA », qui indique à l’encodeur d’écrire un **BITMAPV5HEADER** avec les données de l’image 32bppBGRA.

Pour plus d’informations sur les formats BMP, consultez [vue d’ensemble du format BMP](bmp-format-overview.md).

### <a name="new-pixel-formats"></a>Nouveaux formats de pixel

WIC dans Windows 8 définit ces nouveaux formats de pixel :

-   GUID \_ WICPixelFormat32bppRGB
-   GUID \_ WICPixelFormat64bppRGB
-   GUID \_ WICPixelFormat96bppRGBFloat
-   GUID \_ WICPixelFormat64bppPRGBAHalf

> [!Note]  
> Le codec intégré TIFF renverra les \_ données GUID WICPixelFormat96bppRGBFloat. Les trois autres formats ne sont pas utilisés par les codecs intégrés.

 

### <a name="restrictions-to-component-extensibility-in-appcontainer"></a>Restrictions relatives à l’extensibilité des composants dans AppContainer

En cas d’exécution dans un processus AppContainer, qui comprend toutes les applications du Windows Store, WIC utilise uniquement les composants fournis par Windows, que des composants supplémentaires soient installés ou non sur le système. L’application qui n’est pas en cours d’exécution dans AppContainer n’est pas affectée.

Les applications n’ont pas besoin d’apporter des modifications de code pour s’exécuter dans un AppContainger, mais les paramètres de l’indicateur [**WICComponentEnumerateOptions**](/windows/win32/api/Wincodec/ne-wincodec-wiccomponentenumerateoptions) et du GUID du fournisseur n’ont aucun effet. WIC ne parvient pas à charger une image si elle ne peut pas être décodée par un codec fourni par Windows, et l’appel de la méthode [**CreateComponentEnumerator**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createcomponentenumerator) retourne uniquement les composants fournis par Windows.

### <a name="changes-to-clsid_wicpngdecoder-and-png-decoder-color-context-support"></a>Modifications apportées au CLSID \_ WICPngDecoder et au décodeur png couleur du contexte de couleur

**CLSID \_ WICPngDecoder1** a été ajouté avec le même GUID que le **CLSID \_ WICPngDecoder** et le **CLSID \_ WICPngDecoder2** a été ajouté.

En cas de compilation sur le kit de développement logiciel (SDK) Windows 8, **CLSID \_ WICPngDecoder** est \# défini sur **CLSID \_ WICPngDecoder2** pour promouvoir les applications nouvellement compilées à l’aide du nouveau comportement de décodeur png. Les applications doivent continuer à spécifier le **CLSID \_ WICPngDecoder**.

Si vous spécifiez **CLSID \_ WICPngDecoder2** , vous créez une version du décodeur png WIC qui générera un [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) à partir de segments cHRM et Gama. Cela permet d’utiliser ces métadonnées d’espace colorimétrique avec d’autres API Windows pour la gestion des couleurs de l’image source. Un **IWICColorContext** n’est pas généré à partir des segments Gama et cHRM si un segment iCCP est présent, si un segment sRVB est présent ou si les segments Gama et cHRM indiquent un espace de couleurs sRVB.

Une application peut spécifier le **CLSID \_ WICPngDecoder1** pour créer une version du décodeur png WIC qui ne génère pas de [**IWICColorContext**](/windows/win32/api/Wincodec/nn-wincodec-iwiccolorcontext) à partir des segments Gama et cHRM. Cela correspond au comportement du décodeur PNG dans les versions précédentes de Windows.

### <a name="changes-to-wincodec_sdk_version"></a>Modifications apportées à la \_ version du SDK WINCODEC \_

En cas de compilation sur le kit de développement logiciel (SDK) Windows 8, **WINCODEC \_ SDK \_ version** est \# défini sur **WINCODEC \_ SDK \_ VERSION2** pour promouvoir les nouvelles applications compilées à l’aide du nouveau comportement de décodeur png. Dans le cas contraire, il est \# défini sur **WINCODEC \_ SDK \_ version1**. Les applications doivent continuer à spécifier la **\_ \_ version du kit de développement logiciel (SDK) WINCODEC**.

La spécification de la **\_ \_ version du kit de développement logiciel (SDK) WINCODEC** lors de l’appel du [**\_ proxy WICCreateImagingFactory**](-wic-codec-wiccreateimagingfactory-proxy.md) pour créer la fabrique d’images entraîne la création de **CLSID \_ WICPngDecoder2** à la place de **CLSID \_ WICPngDecoder1** à partir de la méthode [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) et de ses variantes. En outre, l’énumérateur des informations sur les composants du décodeur retourne les informations du composant **CLSID \_ WICPngDecoder2** , mais pas les informations **\_ WICPngDecoder1 CLSID** .

Si vous spécifiez **WINCODEC \_ SDK \_ version1** , le **CLSID \_ WICPngDecoder1** est utilisé à la place de **CLSID \_ WICPngDecoder2** dans les cas mentionnés ci-dessus.

### <a name="changes-to-clsid_wicimagingfactory"></a>Modifications apportées au CLSID \_ WICImagingFactory

**CLSID \_ WICImagingFactory1** a été ajouté avec le même GUID que le **CLSID \_ WICImagingFactory** et le **CLSID \_ WICImagingFactory2** a été ajouté.

En cas de compilation sur le kit de développement logiciel (SDK) Windows 8, **CLSID \_ WICImagingFactory** est \# défini sur **CLSID \_ WICImagingFactory2** pour promouvoir les applications nouvellement compilées à l’aide du nouveau comportement de décodeur png. Les applications doivent continuer à spécifier le **CLSID \_ WICImagingFactory**.

La spécification du **CLSID \_ WICImagingFactory2** lors de l’appel de [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer la fabrique d’images entraîne la création du **CLSID \_ WICPngDecoder2** à la place de **CLSID \_ WICPngDecoder1** à partir de la méthode [**CreateDecoder**](/windows/win32/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder) et de ses variantes. En outre, l’énumérateur des informations sur les composants du décodeur retourne les informations du composant **CLSID \_ WICPngDecoder2** , mais pas les informations **\_ WICPngDecoder1 CLSID** .

La spécification du **CLSID \_ WICImagingFactory1** entraîne l’utilisation de CLSID **\_ WICPngDecoder1** à la place de **CLSID \_ WICPngDecoder2** dans les cas ci-dessus.

## <a name="whats-new-for-windows-7"></a>Nouveautés de Windows 7

Dans Windows 7, WIC a été mis à jour avec plusieurs nouvelles fonctionnalités. Cette rubrique fournit une présentation rapide de ces nouvelles fonctionnalités.

### <a name="updates-to-the-tiff-codec"></a>Mises à jour du codec TIFF

Le codec WIC TIFF a été mis à jour pour Windows 7 afin de prendre en charge plusieurs fonctionnalités non prises en charge par la version précédente de WIC.

-   Prise en charge des fichiers TIFF volumineux.
-   Décoder des images TIFF en mosaïque.
-   Décodez les images TIFF plat (planaires).
-   Décoder des images TIFF encodées au format JPEG.

### <a name="progressive-decoding"></a>Décodage progressif

Le décodage progressif permet de décoder et de restituer de façon incrémentielle des parties d’une image avant la fin du téléchargement de l’image entière. Cette fonctionnalité améliore considérablement l’expérience utilisateur lors de l’affichage d’images à partir d’Internet, car l’utilisateur n’a pas besoin d’attendre que l’intégralité de l’image soit téléchargée avant de commencer le décodage. Avec le décodage progressif, les utilisateurs peuvent voir une image en préversion avec des données disponibles avant le téléchargement de l’image entière. Cette fonctionnalité est essentielle pour toute application utilisée pour afficher des images à partir d’Internet ou de sources de données avec une bande passante limitée.

Pour plus d’informations, consultez la [vue d’ensemble du décodage progressif](-wic-progressive-decoding.md).

### <a name="extended-metadata-support-for-jpeg-png-and-gif"></a>Prise en charge des métadonnées étendues pour JPEG, PNG et GIF

Dans Windows 7, WIC a étendu la prise en charge des métadonnées pour les images JPEG, PNG et GIF.

-   Ajout de la prise en charge des propriétés GIF et GIF animées.
-   Gestionnaires de métadonnées JPG étendus pour prendre en charge les métadonnées de chrominance, de luminance et de commentaire.
-   Gestionnaires de métadonnées PNG étendus pour prendre en charge les métadonnées tIME, sRVB, iCCP, historiques, cHRM, iTXt, bKGD et gAMA.
-   Ajout de nouveaux gestionnaires de métadonnées 8BIM pour les métadonnées ResolutionInfo et les métadonnées IPTC Digest.
-   Ajout de nouveaux gestionnaires de métadonnées pour le descripteur d’écran logique (LSD), le descripteur d’image (IMD), les extensions de contrôle graphique (GCE) et les métadonnées d’extensions d’application (APE).
-   Prise en charge des métadonnées qui s’étendent sur les blocs APPn.

### <a name="multi-threaded-apartment-support"></a>Prise en charge du cloisonnement multithread

Les objets d’un cloisonnement multithread (MTA) peuvent être appelés simultanément par un nombre quelconque de threads dans le MTA, ce qui permet de meilleures performances sur les systèmes multicœurs et certains scénarios de serveur. En outre, les codecs WIC qui résident dans un MTA peuvent appeler d’autres objets qui résident dans le MTA sans le coût de marshaling associé à l’appel entre les threads qui résident dans différents Apartments STA. Dans Windows 7, tous les codecs WIC intégrés ont été mis à jour pour prendre en charge le MTA, y compris JPEG, TIFF, PNG, GIF, ICO et BMP. Il est vivement recommandé d’écrire les codecs pour prendre en charge le MTA. Les codecs qui ne prennent pas en charge le MTA entraînent des dégradation de performances significatifs dans les applications multithread en raison du marshaling. L’activation de la prise en charge de MTA nécessite une synchronisation appropriée à implémenter dans le codec. L’implémentation exacte de ces techniques de synchronisation dépasse le cadre de ce document. Vous trouverez ci-dessous une référence générale pour la synchronisation des objets COM (Component Object Model).

### <a name="metadata-working-group-implementations"></a>Implémentations du groupe de travail des métadonnées

Il existe actuellement un large éventail de formats de stockage des métadonnées qui contiennent des propriétés qui se chevauchent, sans une norme de l’industrie claire ou des conseils sur les méthodes cohérentes pour lire et écrire ces formats de métadonnées. Pour faciliter cette variété de formats et de propriétés, le groupe de travail des métadonnées (MWG) a été formé. L’objectif de l’MWG est de fournir des indications qui garantissent l’interopérabilité entre une large gamme de plateformes, d’applications et d’appareils. Les recommandations établies par MWG s’appliquent aux champs de métadonnées XMP, EXIF et IPTC, ainsi qu’aux formats d’image JPEG, TIFF et PSD.

Dans Windows 7, le gestionnaire de métadonnées de photos et la couche de stratégie de métadonnées ont été mis à jour pour lire et écrire des métadonnées d’image conformément aux directives établies par MWG. Pour plus d’informations sur le groupe de travail des métadonnées (MWG), consultez les [instructions relatives aux métadonnées établies](https://s3.amazonaws.com/software.tagthatphoto.com/docs/mwg_guidance.pdf).

### <a name="windows-7-features-supported-on-windows-vista-and-windows-server-2008"></a>Fonctionnalités Windows 7 prises en charge sur Windows Vista et Windows Server 2008

La [mise à jour de plateforme pour Windows Vista](../win7ip/platform-update-for-windows-vista-portal.md) est un ensemble de bibliothèques Runtime qui permet aux développeurs de cibler des applications à la fois sur Windows 7 et Windows Vista. La mise à jour de plateforme pour Windows Server 2008 est un ensemble de bibliothèques Runtime qui permet aux développeurs de cibler des applications à la fois sur Windows Server 2008 R2 et Windows Server 2008. La mise à jour de plateforme pour Windows Vista et la mise à jour de plateforme pour Windows Server 2008 seront disponibles pour tous les clients Windows Vista et Windows Server 2008 via Windows Update. Les applications tierces qui requièrent une mise à jour de plateforme pour Windows Vista ou une mise à jour de plateforme pour Windows Server 2008 peuvent avoir Windows Update détecter si la mise à jour requise est installée ; Si ce n’est pas le cas, Windows Update le télécharge et l’installe en arrière-plan. Pour plus d’informations sur les deux mises à jour, consultez Mise à jour de la plateforme pour Windows Vista.

 

 
